---
description: Die Unlock-Methode entsperrt das kritische Abschnittsobjekt.
ms.assetid: 61811e0e-df77-48e9-96d5-b7dff8c8db9b
title: CCritSec.Unlock-Methode (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Unlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 919b73e5e1fc0becfb7c5fad40b87a5eb28fa008ba5cea1706373ddec9128682
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074384"
---
# <a name="ccritsecunlock-method"></a>CCritSec.Unlock-Methode

Die **Unlock-Methode** entsperrt das kritische Abschnittsobjekt.

## <a name="syntax"></a>Syntax


```C++
void Unlock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode ruft die [**LeaveCriticalSection-Funktion**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection) auf. Rufen Sie diese Methode einmal für jeden Aufruf der [**CCritSec::Lock-Methode**](ccritsec-lock.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CCritSec-Klasse**](ccritsec.md)
</dt> </dl>

 

