# VaryStrongData
Open source database of exercises and equipment

## Directory Structure

`exercises/` - Holds data about exercises  
`exercises/<id>/` - Holds data about the exercise with that ID  
`exercises/<id>/info.json`
`exercises/<id>/symbol.svg` - SVG graphic intended for a thumbnail/status/quick depiction of this exercise  
`exercises/<id>/progression.`  
`exercises/<id>/activation_chart.svg` - 

`exercises/default/symbol.svg` - Default SVG graphic for when an exercise lacks it's own symbol

`equipment/` - Holds data about equipment  
`equipment/<id>/` - Holds data for a specific piece of equipment   
`equipment/<id>/info.json`  
`equipment/<id>/symbol.svg` - SVG graphic intended for a thumbnail/status/quick depiction of this equipment  
`equipment/<id>/photo.jpg` - A real photo of this type of equipment  

`equipment/default/symbol.svg` - Default SVG graphic for when an equipment lacks it's own symbol  
`equipment/default/photo.jpg` - Default photo for when an equipment lacks it's own photo  

`disciplines.csv` - A list of athletic disciplines/programs/techniques referenced in this database    
`athletic_targets.csv` - A list of athletic targets referenced in this database    

`docs/` - A directory containing information about how to use this database and how to contribute  

## Exercise Info File

The `info.json` file for an exercise will have the following fields:

|Field | Description | Type |
| ---:| --- |:--- |
|`id`| ID of this exercise in the VaryStrongData database. | `int` |
|`canonicalName` | Unique name assigned to this exercise within the VaryStrongData database. An exercise may commonly go by other names, but this is the name used within VaryStrongData for linking between exercises | `string`|
|`alternateNames` | Other common names used to refer to this exercise. | `string[]` |
|`prescribeTime` | Whether or not this exercise is usually prescribed in timed intervals. For example, a 1 minute plank or running for a half hour| `boolean` |
|`prescribeWeight` | Whether or not this exercise is usually prescribed with weight. For example, barbell bench press or kettle bell swings | `boolean`|
|`prescribeDistance` | Whether or not this exercise is usually prescribed with a distance. For example, a 2 mile run or 100 yard sprints. | `boolean`|
|`athleticTargets` | A list of athletic goals that this exercise is usually used for. For example, endurance for long runs, or strength for barbell back squats. | `string[]`|
|`disciplines` | A list of athletic disciplines/programs/techniques that utilitze this exercise. For example, strength training for bench press. | `string[]`|
|`variations` | A list of canonical names of other exercises that can be considered a variation of this exercise. | `string[]` |
|`variationOf` | A list of canonical names of other exercises that this exercise can be considered as a variation of. | `string[]` |

## Equipment Info File

The `info.json` file for equipment will have the following rules:

|Field | Description | Type |
| ---: | --- | :--- |
|`id`| ID of this equipment in the VaryStrongData database. | `int` |
|`canonicalName` | Unique name assigned to this equipment within the VaryStrongData database. Equipment may go by other names, but this is the name used within the VaryStrongData for linking between exercises. | `string` |
|`alternateNames` | Other common names used to refer to this equipment. | `string[]` |

