---
description: Anzahl der zu bereitstellenden Puffer.
ms.assetid: 73f87b14-4346-4909-bd1e-c4981cde403d
title: CBaseAllocator::m_lCount Member (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c33749ee6293c301501962939e25118595db10592713fb46dc10d01083c0096f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661692"
---
# <a name="cbaseallocatorm_lcount-member"></a>CBaseAllocator::m \_ lCount-Mitglied

Anzahl der zu bereitstellenden Puffer. Die [**CBaseAllocator::SetProperties-Methode legt**](cbaseallocator-setproperties.md) diesen Wert fest. Die Puffer werden erst zugeordnet, wenn die [**CBaseAllocator::Commit-Methode**](cbaseallocator-commit.md) aufgerufen wird. Die aktuelle Anzahl zugeordneter Puffer wird von der [**CBaseAllocator::m \_ lAllocated-Membervariablen**](cbaseallocator-m-lallocated.md) angegeben.

## <a name="syntax"></a>Syntax


```C++
long m_lCount;
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

 

 




