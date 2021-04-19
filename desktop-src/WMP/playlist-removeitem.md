---
title: Wiedergabe. RemoveItem-Methode
description: Die RemoveItem-Methode entfernt das angegebene Element aus der Wiedergabeliste.
ms.assetid: 294ba4fb-967b-4a03-b0c5-6e9c15db3bff
keywords:
- RemoveItem-Methode, Windows-Media Player
- RemoveItem-Methode, Windows Media Player, Wiedergabelisten Klasse
- Wiedergabelisten-Klasse, Windows Media Player, RemoveItem-Methode
topic_type:
- apiref
api_name:
- Playlist.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de03333e2373744f9e9197be8ed8582997c557d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368411"
---
# <a name="playlistremoveitem-method"></a>Wiedergabe. RemoveItem-Methode

Die **RemoveItem** -Methode entfernt das angegebene Element aus der Wiedergabeliste.

## <a name="syntax"></a>Syntax


```JScript
Playlist.removeItem(
  item
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Element* \[ in\]
</dt> <dd>

Das zu entfernende **Medien** Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

, Wenn das entfernte Element die aktuell wiedergegebene Spur (*Player*) ist.**currentMedia**), Wiedergabe wird beendet, und das nächste Element in der Wiedergabeliste wird zum aktuellen Element. Wenn kein nächstes Element vorhanden ist, wird das vorherige Element verwendet, oder wenn keine anderen Elemente vorhanden sind, dann *Player*. **currentMedia** wird auf **null** festgelegt.

Um diese Methode verwenden zu können, ist der vollständige Zugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Wiedergabelisten Objekt**](playlist-object.md)
</dt> <dt>

[**Wiedergabeliste. InsertItem**](playlist-insertitem.md)
</dt> <dt>

[**Wiedergabeliste. Element**](playlist-item.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





