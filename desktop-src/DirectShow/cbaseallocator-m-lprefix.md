---
description: Präfix jedes Puffers in Bytes.
ms.assetid: 471b73bf-f959-41aa-84ba-324a2738dd0e
title: CBaseAllocator::m_lPrefix Member (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lPrefix
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a22f2ac1a54c4820f109b55002428c87df321328ef6b6b6d6096343df8cde85f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955289"
---
# <a name="cbaseallocatorm_lprefix-member"></a>CBaseAllocator::m \_ lPrefix-Member

Präfix jedes Puffers in Bytes. Wenn der Wert nicht 0 (null) ist, wird jedem Pufferzeiger, der von der [**CBaseAllocator::GetBuffer-Methode**](cbaseallocator-getbuffer.md) zurückgegeben wird, ein Byteblock der Größe *m \_ lPrefix voranstehen.* Dieser Speicherblock wird als Präfix *bezeichnet.* Die [**CBaseAllocator::m \_ lSize-Membervariable**](cbaseallocator-m-lsize.md) enthält nicht den Präfixwert.

## <a name="syntax"></a>Syntax


```C++
long m_lPrefix;
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseAllocator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




