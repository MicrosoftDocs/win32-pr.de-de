---
description: Die pStateLock-Methode ruft einen Zeiger auf das kritische Abschnittsobjekt des Filters ab.
ms.assetid: 10a2e74b-a5aa-4d68-958e-d86f4b78037e
title: CSource.pStateLock-Methode (Source.h)
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
ms.openlocfilehash: b74027e2ee2339e647938592e05162ce85108eb6985061b30a825394c2f2e7be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953789"
---
# <a name="csourcepstatelock-method"></a>CSource.pStateLock-Methode

Die **pStateLock-Methode** ruft einen Zeiger auf das kritische Abschnittsobjekt des Filters ab.

> [!Note]  
> Obwohl sie wie eine Membervariable benannt ist, **ist pStateLock** eine Methode.

 

## <a name="syntax"></a>Syntax


```C++
CCritSec* pStateLock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf die [**CSource::m \_ cStateLock-Membervariable**](csource-m-cstatelock.md) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSource-Klasse**](csource.md)
</dt> </dl>

 

 




