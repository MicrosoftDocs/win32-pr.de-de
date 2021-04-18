---
title: Deducingstringgetter (D2d1effecthelpers. h)
description: Leitet die-Klasse und die-Argumente ab und ruft dann für eine Eigenschaft vom Typ "String" einen Eigenschaften-Getter-Rückruf für eine Element Funktion auf.
ms.assetid: 434E3360-D6C3-46CB-818E-15A185F4BB84
keywords:
- Deducingstringgetter Direct2D
topic_type:
- apiref
api_name:
- DeducingStringGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac65b9e5d7e37e2db83f06f80172e90f9f27f80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351351"
---
# <a name="deducingstringgetter"></a>Deducingstringgetter

Leitet die-Klasse und die-Argumente ab und ruft dann für eine Eigenschaft vom Typ "String" einen Eigenschaften-Getter-Rückruf für eine Element Funktion auf.

> [!Note]  
> Deducingstringgetter sollte nicht direkt aufgerufen werden.

 

``` syntax
template<class C, typename I>  
HRESULT DeducingStringGetter(
    _In_ HRESULT (C::*callback)(PWSTR, UINT32, UINT32*) const,
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

[**Direct2D::D educingstringsetter**](deducingstringsetter.md)
</dt> </dl>

 

 





