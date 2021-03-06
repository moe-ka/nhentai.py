# nhentai.py

## API

`nhentai.get_doujin(id:int) -> Doujin`
<br>
Returns a doujin by given /g/id.
<br>

`nhentai.get_random_id() -> int`
<br>
Returns a random and valid /g/id.
<br>

`nhentai.get_homepage(page:int) -> List[Doujin]`
<br>
Returns a list of the most recently uploaded doujins on the homepage.
<br>

`nhentai.search(query:str, page:int, sort_by:str) -> List[Doujin]` <br>
Returns a list of doujins related to a given [keyword](https://nhentai.net/info/).

`nhentai.search_tagged(tag_id:int, page:int, sort_by:str) -> List[Doujin]`<br>
Returns a list of doujins that have the given tag id.
<br>
<br>


## Examples
### Getting doujin using a /g/id
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
### Getting a random doujin
```
>>> id = nhentai.get_random_id()
>>> id
118927
>>>
>>> nhentai.get_doujin(id).tags
[Tag(id=17249, type='language', name='translated', url='/language/translated/', count=109734), 
...]
```
