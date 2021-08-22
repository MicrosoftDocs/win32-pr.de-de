---
description: Threadbezeichner des besitzenden Threads.
ms.assetid: 495598db-a0c9-473b-8184-121a1939b55a
title: CCritSec::m_currentOwner-Member (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_currentOwner
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71c88055f5068a5486c1eb6e3ac739235a6b7cde2e8d6b767380160ff12503be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657213"
---
# <a name="ccritsecm_currentowner-member"></a>CCritSec::m \_ currentOwner-Member

Threadbezeichner des besitzenden Threads.

## <a name="syntax"></a>Syntax


```C++
DWORD m_currentOwner;
```



## <a name="remarks"></a>Hinweise

Diese Membervariable wird nur in der Debugversion der Basisklasse definiert. Die [Debugfunktionen des kritischen Abschnitts](critical-section-debugging-functions.md) verwenden diesen Member.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CCritSec-Klasse**](ccritsec.md)
</dt> </dl>

 

 




