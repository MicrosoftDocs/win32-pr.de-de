---
title: Playlist.moveItem-Methode
description: Die moveItem-Methode ändert den Speicherort eines Elements in der Wiedergabeliste.
ms.assetid: 82a8de86-4419-48a7-89f8-f7b9084b51d4
keywords:
- moveItem-Windows Media Player
- moveItem-Methode Windows Media Player , Playlist-Klasse
- Playlist-Klasse Windows Media Player , moveItem-Methode
topic_type:
- apiref
api_name:
- Playlist.moveItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a725ae53e38d1903d31dc47a3362f90c29fb064e3a785b816de0d0b695998aee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746852"
---
# <a name="playlistmoveitem-method"></a>Playlist.moveItem-Methode

Die **moveItem-Methode** ändert den Speicherort eines Elements in der Wiedergabeliste.

## <a name="syntax"></a>Syntax


```JScript
Playlist.moveItem(
  oldIndex,
  newIndex
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*oldIndex* \[ In\]
</dt> <dd>

**Number** (**long**), die den alten Index enthält.

</dd> <dt>

*newIndex* \[ In\]
</dt> <dd>

**Number** (**long**), die den neuen Index enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wiedergabelisten, die in der Bibliothek gespeichert sind, können sich außerhalb Ihres Steuerelements ändern. Achten Sie darauf, alle entsprechenden wiedergabelistenbezogenen Ereignisse zu überwachen und zu behandeln, damit sich die Reihenfolge der Elemente in der Wiedergabeliste nicht unerwartet ändert.

Um diese Methode verwenden zu können, ist Vollzugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Wiedergabelistenobjekt**](playlist-object.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





