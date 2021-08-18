---
title: Controls.currentItem
description: Die currentItem-Eigenschaft gibt das aktuelle Medienelement an oder ruft es ab.
ms.assetid: 77e21585-3cc8-41f5-97b5-da6eb992c7bc
keywords:
- Controls.currentItem Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentItem
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66dc0ad047213e0fbba7dbdd7336e67b8d015e39aba510ac37bd3701462413ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997550"
---
# <a name="controlscurrentitem"></a>Controls.currentItem

Die **currentItem-Eigenschaft** gibt das aktuelle Medienelement an oder ruft es ab.

``` syntax
player.controls.currentItem
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein  Medienobjekt mit Lese-/Schreibzugriff.

## <a name="remarks"></a>Hinweise

Diese Methode funktioniert nur mit Elementen in *Player*. **currentPlaylist**. Das **Aufrufen von currentItem** mit einem Verweis auf ein gespeichertes Medienelement wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden JScript wird **currentItem** verwendet, um das aktuelle Medienelement des Player-Steuerelements auf den ausgewählten Wert in einem HTML SELECT-Element zu setzen. Die aktuelle Wiedergabeliste wurde zuerst mithilfe von *PlaylistCollection angegeben.* **getByName**. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<SELECT ID = playItem  NAME = "playItem"  LANGUAGE = "JScript"

    /* Specify the current item when the selected list value changes. */
    onChange = "Player.controls.currentItem = Player.currentPlaylist.item(playItem.value);">

    /* Fill the SELECT element list with three items that match
       the songs in the playlist. */
    <OPTION VALUE = 0 >Laure
    <OPTION VALUE = 1 >Jeanne
    <OPTION VALUE = 2 >House
</SELECT>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





