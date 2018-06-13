# Godot-TilemapBug 

This bug is really, really easy to replicate. When you create a scene and export it as a tileset, if you at any point modify the StaticBody2D size at all (even if you modify it and then return it to what it was), the resulting collision info ends up messed up when you use it in a tile map.

Here is a visual of the resulting scene, running, with 'Visible Collision Shapes' turned on from the 'Debug Menu':
![running](https://github.com/z4rdoz/Godot-TilemapBug/blob/master/screenshots/running.PNG)

On the left is the bad tileset, where I changed the StaticBody2D size, and on the right is where I left it alone. Note, it doesn't appear to matter whether I use CollisionPolygon or CollisionShape2D. I noticed that when people were talking about this, they were saying they used the latter, so I thought I'd show an example of the former to demonstrate that it's a problem for both. For reference, this is the scene being run:
![scene](https://github.com/z4rdoz/Godot-TilemapBug/blob/master/screenshots/scene.PNG)

This is the scene that generated the bad tileset/the one on the left:
![bad-tile-scene](https://github.com/z4rdoz/Godot-TilemapBug/blob/master/screenshots/bad-tile-scene.PNG)

and this is the scene that generated the good tileset/the one on the right:
![good-tile-scene](https://github.com/z4rdoz/Godot-TilemapBug/blob/master/screenshots/goodd-tile-scene.PNG)
