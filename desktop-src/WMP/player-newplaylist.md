---
title: Player. newwiedergabe-Methode
description: Die newwiedergabe-Methode erstellt ein neues Wiedergabelisten Objekt.
ms.assetid: a566006e-8647-4c51-ab77-762728f25a30
keywords:
- newwiedergabe-Methode, Windows-Media Player
- newwiedergabe-Methode, Windows Media Player, Player-Klasse
- Player-Klasse, Windows Media Player, newwiedergabe-Methode
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
ms.openlocfilehash: fa65ae4b453fe919116a33c5ee86b14ba353f681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354035"
---
# <a name="playernewplaylist-method"></a>Player. newwiedergabe-Methode

Die **newwiedergabe** -Methode erstellt ein neues **Wiedergabe** Listen Objekt.

## <a name="syntax"></a>Syntax


```JScript
retVal = Player.newPlaylist(
  name,
  URL
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Namen der neuen Wiedergabeliste enthält.

</dd> <dt>

*URL* \[ in\]
</dt> <dd>

**Zeichenfolge** , die die URL der Windows Media-Metadatei-Wiedergabeliste enthält, mit der das **Wiedergabe** Listen Objekt erstellt

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Wiedergabe** Listen Objekt zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der *URL* -Parameter auf NULL oder "" (leere Zeichenfolge) festgelegt ist, wird ein leeres **Wiedergabe** Listen Objekt erstellt. Wenn der *Name* -Parameter auf "" festgelegt ist, wird der Name in der Metadatei verwendet.

Die neue Wiedergabeliste, die mit dieser Methode erstellt wurde, wird nicht der Bibliothek hinzugefügt. Verwenden Sie *playlistcollection*, um der Bibliothek eine neue Wiedergabeliste hinzuzufügen. **importwiedergabe Liste** oder *playlistcollection*. **newwiedergabe**. Alle führenden oder nachfolgenden Leerzeichen im Wiedergabelisten Namen werden automatisch entfernt, wenn Sie der Bibliothek hinzugefügt werden.

Da die Bibliothek mehrere Wiedergabelisten mit dem gleichen Namen zulässt, sollten Sie überprüfen, ob eine Wiedergabeliste mit einem bestimmten Namen vorhanden ist, bevor Sie einen neuen hinzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Playlistcollection. importwiedergabe**](playlistcollection-importplaylist.md)
</dt> <dt>

[**Playlistcollection. newwiedergabe**](playlistcollection-newplaylist.md)
</dt> <dt>

[**Windows Media-Metadateien**](windows-media-metafiles.md)
</dt> </dl>

 

 





