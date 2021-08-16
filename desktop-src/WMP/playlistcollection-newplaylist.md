---
title: PlaylistCollection.newPlaylist-Methode
description: Die newPlaylist-Methode erstellt eine neue Wiedergabeliste in der Bibliothek.
ms.assetid: 428b5779-4dc0-466b-9834-6b2c43324013
keywords:
- newPlaylist-Methode Windows Media Player
- newPlaylist-Methode Windows Media Player , PlaylistCollection-Klasse
- PlaylistCollection-Klasse Windows Media Player , newPlaylist-Methode
topic_type:
- apiref
api_name:
- PlaylistCollection.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af40d4de424997cb943711d84bf62805f2036afeb551c5d397ce82ae0975e812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334595"
---
# <a name="playlistcollectionnewplaylist-method"></a>PlaylistCollection.newPlaylist-Methode

Die **newPlaylist-Methode** erstellt eine neue Wiedergabeliste in der Bibliothek.

## <a name="syntax"></a>Syntax


```JScript
retVal = PlaylistCollection.newPlaylist(
  name
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*name* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Namen der zu erstellenden Wiedergabeliste enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Playlist-Objekt** zurück.

## <a name="remarks"></a>Hinweise

Diese Methode erstellt eine leere Wiedergabeliste in der Bibliothek. Um die Wiedergabeliste mit Medienelementen zu füllen, verwenden Sie *Wiedergabeliste*. **appendItem** oder *Playlist*. **insertItem**.

Mehrere Wiedergabelisten mit dem gleichen Namen sind in der Bibliothek zulässig. Verwenden Sie **getByName** und *PlaylistArray,* um zu vermeiden, dass mit dieser Methode ein doppelter Wiedergabelistenname erstellt wird. **count,** um zu bestimmen, ob bereits eine Wiedergabeliste mit einem bestimmten Namen vorhanden ist.

Führende und nachfolgende Leerzeichen sind in Wiedergabelistennamen nicht zulässig und werden automatisch aus dem für den *name-Parameter* angegebenen Wert entfernt.

Um diese Methode verwenden zu können, ist vollzugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird eine neue leere Wiedergabeliste namens "ThreeList" erstellt. Das **Player-Objekt** wurde mit ID="Player" erstellt.


```JScript
//Add a new empty playlist, named ThreeList, to the playlist collection.
var NewList = Player.playlistCollection.newPlaylist("ThreeList");

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MediaCollection.add**](mediacollection-add.md)
</dt> <dt>

[**Playlist.appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Playlist.insertItem**](playlist-insertitem.md)
</dt> <dt>

[**PlaylistArray.count**](playlistarray-count.md)
</dt> <dt>

[**PlaylistCollection-Objekt**](playlistcollection-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> <dt>

[**PlaylistCollection.importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**PlaylistCollection.remove**](playlistcollection-remove.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





