---
description: Dekonstruktormethode.
ms.assetid: e0a04d93-fb77-4dc1-9bc8-7d3965bc6803
title: Cmemzuordcator. ~ cmemzugerdebugtor (amfilter. h)
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
ms.openlocfilehash: d49046eccd8d7ef71c4eeb4c75acffbf90f7d826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369670"
---
# <a name="cmemallocatorcmemallocator-destructor"></a>Cmemzuordcator. ~ cmemzugerdekonstruktor

Dekonstruktormethode.

## <a name="syntax"></a>Syntax


```C++
~CMemAllocator();
```



## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt den basisklassendekonstruktor zum Aufrufen von [**cbasezucator::D ecommit**](cbaseallocator-decommit.md) und [**cmemzucator:: reallyfree**](cmemallocator-reallyfree.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmemzuordcator-Klasse**](cmemallocator.md)
</dt> </dl>

 

 




