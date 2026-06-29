# Layer3D
L3D is 3D with layers stacked on top of each other.

//% color="#9999FF" weight=100 icon="\uf1b3" block="L3D"
namespace layers {
    //% block="L3D stop engine"
    //% group="Engine"
    export function stopEngine() {
let enginrononon = false
    }
        //% block="L3D start engine"
    //% group="Engine"
    export function startEngine() {
let enginrononon = true
    }
    //% block="L3D create engine based on tilemap"
    //% group="Create"
    
    export function createWorld() {
namespace SpriteKind {
    export const wall = SpriteKind.create()
}
controller.right.onEvent(ControllerButtonEvent.Repeated, function () {
    index = 0
    for (let index2 = 0; index2 < players.length; index2++) {
        players[index].rotationDegrees += 2
        index += 1
    }
})
controller.left.onEvent(ControllerButtonEvent.Pressed, function () {
    index = 0
    for (let index2 = 0; index2 < players.length; index2++) {
        players[index].rotationDegrees += 2
        index += 1
    }
})
controller.right.onEvent(ControllerButtonEvent.Pressed, function () {
    index = 0
    for (let index2 = 0; index2 < players.length; index2++) {
        players[index].rotationDegrees += 2
        index += 1
    }
})
controller.left.onEvent(ControllerButtonEvent.Repeated, function () {
    index = 0
    for (let index2 = 0; index2 < players.length; index2++) {
        players[index].rotationDegrees += 2
        index += 1
    }
})
let index = 0
let players: Sprite[] = []
let cubeeee: Sprite = null
let ynovy = 0
let currentTileImage: Image = null
let rowsExtra = 0
let columnsExtra = 0
let rows = 0
let columns = 0
let randomthingtocheckthelocationandheightandwidthoftheitlemwpa: Sprite = null
let enginrononon = 0
if (enginrononon) {
    randomthingtocheckthelocationandheightandwidthoftheitlemwpa = sprites.create(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        `, SpriteKind.Enemy)
    randomthingtocheckthelocationandheightandwidthoftheitlemwpa.setVelocity(500000, 0)
    pause(100)
    columns = randomthingtocheckthelocationandheightandwidthoftheitlemwpa.tilemapLocation().column
    randomthingtocheckthelocationandheightandwidthoftheitlemwpa.setVelocity(0, 99999999999)
    pause(100)
    rows = randomthingtocheckthelocationandheightandwidthoftheitlemwpa.tilemapLocation().row
    columnsExtra = 0
    rowsExtra = 0
    for (let index2 = 0; index2 < rows + 1; index2++) {
        for (let index2 = 0; index2 < columns + 1; index2++) {
            currentTileImage = tiles.tileImageAtLocation(tiles.getTileLocation(columnsExtra, rowsExtra))
            ynovy = rowsExtra * 16 - 16
            if (tiles.tileAtLocationIsWall(tiles.getTileLocation(columnsExtra, rowsExtra))) {
                for (let index2 = 0; index2 < image.getDimension(currentTileImage, image.Dimension.Width); index2++) {
                    cubeeee = sprites.create(currentTileImage, SpriteKind.wall)
                    cubeeee.setPosition(columnsExtra * 16 - 16, ynovy)
                }
            }
            columnsExtra += 1
        }
        rowsExtra += 1
        columnsExtra = 0
    }
    players = sprites.allOfKind(SpriteKind.wall)
}

    }
}
  
