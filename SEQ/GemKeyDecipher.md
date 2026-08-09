# 3301 Gematria Keyword (GEMKEY)

A short summary:

> Exploring possible methods to decipher the 3301 - Liber Primus. I found that words can be transformed into sequences of shifts using the Gematria Primus provided by (Cicada) 3301.  It was noticed that within the LP  is a _Mobius Strip_ (unsolved pages of the LP).  I decided to create a function which allows us to convert words into shift sequences in the same style as the twitter username which might then be used to decipher some of the unsolved pages if to be explored further.

_I have not tried this method against any other pages only the runes included in this document._

For us to be able to perform this method we will have to use https://github.com/Taiiwo/cicada Lib with some of our own code.

```python
from cicada.gematria import Latin, Runes
```

GemKey Keyword:

```python
 def CreateGemKeyword(keyword):
     backwards = keyword[:-1]
     return keyword + backwards[::-1]
    # DIVINITYTINIVID
```

 GemKey Sequence:
 ```python
 def GetGemKeySeq(keyword):
     return Latin(CreateGemKey(keyword)).to_numbers()
  # [89, 31, 3, 31, 29, 31, 59, 103, 59, 31, 29, 31, 3, 31, 89]
```
