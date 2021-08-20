---
title: PlaylistArray.item-Methode
description: Die Item-Methode ruft die Wiedergabeliste am angegebenen Index ab.
ms.assetid: cc851695-f9a2-4594-8bd3-3555c18bfa10
keywords:
- item-Methode Windows Media Player
- item-Methode Windows Media Player , PlaylistArray-Klasse
- PlaylistArray-Klasse Windows Media Player , Item-Methode
topic_type:
- apiref
api_name:
- PlaylistArray.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a45bb38250285563d9e4b7abcc1a4bfd1f7a0bea35b41b7e4cd801f8eff1d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335427"
---
# <a name="playlistarrayitem-method"></a>PlaylistArray.item-Methode

Die **Item-Methode** ruft die Wiedergabeliste am angegebenen Index ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = PlaylistArray.item(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

**Zahl** (**long**), die den Index der abzurufenden Wiedergabeliste enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Playlist-Objekt** zurück.

## <a name="remarks"></a>Hinweise

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PlaylistArray-Objekt**](playlistarray-object.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





