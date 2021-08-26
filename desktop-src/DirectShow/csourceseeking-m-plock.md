---
description: Zeiger auf ein kritisches Abschnittsobjekt.
ms.assetid: dc791bc4-857c-4a79-9aa8-3c5974c23483
title: CSourceSeeking::m_pLock Member (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f230fcaee4ebb59520319d5dfd7cf8295ce8721716cd1ffb02b534e242bd99b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054020"
---
# <a name="csourceseekingm_plock-member"></a>CSourceSeeking::m \_ pLock-Member

Zeiger auf ein kritisches Abschnittsobjekt. Die -Klasse verwendet diesen kritischen Abschnitt, um den Zugriff auf die Start- und `CSourceSeeking` Stoppzeiten, die Dauer und die Rate-Variablen zu synchronisieren. Diese Variable wird in der Konstruktormethode initialisiert. siehe [**CSourceSeeking::CSourceSeeking**](csourceseeking-csourceseeking.md).

## <a name="syntax"></a>Syntax


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




