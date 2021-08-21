---
description: Flag, das angibt, ob der Pin seine eigenen bevorzugten Medientypen vor denen des empfangenden Pins versucht.
ms.assetid: 50462ee4-4a61-472f-9a7e-9cdb39be4dea
title: CBasePin::m_bTryMyTypesFirst-Member (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bTryMyTypesFirst
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df94a95783d15c09fd53bd8659db71f2ce0b1aefe5d855fef5f5a03e71445493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158371"
---
# <a name="cbasepinm_btrymytypesfirst-member"></a>CBasePin::m \_ bTryMyTypesFirst-Member

Flag, das angibt, ob der Pin seine eigenen bevorzugten Medientypen vor denen des empfangenden Pins versucht.

## <a name="syntax"></a>Syntax


```C++
bool m_bTryMyTypesFirst;
```



## <a name="remarks"></a>Hinweise

Dieses Flag ist standardmäßig auf **FALSE festgelegt.** Wenn das Flag **TRUE** ist, kehrt die [**CBasePin::AgreeMediaType-Methode**](cbasepin-agreemediatype.md) die Reihenfolge um, in der Medientypen versucht werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




