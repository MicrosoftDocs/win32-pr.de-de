---
title: Playlistcollection. importwiedergabe-Methode
description: Die importwiedergabe-Methode fügt der Bibliothek eine statische Wiedergabeliste hinzu. | Playlistcollection. importwiedergabe-Methode
ms.assetid: 0611ba42-fd8f-4fb9-9fbb-809a82775c2a
keywords:
- importwiedergabe-Methode, Windows-Media Player
- importwiedergabe-Methode, Windows Media Player, playlistcollection-Klasse
- Playlistcollection-Klasse, Windows Media Player, importwiedergabe-Methode
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
ms.openlocfilehash: 736e9afa17f571428fada48660726b606268796a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351376"
---
# <a name="playlistcollectionimportplaylist-method"></a>Playlistcollection. importwiedergabe-Methode

Die **importwiedergabe** -Methode fügt der Bibliothek eine statische Wiedergabeliste hinzu.

## <a name="syntax"></a>Syntax


```JScript
retVal = PlaylistCollection.importPlaylist(
  playlist
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wiedergabeliste* \[ in\]
</dt> <dd>

Das hinzu zufügende **Wiedergabe** Listen Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt das **Wiedergabe** Listen Objekt zurück, das hinzugefügt wurde.

## <a name="remarks"></a>Bemerkungen

Wiedergabelisten, die keine Medienelemente enthalten, können der Bibliothek nicht mithilfe dieser Methode hinzugefügt werden. Verwenden Sie die **newwiedergabe** -Methode, um eine leere Wiedergabeliste in der Bibliothek zu erstellen. Anschließend können Sie die resultierende Wiedergabeliste mithilfe von *Wiedergabe* Listen mit Medien Elementen ausfüllen. **appendItem** oder *Wiedergabeliste*. **InsertItem**.

Wenn Sie diese Methode an eine automatische Wiedergabeliste übergeben, wird die Abfrage einmal ausgeführt, und das Ergebnis wird der Bibliothek als statische Wiedergabeliste hinzugefügt. Wenn Sie der Bibliothek eine automatische Wiedergabeliste hinzufügen und das automatische Verhalten beibehalten möchten, verwenden Sie *mediacollection*. **fügen Sie hinzu**. Weitere Informationen finden Sie unter [statische und automatische Wiedergabelisten](static-and-auto-playlists.md).

Um diese Methode verwenden zu können, ist der vollständige Zugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verwalten von Wiedergabelisten**](managing-playlists.md)
</dt> <dt>

[**Mediacollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Mediacollection. Add**](mediacollection-add.md)
</dt> <dt>

[**Wiedergabeliste. appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Wiedergabeliste. InsertItem**](playlist-insertitem.md)
</dt> <dt>

[**Playlistcollection-Objekt**](playlistcollection-object.md)
</dt> <dt>

[**Playlistcollection. newwiedergabe**](playlistcollection-newplaylist.md)
</dt> <dt>

[**Playlistcollection. Remove**](playlistcollection-remove.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





