---
description: Die \_ m bModifiesData-Membervariable gibt an, ob der Filter die empfangenen Beispieldaten ändert. Der Wert wird im CTransInPlaceFilter-Konstruktor festgelegt, ist jedoch standardmäßig auf TRUE festgelegt.
ms.assetid: 8ccdba46-315f-4519-b363-6870d1217f98
title: CTransInPlaceFilter::m_bModifiesData-Member (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bModifiesData
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7461f7f62a6cbd1fea2ff18f6e8f2e4b73825ea04cb9e3b0a679ee7cf15fef90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654879"
---
# <a name="ctransinplacefilterm_bmodifiesdata-member"></a>CTransInPlaceFilter::m \_ bModifiesData-Member

Die `m_bModifiesData` Membervariable gibt an, ob der Filter die empfangenen Beispieldaten ändert. Der Wert wird im **CTransInPlaceFilter-Konstruktor** festgelegt, ist jedoch standardmäßig auf **TRUE** festgelegt.

## <a name="syntax"></a>Syntax


```C++
bool m_bModifiesData;
```



## <a name="remarks"></a>Hinweise

Diese Variable wirkt sich darauf aus, wie der Filter die Zuweisung aushandelt. Wenn der Wert **TRUE** ist, kann der Filter keine schreibgeschützte Zuweisung für beide Pinverbindungen verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransInPlaceFilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




