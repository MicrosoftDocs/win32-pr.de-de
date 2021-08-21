---
description: Die \_ m pAlloc-Membervariable ist ein Zeiger auf die IMemAllocator-Schnittstelle der Speicherzuweisung.
ms.assetid: a3be5982-83f0-4552-9bcd-85da4a4918ff
title: CPullPin::m_pAlloc-Member (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAlloc
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 76abcdadf24006d545a8e8cf51205a99656a634094487104b9bad5d9b553c33c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073454"
---
# <a name="cpullpinm_palloc-member"></a>CPullPin::m \_ pAlloc-Member

Die `m_pAlloc` Membervariable ist ein Zeiger auf die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) der Speicherzuweisung.

## <a name="syntax"></a>Syntax


```C++
IMemAllocator *m_pAlloc;
```



## <a name="remarks"></a>Hinweise

Die [**CPullPin::D ecideAllocator-Methode**](cpullpin-decideallocator.md) legt diese Membervariable fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPullPin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




