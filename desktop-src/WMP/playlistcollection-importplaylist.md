---
title: PlaylistCollection.importPlaylist-Methode
description: Die importPlaylist-Methode fügt der Bibliothek eine statische Wiedergabeliste hinzu. | PlaylistCollection.importPlaylist-Methode
ms.assetid: 0611ba42-fd8f-4fb9-9fbb-809a82775c2a
keywords:
- importPlaylist-Methode Windows Media Player
- importPlaylist-Methode Windows Media Player , PlaylistCollection-Klasse
- PlaylistCollection-Klasse Windows Media Player , importPlaylist-Methode
topic_type:
- apiref
api_name:
- PlaylistCollection.importPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f6c2a61b6603c0bfb38025548eaa4b0943bcdd1a5e81cb1ac27c17969fe87ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334842"
---
# <a name="playlistcollectionimportplaylist-method"></a>PlaylistCollection.importPlaylist-Methode

Die **importPlaylist-Methode** fügt der Bibliothek eine statische Wiedergabeliste hinzu.

## <a name="syntax"></a>Syntax


```JScript
retVal = PlaylistCollection.importPlaylist(
  playlist
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wiedergabeliste* \[ In\]
</dt> <dd>

**Wiedergabelistenobjekt,** das hinzugefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt das **hinzugefügte Playlist-Objekt** zurück.

## <a name="remarks"></a>Hinweise

Wiedergabelisten, die keine Medienelemente enthalten, können der Bibliothek mit dieser Methode nicht hinzugefügt werden. Verwenden Sie die **newPlaylist-Methode,** um eine leere Wiedergabeliste in der Bibliothek zu erstellen. Anschließend können Sie die resultierende Wiedergabeliste mit Medienelementen füllen, indem Sie *Wiedergabeliste* verwenden. **appendItem** oder *Playlist*. **insertItem**.

Wenn Sie diese Methode an eine automatische Wiedergabeliste übergeben, wird die Abfrage einmal ausgeführt, und das Ergebnis wird der Bibliothek als statische Wiedergabeliste hinzugefügt. Verwenden Sie *MediaCollection,* um der Bibliothek eine automatische Wiedergabeliste hinzuzufügen und ihr automatisches Verhalten beizubehalten. **fügen Sie hinzu.** Weitere Informationen finden Sie unter [Statische und automatische Wiedergabelisten.](static-and-auto-playlists.md)

Um diese Methode verwenden zu können, ist vollzugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Verwalten von Wiedergabelisten**](managing-playlists.md)
</dt> <dt>

[**MediaCollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection.add**](mediacollection-add.md)
</dt> <dt>

[**Playlist.appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Playlist.insertItem**](playlist-insertitem.md)
</dt> <dt>

[**PlaylistCollection-Objekt**](playlistcollection-object.md)
</dt> <dt>

[**PlaylistCollection.newPlaylist**](playlistcollection-newplaylist.md)
</dt> <dt>

[**PlaylistCollection.remove**](playlistcollection-remove.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





