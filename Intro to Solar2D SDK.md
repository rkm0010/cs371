- Corona SDK online documentation / references
	- https://docs.coronalabs.com
#### Corona: Display Object
- Anything you put on the screen is done via display objects
	- Standard Image
	- Text
	- Animated Sprite
	- Rectangle
	- Rounded Rectangle
	- Line
	- Polygon
	- Display Group
	- ...
- We can create and show the above by calling methods:
```lua
display.newCircle()
-- Will create a circle with an instance of the display object
```

#### Display Group
- Group objects are special type of display object
- In a display group, can add / remove display objects as children of the group
- In this case, the display group becomes a ***parent*** of those display objects

##### Code Example
```lua
local group = display.newGroup()
local rect = display.newRect(100, 100, 50, 50)
rect:setFillColor(0.7)
group:insert(rect) --add rect to group
rect.parent:remove(rect) -- removes rect from group
```

#### Rectangle Example
```lua
local box = display.newRect (200, 300, 100, 100);
box.strokeWidth = 10;
box:setStrokeColor(0.5,0.5,1);
```