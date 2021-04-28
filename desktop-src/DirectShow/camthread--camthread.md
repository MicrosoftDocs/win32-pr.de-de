---
description: CABThread.~CABThread-Destruktor – Destruktormethode.
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
ms.openlocfilehash: 84a40205fc93677f20256676ad09a18357d46acb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096438"
---
# <a name="camthreadcamthread-destructor"></a>CABThread.~CABThread-Destruktor

Destruktormethode.

## <a name="syntax"></a>Syntax


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a>Bemerkungen

Der Destruktor ruft die [**METHODE CABThread::Close**](camthread-close.md) auf, die darauf wartet, dass der Thread beendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WEBCAMThread-Klasse**](camthread.md)
</dt> </dl>

 

 




