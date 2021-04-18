---
description: Dekonstruktormethode.
ms.assetid: 678085c2-5999-4e62-8749-99b783787cc6
title: Csourcestream. ~ csourcestream-debugtor (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.~CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa27d50a9c1acbc9c8a27407cb97673d60158e4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372106"
---
# <a name="csourcestreamcsourcestream-destructor"></a>Csourcestream. ~ csourcestream-Dekonstruktor

Dekonstruktormethode.

## <a name="syntax"></a>Syntax


```C++
~CSourceStream();
```



## <a name="remarks"></a>Bemerkungen

Der Dekonstruktor entfernt die PIN automatisch aus dem besitzenden Filter, indem [**CSource:: removepin**](csource-removepin.md)aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourcestream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




