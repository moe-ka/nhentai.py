# nhentai.py

## API

`nhentai.get_doujin(id:int)`
<br>
Get a doujin by its /g/id.
<br>

`nhentai.get_homepage(page:int)`
<br>
Get the list of the most recently uploaded doujins on the homepage.
<br>

`nhentai.search(query:str, page:int, sort_by:str)` <br>
Looks for doujins related to a given [keyword](https://nhentai.net/info/).

`nhentai.search_tagged(tag_id:int, page:int, sort_by:str)`<br>
Looks for doujins that have the given tag id.
<br>
<br>


## Examples
### Getting doujin by an id
```
>>> d = nhentai.get_doujin(123)
>>>
>>> # URL to first page's image.
>>> d[0].url 
'https://i.nhentai.net/galleries/635/1.jpg'
>>>
>>> d.__dict__
{'id': 123, 
'media_id': '635',
'thumbnail': 'https://t.nhentai.net/galleries/635/thumb.jpg',
'cover': 'https://t.nhentai.net/galleries/635/cover.jpg'}
'titles': {'english': '(C69) [Nakayohi Mogudan (Mogudan)] Omakehon 2005 (Neon Genesis Evangelion)', 'japanese': '(C69) [なかよひモグダン (モグダン)] おまけ本 2005 (新世紀エヴァンゲリオン)', 'pretty': 'Omakehon 2005'},
'tags': [Tag(id=17202, type='artist', name='mogudan', url='/artist/mogudan/', count=213)
...
```
