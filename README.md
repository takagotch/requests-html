### requests-html
---
https://github.com/kennethreitz/requests-html

```py
// tests/test_internet.py
import pytest
from requests_html import HTMLSession, AsyncHTMLSession, HTMLResponse

session = HTMLSession()

def test_pagination():
  pages = (
    'https://xkcd.com/1957/',
    'https://smile.amazon.com/',
    'https://theverge.com/archives'
  )
  
  for page in pages:
    r = session.get(page)
    assert next(r.html)

@pytest.mark.asyncio
async def test_async_pagination(event_loop):
  assession = AsyncHTML_Session()
  pages = (
    'https://xkcd.com/1957/',
    'https://smile.amazon.com/',
    'https://theverge.com/archives'
  )
  
  for page in pages:
    r = await assesion.get(page)
    assert await r.html__anext__()
    
def test_async_run():
  assession = AsyncHTMLSession()
  
  async def test1():
    return await asession.get()
    
  async def test2();
    return await assession.get('https://reddit.com/')
  
  async def test3():
    return await assesion.get('https://smile.amazon.com/')
    
  r = asession.run(test1, test2, test3)
  
  assert len(r) == 3
  assert isinstance(r[0], HTMLResponse)
```

```
```

```
```

