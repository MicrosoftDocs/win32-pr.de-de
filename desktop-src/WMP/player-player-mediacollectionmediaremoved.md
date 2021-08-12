---
title: Player.MediaCollectionMediaRemoved-Ereignis
description: Das MediaCollectionMediaRemoved-Ereignis tritt auf, wenn ein Medienelement aus der lokalen Bibliothek entfernt wird. | Player.MediaCollectionMediaRemoved-Ereignis
ms.assetid: a1df6faf-38dc-4f5f-8f8a-953c91ea026c
keywords:
- MediaCollectionMediaRemoved-Ereignis Windows Media Player
- MediaCollectionMediaRemoved-Ereignis Windows Media Player , Player-Klasse
- Player-Windows Media Player , MediaCollectionMediaRemoved-Ereignis
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 009432040deace140dd3cf4d7d7da1246c0a38dbd9fc0da028832af137cefa83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572850"
---
# <a name="playermediacollectionmediaremoved-event"></a>Player.MediaCollectionMediaRemoved-Ereignis

Das MediaCollectionMediaRemoved-Ereignis tritt auf, wenn ein Medienelement aus der lokalen Bibliothek entfernt wird.

## <a name="syntax"></a>Syntax


```JScript
Player.MediaCollectionMediaRemoved(
  pdispMedia
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdispMedia* 
</dt> <dd>

**Medienobjekt,** das entfernt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dieses Ereignis tritt nur für die lokale Bibliothek auf.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MediaCollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player.mediaCollection**](player-mediacollection.md)
</dt> </dl>

 

 





