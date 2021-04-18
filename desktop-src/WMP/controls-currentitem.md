---
title: Controls. happtitem
description: Die Eigenschaft "ustitem" gibt das aktuelle Medien Element an oder ruft es ab.
ms.assetid: 77e21585-3cc8-41f5-97b5-da6eb992c7bc
keywords:
- Steuerelemente. Fenster Media Player
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
ms.openlocfilehash: 81658665cb6f31acd327f5050a733a2fc3c70371
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361349"
---
# <a name="controlscurrentitem"></a>Controls. happtitem

Die Eigenschaft " **ustitem** " gibt das aktuelle Medien Element an oder ruft es ab.

``` syntax
player.controls.currentItem
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein **Medien** Objekt mit Lese-/Schreibzugriff.

## <a name="remarks"></a>Bemerkungen

Diese Methode funktioniert nur mit Elementen in *Player*. **currentwiedergabe**. Das Aufrufen von " **happtitem** " mit einem Verweis auf ein gespeichertes Medien Element wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird das Steuer **Element für das** Player-Steuerelement in einem HTML-SELECT-Element auf den ausgewählten Wert festgelegt. Die aktuelle Wiedergabeliste wurde zuerst mithilfe von *playlistcollection* angegeben. **getByName**. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Playlistcollection. getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





