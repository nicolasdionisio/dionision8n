URL airtable y dashboard
https://airtable.com/invite/l?inviteId=invjYnnaeMliphmQ9&inviteToken=6e109f3cb47c00631a1547c8f38e000517e389d8fdaffcc4427d304d3e11a343&utm_medium=email&utm_source=product_team&utm_content=transactional-alerts

El repositorio contiene: 
2 imagenes del recorrido del work flowx 
1 Video explicativo 
1 PDF con la documentacion 
1 Archivo txt que tambien lo muestro a continuacion con el JSON del trabajo 

Entrega final JSON 

{
    "name": "Clasificación de Leads",
    "flow": [
        {
            "id": 2,
            "module": "google-sheets:watchRows",
            "version": 2,
            "parameters": {
                "mode": "fromAll",
                "limit": 10,
                "sheetId": "Sheet1",
                "__IMTCONN__": 14438244,
                "spreadsheetId": "/1cf_cvgvuc8_2RNH5hnNKSpjKrO-bmebjDwnqLbVa1QM",
                "tableFirstRow": "A1:M1",
                "includesHeaders": true,
                "valueRenderOption": "FORMATTED_VALUE",
                "dateTimeRenderOption": "FORMATTED_STRING"
            },
            "mapper": {},
            "metadata": {
                "designer": {
                    "x": 0,
                    "y": 150,
                    "name": "LEAD ENTRANTE"
                },
                "restore": {
                    "parameters": {
                        "mode": {
                            "label": "Select from all"
                        },
                        "sheetId": {
                            "label": "Sheet1"
                        },
                        "__IMTCONN__": {
                            "data": {
                                "scoped": "true",
                                "connection": "google"
                            },
                            "label": "My Google connection (nicodionisio2@gmail.com)"
                        },
                        "includesHeaders": {
                            "label": "Yes"
                        },
                        "valueRenderOption": {
                            "mode": "chose",
                            "label": "Formatted value"
                        },
                        "dateTimeRenderOption": {
                            "mode": "chose",
                            "label": "Formatted string"
                        }
                    }
                },
                "parameters": [
                    {
                        "name": "__IMTCONN__",
                        "type": "account:google",
                        "label": "Connection",
                        "required": true
                    },
                    {
                        "name": "mode",
                        "type": "select",
                        "label": "Search Method",
                        "required": true,
                        "validate": {
                            "enum": [
                                "select",
                                "fromAll",
                                "map"
                            ]
                        }
                    },
                    {
                        "name": "includesHeaders",
                        "type": "select",
                        "label": "Table contains headers",
                        "required": true,
                        "validate": {
                            "enum": [
                                true,
                                false
                            ]
                        }
                    },
                    {
                        "name": "limit",
                        "type": "uinteger",
                        "label": "Limit",
                        "required": true
                    },
                    {
                        "name": "valueRenderOption",
                        "type": "select",
                        "label": "Value render option",
                        "validate": {
                            "enum": [
                                "FORMATTED_VALUE",
                                "UNFORMATTED_VALUE",
                                "FORMULA"
                            ]
                        }
                    },
                    {
                        "name": "dateTimeRenderOption",
                        "type": "select",
                        "label": "Date and time render option",
                        "validate": {
                            "enum": [
                                "SERIAL_NUMBER",
                                "FORMATTED_STRING"
                            ]
                        }
                    },
                    {
                        "name": "spreadsheetId",
                        "type": "text",
                        "label": "Spreadsheet ID",
                        "required": true
                    },
                    {
                        "name": "sheetId",
                        "type": "select",
                        "label": "Sheet Name",
                        "required": true
                    },
                    {
                        "name": "tableFirstRow",
                        "type": "text",
                        "label": "Row with headers",
                        "required": true
                    }
                ],
                "interface": [
                    {
                        "name": "__ROW_NUMBER__",
                        "type": "number",
                        "label": "Row number"
                    },
                    {
                        "name": "__SPREADSHEET_ID__",
                        "type": "text",
                        "label": "Spreadsheet ID"
                    },
                    {
                        "name": "__SHEET__",
                        "type": "text",
                        "label": "Sheet"
                    },
                    {
                        "name": "0",
                        "type": "text",
                        "label": "Order_Number (A)"
                    },
                    {
                        "name": "1",
                        "type": "text",
                        "label": "Name  (B)"
                    },
                    {
                        "name": "2",
                        "type": "text",
                        "label": "Email  (C)"
                    },
                    {
                        "name": "3",
                        "type": "text",
                        "label": "Code_Phone (D)"
                    },
                    {
                        "name": "4",
                        "type": "text",
                        "label": "Phone  (E)"
                    },
                    {
                        "name": "5",
                        "type": "text",
                        "label": "Country  (F)"
                    },
                    {
                        "name": "6",
                        "type": "text",
                        "label": "Company  (G)"
                    },
                    {
                        "name": "7",
                        "type": "text",
                        "label": "Job_Title  (H)"
                    },
                    {
                        "name": "8",
                        "type": "text",
                        "label": "Industry (I)"
                    },
                    {
                        "name": "9",
                        "type": "text",
                        "label": "Revenues (J)"
                    },
                    {
                        "name": "10",
                        "type": "text",
                        "label": "Lead (K)"
                    },
                    {
                        "name": "11",
                        "type": "text",
                        "label": "LinkedIn (L)"
                    },
                    {
                        "name": "12",
                        "type": "text",
                        "label": "website  (M)"
                    }
                ]
            }
        },
        {
            "id": 9,
            "module": "util:SetVariable2",
            "version": 1,
            "parameters": {},
            "mapper": {
                "name": "RevenuesLimpio",
                "scope": "roundtrip",
                "value": "{{parseNumber(replace(2.`9`; \",\"; ); \".\")}}"
            },
            "metadata": {
                "designer": {
                    "x": 323,
                    "y": 144
                },
                "restore": {
                    "expect": {
                        "scope": {
                            "label": "One cycle"
                        }
                    }
                },
                "expect": [
                    {
                        "name": "name",
                        "type": "text",
                        "label": "Variable name",
                        "required": true
                    },
                    {
                        "name": "scope",
                        "type": "select",
                        "label": "Variable lifetime",
                        "required": true,
                        "validate": {
                            "enum": [
                                "roundtrip",
                                "execution"
                            ]
                        }
                    },
                    {
                        "name": "value",
                        "type": "any",
                        "label": "Variable value"
                    }
                ],
                "interface": [
                    {
                        "name": "RevenuesLimpio",
                        "type": "any",
                        "label": "RevenuesLimpio"
                    }
                ]
            }
        },
        {
            "id": 18,
            "module": "openai-gpt-3:CreateCompletion",
            "version": 1,
            "parameters": {
                "__IMTCONN__": 14448469
            },
            "filter": null,
            "mapper": {
                "select": "chat",
                "temperature": "1",
                "top_p": "1",
                "n_completions": "1",
                "model": "gpt-4o",
                "max_tokens": "100",
                "messages": [
                    {
                        "role": "user",
                        "content": "Sos un asistente de clasificación de leads.\r\nEvaluá el lead según estos criterios:\r\n\r\nSi {{9.RevenuesLimpio}}es mayor a 150000 → prioridad: Prioridad Alta\r\nSi {{9.RevenuesLimpio}} es menor o igual a 150000 → prioridad: Prioridad Baja\r\nRespondé EXCLUSIVAMENTE con una de estas dos opciones (una sola línea):\r\nPrioridad Alta\r\nPrioridad Baja",
                        "imageDetail": "auto"
                    }
                ],
                "response_format": "text"
            },
            "metadata": {
                "designer": {
                    "x": 672,
                    "y": 137
                },
                "restore": {
                    "parameters": {
                        "__IMTCONN__": {
                            "label": "My OpenAI connection",
                            "data": {
                                "scoped": "true",
                                "connection": "openai-gpt-3"
                            }
                        }
                    },
                    "expect": {
                        "select": {
                            "label": "Create a Chat Completion (GPT and o1 models)"
                        },
                        "logit_bias": {
                            "mode": "chose"
                        },
                        "tool_choice": {
                            "mode": "chose",
                            "label": "Empty"
                        },
                        "stop": {
                            "mode": "chose"
                        },
                        "additionalParameters": {
                            "mode": "chose"
                        },
                        "model": {
                            "mode": "chose",
                            "label": "gpt-4o (system)Fast, intelligent, flexible GPT model"
                        },
                        "messages": {
                            "mode": "chose",
                            "items": [
                                {
                                    "role": {
                                        "mode": "chose",
                                        "label": "User"
                                    },
                                    "imageInputType": {
                                        "mode": "chose",
                                        "label": "Empty"
                                    },
                                    "imageDetail": {
                                        "mode": "chose",
                                        "label": "Auto"
                                    }
                                }
                            ]
                        },
                        "response_format": {
                            "mode": "chose",
                            "label": "Text"
                        }
                    }
                },
                "parameters": [
                    {
                        "name": "__IMTCONN__",
                        "type": "account:openai-gpt-3",
                        "label": "Connection",
                        "required": true
                    }
                ],
                "expect": [
                    {
                        "name": "select",
                        "type": "select",
                        "label": "Select Method",
                        "required": true,
                        "validate": {
                            "enum": [
                                "chat",
                                "prompt"
                            ]
                        }
                    },
                    {
                        "name": "temperature",
                        "type": "number",
                        "label": "Temperature",
                        "validate": {
                            "max": 2,
                            "min": 0
                        }
                    },
                    {
                        "name": "top_p",
                        "type": "number",
                        "label": "Top P",
                        "validate": {
                            "max": 1,
                            "min": 0
                        }
                    },
                    {
                        "name": "n_completions",
                        "type": "number",
                        "label": "Number"
                    },
                    {
                        "name": "frequency_penalty",
                        "type": "number",
                        "label": "Frequency Penalty",
                        "validate": {
                            "max": 2,
                            "min": -2
                        }
                    },
                    {
                        "name": "presence_penalty",
                        "type": "number",
                        "label": "Presence Penalty",
                        "validate": {
                            "max": 2,
                            "min": -2
                        }
                    },
                    {
                        "name": "logit_bias",
                        "type": "array",
                        "label": "Token Probability",
                        "spec": {
                            "spec": [
                                {
                                    "name": "token",
                                    "type": "text",
                                    "label": "Token ID",
                                    "required": true
                                },
                                {
                                    "name": "probability",
                                    "type": "number",
                                    "label": "Probability",
                                    "required": true,
                                    "validate": {
                                        "max": 100,
                                        "min": -100
                                    }
                                }
                            ],
                            "type": "collection",
                            "label": "Token Probability",
                            "name": "value"
                        }
                    },
                    {
                        "name": "seed",
                        "type": "integer",
                        "label": "Seed"
                    },
                    {
                        "name": "tool_choice",
                        "type": "select",
                        "label": "Tool Choice",
                        "validate": {
                            "enum": [
                                "none",
                                "auto",
                                "required"
                            ]
                        }
                    },
                    {
                        "name": "stop",
                        "type": "array",
                        "label": "Stop Sequences",
                        "validate": {
                            "maxItems": 4
                        },
                        "spec": {
                            "type": "text",
                            "label": "Stop Sequence",
                            "name": "value"
                        }
                    },
                    {
                        "name": "additionalParameters",
                        "type": "array",
                        "label": "Other Input Parameters",
                        "spec": {
                            "spec": [
                                {
                                    "name": "key",
                                    "type": "text",
                                    "label": "Parameter Name",
                                    "required": true
                                },
                                {
                                    "name": "type",
                                    "type": "select",
                                    "label": "Input Type",
                                    "options": [
                                        {
                                            "label": "Text",
                                            "value": "text",
                                            "nested": [
                                                {
                                                    "name": "value",
                                                    "type": "text",
                                                    "label": "Parameter Value"
                                                }
                                            ],
                                            "default": true
                                        },
                                        {
                                            "label": "Number",
                                            "value": "number",
                                            "nested": [
                                                {
                                                    "name": "value",
                                                    "type": "number",
                                                    "label": "Parameter Value"
                                                }
                                            ]
                                        },
                                        {
                                            "label": "Boolean",
                                            "value": "boolean",
                                            "nested": [
                                                {
                                                    "name": "value",
                                                    "type": "boolean",
                                                    "label": "Parameter Value"
                                                }
                                            ]
                                        },
                                        {
                                            "label": "Date",
                                            "value": "date",
                                            "nested": [
                                                {
                                                    "name": "value",
                                                    "type": "date",
                                                    "label": "Parameter Value"
                                                }
                                            ]
                                        },
                                        {
                                            "label": "Any",
                                            "value": "any",
                                            "nested": [
                                                {
                                                    "name": "value",
                                                    "type": "any",
                                                    "label": "Parameter Value"
                                                }
                                            ]
                                        }
                                    ]
                                }
                            ],
                            "type": "collection",
                            "label": "Input Parameter",
                            "name": "value"
                        }
                    },
                    {
                        "name": "model",
                        "type": "select",
                        "label": "Model",
                        "required": true
                    },
                    {
                        "name": "max_tokens",
                        "type": "uinteger",
                        "label": "Max Output Tokens"
                    },
                    {
                        "name": "messages",
                        "type": "array",
                        "label": "Messages",
                        "required": true,
                        "spec": {
                            "label": "Message",
                            "type": "collection",
                            "spec": [
                                {
                                    "name": "role",
                                    "type": "select",
                                    "label": "Role",
                                    "required": true,
                                    "options": {
                                        "store": [
                                            {
                                                "label": "User",
                                                "value": "user",
                                                "default": true,
                                                "nested": [
                                                    {
                                                        "help": "Text content of the message on behalf of the selected __Role__.",
                                                        "name": "content",
                                                        "type": "text",
                                                        "label": "Text Content"
                                                    },
                                                    {
                                                        "name": "imageInputType",
                                                        "type": "select",
                                                        "label": "Image Input Type",
                                                        "mappable": false,
                                                        "options": [
                                                            {
                                                                "value": "url",
                                                                "label": "URL",
                                                                "nested": [
                                                                    {
                                                                        "name": "imageUrl",
                                                                        "label": "Image URL",
                                                                        "type": "url",
                                                                        "help": "Make sure to use a publicly accessible URL.\nYou can test if your image is publicly accessible by opening the link in an incognito tab."
                                                                    }
                                                                ]
                                                            },
                                                            {
                                                                "value": "file",
                                                                "label": "Image File",
                                                                "nested": [
                                                                    {
                                                                        "name": "imageFile",
                                                                        "label": "Image",
                                                                        "type": "collection",
                                                                        "spec": [
                                                                            {
                                                                                "name": "imageFilename",
                                                                                "type": "filename",
                                                                                "label": "Image Filename",
                                                                                "semantic": "file:name",
                                                                                "extension": [
                                                                                    "jpg",
                                                                                    "jpeg",
                                                                                    "png",
                                                                                    "webp",
                                                                                    "gif"
                                                                                ],
                                                                                "help": "Accepted extensions: `.jpg`, `.jpeg`, `.png`, `.webp` and `.gif`."
                                                                            },
                                                                            {
                                                                                "name": "imageData",
                                                                                "type": "buffer",
                                                                                "label": "Image Data",
                                                                                "semantic": "file:data"
                                                                            }
                                                                        ]
                                                                    }
                                                                ]
                                                            }
                                                        ]
                                                    },
                                                    {
                                                        "name": "imageDetail",
                                                        "type": "select",
                                                        "label": "Image Detail",
                                                        "help": "Recommended value: `Auto`",
                                                        "options": [
                                                            {
                                                                "value": "auto",
                                                                "default": true,
                                                                "label": "Auto"
                                                            },
                                                            {
                                                                "value": "high",
                                                                "label": "High"
                                                            },
                                                            {
                                                                "value": "low",
                                                                "label": "Low"
                                                            }
                                                        ]
                                                    }
                                                ]
                                            },
                                            {
                                                "label": "Assistant",
                                                "value": "assistant",
                                                "nested": [
                                                    {
                                                        "help": "Text content of the message on behalf of the selected __Role__.",
                                                        "name": "content",
                                                        "type": "text",
                                                        "label": "Text Content"
                                                    },
                                                    {
                                                        "name": "tool_calls",
                                                        "label": "Tool Calls",
                                                        "type": "array",
                                                        "labels": {
                                                            "add": "Add tool call"
                                                        },
                                                        "mode": "edit",
                                                        "mappable": {
                                                            "help": "You can map the entire `Choices[]: Message.Tool Calls` array from a previous Create a Completion module here."
                                                        },
                                                        "spec": {
                                                            "label": "Tool Call",
                                                            "type": "collection",
                                                            "spec": [
                                                                {
                                                                    "name": "type",
                                                                    "type": "hidden",
                                                                    "default": "function"
                                                                },
                                                                {
                                                                    "name": "id",
                                                                    "type": "text",
                                                                    "label": "Tool call ID",
                                                                    "help": "Map this directly from the output of a previous **Create a Completion** module. Look for `Choices[]: Message.Tool Calls[]: ID`."
                                                                },
                                                                {
                                                                    "name": "function",
                                                                    "type": "collection",
                                                                    "label": "Function",
                                                                    "spec": [
                                                                        {
                                                                            "name": "name",
                                                                            "label": "Name",
                                                                            "type": "text",
                                                                            "required": true,
                                                                            "help": "The name of the function previously called."
                                                                        },
                                                                        {
                                                                            "name": "arguments",
                                                                            "label": "Arguments",
                                                                            "type": "text",
                                                                            "required": true,
                                                                            "help": "The arguments previously output by the AI."
                                                                        }
                                                                    ]
                                                                }
                                                            ]
                                                        }
                                                    }
                                                ]
                                            },
                                            {
                                                "label": "Developer / System",
                                                "nested": [
                                                    {
                                                        "help": "Text content of the message on behalf of the selected __Role__.",
                                                        "name": "content",
                                                        "type": "text",
                                                        "label": "Text Content"
                                                    }
                                                ],
                                                "value": "system"
                                            },
                                            {
                                                "label": "Tool",
                                                "value": "tool",
                                                "nested": [
                                                    {
                                                        "help": "The return of the function. This role should only be used when you have processed a previous function call and want to send the output of the function execution back to the AI.",
                                                        "name": "content",
                                                        "type": "text",
                                                        "label": "Text Content",
                                                        "required": true
                                                    },
                                                    {
                                                        "label": "Tool Call ID.",
                                                        "name": "tool_call_id",
                                                        "type": "text",
                                                        "required": true,
                                                        "help": "Map this directly from the output of a previous **Create a Completion** module. Look for `Choices[]: Message.Tool Calls[]: ID`."
                                                    }
                                                ]
                                            }
                                        ]
                                    }
                                }
                            ],
                            "name": "value"
                        }
                    },
                    {
                        "name": "response_format",
                        "type": "select",
                        "label": "Response Format",
                        "validate": {
                            "enum": [
                                "text",
                                "json_object"
                            ]
                        }
                    },
                    {
                        "name": "prediction",
                        "type": "text",
                        "label": "Predicted Outputs"
                    }
                ],
                "interface": [
                    {
                        "name": "result",
                        "type": "any",
                        "label": "Result"
                    },
                    {
                        "name": "id",
                        "type": "text",
                        "label": "ID"
                    },
                    {
                        "name": "object",
                        "type": "text",
                        "label": "Object"
                    },
                    {
                        "name": "created",
                        "type": "date",
                        "label": "Created"
                    },
                    {
                        "name": "model",
                        "type": "text",
                        "label": "Model"
                    },
                    {
                        "name": "choices",
                        "spec": [
                            {
                                "name": "text",
                                "type": "text",
                                "label": "Text"
                            },
                            {
                                "name": "index",
                                "type": "number",
                                "label": "Index"
                            },
                            {
                                "name": "logprobs",
                                "type": "text",
                                "label": "Log Probs"
                            },
                            {
                                "name": "finish_reason",
                                "type": "text",
                                "label": "Finish Reason"
                            },
                            {
                                "name": "message",
                                "spec": [
                                    {
                                        "name": "role",
                                        "type": "text",
                                        "label": "Role"
                                    },
                                    {
                                        "name": "content",
                                        "type": "text",
                                        "label": "Content"
                                    },
                                    {
                                        "name": "tool_calls",
                                        "spec": [
                                            {
                                                "name": "id",
                                                "type": "text",
                                                "label": "ID"
                                            },
                                            {
                                                "name": "type",
                                                "type": "text",
                                                "label": "Type"
                                            },
                                            {
                                                "name": "function",
                                                "spec": [
                                                    {
                                                        "name": "name",
                                                        "type": "text",
                                                        "label": "Name"
                                                    },
                                                    {
                                                        "name": "arguments",
                                                        "type": "text",
                                                        "label": "Arguments"
                                                    }
                                                ],
                                                "type": "collection",
                                                "label": "Function"
                                            }
                                        ],
                                        "type": "array",
                                        "label": "Tool Calls"
                                    },
                                    {
                                        "name": "refusal",
                                        "type": "text",
                                        "label": "Refusal"
                                    },
                                    {
                                        "name": "annotations",
                                        "spec": [
                                            {
                                                "name": "type",
                                                "type": "text",
                                                "label": "Type"
                                            },
                                            {
                                                "name": "url_citation",
                                                "spec": [
                                                    {
                                                        "name": "end_index",
                                                        "type": "number",
                                                        "label": "End Index"
                                                    },
                                                    {
                                                        "name": "start_index",
                                                        "type": "number",
                                                        "label": "Start Index"
                                                    },
                                                    {
                                                        "name": "title",
                                                        "type": "text",
                                                        "label": "Title"
                                                    },
                                                    {
                                                        "name": "url",
                                                        "type": "text",
                                                        "label": "URL"
                                                    }
                                                ],
                                                "type": "collection",
                                                "label": "URL Citation"
                                            }
                                        ],
                                        "type": "array",
                                        "label": "Annotations"
                                    }
                                ],
                                "type": "collection",
                                "label": "Message"
                            }
                        ],
                        "type": "array",
                        "label": "Choices"
                    },
                    {
                        "name": "usage",
                        "spec": [
                            {
                                "name": "prompt_tokens",
                                "type": "number",
                                "label": "Prompt Tokens"
                            },
                            {
                                "name": "completion_tokens",
                                "type": "text",
                                "label": "Completion Tokens"
                            },
                            {
                                "name": "total_tokens",
                                "type": "number",
                                "label": "Total Tokens"
                            },
                            {
                                "name": "prompt_tokens_details",
                                "spec": [
                                    {
                                        "name": "cached_tokens",
                                        "type": "uinteger",
                                        "label": "Cached Tokens"
                                    },
                                    {
                                        "name": "text_tokens",
                                        "type": "uinteger",
                                        "label": "Text Tokens"
                                    },
                                    {
                                        "name": "image_tokens",
                                        "type": "uinteger",
                                        "label": "Image Tokens"
                                    },
                                    {
                                        "name": "audio_tokens",
                                        "type": "uinteger",
                                        "label": "Audio Tokens"
                                    }
                                ],
                                "type": "collection",
                                "label": "Prompt Tokens Details"
                            },
                            {
                                "name": "completion_tokens_details",
                                "spec": [
                                    {
                                        "name": "reasoning_tokens",
                                        "type": "uinteger",
                                        "label": "Reasoning Tokens"
                                    },
                                    {
                                        "name": "text_tokens",
                                        "type": "uinteger",
                                        "label": "Text Tokens"
                                    },
                                    {
                                        "name": "audio_tokens",
                                        "type": "uinteger",
                                        "label": "Audio Tokens"
                                    },
                                    {
                                        "name": "accepted_prediction_tokens",
                                        "type": "uinteger",
                                        "label": "Accepted Prediction Tokens"
                                    },
                                    {
                                        "name": "rejected_prediction_tokens",
                                        "type": "uinteger",
                                        "label": "Rejected Prediction Tokens"
                                    }
                                ],
                                "type": "collection",
                                "label": "Completion Tokens Details"
                            }
                        ],
                        "type": "collection",
                        "label": "Usage"
                    },
                    {
                        "name": "service_tier",
                        "type": "text",
                        "label": "Service Tier"
                    },
                    {
                        "name": "system_fingerprint",
                        "type": "text",
                        "label": "System Fingerprint"
                    }
                ]
            },
            "onerror": [
                {
                    "id": 19,
                    "module": "builtin:Break",
                    "version": 1,
                    "parameters": {},
                    "mapper": {
                        "retry": true,
                        "count": "3",
                        "interval": "15"
                    },
                    "metadata": {
                        "designer": {
                            "x": 902,
                            "y": 403
                        },
                        "restore": {
                            "expect": {
                                "retry": {
                                    "mode": "chose"
                                }
                            }
                        },
                        "expect": [
                            {
                                "name": "retry",
                                "type": "boolean",
                                "label": "Retry automatically",
                                "required": true
                            },
                            {
                                "name": "count",
                                "type": "uinteger",
                                "label": "Number of retries",
                                "validate": {
                                    "min": 1,
                                    "max": 10000
                                },
                                "required": true
                            },
                            {
                                "name": "interval",
                                "type": "uinteger",
                                "label": "Minutes between retries",
                                "validate": {
                                    "min": 1,
                                    "max": 44640
                                },
                                "required": true
                            }
                        ]
                    }
                }
            ]
        },
        {
            "id": 3,
            "module": "builtin:BasicRouter",
            "version": 1,
            "mapper": null,
            "metadata": {
                "designer": {
                    "x": 1050,
                    "y": 126,
                    "name": "VIP o STANDAR"
                }
            },
            "routes": [
                {
                    "flow": [
                        {
                            "id": 4,
                            "module": "google-email:sendAnEmail",
                            "version": 4,
                            "parameters": {
                                "__IMTCONN__": 14438447
                            },
                            "filter": {
                                "name": "Lead VIP",
                                "conditions": [
                                    [
                                        {
                                            "a": "{{18.result}}",
                                            "o": "text:contain",
                                            "b": "Prioridad Alta"
                                        }
                                    ]
                                ]
                            },
                            "mapper": {
                                "to": [
                                    "miguel@b2meets.com"
                                ],
                                "content": "<div style=\"font-family: Arial, sans-serif; color: #333; max-width: 600px; padding: 20px; border: 1px solid #e0e0e0; border-radius: 8px;\">\r\n  <h2 style=\"color: #2b6cb0; margin-top: 0;\">🚀 Nuevo Lead VIP Registrado</h2>\r\n  <p>Hola Miguel,</p>\r\n  <p>Se ha registrado un nuevo contacto categorizado como <strong>LEAD VIP</strong>:</p>\r\n  \r\n  <table style=\"width: 100%; border-collapse: collapse; margin: 20px 0;\">\r\n    <tr style=\"background-color: #f7fafc;\"><td style=\"padding: 10px; border: 1px solid #edf2f7; font-weight: bold;\">Orden:</td><td style=\"padding: 10px; border: 1px solid #edf2f7;\">{{2.`0`}}</td></tr>\r\n    <tr><td style=\"padding: 10px; border: 1px solid #edf2f7; font-weight: bold;\">Nombre:</td><td style=\"padding: 10px; border: 1px solid #edf2f7;\">{{2.`1`}}</td></tr>\r\n    <tr style=\"background-color: #f7fafc;\"><td style=\"padding: 10px; border: 1px solid #edf2f7; font-weight: bold;\">Email:</td><td style=\"padding: 10px; border: 1px solid #edf2f7;\">{{2.`2`}}</td></tr>\r\n    <tr><td style=\"padding: 10px; border: 1px solid #edf2f7; font-weight: bold;\">Empresa:</td><td style=\"padding: 10px; border: 1px solid #edf2f7;\">{{2.`6`}}</td></tr>\r\n    <tr style=\"background-color: #f7fafc;\"><td style=\"padding: 10px; border: 1px solid #edf2f7; font-weight: bold;\">Presupuesto (Revenues):</td><td style=\"padding: 10px; border: 1px solid #edf2f7; color: #2b6cb0; font-weight: bold;\">${{9.RevenuesLimpio}}</td></tr>\r\n  </table>\r\n\r\n  <p style=\"margin-bottom: 0;\">Saludos,<br><strong>Equipo B2M</strong></p>\r\n</div>",
                                "subject": "LEAD VIP -  {{upper}}{{(2.`1`)}} - Order_Number: {{2.`0`}}",
                                "bodyType": "rawHtml"
                            },
                            "metadata": {
                                "designer": {
                                    "x": 1372,
                                    "y": -31,
                                    "name": "AVISAR LEAD VIP"
                                },
                                "restore": {
                                    "expect": {
                                        "cc": {
                                            "mode": "chose"
                                        },
                                        "to": {
                                            "mode": "chose",
                                            "items": [
                                                null
                                            ]
                                        },
                                        "bcc": {
                                            "mode": "chose"
                                        },
                                        "from": {
                                            "mode": "chose"
                                        },
                                        "bodyType": {
                                            "label": "Raw HTML"
                                        },
                                        "attachments": {
                                            "mode": "chose"
                                        },
                                        "emailHeaders": {
                                            "mode": "chose"
                                        }
                                    },
                                    "parameters": {
                                        "__IMTCONN__": {
                                            "data": {
                                                "scoped": "true",
                                                "connection": "google-email"
                                            },
                                            "label": "My Gmail connection (nicodionisio2@gmail.com)"
                                        }
                                    }
                                },
                                "parameters": [
                                    {
                                        "name": "__IMTCONN__",
                                        "type": "account:google-email",
                                        "label": "Connection",
                                        "required": true
                                    }
                                ],
                                "expect": [
                                    {
                                        "name": "to",
                                        "spec": {
                                            "name": "value",
                                            "type": "email",
                                            "label": "Recipient email address",
                                            "required": true,
                                            "validate": true
                                        },
                                        "type": "array",
                                        "label": "To",
                                        "required": true
                                    },
                                    {
                                        "name": "subject",
                                        "type": "text",
                                        "label": "Subject"
                                    },
                                    {
                                        "name": "bodyType",
                                        "type": "select",
                                        "label": "Body type",
                                        "required": true,
                                        "validate": {
                                            "enum": [
                                                "rawHtml",
                                                "collection"
                                            ]
                                        }
                                    },
                                    {
                                        "name": "attachments",
                                        "spec": {
                                            "name": "value",
                                            "spec": [
                                                {
                                                    "name": "filename",
                                                    "type": "filename",
                                                    "label": "File name",
                                                    "required": true,
                                                    "semantic": "file:name"
                                                },
                                                {
                                                    "name": "data",
                                                    "type": "buffer",
                                                    "label": "Data",
                                                    "required": true,
                                                    "semantic": "file:data"
                                                }
                                            ],
                                            "type": "collection",
                                            "label": "Attachment"
                                        },
                                        "type": "array",
                                        "label": "Attachments"
                                    },
                                    {
                                        "name": "from",
                                        "type": "select",
                                        "label": "From"
                                    },
                                    {
                                        "name": "cc",
                                        "spec": {
                                            "name": "value",
                                            "type": "email",
                                            "label": "Recipient email address"
                                        },
                                        "type": "array",
                                        "label": "CC recipients"
                                    },
                                    {
                                        "name": "bcc",
                                        "spec": {
                                            "name": "value",
                                            "type": "email",
                                            "label": "Recipient email address"
                                        },
                                        "type": "array",
                                        "label": "BCC recipients"
                                    },
                                    {
                                        "name": "emailHeaders",
                                        "spec": {
                                            "name": "value",
                                            "spec": [
                                                {
                                                    "name": "key",
                                                    "type": "text",
                                                    "label": "Key",
                                                    "required": true
                                                },
                                                {
                                                    "name": "value",
                                                    "type": "text",
                                                    "label": "Value"
                                                }
                                            ],
                                            "type": "collection",
                                            "label": "Email header"
                                        },
                                        "type": "array",
                                        "label": "Additional email headers"
                                    },
                                    {
                                        "name": "content",
                                        "type": "text",
                                        "label": "Content"
                                    }
                                ]
                            }
                        }
                    ]
                },
                {
                    "flow": [
                        {
                            "id": 8,
                            "module": "airtable:ActionCreateRecord",
                            "version": 3,
                            "parameters": {
                                "__IMTCONN__": 14438595
                            },
                            "filter": {
                                "name": "Lead Standar",
                                "conditions": [
                                    [
                                        {
                                            "a": "{{18.result}}",
                                            "o": "text:contain",
                                            "b": "Prioridad Baja"
                                        }
                                    ]
                                ]
                            },
                            "mapper": {
                                "base": "appXsXCz9nQaAKUVB",
                                "table": "tbluXOuiXMlPJQDrA",
                                "record": {
                                    "fldRYKRahUlCB48he": "{{2.`10`}}",
                                    "fldTO9dxOr3mYUyJI": "{{2.`1`}}",
                                    "fldkMC49a3XhnRByq": "{{2.`2`}}",
                                    "fldqE1utzvRuYVTD4": "{{9.RevenuesLimpio}}"
                                },
                                "typecast": false,
                                "useColumnId": false
                            },
                            "metadata": {
                                "designer": {
                                    "x": 1372,
                                    "y": 280,
                                    "name": "Registrar LEAD STANDAR"
                                },
                                "restore": {
                                    "expect": {
                                        "base": {
                                            "label": "LEADS_B2M"
                                        },
                                        "table": {
                                            "label": "Table 1",
                                            "nested": [
                                                {
                                                    "name": "record",
                                                    "spec": [
                                                        {
                                                            "name": "fldTO9dxOr3mYUyJI",
                                                            "type": "text",
                                                            "label": "Name"
                                                        },
                                                        {
                                                            "name": "fldkMC49a3XhnRByq",
                                                            "type": "text",
                                                            "label": "Email"
                                                        },
                                                        {
                                                            "name": "fldqE1utzvRuYVTD4",
                                                            "type": "number",
                                                            "label": "Revenues"
                                                        },
                                                        {
                                                            "name": "fldRYKRahUlCB48he",
                                                            "type": "text",
                                                            "label": "LEAD"
                                                        }
                                                    ],
                                                    "type": "collection",
                                                    "label": "Record"
                                                }
                                            ]
                                        },
                                        "typecast": {
                                            "mode": "chose"
                                        },
                                        "useColumnId": {
                                            "mode": "chose"
                                        }
                                    },
                                    "parameters": {
                                        "__IMTCONN__": {
                                            "data": {
                                                "scoped": "true",
                                                "connection": "airtable3"
                                            },
                                            "label": "Airtable Base LEADS (User ID: usr79PcGJ7vQOVzMG)"
                                        }
                                    }
                                },
                                "parameters": [
                                    {
                                        "name": "__IMTCONN__",
                                        "type": "account:airtable3,airtable2",
                                        "label": "Connection",
                                        "required": true
                                    }
                                ],
                                "expect": [
                                    {
                                        "name": "base",
                                        "type": "select",
                                        "label": "Base",
                                        "required": true
                                    },
                                    {
                                        "name": "typecast",
                                        "type": "boolean",
                                        "label": "Smart links",
                                        "required": true
                                    },
                                    {
                                        "name": "useColumnId",
                                        "type": "boolean",
                                        "label": "Use Column ID",
                                        "required": true
                                    },
                                    {
                                        "name": "table",
                                        "type": "select",
                                        "label": "Table",
                                        "required": true
                                    },
                                    {
                                        "name": "record",
                                        "spec": [
                                            {
                                                "name": "fldTO9dxOr3mYUyJI",
                                                "type": "text",
                                                "label": "Name"
                                            },
                                            {
                                                "name": "fldkMC49a3XhnRByq",
                                                "type": "text",
                                                "label": "Email"
                                            },
                                            {
                                                "name": "fldqE1utzvRuYVTD4",
                                                "type": "number",
                                                "label": "Revenues"
                                            },
                                            {
                                                "name": "fldRYKRahUlCB48he",
                                                "type": "text",
                                                "label": "LEAD"
                                            }
                                        ],
                                        "type": "collection",
                                        "label": "Record"
                                    }
                                ],
                                "interface": [
                                    {
                                        "name": "id",
                                        "type": "text",
                                        "label": "ID"
                                    },
                                    {
                                        "name": "createdTime",
                                        "type": "date",
                                        "label": "Created Time"
                                    },
                                    {
                                        "name": "Name",
                                        "type": "text",
                                        "label": "Name"
                                    },
                                    {
                                        "name": "Email",
                                        "type": "text",
                                        "label": "Email"
                                    },
                                    {
                                        "name": "Revenues",
                                        "type": "number",
                                        "label": "Revenues"
                                    },
                                    {
                                        "name": "LEAD",
                                        "type": "text",
                                        "label": "LEAD"
                                    }
                                ]
                            }
                        }
                    ]
                }
            ]
        }
    ],	
    "metadata": {
        "instant": false,
        "version": 1,
        "scenario": {
            "roundtrips": 1,
            "maxErrors": 3,
            "autoCommit": true,
            "autoCommitTriggerLast": true,
            "sequential": false,
            "slots": null,
            "confidential": false,
            "dataloss": false,
            "dlq": true,
            "freshVariables": false
        },
        "designer": {
            "orphans": []
        },
        "zone": "eu2.make.com",
        "notes": []
    }
}
