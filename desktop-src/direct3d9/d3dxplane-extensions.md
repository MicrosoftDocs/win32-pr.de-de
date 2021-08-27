---
description: Stellt die folgenden Operatorüberladungen und Typcasts für D3DXPLANE-Strukturen zur Folge.
ms.assetid: 05f80b68-fb2b-4fd7-94e9-e5b40968c4aa
title: D3DXPLANE-Erweiterungen (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: ec6d2724c9c151aca203592cb0bf3caf0b30c4f359b4f95ec2ac734500e59197
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096110"
---
# <a name="d3dxplane-extensions"></a>D3DXPLANE-Erweiterungen

Stellt die folgenden Operatorüberladungen und Typcasts für [**D3DXPLANE-Strukturen**](d3dxplane.md) zur Folge.

``` syntax
typedef struct D3DXPLANE
{
#ifdef __cplusplus
public:
    D3DXPLANE() {}
    D3DXPLANE( CONST FLOAT* );
    D3DXPLANE( CONST D3DXFLOAT16* );
    D3DXPLANE( FLOAT a, FLOAT b, FLOAT c, FLOAT d );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXPLANE& operator *= ( FLOAT );
    D3DXPLANE& operator /= ( FLOAT );

    // unary operators
    D3DXPLANE operator + () const;
    D3DXPLANE operator - () const;

    // binary operators
    D3DXPLANE operator * ( FLOAT ) const;
    D3DXPLANE operator / ( FLOAT ) const;

    friend D3DXPLANE operator * ( FLOAT, CONST D3DXPLANE& );

    BOOL operator == ( CONST D3DXPLANE& ) const;
    BOOL operator != ( CONST D3DXPLANE& ) const;

#endif //__cplusplus
    FLOAT a, b, c, d;
} D3DXPLANE, *LPD3DXPLANE;
```

Abgeleitete Typen: \* LPD3DXPLANE

## <a name="remarks"></a>Hinweise

Weitere Informationen zu Strukturmitgliedern finden Sie unter [**D3DXPLANE**](d3dxplane.md).

Operatorüberladungen und Typcasts für diese Struktur werden in d3dx9math.inl implementiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




