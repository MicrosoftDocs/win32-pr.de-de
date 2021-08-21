---
description: Boolescher Wert, der angibt, ob diese Sperre verfolgt werden soll.
ms.assetid: 23417410-cfdc-426e-a662-7d6580b43a28
title: CCritSec::m_fTrace-Member (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5a47437e4f9ab475b64979ec970604ac7a621d2ab53ea7a3c87742fa81a8aab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074394"
---
# <a name="ccritsecm_ftrace-member"></a>CCritSec::m \_ fTrace-Member

Boolescher Wert, der angibt, ob diese Sperre verfolgt werden soll.

## <a name="syntax"></a>Syntax


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a>Hinweise

Diese Membervariable wird nur in der Debugversion der Basisklasse definiert. Wenn der Wert **TRUE ist,** wird eine Ablaufverfolgung des Sperrzustands in das Debugprotokoll geschrieben. (Debugprotokollierung für kritische Abschnitte muss aktiv sein.) Weitere Informationen finden Sie unter [**DbgLockTrace**](dbglocktrace.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CCritSec-Klasse**](ccritsec.md)
</dt> </dl>

 

 




