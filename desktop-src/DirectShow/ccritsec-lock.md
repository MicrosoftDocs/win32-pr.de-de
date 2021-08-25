---
description: Die Lock-Methode sperrt das kritische Abschnittsobjekt.
ms.assetid: b08be5ec-3f02-4ed8-8791-20e4d2a0c55f
title: CCritSec.Lock-Methode (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Lock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4241b2cd5e94fbd6a3cbe0abd91d47ad6312c44b71f76c214cffb22836033a7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928589"
---
# <a name="ccritseclock-method"></a>CCritSec.Lock-Methode

Die **Lock-Methode** sperrt das kritische Abschnittsobjekt.

## <a name="syntax"></a>Syntax


```C++
void Lock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode ruft die [**EnterCriticalSection-Funktion**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) auf.

Rufen Sie die [**CCritSec::Unlock-Memberfunktion**](ccritsec-unlock.md) auf, um den kritischen Abschnitt zu entsperren. Sie können mehrere Aufrufe der **Lock-Methode** für denselben Thread tätigen. Stellen Sie sicher, dass **Sie Die** Entsperrung entsprechend oft aufrufen.

Wenn das Objekt bereits von einem anderen Thread gesperrt ist, wird die **CCritSec::Lock-Methode** blockiert, bis das Objekt freigegeben wird oder bis eine mögliche Deadlockausnahme auftritt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CCritSec-Klasse**](ccritsec.md)
</dt> </dl>

 

