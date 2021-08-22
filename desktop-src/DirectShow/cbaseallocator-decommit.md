---
description: Die Decommit-Methode dekommitiert die Zuweisung. Diese Methode implementiert die IMemAllocator::D ecommit-Methode.
ms.assetid: 0c8d44e0-17ea-4f7f-be44-f9ae2e34fbef
title: CBaseAllocator.Decommit-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Decommit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 614986a912f08d918d4fbbaf6b3eeeb0d3b2c3eabc47748351934a08b8280cca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017548"
---
# <a name="cbaseallocatordecommit-method"></a>CBaseAllocator.Decommit-Methode

Die `Decommit` -Methode dekommitiert die Zuweisung. Diese Methode implementiert die [**IMemAllocator::D ecommit-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit)

## <a name="syntax"></a>Syntax


```C++
HRESULT Decommit();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Nachdem diese Methode aufgerufen wurde, schlagen Aufrufe der [**CBaseAllocator::GetBuffer-Methode**](cbaseallocator-getbuffer.md) fehl. Wenn Die Beispiele veröffentlicht werden, werden sie in die kostenlose Liste zurückgegeben. Wenn das letzte Beispiel zurückgegeben wird, ruft der Allocator die [**CBaseAllocator::Free-Methode**](cbaseallocator-free.md) auf, die den zugeordneten Arbeitsspeicher freigibt. (In der Basisklasse ist **Free** eine reine virtuelle Methode.)

Darüber hinaus gibt diese Methode alle Threads frei, die für **GetBuffer-Aufrufe** blockiert sind. Die Aufrufe von **GetBuffer** schlagen fehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseAllocator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




