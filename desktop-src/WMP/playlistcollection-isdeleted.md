---
title: Playlistcollection. IsDeleted-Methode
description: Die IsDeleted-Methode ruft einen Wert ab, der angibt, ob sich die angegebene Wiedergabeliste im Ordner "Gelöschte Elemente" befindet.
ms.assetid: 5023927a-5d1a-4b61-8122-476947d537c4
keywords:
- IsDeleted-Methode (Windows Media Player)
- IsDeleted-Methode, Windows Media Player, playlistcollection-Klasse
- Playlistcollection-Klasse, Windows Media Player, IsDeleted-Methode
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
ms.openlocfilehash: 3fed3e7e8ff41f23d0f9f741ea99f3382d20532e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371175"
---
# <a name="playlistcollectionisdeleted-method"></a>Playlistcollection. IsDeleted-Methode

Die **isDeleted** -Methode ruft einen Wert ab, der angibt, ob sich die angegebene Wiedergabeliste im Ordner "Gelöschte Elemente" befindet.

## <a name="syntax"></a>Syntax


```JScript
bRetVal = PlaylistCollection.isDeleted(
  playlist
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wiedergabeliste* \[ in\]
</dt> <dd>

Das **Wiedergabe** Listen Objekt, nach dem gesucht werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen **booleschen** Wert zurück.

**Windows Media Player 10 Mobile**: Diese Methode gibt immer **false** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0, Windows Media Player Version 7,1 oder Windows Media Player für Windows XP. Diese Methode wird für Windows Media Player 9-Serie oder höher nicht unterstützt.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Playlistcollection-Objekt**](playlistcollection-object.md)
</dt> </dl>

 

 





