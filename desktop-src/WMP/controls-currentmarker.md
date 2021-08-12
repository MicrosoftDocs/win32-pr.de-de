---
title: Controls.currentMarker
description: Die currentMarker-Eigenschaft gibt die aktuelle Markernummer an oder ruft sie ab.
ms.assetid: 4b4eacd4-3df0-4e11-8755-1ac326fad027
keywords:
- Controls.currentMarker Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentMarker
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcc11f79460661b6622da529b0de025672794af660aeb27bf56c7910a6d5a50b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580306"
---
# <a name="controlscurrentmarker"></a>Controls.currentMarker

Die **currentMarker-Eigenschaft** gibt die aktuelle Markernummer an oder ruft sie ab.

``` syntax
player.controls.currentMarker
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine  Lese-/Schreibnummer **(long**) mit dem Standardwert 0 (null).

## <a name="remarks"></a>Hinweise

Das Festlegen von **currentMarker** bewirkt, dass die Wiedergabe mit dem angegebenen Marker beginnt. Bevor Sie versuchen, **currentMarker** festzulegen, bestimmen Sie mit **markerCount,** ob eine Datei Marker und wie viele sie enthält. Wenn eine Datei keine Marker aufweist, führt das Festlegen von **currentMarker** auf alles andere als 0 (null) zu einem Fehler. Das Festlegen von **currentMarker** auf eine Zahl, die höher als **markerCount** ist, führt ebenfalls zu einem Fehler.

Die **currentMarker-Eigenschaft** gibt immer den aktuellen oder letzten Marker zurück, was bedeutet, dass sich die tatsächliche Dateiposition entweder am aktuellen Marker oder vor dem nächsten Marker befinden kann. Marker werden beginnend mit 1 nummeriert. Wenn also eine Datei Marker enthält, können Sie **currentMarker** auf 0 (null) festlegen, um die Dateiposition in 0 (null) zu ändern.

Bis das aktuelle Medienelement festgelegt ist (mit *player*.**URL** oder *Player*. **currentMedia**), **currentMarker** gibt 0 (null) zurück.

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird **currentMarker** verwendet, um die Videowiedergabe über den Marker zu starten, der der **selectedIndex-Eigenschaft** eines HTML SELECT-Elements entspricht. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<SELECT ID = "markers"  NAME = "markers"  LANGUAGE = "JScript"

    /* Seek to the marker number that corresponds to the SELECT element
       selectedIndex value when the list selection changes. */
    onChange = "Player.controls.currentMarker = markers.selectedIndex + 1;
">

    /* Fill the SELECT element with the marker identifiers. */
    <OPTION SELECTED>Sunrise
    <OPTION>Car chase 
    <OPTION>Happy ending
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

[**Media.markerCount**](media-markercount.md)
</dt> <dt>

[**Player.currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> </dl>

 

 





