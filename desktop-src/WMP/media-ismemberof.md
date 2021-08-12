---
title: Media.isMemberOf-Methode
description: Die isMemberOf-Methode gibt einen Wert zurück, der angibt, ob das Medienelement ein Member der angegebenen Wiedergabeliste ist.
ms.assetid: e620741f-6807-4a61-ba9b-f45426d6e33e
keywords:
- isMemberOf-Windows Media Player
- isMemberOf-Methode Windows Media Player , Media-Klasse
- Medienklasse Windows Media Player , isMemberOf-Methode
topic_type:
- apiref
api_name:
- Media.isMemberOf
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef9fc5eb55a306dad8b9d5de6d6501b615a9156c026c8e0fc12664795a23ab21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574802"
---
# <a name="mediaismemberof-method"></a>Media.isMemberOf-Methode

Die **isMemberOf-Methode** gibt einen Wert zurück, der angibt, ob das Medienelement ein Member der angegebenen Wiedergabeliste ist.

## <a name="syntax"></a>Syntax


```JScript
bRetVal = Media.isMemberOf(
  playlist
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wiedergabeliste* \[ In\]
</dt> <dd>

**Wiedergabelistenobjekt,** das möglicherweise das Medienelement enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen **booleschen zurück.**

## <a name="remarks"></a>Hinweise

Diese Methode kann keine Wiedergabelisten überprüfen, die über das **MediaCollection-Objekt abgerufen** wurden. Um zu testen, ob ein Medienelement Mitglied einer bestimmten benannten Wiedergabeliste ist, rufen Sie die Wiedergabeliste mit dem *Player ab.* *playlistCollection*. **getByName**(*Name*). **item**(0). Diese Methode kann auch mit CD-Wiedergabelisten und Metadateiwiedergabelisten verwendet werden.

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript Media *verwendet.* **isMemberOf,** um zu testen, ob das aktuelle Medienelement ein Mitglied der Wiedergabeliste mit dem Namen Sample Playlist ist. Wenn dies nicht der Status ist, wird das aktuelle Medienelement an die Beispielwiedergabeliste angefügt. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
// Store the playlist object named Sample Playlist.
var sPlaylist = Player.playlistcollection.getbyname("Sample Playlist").item(0);

// Test whether the current media item is a member of Sample Playlist.
 var answer = ((Player.currentMedia.isMemberOf(sPlaylist))?"Yes":"No");

// If the current media item is not a member of Sample Playlist,
// append the current media item to the playlist.
if (answer == "No"){
   sPlaylist.appendItem(Player.currentMedia);
}

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Wiedergabelistenobjekt**](playlist-object.md)
</dt> <dt>

[**PlaylistCollection-Objekt**](playlistcollection-object.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





