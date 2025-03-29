# JSON UI Examples

Find useful JSON UI snippets and resources for your Minecraft Bedrock Resource Pack. Credit goes to the person who provided the resource or me if not specified.

Content: 
- [Links](#Links)
- [Tutorials](#Tutorials)
- [Code Snippets](#Codes)

## Links

1. For Beginners: [https://wiki.bedrock.dev/json-ui/json-ui-intro](https://wiki.bedrock.dev/json-ui/json-ui-intro)
2. Documentation: [https://wiki.bedrock.dev/json-ui/json-ui-documentation](https://wiki.bedrock.dev/json-ui/json-ui-documentation)
3. Wiki: [https://wiki.bedrock.dev/json-ui/](https://wiki.bedrock.dev/json-ui/)
4. Chest UI Editor Tool by Minato: [https://minato-mba.github.io/web-apps/chest-ui-editor/](https://minato-mba.github.io/web-apps/chest-ui-editor/)
5. JSON UI VSCode Extension by Dingsel: [https://marketplace.visualstudio.com/items?itemName=Dingsel.bedrock-ui](https://marketplace.visualstudio.com/items?itemName=Dingsel.bedrock-ui)
6. JSON UI Tutorial Playlist I recommend: [https://www.youtube.com/watch?v=QhJkCDIZ-NU&list=PLu4XsMgGIrCqdU44JbWvgv1z_kt_ZpJyw](https://www.youtube.com/watch?v=QhJkCDIZ-NU&list=PLu4XsMgGIrCqdU44JbWvgv1z_kt_ZpJyw)

## Tutorials

1. [Editing Server Forms](https://www.youtube.com/watch?v=QhJkCDIZ-NU&list=PLu4XsMgGIrCqdU44JbWvgv1z_kt_ZpJyw)
2. [Creating Custom Progress Bar](https://www.youtube.com/watch?v=_J5Bi-krhw8)
3. [AgentMindStorm's UI Basics](https://www.youtube.com/watch?v=K7UyzmmML-g)

## Codes

1. Custom Text Button and Toggle:
```json
{
  "button@common_buttons.light_text_button": {
    "$button_text": "Click",
    "$pressed_button_name": "button.id",
    "$size": [50, 25]
  },

  "toggle@common_toggles.light_text_toggle": {
    "$button_text": "Toggle",
    "$toggle_name": "toggle"
    "$toggle_view_binding_name": "panel_toggle" // control name used in bindings
    "size": [50, 25]
  }
}
```

2. [Custom Tabs (like in play screen)](https://discord.com/channels/523663022053392405/1279568076404293652/1279778678687010839)

3. 3x3 Hotbar Grid:
```json
{
  "stack_1": {
    "type": "grid",
    "grid_dimensions": [
      3,
      3
    ],
    "$hotbar_collection_name|default": "hotbar_items",
    "grid_item_template": "hud.gui_hotbar_grid_item",
    "grid_dimension_binding": "#hotbar_grid_dimensions",
    "collection_name": "$hotbar_collection_name",
    "bindings": [
      {}
    ]
  }
}
```

4. [Custom Element Factories](https://discord.com/channels/523663022053392405/868073903703093259/994365337401315498)

5. Custom Slider: [./custom_slider.json](https://github.com/LeGend077/json-ui-examples/blob/main/custom_slider.json)

6. [Draggable Element](https://discord.com/channels/494194063730278411/1129449905388269647) (Bedrock-OSS Discord Server)

7. [Determine String Length](https://discord.com/channels/494194063730278411/1164751772208865301) (Bedrock-OSS Discord Server)

8. [Simple Chunk Display](https://discord.com/channels/494194063730278411/1115457940472746014) (Bedrock-OSS Discord Server)

9. [Image/Label Cyclers](https://discord.com/channels/494194063730278411/1090928017431339071) (Image Gallery sort of)

10. [Preserve Title Text](https://wiki.bedrock.dev/json-ui/preserve-title-texts)

11. Custom Toggle (with any state texture you want): [./custom_toggle.json](https://github.com/LeGend077/json-ui-examples/blob/main/custom_toggle.json)

12. Custom Progress Bar: [./custom_progress_bar.json](https://github.com/LeGend077/json-ui-examples/blob/main/custom_progress_bar.json)

13. Text/Input Box (text binding: `#item_name`):
```json
{
  "input_box@common.text_edit_box": {
    "size": [ "100%", 28 ],
    "max_length": 99,
    // "$text_edit_box_text_type": "NumberChars", (If you want only numbers)
    "$text_edit_text_control": "input_text_control",
    "$place_holder_text": "Input here..",
    "$text_alignment": "center"
  }
}
```

14. Change Size and Offset using Bindings: [./size_offset.json](https://github.com/LeGend077/json-ui-examples/blob/main/size_offset.json)

15. Progress Icons like heart or hunger bars: [./custom_heart_or_hunger_like_progress_bar_icons.json](https://github.com/LeGend077/json-ui-examples/blob/main/custom_heart_or_hunger_like_progress_bar_icons.json)

16. Custom Title base NPC Screen Form: [./custom_npc_screen_layout_reference_file.json](https://github.com/LeGend077/json-ui-examples/blob/main/custom_npc_screen_layout_reference_file.json)

17. [Animated Toggle](https://discord.com/channels/523663022053392405/1338743808187174922/1338743808187174922)

18. [Grayscaled Image](https://discord.com/channels/523663022053392405/1223427312192716860):
```json
{
  "grayscaled_image": {
    "type": "image",
    "size": [ 16, 16 ],
    "texture": "textures/items/apple",
    "color": [0.4666, 0.4666, 0.4666]
  }
}
```

19. [Custom Crafting Table UI](https://discord.com/channels/523663022053392405/1330589149711040573/1330589149711040573)

20. Prevent Touch Icon when clicking a button on hud screen: `"prevent_touch_input": true`

21. [Search bar with Textbox](https://discord.com/channels/523663022053392405/1246801922917138512)

22. [Make Server Form unclosable](https://discord.com/channels/523663022053392405/1067870274894172260/1342318716179976253):
```json
{
    "namespace": "server_form",
    "third_party_server_screen": {
        "button_mappings": []
    },
    "long_form": {
        "$show_close_button": false
    },
    "custom_form": {
        "$show_close_button": false
    }
}
```

23. [Modify item lore/hover text (ui_common.json)](https://discord.com/channels/523663022053392405/1067870274894172260/1332401225693532261)
