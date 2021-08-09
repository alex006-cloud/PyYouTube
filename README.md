# PyYouTube 

<p align="center">
  <a href="https://www.python.org">
    <img src="https://tg-link.herokuapp.com/dl/0/AgADkawxG1bbiVQ.jpg">

  </a>


Get Video Data from YouTube link 

## Installation 
```bash
pip install PyYouTube
```

## How to use it ?
#### Get Videos Data 

```python
from pyyoutube import Data
yt = Data("https://youtu.be/HhHzCfrqsoE")
print(yt.data)
```
>Example Result
```json
{
  "id": "HhHzCfrqsoE",
  "title": "How To Create MongoDB Database  Url",
  "thumbnails": "https://i.ytimg.com/vi/HhHzCfrqsoE/hqdefault.jpg?sqp=-oaymwEiCKgBEF5IWvKriqkDFQgBFQAAAAAYASUAAMhCPQCAokN4AQ==\\u0026rs=AOn4CLBOkJZAdEpYxQOVdaUxFHdbThH_DQ",
  "views": "91",
  "likes": "11",
  "dislikes": "No",
  "publishdate": "2021-08-04",
  "category": "Howto \\u0026 Style",
  "channel_name": "Ln Technical",
  "subscriber": "1.15K subscribers"
}
```
  
#### Search Videos
> Get videos link 
```python 
from pyyoutube import Search
yt = Search("ln technical")
print(yt.videos)
```
> Example Result
```bash
['https://youtu.be/jEnlga0hYyY', 'https://youtu.be/jEnlga0hYyY', 'https://youtu.be/Fxj5ZpaNq24', 'https://youtu.be/bAyh6FU01ho', 'https://youtu.be/DPCN3abXmsc', 'https://youtu.be/ros6m2BBI84', 'https://youtu.be/jEnlga0hYyY', 'https://youtu.be/hbtfaAx4bBE', 'https://youtu.be/qvBt04Q60Mg', 'https://youtu.be/1T3rAZH4rmw']
```

> Get Video Data 
```python 
from pyyoutube import Search ,Data 
yt = Search("ln technical").videos
for vid in yt:
  res = Data(vid).data
  print(res)
```
>Example Result
```json
[
  {
    "id": "jEnlga0hYyY",
    "title": "Tutorial 1 - History of Infor ERP LN",
    "thumbnails": "https://i.ytimg.com/vi/jEnlga0hYyY/hqdefault.jpg?sqp=-oaymwEiCKgBEF5IWvKriqkDFQgBFQAAAAAYASUAAMhCPQCAokN4AQ==\\u0026rs=AOn4CLC9vnXpG2XmDpNfwZHEBMdo8GVf-A",
    "views": "9957",
    "likes": "80",
    "dislikes": "1",
    "publishdate": "2017-11-07",
    "category": "Education",
    "channel_name": "Infor LN Technical Trainer",
    "subscriber": "935 subscribers"
  },
  {
    "id": "jEnlga0hYyY",
    "title": "Tutorial 1 - History of Infor ERP LN",
    "thumbnails": "https://i.ytimg.com/vi/jEnlga0hYyY/hqdefault.jpg?sqp=-oaymwEiCKgBEF5IWvKriqkDFQgBFQAAAAAYASUAAMhCPQCAokN4AQ==\\u0026rs=AOn4CLC9vnXpG2XmDpNfwZHEBMdo8GVf-A",
    "views": "9957",
    "likes": "80",
    "dislikes": "1",
    "publishdate": "2017-11-07",
    "category": "Education",
    "channel_name": "Infor LN Technical Trainer",
    "subscriber": "935 subscribers"
  }
]
```

#### Search Limits Video 
```python 
from pyyoutube import Search ,Data 
yt = Search("ln technical").videos[:3] #limit [:3]
print(yt)
```
>Example Result 
```bash
['https://youtu.be/jEnlga0hYyY', 'https://youtu.be/jEnlga0hYyY', 'https://youtu.be/Fxj5ZpaNq24']
```
## License 
Copyright (c) 2021 Lntechnical

This repository is licensed under the MIT license.
