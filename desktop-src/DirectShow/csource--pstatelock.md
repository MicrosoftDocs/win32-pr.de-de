---
description: Die pstatus-Methode ruft einen Zeiger auf das kritische Abschnitts Objekt des Filters ab.
ms.assetid: 10a2e74b-a5aa-4d68-958e-d86f4b78037e
title: CSource. pstatuelock-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.pStateLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0705584a513d64dfd1cd17075d95617234f7f8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367445"
---
# <a name="csourcepstatelock-method"></a>CSource. pstatuelock-Methode

Die **pstatus** -Methode ruft einen Zeiger auf das kritische Abschnitts Objekt des Filters ab.

> [!Note]  
> Obwohl der benannte Wert wie eine Member-Variable lautet, ist **pstatuelock** eine-Methode.

 

## <a name="syntax"></a>Syntax


```C++
CCritSec* pStateLock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf die [**CSource:: m \_ cstatus**](csource-m-cstatelock.md) -Member-Variable zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSource-Klasse**](csource.md)
</dt> </dl>

 

 




