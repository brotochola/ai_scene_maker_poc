ChatGPT prompt:

You are helping me create therapy content in JSON format for my SLP app.

Please generate a JSON file with the following structure:

scene_description: A vivid description of the setting. Make it age-appropriate and include sensory details (colors, sounds, feelings, background). Do not list specific items here. You can use Movie Making language to make it more clear for the AI image generator.

items: A descriptive list of the people, animals, objects, and details visible in the shot. If they are characters add a full description of how they are wearing, their poses, how they look, etc. If they are objects, include their angle, position, etc. The number of items and their detail should match the chosen scene_type (shot type in movie-making language):

Extreme Long Shot (ELS/EWS): many broad details, landscape, multiple groups

Long Shot (LS/WS): whole subject head-to-toe plus surroundings

Medium Shot (MS): subject from waist up plus immediate details

Close-Up (CU): only face or object with 2–4 details

Extreme Close-Up (ECU): one small detail with 1–2 items

scene_type: Copy exactly the shot type provided (e.g., “long shot (shows the entire subject head-to-toe along with their surroundings)”). Always include both the shot name and a short definition in parentheses.

questions: Create 10 multiple-choice questions that match the therapy goal and adjust them accordingly to target that skill.

Also please include in the output, the info you get as input.
Your response json must be formatted like so:

`{
    "input_info": {
        "student_grade": "string (e.g., '10th grade')",
        "theme": [
            "string (theme keyword 1)",
            "string (theme keyword 2)",
            "string (theme keyword 3)"
        ],
        "therapy_goal": "string (e.g., 'sequencing')",
        "scene_type": "string (description of camera angle/shot type)"
    },
    "scene_description": "string (detailed description of the scene setting and atmosphere)",
    "items": [
        "string (description of item/person/activity 1)",
        "string (description of item/person/activity 2)",
        "... (continue with 8-10 items total)"
    ],
    "questions": [
        {
            "question": "string (the question text)",
            "options": [
                "string (option A)",
                "string (option B)", 
                "string (option C)",
                "string (option D)"
            ],
            "answer": "string (the correct answer, must match one of the options exactly)"
        }
        // Repeat this question object structure 
    ]
}`

---

{"student_grade": "3rd grade", "theme": ["snowboarding", "snow", "winter"], "therapy_goal": "Semantics-wh-questions-mixed", "scene_type":"long shot"}

---

Nano Banana prompt:

Generate a photorealistic image based on the JSON file provided. Use scene_description as the main scaffold for the setting, including colors, lighting, and atmosphere. Include all items listed, accurately represented with proper scale, proportion, and detail, each being a single thing, you are not allowed to fuse 2 Items together in the image. Position the camera according to scene_type, as if it were a movie shot, so all items and relevant details for the questions are clearly visible. Ensure that any objects or characters needed to answer the questions can be easily identified in the image. Maintain realism, coherence, and spatial consistency throughout.
Make sure the questions must be answered by just looking at the picture. So the priority, in case you cannot add all the items to the scene, are the items that are referenced by the questions and their right answer
