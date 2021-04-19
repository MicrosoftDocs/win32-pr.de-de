---
title: Media. ismembership of-Methode
description: Die ismembership of-Methode gibt einen Wert zurück, der angibt, ob das Medien Element ein Member der angegebenen Wiedergabeliste ist.
ms.assetid: e620741f-6807-4a61-ba9b-f45426d6e33e
keywords:
- ismembership of-Methode, Windows-Media Player
- ismembership of-Methode, Windows Media Player, Medienklasse
- Media Class Windows Media Player, ismembership of-Methode
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
ms.openlocfilehash: 41555bd5910ddb3151468a458c5becbf247ea484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369594"
---
# <a name="mediaismemberof-method"></a>Media. ismembership of-Methode

Die **ismembership of** -Methode gibt einen Wert zurück, der angibt, ob das Medien Element ein Member der angegebenen Wiedergabeliste ist.

## <a name="syntax"></a>Syntax


```JScript
bRetVal = Media.isMemberOf(
  playlist
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wiedergabeliste* \[ in\]
</dt> <dd>

**Wiedergabe** Listen Objekt, das das Medien Element enthalten kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen **booleschen** Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode kann keine Wiedergabelisten überprüfen, die über das **mediacollection** -Objekt abgerufen wurden. Um zu testen, ob ein Medien Element ein Member einer bestimmten benannten Wiedergabeliste ist, rufen Sie die Wiedergabeliste mit *Player* ab. *playlistcollection*. **getByName**(*Name*). **Element**(0). Diese Methode kann auch mit CD-und metadatenwiedergabe-Wiedergabelisten verwendet werden.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel werden *Medien* verwendet. **ismembership of** , um zu testen, ob das aktuelle Medien Element ein Member der Wiedergabeliste mit dem Namen "Beispiel Wiedergabeliste" ist. Wenn dies nicht der Fall ist, wird das aktuelle Medien Element an die Beispiel Wiedergabeliste angehängt. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Wiedergabelisten Objekt**](playlist-object.md)
</dt> <dt>

[**Playlistcollection-Objekt**](playlistcollection-object.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





