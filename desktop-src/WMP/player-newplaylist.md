---
title: Player.newPlaylist-Methode
description: Die newPlaylist-Methode erstellt ein neues Wiedergabelistenobjekt.
ms.assetid: a566006e-8647-4c51-ab77-762728f25a30
keywords:
- newPlaylist-Methode Windows Media Player
- newPlaylist-Methode Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , newPlaylist-Methode
topic_type:
- apiref
api_name:
- Player.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 380d1f2751487f5c648b154852be625a5c93103851541dea7e2488ba75080ca0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572830"
---
# <a name="playernewplaylist-method"></a>Player.newPlaylist-Methode

Die **newPlaylist-Methode** erstellt ein neues **Wiedergabelistenobjekt.**

## <a name="syntax"></a>Syntax


```JScript
retVal = Player.newPlaylist(
  name,
  URL
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*name* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Namen der neuen Wiedergabeliste enthält.

</dd> <dt>

*URL* \[ In\]
</dt> <dd>

**Zeichenfolge,** die die URL der Windows Media-Metadateiwiedergabeliste enthält, mit der das **Wiedergabelistenobjekt** erstellt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Playlist-Objekt** zurück.

## <a name="remarks"></a>Hinweise

Wenn der *URL-Parameter* auf NULL oder "" (leere Zeichenfolge) festgelegt ist, wird ein leeres **Wiedergabelistenobjekt** erstellt. Wenn der *name-Parameter* auf "" festgelegt ist, wird der Name in der Metadatei verwendet.

Die mit dieser Methode erstellte neue Wiedergabeliste wird der Bibliothek nicht hinzugefügt. Um der Bibliothek eine neue Wiedergabeliste hinzuzufügen, verwenden Sie *PlaylistCollection*. **importPlaylist** oder *PlaylistCollection*. **newPlaylist**. Führende oder nachfolgende Leerzeichen im Wiedergabelistennamen werden automatisch entfernt, wenn sie der Bibliothek hinzugefügt werden.

Da die Bibliothek mehrere Wiedergabelisten mit dem gleichen Namen zulässt, sollten Sie vor dem Hinzufügen einer neuen Wiedergabeliste überprüfen, ob eine Wiedergabeliste mit einem bestimmten Namen vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player serie 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**PlaylistCollection.importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**PlaylistCollection.newPlaylist**](playlistcollection-newplaylist.md)
</dt> <dt>

[**Windows Medienmetadateien**](windows-media-metafiles.md)
</dt> </dl>

 

 





