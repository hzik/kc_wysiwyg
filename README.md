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
         "insert":"Hello Wrold!\n"
      },
      { 
         "insert":{ 
            "image":"https://somedomain/someimage.png"
         }
      },
      { 
         "insert":"\n"
      }
   ]
}
```

