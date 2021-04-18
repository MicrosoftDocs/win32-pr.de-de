---
description: Gibt true zurück, wenn der aktuelle Thread der Besitzer des angegebenen kritischen Abschnitts ist.
ms.assetid: 96158f08-07a0-42a9-b173-0a05456a5f3a
title: Critcheckin-Funktion (wxutil. h)
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
ms.openlocfilehash: ff31707dc409db1e72c36866150c5a0b24c53f9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368390"
---
# <a name="critcheckin-function"></a>Critcheckin-Funktion

Gibt **true** zurück, wenn der aktuelle Thread der Besitzer des angegebenen kritischen Abschnitts ist.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CritCheckIn(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pccrit* 
</dt> <dd>

Zeiger auf einen kritischen [**ccritsec**](ccritsec.md) -Abschnitt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

In Debugbuilds gibt **true** zurück, wenn der aktuelle Thread der Besitzer dieses kritischen Abschnitts ist, andernfalls **false** . In Einzelhandels Builds gibt immer **true** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist im [**Assert**](assert.md) -Makro besonders nützlich, um zu testen, ob ein Thread eine bestimmte Sperre besitzt.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt die Verwendung dieser Funktion:


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
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kritische Abschnitts Debuggingfunktionen](critical-section-debugging-functions.md)
</dt> </dl>

 

 




