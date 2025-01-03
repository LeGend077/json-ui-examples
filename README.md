# JSON UI Resources

Find useful JSON UI snippets and resources for your Minecraft Resource Pack.

Everything here is usable and non-copyrighted. Credit goes to the person who provided the resource. **Contribute if possible**!

## Links

1. For Beginners: [https://wiki.bedrock.dev/json-ui/json-ui-intro](https://wiki.bedrock.dev/json-ui/json-ui-intro)
2. Documentation: [https://wiki.bedrock.dev/json-ui/json-ui-documentation](https://wiki.bedrock.dev/json-ui/json-ui-documentation)
3. Wiki: [https://wiki.bedrock.dev/json-ui/](https://wiki.bedrock.dev/json-ui/)

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

5. Custom Slider:

   
```json
{
    "start_screen_content": {
        "modifications": [
            {
                "array_name": "controls",
                "operation": "insert_front",
                "value": [
                    {
                        "my_slider@common.slider": {
                            "size": [
                                40,
                                20
                            ],
                            "anchor_from": "top_left",
                            "anchor_to": "top_left",
                            "offset": [
                                10,
                                10
                            ],
                            "$slider_name": "my_slider",
                            "$slider_steps": 10,
                            "property_bag": {
                                "#slider_steps": 10,
                                "#slider_value": 0
                            }
                        }
                    },
                    {
                        "conditional_image": {
                            "type": "image",
                            "texture": "textures/items/apple",
                            "anchor_from": "left_middle",
                            "anchor_to": "left_middle",
                            "size": [
                                200,
                                200
                            ],
                            "bindings": [
                                {
                                    "binding_type": "view",
                                    "source_control_name": "my_slider",
                                    "source_property_name": "#slider_value",
                                    "target_property_name": "#val"
                                },
                                {
                                    "binding_type": "view",
                                    "source_property_name": "(#val * 1)",
                                    "target_property_name": "#float_val"
                                },
                                {
                                    "binding_type": "view",
                                    "source_property_name": "(#float_val / 10)",
                                    "target_property_name": "#alpha"
                                }
                            ]
                        }
                    }
                ]
            }
        ]
    }
}
```

6. [Draggable Element](https://discord.com/channels/494194063730278411/1129449905388269647) (Bedrock-OSS Discord Server)

7. [Determine String Length](https://discord.com/channels/494194063730278411/1164751772208865301) (Bedrock-OSS Discord Server)

8. [Simple Chunk Display](https://discord.com/channels/494194063730278411/1115457940472746014) (Bedrock-OSS Discord Server)

9. [Image/Label Cyclers](https://discord.com/channels/494194063730278411/1090928017431339071) (Image Gallery sort of)

10. [Preserve Title Text](https://wiki.bedrock.dev/json-ui/preserve-title-texts)

11. Custom Toggle (with any state texture you want): [./custom_toggles.json](https://github.com/LeGend077/json-ui-resources/blob/main/custom_toggle.json)
