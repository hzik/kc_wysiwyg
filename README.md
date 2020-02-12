# Quill WYSIWYG editor
This Kontent custom element is based on the https://quilljs.com/ rich text editor.
It stores content in JSON format, so it's omni-channel friendly :)

![screenshot](https://amend.cz/wysiwyg/quill.png)

## Quick Setup (for testing)

You can get started quickly using the currently version currently deployed to GitHub Pages. I do not recommend using this for anything other than **quick testing only**.

## Deploying

Netlify has made this easy. If you click the deploy button below, it will guide you through the process of deploying it to Netlify and leave you with a copy of the repository in your GitHub account as well.

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/hzik/kc_wysiwyg)

## JSON Parameters

For RTL support specify the Parameters {JSON} part of the configuration with:

```Json
{
    "rtl": true
}
```

## What is Saved?

The JSON object returned from the Deliver API matches the following signature:

```Json
{
   "ops":[ 
      { 
         "attributes":{ 
            "size":"huge"
         },
         "insert":"Hello World!"
      },
      { 
         "insert":"\n"
      },
      { 
         "insert":{ 
            {"item":{
                "codename":"testing_name",
                "id":"e8015d16-61f9-41d4-ab30-fec7b910ff0d",
                "name":"testing name"
                }
             }
         }
      },
      { 
         "attributes":{ 
            "underline":true,
            "color":"#e60000",
            "bold":true
         },
         "insert":"Image asset:"
      },
      { 
         "insert":"\n"
      },
      { 
         "insert":{ 
            "image":"https://assets-us-01.kc-usercontent.com/1f33698f-a270-4b2d-90c5-9658a99c3140/327d63ce-c56f-4e86-950d-dd0747470660/f6e49c5bb987a4a1b11e2d344f58d745.jpg"
         }
      },
      { 
         "insert":"\n"
      }
   ]
}
```

