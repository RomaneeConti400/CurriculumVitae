# CV

## Name and Surname
Sergey Stykalskiy 

## Contacts
- Phone: +375(29)691887
- Email: romaneeconti400@mail.ru
- GitHub: 
- Telegram: @grantarina 
- Vk: https://vk.com/sho_ron

## About Me
Dedicated and detail-oriented second-year BRU student majoring in software engineering. Constantly improving my programming skills by writing applications for personal use. My hobbies are playing music and cooking. I am interested in AI and robotics.

## Skills
Hard skills:

  - Programming languages: C# and JavaScript
  -  Version control systems: Git
  -  Development tools: Visual Studio, Visual Studio Code, PyCharm, Adobe Photoshop, Figma, Enterprise Architect, Sql server, Blender, and UE4.

Soft skills:

- Communication: The ability to effectively convey information and ideas to others through various mediums, such as speaking, writing, and listening.

- Collaboration: The capacity to work cooperatively with others, fostering teamwork, and contributing to the achievement of shared goals.

- Adaptability: The willingness and ability to adjust to new situations, environments, and changes with flexibility, resilience, and a positive attitude.

- Problem-solving: The capability to identify, analyze, and find solutions to complex problems by employing critical thinking, creativity, and logical reasoning.

- Time management: The skill of effectively organizing and prioritizing tasks, setting goals, and managing one's time to optimize productivity and meet deadlines.

- Leadership: The ability to inspire, motivate, and guide individuals or teams towards achieving objectives, while demonstrating integrity and responsibility.

- Emotional intelligence: The capacity to recognize, understand, and manage one's own emotions and empathize with others, leading to improved relationships and effective interpersonal interactions.

- Conflict resolution: The skill of addressing and resolving disagreements or conflicts constructively, seeking common ground and maintaining positive relationships.

## Code example
```C#
//C#
public List<object> ReadDatabase(string filePath)
        {
            List<object> database = new List<object>();

            try
            {
                string[] lines = File.ReadAllLines(filePath);

                foreach (string line in lines)
                {
                    object obj = CreateObjectFromLine(line);
                    if (obj != null)
                    {
                        database.Add(obj);
                    }
                }
            }
            catch (IOException e)
            {
                throw new Exception("Ошибка чтения БД.", e);
            }

            return database;
        }

        private object CreateObjectFromLine(string line)
        {
            string[] parts = line.Split(':');
            if (parts.Length != 2)
            {
                throw new Exception("Некорректный формат строки: " + line);
            }

            string objectType = parts[0].Trim();
            string[] parameters = parts[1].Split(',');

            switch (objectType)
            {
                case "PropellantWeapon":
                    return CreatePropellantWeapon(parameters);

                case "MechanicalWeapon":
                    return CreateMechanicalWeapon(parameters);

                case "StrikeWeapon":
                    return CreateStrikeWeapon(parameters);

                case "StabbingWeapon":
                    return CreateStabbingWeapon(parameters);

                case "ChoppingWeapon":
                    return CreateChoppingWeapon(parameters);

                default:
                    throw new Exception("Некорректное  название класса: " + objectType);
            }
       }  
```

## Work experience and training projects

### Project: ObiumProject
- Link to [project](https://obiumproject.github.io/index.html)
- Skills used: The basics of graphic design, HTML, CSS, JavaScript, Bootstrap
### Order: A virtual tour of the polling station 
- [Screenshot](/img/gp.png)
- Skills used: The basics of graphic design, 3D modeling basics, UE4, Blender.

## English
The level of English is B1. I speak English well enough to read documentation, communicate and learn new technologies.

## Photo
![photo](/img/me.jpg "Моё фото")