---
description: 'CSourceStream.~CSourceStream-Destruktor : Destruktormethode.'
ms.assetid: 678085c2-5999-4e62-8749-99b783787cc6
title: CSourceStream.~CSourceStream-Destruktor (Source.h)
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
ms.openlocfilehash: bbf53184dadc42145758ab387d15e8b0a1bfe09d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085208"
---
# <a name="csourcestreamcsourcestream-destructor"></a>CSourceStream.~CSourceStream-Destruktor

Destruktormethode.

## <a name="syntax"></a>Syntax


```C++
~CSourceStream();
```



## <a name="remarks"></a>Bemerkungen

Der Destruktor entfernt den Pin automatisch aus dem besitzenden Filter, indem er [**CSource::RemovePin aufruft.**](csource-removepin.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CSourceStream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




