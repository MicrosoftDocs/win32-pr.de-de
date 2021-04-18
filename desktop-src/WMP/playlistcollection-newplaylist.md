---
title: Playlistcollection. newwiedergabe-Methode
description: Die newwiedergabe-Methode erstellt eine neue Wiedergabeliste in der Bibliothek.
ms.assetid: 428b5779-4dc0-466b-9834-6b2c43324013
keywords:
- newwiedergabe-Methode, Windows-Media Player
- newwiedergabe-Methode, Windows Media Player, playlistcollection-Klasse
- Playlistcollection-Klasse, Windows Media Player, newwiedergabe-Methode
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
ms.openlocfilehash: d94c25a8dfe6f1eb7c4dac40dd644433a5f0d7e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371690"
---
# <a name="playlistcollectionnewplaylist-method"></a>Playlistcollection. newwiedergabe-Methode

Die **newwiedergabe** -Methode erstellt eine neue Wiedergabeliste in der Bibliothek.

## <a name="syntax"></a>Syntax


```JScript
retVal = PlaylistCollection.newPlaylist(
  name
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Namen der zu erstellenden Wiedergabeliste enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Wiedergabe** Listen Objekt zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode erstellt eine leere Wiedergabeliste in der Bibliothek. Verwenden Sie die *Wiedergabeliste*, um die Wiedergabeliste mit Medien Elementen auszufüllen. **appendItem** oder *Wiedergabeliste*. **InsertItem**.

In der Bibliothek sind mehrere Wiedergabelisten mit dem gleichen Namen zulässig. Verwenden Sie **getByName** und *playlistarray*, um zu vermeiden, dass ein doppelter Wiedergabelisten Name mit dieser Methode erstellt wird. **count** , um zu bestimmen, ob eine Wiedergabeliste mit einem bestimmten Namen bereits vorhanden ist.

Führende und nachfolgende Leerzeichen sind in Wiedergabelisten Namen nicht zulässig und werden automatisch aus dem für den *Name* -Parameter angegebenen Wert entfernt.

Um diese Methode verwenden zu können, ist der vollständige Zugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird eine neue leere Wiedergabeliste mit dem Namen "threelist" erstellt. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
//Add a new empty playlist, named ThreeList, to the playlist collection.
var NewList = Player.playlistCollection.newPlaylist("ThreeList");

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mediacollection. Add**](mediacollection-add.md)
</dt> <dt>

[**Wiedergabeliste. appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Wiedergabeliste. InsertItem**](playlist-insertitem.md)
</dt> <dt>

[**Playlistarray. Count**](playlistarray-count.md)
</dt> <dt>

[**Playlistcollection-Objekt**](playlistcollection-object.md)
</dt> <dt>

[**Playlistcollection. getByName**](playlistcollection-getbyname.md)
</dt> <dt>

[**Playlistcollection. importwiedergabe**](playlistcollection-importplaylist.md)
</dt> <dt>

[**Playlistcollection. Remove**](playlistcollection-remove.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





