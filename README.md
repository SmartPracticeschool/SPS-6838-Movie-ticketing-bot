# SPS-6838-Movie-ticketing-bot
Movie ticketing bot

Preview Link 

https://web-chat.global.assistant.watson.cloud.ibm.com/preview.html?region=us-south&integrationID=c44a5175-0f2d-4ca1-852c-d2bb06e63753&serviceInstanceID=fe21989f-f0bb-4c41-b5c9-85b17acef0df

Nodered URL link

https://node-red-omqvn-2020-10-23.eu-gb.mybluemix.net/ui/#!/0?socketid=QF1enEgwC8MVKor1AAAE


Project Document
1 INTRODUCTION
 
Today, many people are following e-commerce website for purchasing products.But sometimes  the quality of the  customer service that they provide is not so good. The customers have to wait for a long time to get a response from the buisness models. So to overcome this problem a solution is proposed which is called as a Chatbot. The Chatbot automatically gives immediate responses to the users queries based on the common questions which are frequently asked by them.Some template based questions like greetings and general questions are answered by Chatbot.
 
  1.1  Overview
 
In this project, a chatbot is developed using Watson assistant. This Chatbot provides following capabilities:
1.	Generates the list of movies available
2.	Different show timings
3.	Respective Ticket Prices as per the Type of Ticket.
4.	The bot is in the position to book tickets.
 
  1.2  Purpose
 
The purpose of a Chatbot is to give immediate responses to the users  Frequently Answered Questions (FAQs) and provide services efiiciently.
 
 
2 LITERATURE SURVEY
 
Many researchers have implemented a Chatbot system. One following research is considered here where they have created chatbot for movie booking using NLP.
1)Chatbot Implementation for Movie Booking Using NLP, Ms. Deepika Borade , Dr. Sachin Bojewar[1] have proposed a Chatbot which automatically gives immediate responses to the users queries using Natural language Processing (NLP) and Latent Semantic Analysis (LSA). 
 
  2.1  Existing problem
 
In traditional approach, means the ticket window where people are used to wait for booking tickets. So waiting time is one of the problem which occurs with traditional method.
  2.2  Proposed solution
 
Here a Movie Ticketing chatbot is proposed which automatically gives immediate responses to the users based on the Frequently Answered Questions (FAQs) and booked tickets.
 
 
3 THEORITICAL ANALYSIS
 
  3.1  Block diagram
 



 

Dia. 1 Block Diagram





  3.2  Hardware / Software designing
 
 

 

 

Dia 2. Flow diagram of Node Red Application
 
Above diagram shows the flow of working where assistant component plays very important role. When we integrate IBM watson assistant with node red application then deploy this flow.   
 
 
 
Dia. 3 Project Description


4 EXPERIMENTAL INVESTIGATIONS

5  FLOWCHART
 

  
 
                                                               Dia. 4 Flow Chart




6 RESULT
Preview Link output


  
 
 


 
  
 
Project output


       


  






        
 

7 ADVANTAGES & DISADVANTAGES
 
Advantages: 
1) Easy and quick to do
2) You can book tickets in advance without travelling
3) You can gets the information about other movies also
4) You can access more information
 
Disadvantages: 
1) Need to have knowledge about online transaction
2) Need to have credit card or similar type of payment entity
3) If website for the same is down then you will not be able to book tickets.
 
8 APPLICATIONS
 
Online Movie Booking Application
 
 
 
 
9 CONCLUSION
 
Chatbot is one of the simpler, easier and more interactive user interface. So the movie ticketing bot helps users to book tickets online more efficiently. The system can move from the traditional method like window booking to Chatbot for better experience with the help of automated movie ticketing bot. An IBM watson assistant services and their integration with Node red application helps to create this bot more efficiently. 
  
 
10 FUTURE SCOPE
 
Further enhancements can also be there through which this movie ticketing bot becomes more automated. 
 
 
11 BIBILOGRAPHY
 
1. "Chatbot Implementation for Movie Booking Using NLP", Ms. Deepika Borade , Dr. Sachin Bojewar,International Journal of Advance Engineering and Research Development Volume 6, Issue 03, March -2019.
 
 
 
APPENDIX
 
  A. Source code
Chat Bot JSON File
{
  "intents": [
    {
      "intent": "Enquiry",
      "examples": [
        {
          "text": "Are Tickets Available?"
        },
        {
          "text": "What is the price for Tickets of specific category?"
        },
        {
          "text": "Which Type of Tickets are avilable?"
        }
      ],
      "description": ""
    },
    {
      "intent": "Greetings",
      "examples": [
        {
          "text": "Good afternoon"
        },
        {
          "text": "Good evening"
        },
        {
          "text": "Good morning"
        },
        {
          "text": "Hello"
        },
        {
          "text": "Hey"
        },
        {
          "text": "Hi"
        }
      ],
      "description": ""
    },
    {
      "intent": "Orders",
      "examples": [
        {
          "text": "Book my seats"
        },
        {
          "text": "Book my show"
        },
        {
          "text": "Give me tickets"
        },
        {
          "text": "Show me tickets"
        }
      ],
      "description": ""
    }
  ],
  "entities": [
    {
      "entity": "Enquiry",
      "values": [
        {
          "type": "synonyms",
          "value": "List of Movies",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "Offers",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "Options",
          "synonyms": [
            "Types of Tickets"
          ]
        },
        {
          "type": "synonyms",
          "value": "Ticket Price",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "Time Slots",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "Timings",
          "synonyms": []
        }
      ],
      "fuzzy_match": true
    },
    {
      "entity": "Greetings",
      "values": [
        {
          "type": "synonyms",
          "value": "Good afternoon",
          "synonyms": [
            "gd afternoon",
            "gd noon",
            "noon"
          ]
        },
        {
          "type": "synonyms",
          "value": "Good evening",
          "synonyms": [
            "evening",
            "gd eve",
            "gd evng"
          ]
        },
        {
          "type": "synonyms",
          "value": "Good morning",
          "synonyms": [
            "gd morning",
            "gd mrng",
            "gm",
            "morning"
          ]
        }
      ],
      "fuzzy_match": true
    },
    {
      "entity": "ListOfMovies",
      "values": [
        {
          "type": "synonyms",
          "value": "ChakdeIndia",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "Dangal",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "Uri",
          "synonyms": []
        }
      ],
      "fuzzy_match": true
    },
    {
      "entity": "sys-number",
      "values": [],
      "fuzzy_match": true
    },
    {
      "entity": "Ticket_Price",
      "values": [
        {
          "type": "synonyms",
          "value": "100",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "300",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "500",
          "synonyms": []
        }
      ],
      "fuzzy_match": true
    },
    {
      "entity": "Ticket_Types",
      "values": [
        {
          "type": "synonyms",
          "value": "Gold",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "Platinum",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "Silver",
          "synonyms": []
        }
      ],
      "fuzzy_match": true
    },
    {
      "entity": "Timing",
      "values": [
        {
          "type": "synonyms",
          "value": "1.00 pm",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "11.00 am",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "9.00 am",
          "synonyms": []
        }
      ],
      "fuzzy_match": true
    },
    {
      "entity": "Timings",
      "values": [],
      "fuzzy_match": true
    }
  ],
  "metadata": {
    "api_version": {
      "major_version": "v2",
      "minor_version": "2018-11-08"
    }
  },
  "dialog_nodes": [
    {
      "type": "standard",
      "title": "Anything else",
      "output": {
        "generic": [
          {
            "values": [
              {
                "text": "I didn't understand. You can try rephrasing."
              },
              {
                "text": "Can you reword your statement? I'm not understanding."
              },
              {
                "text": "I didn't get your meaning."
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "conditions": "anything_else",
      "dialog_node": "Anything else",
      "previous_sibling": "node_4_1602998176332",
      "disambiguation_opt_out": true
    },
    {
      "type": "event_handler",
      "output": {
        "text": {
          "values": [
            "Enter Number of  Tickets"
          ],
          "selection_policy": "sequential"
        }
      },
      "parent": "slot_6_1602998736716",
      "event_name": "focus",
      "dialog_node": "handler_10_1602998736721",
      "previous_sibling": "handler_1_1602998736721"
    },
    {
      "type": "event_handler",
      "output": {},
      "parent": "slot_6_1602998736716",
      "context": {
        "s": "@sys-number"
      },
      "conditions": "@sys-number",
      "event_name": "input",
      "dialog_node": "handler_1_1602998736721"
    },
    {
      "type": "event_handler",
      "output": {},
      "parent": "slot_6_1603519376600",
      "context": {
        "ListOfMovies": "@ListOfMovies"
      },
      "conditions": "@ListOfMovies",
      "event_name": "input",
      "dialog_node": "handler_1_1603519376609"
    },
    {
      "type": "event_handler",
      "output": {
        "generic": [
          {
            "values": [
              {
                "text": "List of Movies:  Uri Dangal ChakDeIndia"
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "parent": "slot_6_1603519376600",
      "event_name": "focus",
      "dialog_node": "handler_2_1603519376609",
      "previous_sibling": "handler_1_1603519376609"
    },
    {
      "type": "event_handler",
      "output": {
        "text": {
          "values": [
            "Enter Timing  9.00am   11.00am   1.00pm"
          ],
          "selection_policy": "sequential"
        }
      },
      "parent": "slot_10_1603523125589",
      "event_name": "focus",
      "dialog_node": "handler_2_1603523125597",
      "previous_sibling": "handler_8_1603523125597"
    },
    {
      "type": "event_handler",
      "output": {},
      "parent": "slot_4_1602999843176",
      "context": {
        "Ticket_Types": "@Ticket_Types"
      },
      "conditions": "@Ticket_Types",
      "event_name": "input",
      "dialog_node": "handler_4_1602999843184"
    },
    {
      "type": "event_handler",
      "output": {
        "text": {
          "values": [
            "Enter Type of Ticket  Gold Silver Platinum , Ticket Price are Gold-500Rs Silver-200Rs Platinum-200Rs",
            ""
          ],
          "selection_policy": "sequential"
        }
      },
      "parent": "slot_4_1602999843176",
      "event_name": "focus",
      "dialog_node": "handler_5_1602999843184",
      "previous_sibling": "handler_4_1602999843184"
    },
    {
      "type": "event_handler",
      "output": {},
      "parent": "slot_10_1603523125589",
      "context": {
        "Timing": "@Timing"
      },
      "conditions": "@Timing",
      "event_name": "input",
      "dialog_node": "handler_8_1603523125597"
    },
    {
      "type": "standard",
      "title": "Deleting the context variables",
      "output": {
        "deleted": "<?context.remove('Ticket_Types')?><?context.remove('s')?><?context.remove('ListOfMovies')?><?context.remove('Timing')?>",
        "generic": [
          {
            "values": [],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "parent": "node_4_1602998176332",
      "conditions": "true",
      "dialog_node": "node_10_1603000116073"
    },
    {
      "type": "standard",
      "title": "Greetings Node",
      "metadata": {
        "_customization": {
          "mcr": true
        }
      },
      "conditions": "#Greetings || @Greetings",
      "dialog_node": "node_1_1602973400039",
      "previous_sibling": "Welcome"
    },
    {
      "type": "standard",
      "title": "Enquiry",
      "metadata": {
        "_customization": {
          "mcr": true
        }
      },
      "conditions": "@Enquiry",
      "dialog_node": "node_1_1602977414301",
      "previous_sibling": "node_1_1602973400039"
    },
    {
      "type": "frame",
      "title": "Order ",
      "output": {
        "generic": [
          {
            "values": [],
            "response_type": "text",
            "selection_policy": "sequential"
          },
          {
            "values": [
              {
                "text": "Your $s $Ticket_Types Tickets are booked for movie $ListOfMovies at $Timing"
              },
              {
                "text": ""
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "next_step": {
        "behavior": "skip_user_input"
      },
      "conditions": "#Orders",
      "dialog_node": "node_4_1602998176332",
      "previous_sibling": "node_1_1602977414301"
    },
    {
      "type": "response_condition",
      "output": {
        "generic": [
          {
            "title": "",
            "options": [
              {
                "label": "Uri",
                "value": {
                  "input": {
                    "text": ""
                  }
                }
              },
              {
                "label": "ChakDeIndia",
                "value": {
                  "input": {
                    "text": ""
                  }
                }
              },
              {
                "label": "Dangal",
                "value": {
                  "input": {
                    "text": ""
                  }
                }
              }
            ],
            "response_type": "option"
          }
        ]
      },
      "parent": "node_1_1602977414301",
      "conditions": "@Enquiry:(List of Movies)",
      "dialog_node": "response_10_1603004926414",
      "previous_sibling": "response_1_1603003993383"
    },
    {
      "type": "response_condition",
      "output": {
        "generic": [
          {
            "title": "Ticket",
            "options": [
              {
                "label": "Gold ",
                "value": {
                  "input": {
                    "text": "High"
                  }
                }
              },
              {
                "label": "Silver",
                "value": {
                  "input": {
                    "text": "Medium"
                  }
                }
              },
              {
                "label": "Others",
                "value": {
                  "input": {
                    "text": "Low"
                  }
                }
              }
            ],
            "description": "Types",
            "response_type": "option"
          }
        ]
      },
      "parent": "node_1_1602977414301",
      "conditions": "@Enquiry:Options",
      "dialog_node": "response_1_1602977512064"
    },
    {
      "type": "response_condition",
      "output": {
        "generic": [
          {
            "title": "",
            "options": [
              {
                "label": "Gold-500",
                "value": {
                  "input": {
                    "text": "500"
                  }
                }
              },
              {
                "label": "Silver-300",
                "value": {
                  "input": {
                    "text": "300"
                  }
                }
              },
              {
                "label": "Platinum-100",
                "value": {
                  "input": {
                    "text": "100"
                  }
                }
              }
            ],
            "response_type": "option"
          }
        ]
      },
      "parent": "node_1_1602977414301",
      "conditions": "@Enquiry:(Ticket Price)",
      "dialog_node": "response_1_1603003993383",
      "previous_sibling": "response_9_1602978242122"
    },
    {
      "type": "response_condition",
      "output": {
        "generic": [
          {
            "values": [
              {
                "text": "evening"
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "parent": "node_1_1602973400039",
      "conditions": "@Greetings:(Good evening)",
      "dialog_node": "response_2_1602975357862",
      "previous_sibling": "response_8_1602975246887"
    },
    {
      "type": "response_condition",
      "output": {
        "generic": [
          {
            "values": [
              {
                "text": "Good afternoon"
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "parent": "node_1_1602973400039",
      "conditions": "@Greetings:(Good afternoon)",
      "dialog_node": "response_2_1602975372013",
      "previous_sibling": "response_2_1602975357862"
    },
    {
      "type": "response_condition",
      "output": {
        "generic": [
          {
            "title": "Timings",
            "options": [
              {
                "label": "9.00am",
                "value": {
                  "input": {
                    "text": ""
                  }
                }
              },
              {
                "label": "11.ooam",
                "value": {
                  "input": {
                    "text": ""
                  }
                }
              },
              {
                "label": "1.oopm",
                "value": {
                  "input": {
                    "text": ""
                  }
                }
              }
            ],
            "description": "Time",
            "response_type": "option"
          }
        ]
      },
      "parent": "node_1_1602977414301",
      "conditions": "@Enquiry:(Time Slots)",
      "dialog_node": "response_5_1602978024635",
      "previous_sibling": "response_1_1602977512064"
    },
    {
      "type": "response_condition",
      "output": {
        "generic": [
          {
            "values": [
              {
                "text": "Hey Hello Have a nice day"
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "parent": "node_1_1602973400039",
      "conditions": "anything_else",
      "dialog_node": "response_5_1602978306845",
      "previous_sibling": "response_2_1602975372013"
    },
    {
      "type": "response_condition",
      "output": {
        "generic": [
          {
            "values": [
              {
                "text": "Good morning"
              },
              {
                "text": "Good evening"
              },
              {
                "text": "Good morning"
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "parent": "node_1_1602973400039",
      "conditions": "@Greetings:(Good morning)",
      "dialog_node": "response_8_1602975246887"
    },
    {
      "type": "response_condition",
      "output": {
        "generic": [
          {
            "values": [
              {
                "text": "10%Discount on 3 tickets"
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "parent": "node_1_1602977414301",
      "conditions": "@Enquiry:Offers",
      "dialog_node": "response_9_1602978242122",
      "previous_sibling": "response_5_1602978024635"
    },
    {
      "type": "slot",
      "output": {},
      "parent": "node_4_1602998176332",
      "variable": "$Timing",
      "dialog_node": "slot_10_1603523125589",
      "previous_sibling": "slot_4_1602999843176"
    },
    {
      "type": "slot",
      "output": {},
      "parent": "node_4_1602998176332",
      "variable": "$Ticket_Types",
      "dialog_node": "slot_4_1602999843176",
      "previous_sibling": "slot_6_1602998736716"
    },
    {
      "type": "slot",
      "parent": "node_4_1602998176332",
      "variable": "$s",
      "dialog_node": "slot_6_1602998736716",
      "previous_sibling": "slot_6_1603519376600"
    },
    {
      "type": "slot",
      "output": {},
      "parent": "node_4_1602998176332",
      "variable": "$ListOfMovies",
      "dialog_node": "slot_6_1603519376600",
      "previous_sibling": "node_10_1603000116073"
    },
    {
      "type": "standard",
      "title": "Welcome",
      "output": {
        "generic": [
          {
            "values": [
              {
                "text": "Hello. How can I help you?"
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "conditions": "welcome",
      "dialog_node": "Welcome"
    }
  ],
  "counterexamples": [],
  "system_settings": {
    "off_topic": {
      "enabled": true
    },
    "disambiguation": {
      "prompt": "Did you mean:",
      "enabled": true,
      "randomize": true,
      "max_suggestions": 5,
      "suggestion_text_policy": "title",
      "none_of_the_above_prompt": "None of the above"
    },
    "system_entities": {
      "enabled": true
    },
    "human_agent_assist": {
      "prompt": "Did you mean:"
    },
    "spelling_auto_correct": true
  },
  "learning_opt_out": false,
  "name": "Movie Ticketing Bot",
  "language": "en",
  "description": ""
}
 
NodeRed Json File
 
[{"id":"2d57220.49511de","type":"tab","label":"Flow 2","disabled":false,"info":""},{"id":"9e9156c5.f83938","type":"ui_form","z":"2d57220.49511de","name":"","label":"","group":"93943817.fdd3f8","order":0,"width":0,"height":0,"options":[{"label":"Enter your input","value":"input","type":"text","required":true,"rows":null}],"formValue":{"input":""},"payload":"","submit":"submit","cancel":"cancel","topic":"","x":160,"y":200,"wires":[["9f41299f.5852d8"]]},{"id":"9f41299f.5852d8","type":"function","z":"2d57220.49511de","name":"","func":"msg.payload= msg.payload.input;\nreturn msg;","outputs":1,"noerr":0,"x":340,"y":220,"wires":[["c1d2a201.f63c","abfadeea.ec376"]]},{"id":"c1d2a201.f63c","type":"watson-conversation-v1","z":"2d57220.49511de","name":"","workspaceid":"0a199a54-cbb6-483a-8e1f-eb5d7a191ed7","multiuser":false,"context":true,"empty-payload":false,"service-endpoint":"https://api.eu-gb.assistant.watson.cloud.ibm.com/instances/db4304a8-5975-4965-8343-f8878129d326","timeout":"","optout-learning":false,"x":420,"y":360,"wires":[["7cb78b0b.4d0f84","8dbdbf57.08834"]]},{"id":"8dbdbf57.08834","type":"function","z":"2d57220.49511de","name":"","func":"if(msg.payload.output.generic[0].response_type==\"image\"){\n    msg.url = msg.payload.output.generic[0].source\n    msg.payload = msg.payload.output.generic[0].title\n}\nelse{\n    msg.url=\"https://t3.ftcdn.net/jpg/02/20/14/38/240_F_220143804_fc4xRygvJ8bn8JPQumtHJieDN4ORNyjs.jpg\"\n    msg.payload = msg.payload.output.text[0];\n}\nreturn msg;","outputs":1,"noerr":0,"x":550,"y":280,"wires":[["7cb78b0b.4d0f84","10b0576f.e72fb9","e0480af3.79e1a8","6e409a58.f3a404"]]},{"id":"7cb78b0b.4d0f84","type":"debug","z":"2d57220.49511de","name":"","active":true,"tosidebar":true,"console":false,"tostatus":false,"complete":"false","x":600,"y":420,"wires":[]},{"id":"10b0576f.e72fb9","type":"ui_template","z":"2d57220.49511de","group":"93943817.fdd3f8","name":"","order":5,"width":"6","height":"5","format":"<img ng-src={{msg.url}} alt=\"Image\">","storeOutMessages":true,"fwdInMessages":true,"resendOnRefresh":true,"templateScope":"local","x":800,"y":200,"wires":[[]]},{"id":"e0480af3.79e1a8","type":"ui_audio","z":"2d57220.49511de","name":"","group":"93943817.fdd3f8","voice":"de-DE","always":"","x":780,"y":340,"wires":[]},{"id":"abfadeea.ec376","type":"ui_text","z":"2d57220.49511de","group":"93943817.fdd3f8","order":2,"width":0,"height":0,"name":"","label":"text","format":"{{msg.payload}}","layout":"row-spread","x":260,"y":520,"wires":[]},{"id":"6e409a58.f3a404","type":"ui_text","z":"2d57220.49511de","group":"93943817.fdd3f8","order":2,"width":0,"height":0,"name":"","label":"text","format":"{{msg.payload}}","layout":"row-spread","x":830,"y":420,"wires":[]},{"id":"93943817.fdd3f8","type":"ui_group","z":"","name":"UI","tab":"937a2928.80b0a8","order":1,"disp":true,"width":"6","collapse":false},{"id":"937a2928.80b0a8","type":"ui_tab","z":"","name":"Chatbot","icon":"dashboard","disabled":false,"hidden":false}]
 
 








