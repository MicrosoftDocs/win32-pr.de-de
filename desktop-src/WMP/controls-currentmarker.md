---
title: Controls. currentmarker
description: Die currentmarker-Eigenschaft gibt die aktuelle Markernummer an oder ruft Sie ab.
ms.assetid: 4b4eacd4-3df0-4e11-8755-1ac326fad027
keywords:
- Steuerelemente. currentmarker-Fenster Media Player
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
ms.openlocfilehash: 8aae8af226b62550b3faae9389385d321bf10aad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354671"
---
# <a name="controlscurrentmarker"></a>Controls. currentmarker

Die **currentmarker** -Eigenschaft gibt die aktuelle Markernummer an oder ruft Sie ab.

``` syntax
player.controls.currentMarker
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese-/schreibzahl (**Long**) mit einem Standardwert von 0 (null). 

## <a name="remarks"></a>Bemerkungen

Das Festlegen von **currentmarker** bewirkt, dass die Wiedergabe vom angegebenen Marker gestartet wird. Bevor Sie versuchen, **currentmarker** festzulegen, stellen Sie fest, ob eine Datei Marker hat und wie viele Sie mit **markercount** haben. Wenn eine Datei keine Marker hat, führt die Festlegung von **currentmarker** auf alles, aber auf 0 (null) zu einem Fehler. Wenn **currentmarker** auf eine Zahl höher als **markercount** festgelegt wird, führt dies ebenfalls zu einem Fehler.

Die **currentmarker** -Eigenschaft gibt immer den aktuellen oder den letzten Marker zurück. Dies bedeutet, dass sich die tatsächliche Dateiposition entweder am aktuellen Marker oder vor dem nächsten Marker befinden kann. Marker werden beginnend mit 1 nummeriert. Wenn also eine Datei Marker enthält, können Sie **currentmarker** auf NULL festlegen, um die Dateiposition in NULL zu ändern.

Bis zum Festlegen des aktuellen Medien Elements (mithilfe von *Player*).**URL** oder *Player*. **currentMedia**), **currentmarker** gibt 0 (null) zurück.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird **currentmarker** verwendet, um die Videowiedergabe aus dem Marker zu starten, der der **SelectedIndex** -Eigenschaft eines HTML SELECT-Elements entspricht. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> <dt>

[**Media. markercount**](media-markercount.md)
</dt> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





