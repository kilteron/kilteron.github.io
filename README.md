At the moment we do not have a GUI for adding / editing collections / cards. When the GUI is added, all existing json files will be processed automatically and you will see your content in your accounts.

# How to add a new collection
## 1. Clone the repo

```bash
git clone https://github.com/kilteron/kilteron.github.io.git
cd kilteron.github.io
```
## 2. Create a new collection-file 
```[your-name]-[kit]-[collection].json``` E.g. ```alex-braine-javascript-building-7-games.json```

## 3. Add a content
E.g.
```json
{
  "url": "/alex-braine/javascript/building-7-games",
  "title": "Learn JavaScript by Building 7 Games",
  "cards": 7,
  "createdAt": 1586362367,
  "author": "freeCodeCamp.org",
  "source": "https://www.youtube.com/watch?v=lhNdUVh3qCc",
  "children": [
    {
      "title": "JavaScript",
      "children": [
        {
          "title": "Tutorial",
          "children": [
            {
              "title": "Build 7 games",
              "children": [
                {
                  "id": "59a7ab8d-12a0-50df-afdd-738271da8d4f",
                  "title": "Intro",
                  "youtubeId": "lhNdUVh3qCc",
                  "start": 0,
                  "stop": 115
                }
              ]
            }
          ]
        }
      ]
    }
  ]
}
```

## 4. Create a new kit-file

```[your-name]-[kit].json``` E.g. ```alex-braine-javascript.json```

## 4. Add a content
E.g.
```json
{
  "creator": "Alex Braine",
  "title": "JavaScript",
  "url": "/alex-braine/javascript",
  "type": "kit",
  "navigation": [
    {
      "title": "JavaScript",
      "url": "/alex-braine/javascript",
      "children": [
        {
          "title": "Tutorial",
          "url": "/alex-braine/javascript/building-7-games",
          "children": [
            {
              "title": "Build 7 games",
              "url": "/alex-braine/javascript/building-7-games"
            }
          ]
        }
      ]
    }
  ],
  "collections": [
    {
      "url": "/alex-braine/javascript/building-7-games",
      "title": "Learn JavaScript by Building 7 Games",
      "cards": 7,
      "youtubeViews": 379380,
      "youtubeLikes": 12571,
      "createdAt": 1586362367,
      "author": "freeCodeCamp.org",
      "youtubeId": "lhNdUVh3qCc",
      "source": "https://www.youtube.com/watch?v=lhNdUVh3qCc"
    }
  ]
}
```
## 5. Add a kit to kits.json
```json
  {
    "url": "/alex-braine/javascript",
    "title": "JavaScript",
    "description": "Top 15 JavaScript videos, 18M views, 467K likes",
    "cards": 1100,
    "createdAt": 1618078485,
    "logo": "https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Unofficial_JavaScript_logo_2.svg/160px-Unofficial_JavaScript_logo_2.svg.png"
  }
```
## 6. Make sure everything works
Run it on any server
```bash
serve
```
or
```bash
python -m SimpleHTTPServer
```
or
```bash
python3 -m http.server
```
or
```bash
php -S localhost:8000
```

## 7. Create a PR to this repo
After modaration it will be merged and appers on https://kilteron.github.io.