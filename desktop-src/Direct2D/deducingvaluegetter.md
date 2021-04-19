---
title: Deducingvaluegetter (D2d1effecthelpers. h)
description: Leitet die-Klasse und die-Argumente ab und ruft dann einen getget-Rückruf Rückruf für eine Element Funktion für eine Value-Type-Eigenschaft auf.
ms.assetid: E2E5CCC3-B112-4D3C-8840-121A55C4F1A2
keywords:
- Deducingvaluegetter Direct2D
topic_type:
- apiref
api_name:
- DeducingValueGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6332dd6eac823457882513f97557939db884efcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356368"
---
# <a name="deducingvaluegetter"></a>Deducingvaluegetter

Leitet die-Klasse und die-Argumente ab und ruft dann einen getget-Rückruf Rückruf für eine Element Funktion für eine Value-Type-Eigenschaft auf.

> [!Note]  
> Deducingvaluegetter sollte nicht direkt aufgerufen werden.

 

``` syntax
template<class C, typename P, typename I>
HRESULT DeducingValueGetter(
    _In_ P (C::*callback)() const,
    _In_ const I *effect,
    _Out_writes_opt_(dataSize) BYTE *data,
    UINT32 dataSize,
    _Out_opt_ UINT32 *actualSize  
    ) 
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D2d1effecthelpers. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Direct2D::D educingvaluesetter**](deducingvaluesetter.md)
</dt> </dl>

 

 





