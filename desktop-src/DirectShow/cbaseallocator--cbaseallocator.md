---
description: CBaseAllocator.~CBaseAllocator-Destruktor – Destruktormethode.
ms.assetid: b1e5653f-d72f-4cde-a8c9-d25763434374
title: CBaseAllocator.~CBaseAllocator-Destruktor (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.~CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89b87bd4e706e5270b49ca94d1c86a6c5a5326fd3efccb1dcc45b9681e6e2fca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017558"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a>CBaseAllocator.~CBaseAllocator-Destruktor

Destruktormethode.

## <a name="syntax"></a>Syntax


```C++
~CBaseAllocator();
```



## <a name="remarks"></a>Hinweise

Rufen Sie immer [**die CBaseAllocator::D commit-Methode auf,**](cbaseallocator-decommit.md) bevor Sie das Objekt zerstören. Der Basisklassen-Destruktor kann **decommit** nicht aufrufen, da diese Methode die reine virtuelle [**Methode CBaseAllocator::Free aufruft.**](cbaseallocator-free.md) Abgeleitete Klassen sollten diesen Destruktor überschreiben und **Decommit aufrufen.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseAllocator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




