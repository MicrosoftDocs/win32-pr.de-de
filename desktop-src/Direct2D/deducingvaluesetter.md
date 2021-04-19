---
title: Deducingvaluesetter (D2d1effecthelpers. h)
description: Leitet die-Klasse und die-Argumente ab und ruft dann einen Eigenschaften Setter-Rückruf für eine Element Funktion für eine Value-Type-Eigenschaft auf.
ms.assetid: 4C3D64A8-0CC0-405A-A5B3-627C2DF25EA1
keywords:
- Deducingvaluesetter Direct2D
topic_type:
- apiref
api_name:
- DeducingValueSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e002c5a36c8ac0b196dfc5fb25e11f7f9d63806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365673"
---
# <a name="deducingvaluesetter"></a>Deducingvaluesetter

Leitet die-Klasse und die-Argumente ab und ruft dann einen Eigenschaften Setter-Rückruf für eine Element Funktion für eine Value-Type-Eigenschaft auf.

> [!Note]  
> Deducingvaluesetter sollte nicht direkt aufgerufen werden.

 

``` syntax
template<class C, typename P, typename I>
HRESULT DeducingValueSetter(
    _In_ HRESULT (C::*callback)(P),
    _In_ I *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D2d1effecthelpers. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Direct2D::D educingvaluegetter**](deducingvaluegetter.md)
</dt> </dl>

 

 





