# Using Material Icons in RichTextLabel

Example code of using emojis in **RichTextLabel**
(included in addon: *res://addons/material-design-icons/examples/LabelWithIcons.gd*):
```gdscript
@tool
extends RichTextLabel

@export_multiline
var text_with_icons : String:
	set(value):
		text_with_icons = value
		bbcode_enabled = true
		text = MaterialIconsDB.parse_icons(value)

	get: return text_with_icons

func _ready():
	bbcode_enabled = true
	text = MaterialIconsDB.parse_icons(text_with_icons)
```

This is the result of the above code, with 
`text_with_icons = "Label with icons [icon:image-outline]"`

![RichTextLabel Example Screen Shot][LabelWithIcons-screenshot]

[LabelWithIcons-screenshot]:assets/label-with-icons.png
