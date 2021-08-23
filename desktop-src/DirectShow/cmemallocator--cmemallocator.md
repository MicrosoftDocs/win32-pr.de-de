---
description: CMemAllocator.~CMemAllocator-Destruktor – Destruktormethode.
ms.assetid: e0a04d93-fb77-4dc1-9bc8-7d3965bc6803
title: CMemAllocator.~CMemAllocator-Destruktor (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.~CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 588b370fc56f6af547ead19c7a52758a3851dd7e46d88b90f8f621ed6002d6e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954379"
---
# <a name="cmemallocatorcmemallocator-destructor"></a>CMemAllocator.~CMemAllocator-Destruktor

Destruktormethode.

## <a name="syntax"></a>Syntax


```C++
~CMemAllocator();
```



## <a name="remarks"></a>Hinweise

Diese Methode überschreibt den Basisklassen-Destruktor, um [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) und [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md)aufzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMemAllocator-Klasse**](cmemallocator.md)
</dt> </dl>

 

 




