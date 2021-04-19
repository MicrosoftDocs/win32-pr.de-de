---
description: Dekonstruktormethode.
ms.assetid: eed6c566-8a03-4a97-9d99-8e500ce2954c
title: Camthread. ~ camthread-debugtor (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.~CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b0b0a4dde858811a75347105b9fccd2f499c4faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361545"
---
# <a name="camthreadcamthread-destructor"></a>Camthread. ~ camthread-Dekonstruktor

Dekonstruktormethode.

## <a name="syntax"></a>Syntax


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a>Bemerkungen

Der Dekonstruktor Ruft die Methode " [**camthread:: Close**](camthread-close.md) " auf, die darauf wartet, dass der Thread beendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camthread-Klasse**](camthread.md)
</dt> </dl>

 

 




