# Documentation Repo
This just shows how it is done

## Pages
1. Create the docs folder by create file docs/readme.md (go ahead, type the path in the create file box and it will create folder structure for you)
2. Goto repo settings
3. Wander down to Pages and choose base on /docs and choose a theme.

You are done for the basics, for example page for this repo is here : http://petegcole.github.io/Documentation/

What you can note is that it starts with readme.md and you can link between documents like this:

```
[a link](linkedtodoc.md)
```
The Jekyl engine then sorts it all out.

Using a custpm domain name is left as an exercise for the reader.

## Books

Just one book per repository, thats if you want the source to the book linked to the GitHub Repository which kind of makes sense if you want to keep everything together. At the end of the day, books are just pages with a different theme and with a fancier editor. 

If you're going to mix in a 'book of truth' (as the US SATS guide was known as in our house when kids were prepping for application to US Universities, oh the irony of "truth"!) with your repository then you are not going to want the default behaviour as it will polute the root folder with too much gibberish (just  personal opinion thing). So ...

1. At GitBook, create an 'empty' book.
2. At Github, create a folder called docs.
2. create a file book.json in the root of the GitHub repo, copy the book.jspn from your GitBook book and add "root" (it will look like this assuming you want an API theme):
```js
{
    "plugins": [ "theme-api" ],
    "pluginsConfig": {
        "theme-api": {
            "languages": [
                {
                    "lang": "js",
                    "name": "JavaScript",
                    "default": true
                }
            ]
        }
    },
    "root": "./book"
}
```
3. In docs folder, create readme.md, and summary.md and a file or two from the book you created
4. Back at Gitbook, on the book, choose settings and the GitHub, then choose the repo you are working in.
5. Gitbook will go bananas that the sync failed, choose Sync from Github. 

Eventually all will be well and you will be up and running.




