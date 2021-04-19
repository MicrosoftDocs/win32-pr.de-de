---
title: Controls. PlayItem-Methode
description: Die PlayItem-Methode gibt das angegebene Medien Element wieder. | Controls. PlayItem-Methode
ms.assetid: 410e315d-8d5f-4f45-82a7-4249e656c809
keywords:
- PlayItem-Methoden Fenster Media Player
- PlayItem-Methode, Windows Media Player, Controls-Klasse
- Steuerelemente-Klasse, Windows Media Player, PlayItem-Methode
topic_type:
- apiref
api_name:
- Controls.playItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9096e378a328f43147a0a94d97034c8e566b611
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366859"
---
# <a name="controlsplayitem-method"></a>Controls. PlayItem-Methode

Die **PlayItem** -Methode gibt das angegebene Medien Element wieder.

## <a name="syntax"></a>Syntax


```JScript
Controls.playItem(
  theMediaItem
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Das *mediaitem* \[ -Element in\]
</dt> <dd>

Das zu Wiedergabe Ende **Medien** Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Das Medien Element wird unabhängig vom Wert der *Einstellungen* geladen und automatisch wiedergegeben. **Autostart** -Eigenschaft. Wenn Sie ein Element ohne automatische Wiedergabe laden möchten, legen Sie die *Einstellungen* fest. **Autostart** mit false und Zuweisen eines Werts zu einem *Player*. Die **URL**, nach der **Play** aufgerufen werden kann, um mit der Wiedergabe des Elements zu beginnen.

Hinweis

**PlayItem** funktioniert nur mit Elementen in *currentwiedergabe*. Das Aufrufen von **PlayItem** mit einem Verweis auf ein gespeichertes Medien Element wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird **PlayItem** verwendet, um ein Medien Element aus der aktuellen Wiedergabeliste wiederzugeben. Das Element, das abgespielt werden soll, wird basierend auf seiner Position in der Wiedergabeliste ausgewählt. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
var index = 3

// Retrieve the media item at the fourth position in the current playlist.
var media = Player.currentPlaylist.item(index);

// Play the media item.
Player.controls.playItem(media);

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

[**Wiedergabeliste. Element**](playlist-item.md)
</dt> </dl>

 

 





