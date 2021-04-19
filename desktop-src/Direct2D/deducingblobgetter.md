---
title: Deducingblobgetter (D2d1effecthelpers. h)
description: Leitet die-Klasse und die-Argumente ab und ruft dann einen Get-Rückruf Rückruf für eine Element Funktion für eine BLOB-Type-Eigenschaft auf.
ms.assetid: 1B8800CB-2AD0-4684-99D7-986F6C53A6F1
keywords:
- Deducingblobgetter Direct2D
topic_type:
- apiref
api_name:
- DeducingBlobGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f7ca5cc37a9fbd79807e258a87a199be7319ce3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352023"
---
# <a name="deducingblobgetter"></a>Deducingblobgetter

Leitet die-Klasse und die-Argumente ab und ruft dann einen Get-Rückruf Rückruf für eine Element Funktion für eine BLOB-Type-Eigenschaft auf.

> [!Note]  
> Deducingblobgetter sollte nicht direkt aufgerufen werden.

 

``` syntax
template<class C, typename I>  
HRESULT DeducingBlobGetter(  
    _In_ HRESULT (C::*callback)(BYTE *, UINT32, UINT32*) const,  
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

[**Direct2D::D educingblobsetter**](deducingblobsetter.md)
</dt> </dl>

 

 





