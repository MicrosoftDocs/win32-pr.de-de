---
description: Zeiger auf ein kritisches Abschnitts Objekt.
ms.assetid: dc791bc4-857c-4a79-9aa8-3c5974c23483
title: 'Csourceseeking:: m_pLock Member (ctlutil. h)'
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
ms.openlocfilehash: 2f8de9159e917d24701635a428e0f5e6a1b9cb55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373827"
---
# <a name="csourceseekingm_plock-member"></a>Csourceseeking:: m \_ Plock-Member

Zeiger auf ein kritisches Abschnitts Objekt. Die- `CSourceSeeking` Klasse verwendet diesen kritischen Abschnitt, um den Zugriff auf die Start-und Endzeit-, Dauer-und Raten Variablen zu synchronisieren. Diese Variable wird in der Konstruktormethode initialisiert. siehe [**csourceseeking:: csourceseeking**](csourceseeking-csourceseeking.md).

## <a name="syntax"></a>Syntax


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourceseeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




