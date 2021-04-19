---
description: Anzahl der ausstehenden Sperren für dieses Objekt.
ms.assetid: 27506c1d-6a9a-4410-80fb-6d4f2fd2f824
title: 'Ccritsec:: m_lockCount Member (wxutil. h)'
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
ms.openlocfilehash: 88098a8ded025a899e2092a96308bd6c54750758
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373843"
---
# <a name="ccritsecm_lockcount-member"></a>Ccritsec:: m- \_ LockCount-Member

Anzahl der ausstehenden Sperren für dieses Objekt.

## <a name="syntax"></a>Syntax


```C++
DWORD m_lockCount;
```



## <a name="remarks"></a>Bemerkungen

Diese Member-Variable wird nur in der Debugversion der Basisklasse definiert. Der [kritische Abschnitt Debuggingfunktionen](critical-section-debugging-functions.md) verwenden diesen Member.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ccritsec-Klasse**](ccritsec.md)
</dt> </dl>

 

 




