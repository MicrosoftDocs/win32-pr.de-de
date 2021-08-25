---
description: Anzahl ausstehender Sperren für dieses Objekt.
ms.assetid: 27506c1d-6a9a-4410-80fb-6d4f2fd2f824
title: CCritSec::m_lockCount-Member (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lockCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9885f3270c021432342605ad84c1b521672022f4a13cecac5ac49c9248c65d17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872210"
---
# <a name="ccritsecm_lockcount-member"></a>CCritSec::m \_ lockCount-Member

Anzahl ausstehender Sperren für dieses Objekt.

## <a name="syntax"></a>Syntax


```C++
DWORD m_lockCount;
```



## <a name="remarks"></a>Hinweise

Diese Membervariable wird nur in der Debugversion der Basisklasse definiert. Die [Funktionen für das Debuggen von kritischen](critical-section-debugging-functions.md) Abschnitten verwenden diesen Member.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CCritSec-Klasse**](ccritsec.md)
</dt> </dl>

 

 




