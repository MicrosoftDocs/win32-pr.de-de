---
description: Startzeit. In der Standardeinstellung ist dieser Wert auf 0 festgelegt.
ms.assetid: bafa69c3-ead0-4409-abbf-4e8cc325e5f9
title: CSourceSeeking::m_rtStart-Member (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtStart
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98f19edd3d7225882a4b966c6a9916a46fddeb1e4a9340f3c702869c0c8e3c8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053960"
---
# <a name="csourceseekingm_rtstart-member"></a>CSourceSeeking::m \_ rtStart-Member

Startzeit. In der Standardeinstellung ist dieser Wert auf 0 festgelegt.

## <a name="syntax"></a>Syntax


```C++
CRefTime m_rtStart;
```



## <a name="remarks"></a>Hinweise

Halten Sie den kritischen m **\_ pLock-Abschnitt** bei, bevor Sie auf diese Variable zugreifen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




