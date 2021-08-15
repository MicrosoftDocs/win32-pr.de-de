---
title: Playlist.insertItem-Methode
description: Die insertItem-Methode fügt ein Medienelement an der angegebenen Position in die Wiedergabeliste ein.
ms.assetid: c186abc4-0a15-49d2-bbc4-5660e8cc0a4b
keywords:
- insertItem-Windows Media Player
- insertItem-Methode Windows Media Player , Playlist-Klasse
- Playlist-Klasse Windows Media Player , insertItem-Methode
topic_type:
- apiref
api_name:
- Playlist.insertItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a71d9ceb39b29c1627ea7596166c39b3dc2f6c76faf45e5ffb54bea14154ac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995700"
---
# <a name="playlistinsertitem-method"></a>Playlist.insertItem-Methode

Die **insertItem-Methode** fügt ein Medienelement an der angegebenen Position in die Wiedergabeliste ein.

## <a name="syntax"></a>Syntax


```JScript
Playlist.insertItem(
  index,
  item
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

**Number** (**long**), die den Index enthält, an dem das Element hinzugefügt werden soll.

</dd> <dt>

*item* \[ In\]
</dt> <dd>

**Medienobjekt,** das eingefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Für alle Elemente nach dem eingefügten Element werden ihre Indexnummern um eins erhöht.

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

[**Playlist.item**](playlist-item.md)
</dt> <dt>

[**Playlist.removeItem**](playlist-removeitem.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





