---
description: Flag, das angibt, ob sich die Pufferanforderungen geändert haben.
ms.assetid: 34d946f9-125c-40fb-b09e-82457add07d6
title: CBaseAllocator::m_bChanged-Member (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7edb5ed770628d7dfd982017e720ef0136bace74dd7e311121925f6c8657d2fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131500"
---
# <a name="cbaseallocatorm_bchanged-member"></a>CBaseAllocator::m \_ bChanged-Member

Flag, das angibt, ob sich die Pufferanforderungen geändert haben. Die [**CBaseAllocator::SetProperties-Methode**](cbaseallocator-setproperties.md) legt den Wert auf **TRUE** fest. In einer abgeleiteten Klasse sollte die reine virtuelle Methode [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) den Wert wieder auf **FALSE** festlegen. Sobald Puffer zugeordnet wurden, müssen sie nicht erneut zugeordnet werden, während *m \_ bChanged* **AUF FALSE** festgelegt ist.

## <a name="syntax"></a>Syntax


```C++
BOOL m_bChanged;
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseAllocator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




