---
description: 'CABThread.~CABThread-Destruktor : Destruktormethode.'
ms.assetid: eed6c566-8a03-4a97-9d99-8e500ce2954c
title: CABThread.~HIDThread-Destruktor (Wxutil.h)
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
ms.openlocfilehash: 884460b0c1af3b96a610a18b7475d2a144dc32bf308ea0e0191f0f526565726a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662376"
---
# <a name="camthreadcamthread-destructor"></a>CABThread.~MSIThread-Destruktor

Destruktormethode.

## <a name="syntax"></a>Syntax


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a>Hinweise

Der Destruktor ruft die [**METHODE CABThread::Close**](camthread-close.md) auf, die darauf wartet, dass der Thread beendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WEBCAMThread-Klasse**](camthread.md)
</dt> </dl>

 

 




