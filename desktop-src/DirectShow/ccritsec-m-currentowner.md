---
description: Thread Bezeichner des besitzenden Threads.
ms.assetid: 495598db-a0c9-473b-8184-121a1939b55a
title: 'Ccritsec:: m_currentOwner Member (wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_currentOwner
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6dcb8d968f1f437087a94c5b08db12d31952d92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372718"
---
# <a name="ccritsecm_currentowner-member"></a>Ccritsec:: m \_ currentowner-Member

Thread Bezeichner des besitzenden Threads.

## <a name="syntax"></a>Syntax


```C++
DWORD m_currentOwner;
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

 

 




