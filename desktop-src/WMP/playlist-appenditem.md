---
title: Playlist.appendItem-Methode
description: Die appendItem-Methode fügt am Ende der Wiedergabeliste ein Medienelement hinzu.
ms.assetid: cc956491-7936-49e7-90ca-1f71e03448cd
keywords:
- appendItem-Methode Windows Media Player
- appendItem-Methode Windows Media Player , Playlist-Klasse
- Wiedergabelistenklasse Windows Media Player , appendItem-Methode
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
ms.openlocfilehash: 79361ebcf2ea23b754a7bc86cb6fa4a0af465e4e6619ed692c027bc28eb7aa87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747119"
---
# <a name="playlistappenditem-method"></a>Playlist.appendItem-Methode

Die **appendItem-Methode** fügt am Ende der Wiedergabeliste ein Medienelement hinzu.

## <a name="syntax"></a>Syntax


```JScript
Playlist.appendItem(
  item
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Element* \[ In\]
</dt> <dd>

**Medienobjekt,** das hinzugefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Um diese Methode verwenden zu können, ist vollzugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird *Playlist* verwendet. **appendItem** zum Hinzufügen des aktuellen Medienelements zur Wiedergabeliste mit dem Namen "ThreeList". Das **Player-Objekt** wurde mit ID="Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Wiedergabelistenobjekt**](playlist-object.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





