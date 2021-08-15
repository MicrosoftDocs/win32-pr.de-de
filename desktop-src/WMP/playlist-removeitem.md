---
title: Playlist.removeItem-Methode
description: Die removeItem-Methode entfernt das angegebene Element aus der Wiedergabeliste.
ms.assetid: 294ba4fb-967b-4a03-b0c5-6e9c15db3bff
keywords:
- removeItem-Windows Media Player
- removeItem-Methode Windows Media Player , Playlist-Klasse
- Playlist-Klasse Windows Media Player , removeItem-Methode
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
ms.openlocfilehash: a8a55fb45fa7ea8d172d76321d7c907fbedfd3f868448f1ad63e220ff8e69f9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336591"
---
# <a name="playlistremoveitem-method"></a>Playlist.removeItem-Methode

Die **removeItem-Methode** entfernt das angegebene Element aus der Wiedergabeliste.

## <a name="syntax"></a>Syntax


```JScript
Playlist.removeItem(
  item
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*item* \[ In\]
</dt> <dd>

**Medienobjekt,** das entfernt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn das entfernte Element die gerade abspielte Spur ist (*Player*.**currentMedia**), die Wiedergabe wird beendet, und das nächste Element in der Wiedergabeliste wird zum aktuellen Element. Wenn kein nächstes Element enthalten ist, wird das vorherige Element verwendet, oder wenn keine anderen Elemente enthalten sind, dann *Player*. **currentMedia** ist auf **NULL festgelegt.**

Um diese Methode verwenden zu können, ist Vollzugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Player.currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Playlist-Objekt**](playlist-object.md)
</dt> <dt>

[**Playlist.insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Playlist.item**](playlist-item.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





