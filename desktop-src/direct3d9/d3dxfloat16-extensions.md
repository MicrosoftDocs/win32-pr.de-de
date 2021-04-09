---
description: Liefert Operator Überladungen und Typumwandlungen für D3DXFLOAT16-Strukturen.
ms.assetid: d287efb5-d15e-46dc-924d-012e1a108efc
title: D3DXFLOAT16 Extensions (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFLOAT16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: f97e8917f453e7c2c2db99b8f894d557d7b7909f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050852"
---
# <a name="d3dxfloat16-extensions"></a>D3DXFLOAT16-Erweiterungen

Liefert Operator Überladungen und Typumwandlungen für [**D3DXFLOAT16**](d3dxfloat16.md) -Strukturen.

``` syntax
typedef struct D3DXFLOAT16
{
#ifdef __cplusplus
public:
    D3DXFLOAT16() {};
    D3DXFLOAT16( FLOAT );
    D3DXFLOAT16( CONST D3DXFLOAT16& );

    // casting
    operator FLOAT ();

    // binary operators
    BOOL operator == ( CONST D3DXFLOAT16& ) const;
    BOOL operator != ( CONST D3DXFLOAT16& ) const;

protected:
#endif //__cplusplus
    WORD value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```

Abgeleitete Typen: \* LPD3DXFLOAT16

## <a name="members"></a>Member

Weitere Informationen zu Strukturmembern finden Sie unter D3DXFLOAT16.

## <a name="remarks"></a>Bemerkungen

Operator Überladungen und Typumwandlungen für diese Struktur werden in d3dx9math. INL implementiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




