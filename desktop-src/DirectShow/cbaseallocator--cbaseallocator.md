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
ms.openlocfilehash: 9a4b754c8937b87a547f4583b3270f5782a6a415
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096418"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a>CBaseAllocator.~CBaseAllocator-Destruktor

Destruktormethode.

## <a name="syntax"></a>Syntax


```C++
~CBaseAllocator();
```



## <a name="remarks"></a>Bemerkungen

Rufen Sie immer [**die CBaseAllocator::D commit-Methode auf,**](cbaseallocator-decommit.md) bevor Sie das Objekt zerstören. Der Basisklassen-Destruktor kann **decommit** nicht aufrufen, da diese Methode die reine virtuelle [**Methode CBaseAllocator::Free aufruft.**](cbaseallocator-free.md) Abgeleitete Klassen sollten diesen Destruktor überschreiben und **Decommit aufrufen.**

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseAllocator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




