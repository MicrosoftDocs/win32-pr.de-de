---
description: Die Lock-Methode sperrt das Critical Section-Objekt.
ms.assetid: b08be5ec-3f02-4ed8-8791-20e4d2a0c55f
title: Ccritsec. Lock-Methode (wxutil. h)
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
ms.openlocfilehash: 19599e9cd3c3b8fa913bd07d22fe743aaaa1382f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370943"
---
# <a name="ccritseclock-method"></a>Ccritsec. Lock-Methode

Die **Lock** -Methode sperrt das Critical Section-Objekt.

## <a name="syntax"></a>Syntax


```C++
void Lock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) -Funktion auf.

Zum Entsperren des kritischen Abschnitts wird die [**ccritsec:: Unlock**](ccritsec-unlock.md) -Member-Funktion aufgerufen. Sie können mehrere Aufrufe der **Lock** -Methode im gleichen Thread durchführen. Stellen Sie sicher, dass Sie die **Sperre** beliebig oft aufzurufen.

Wenn das Objekt bereits von einem anderen Thread gesperrt ist, wird die **ccritsec:: Lock** -Methode blockiert, bis das Objekt freigegeben wird, oder bis eine mögliche deadlockausnahme auftritt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ccritsec-Klasse**](ccritsec.md)
</dt> </dl>

 

