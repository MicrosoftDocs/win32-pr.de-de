---
description: Gibt TRUE zurück, wenn der aktuelle Thread der Besitzer des angegebenen kritischen Abschnitts ist.
ms.assetid: 96158f08-07a0-42a9-b173-0a05456a5f3a
title: CritCheckIn-Funktion (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckIn
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f4e9ff0078f6efe8dee9b060e61858c24aea0a64e7e35b9fb867125b8612ed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908080"
---
# <a name="critcheckin-function"></a>CritCheckIn-Funktion

Gibt **TRUE zurück,** wenn der aktuelle Thread der Besitzer des angegebenen kritischen Abschnitts ist.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CritCheckIn(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcCrit* 
</dt> <dd>

Zeiger auf einen [**kritischen CCritSec-Abschnitt.**](ccritsec.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

In Debugbuilds gibt **TRUE zurück,** wenn der aktuelle Thread der Besitzer dieses kritischen Abschnitts ist, andernfalls **FALSE.** In Einzelhandels-Builds gibt immer **TRUE zurück.**

## <a name="remarks"></a>Hinweise

Diese Funktion ist besonders [](assert.md) nützlich innerhalb des ASSERT-Makros, um zu testen, ob ein Thread eine bestimmte Sperre besitzt.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird die Verwendung dieser Funktion veranschaulicht:


```
{
    CCritSec MyLock;  // Critical section is not locked yet.
    
    ASSERT(CritCheckIn(&MyLock)); // This assert will fire.

    // Lock the critical section.    
    CAutoLock cObjectLock(&MyLock);
     
    ASSERT(CritCheckIn(&MyLock)); // This assert will not fire.

} // Lock goes out of scope here.
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Wichtige Funktionen für das Debuggen von Abschnitten](critical-section-debugging-functions.md)
</dt> </dl>

 

 




