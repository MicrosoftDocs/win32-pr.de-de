---
title: PlaylistCollection.isDeleted-Methode
description: Die isDeleted-Methode ruft einen Wert ab, der angibt, ob sich die angegebene Wiedergabeliste im Ordner für gelöschte Elemente befindet.
ms.assetid: 5023927a-5d1a-4b61-8122-476947d537c4
keywords:
- isDeleted-Windows Media Player
- isDeleted-Methode Windows Media Player , PlaylistCollection-Klasse
- PlaylistCollection-Klasse Windows Media Player , isDeleted-Methode
topic_type:
- apiref
api_name:
- PlaylistCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59f6ad587740911d55ae2837607c651e3f3be875bfb24f8bfa765ba415e9bc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862200"
---
# <a name="playlistcollectionisdeleted-method"></a>PlaylistCollection.isDeleted-Methode

Die **isDeleted-Methode** ruft einen Wert ab, der angibt, ob sich die angegebene Wiedergabeliste im Ordner für gelöschte Elemente befindet.

## <a name="syntax"></a>Syntax


```JScript
bRetVal = PlaylistCollection.isDeleted(
  playlist
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wiedergabeliste* \[ In\]
</dt> <dd>

Das  Wiedergabelistenobjekt, nach dem gesucht werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen **booleschen zurück.**

**Windows Media Player 10 Mobile:** Diese Methode gibt immer **false zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0, Windows Media Player Version 7.1 oder Windows Media Player für Windows XP. Diese Methode wird für die Windows Media Player 9-Serie oder höher nicht unterstützt.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PlaylistCollection-Objekt**](playlistcollection-object.md)
</dt> </dl>

 

 





