---
description: Dekonstruktormethode.
ms.assetid: b1e5653f-d72f-4cde-a8c9-d25763434374
title: Cbasezucator. ~ cbasezucator-debugtor (amfilter. h)
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
ms.openlocfilehash: 53587482c5d9cf8f5a772453f220c7633c17d383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364030"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a>Cbasezucator. ~ cbasezuweisung-Dekonstruktor

Dekonstruktormethode.

## <a name="syntax"></a>Syntax


```C++
~CBaseAllocator();
```



## <a name="remarks"></a>Bemerkungen

Immer die [**cbasezucator::D ecommit**](cbaseallocator-decommit.md) -Methode aufruft, bevor das Objekt zerstört wird. Der basisklassendekonstruktor kann " **Decommit**" nicht aufrufen, da diese Methode die rein virtuelle Methode " [**cbasezucator:: Free**](cbaseallocator-free.md)" aufruft. Abgeleitete Klassen sollten diesen Dekonstruktor überschreiben und **Decommit** aufzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasezucator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




