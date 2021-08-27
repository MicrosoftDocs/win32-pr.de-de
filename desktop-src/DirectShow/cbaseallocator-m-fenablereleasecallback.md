---
description: Flag, das angibt, ob der Releaserückruf aktiviert ist. Dieses Flag wird in der Konstruktormethode festgelegt. Wenn der Wert FALSE ist, löst der Aufruf der CBaseAllocator::SetNotify-Methode eine Assertion aus (in Debugbuilds).
ms.assetid: cc9adc7c-ec44-41e7-875a-b3e553120804
title: CBaseAllocator::m_fEnableReleaseCallback Member (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fEnableReleaseCallback
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2fc1dfebb051ddffffce341547562901153b47bd5da002ebd847965593a73d93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131460"
---
# <a name="cbaseallocatorm_fenablereleasecallback-member"></a>CBaseAllocator::m \_ fEnableReleaseCallback-Member

Flag, das angibt, ob der Releaserückruf aktiviert ist. Dieses Flag wird in der Konstruktormethode festgelegt. Wenn der Wert **FALSE ist,** bewirkt der Aufruf der [**CBaseAllocator::SetNotify-Methode,**](cbaseallocator-setnotify.md) dass eine Assertion (in Debugbuilds) ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
BOOL m_fEnableReleaseCallback;
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseAllocator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




