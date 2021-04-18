---
title: Wiedergabe. appendItem-Methode
description: Mit der appendItem-Methode wird am Ende der Wiedergabeliste ein Medien Element hinzugefügt.
ms.assetid: cc956491-7936-49e7-90ca-1f71e03448cd
keywords:
- appendItem-Methode, Windows Media Player
- appendItem-Methode, Windows Media Player, Wiedergabelisten Klasse
- Wiedergabelisten-Klasse, Windows Media Player, appendItem-Methode
topic_type:
- apiref
api_name:
- Playlist.appendItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 828799d5b6e71e7ff0e7be4c1e55714f6343be51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358359"
---
# <a name="playlistappenditem-method"></a>Wiedergabe. appendItem-Methode

Mit der **appendItem** -Methode wird am Ende der Wiedergabeliste ein Medien Element hinzugefügt.

## <a name="syntax"></a>Syntax


```JScript
Playlist.appendItem(
  item
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Element* \[ in\]
</dt> <dd>

Das hinzu zufügende **Medien** Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Um diese Methode verwenden zu können, ist der vollständige Zugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird die *Wiedergabeliste* verwendet. **appendItem** , um der Wiedergabeliste mit dem Namen "threelist" das aktuelle Medien Element hinzuzufügen. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Get the current media item.
var currMedia = Player.currentMedia;

// Get the playlist object by name.
var plThreeList = Player.playlistCollection.getByName("ThreeList").item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelisten Objekt**](playlist-object.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





