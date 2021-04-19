---
title: Deducingstringsetter (D2d1effecthelpers. h)
description: Leitet die-Klasse und die-Argumente ab und ruft dann einen Eigenschaften Setter-Rückruf für eine Element Funktion für eine Eigenschaft vom Typ "String" auf.
ms.assetid: D3075B7B-D253-4F85-9FD2-3487C4207122
keywords:
- Deducingstringsetter Direct2D
topic_type:
- apiref
api_name:
- DeducingStringSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7860978fd271b2ff395caae068cd651d3057020
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354210"
---
# <a name="deducingstringsetter"></a>Deducingstringsetter

Leitet die-Klasse und die-Argumente ab und ruft dann einen Eigenschaften Setter-Rückruf für eine Element Funktion für eine Eigenschaft vom Typ "String" auf.

> [!Note]  
> Deducingstringsetter sollte nicht direkt aufgerufen werden.

 

``` syntax
template<class C, typename I>  
HRESULT DeducingStringSetter(  
    _In_ HRESULT (C::*callback)(PCWSTR string),
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

[**Direct2D::D educingstringgetter**](deducingstringgetter.md)
</dt> </dl>

 

 





