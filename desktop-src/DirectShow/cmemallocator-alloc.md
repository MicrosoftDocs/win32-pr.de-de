---
description: Die Methode "Zuweisung" weist Speicher für die Puffer zu.
ms.assetid: 81886163-2f7d-4d4f-be90-4491f76b8514
title: Cmemzuzucator. Zuordnungsmethode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a142f6c0cea6cdb9b18507becabb909ce67b0fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358063"
---
# <a name="cmemallocatoralloc-method"></a>Cmemzuzucator. Zuordnungsmethode

Die- `Alloc` Methode weist Speicher für die Puffer zu.

## <a name="syntax"></a>Syntax


```C++
HRESULT Alloc();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                       | Beschreibung                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Erfolg.<br/>                          |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>     | Nicht genügend Arbeitsspeicher.<br/>              |
| <dl> <dt>**VFW \_ E \_ sizenotset**</dt> </dl> | Die Puffer Anforderungen wurden nicht festgelegt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode wird von der [**cbasezucator:: Commit**](cbaseallocator-commit.md) -Methode aufgerufen. Er ordnet einen zusammenhängenden Speicherblock zu, der für die in der [**cmembelegcator:: SetProperties**](cmemallocator-setproperties.md) -Methode angegebenen Puffer Anforderungen ausreicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmemzuordcator-Klasse**](cmemallocator.md)
</dt> </dl>

 

 




