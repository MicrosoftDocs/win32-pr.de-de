---
description: Identisch mit D3DXVECTOR4, verwendet jedoch 16-Bit-Gleit Komma Werte für x, y und z.
ms.assetid: 2db5fb3e-ffe0-4bcf-8894-a8bc7eefaf82
title: D3DXVECTOR4_16F-Struktur (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR4_16F
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: d3d46e6bc5423260e550fd026ca52420b1c392ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354447"
---
# <a name="d3dxvector4_16f-structure"></a>D3DXVECTOR4 \_ 16f-Struktur

Identisch mit [**D3DXVECTOR4**](d3d10-d3dxvector4.md), verwendet jedoch 16-Bit-Gleit Komma Werte für x, y und z.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXVECTOR4_16F {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXVECTOR4_16F, *LPD3DXVECTOR4_16F;
```



## <a name="members"></a>Member

<dl> <dt>

**x**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Die x-Komponente.

</dd> <dt>

**y**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Die y-Komponente.

</dd> <dt>

**z**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Die z-Komponente.

</dd> <dt>

**w**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Die w-Komponente.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**D3DXVECTOR4 \_ 16f** verfügt über die folgenden C++-Erweiterungen.

### <a name="d3dxvector4_16f-extensions"></a>D3DXVECTOR4 \_ 16f-Erweiterungen


```
typedef struct D3DXVECTOR4_16F
{
#ifdef __cplusplus
public:
    D3DXVECTOR4_16F() {};
    D3DXVECTOR4_16F( CONST FLOAT * );
    D3DXVECTOR4_16F( CONST D3DXFLOAT16 * );
    D3DXVECTOR4_16F( CONST D3DXVECTOR3_16F& xyz, CONST D3DXFLOAT16& w );
    D3DXVECTOR4_16F( CONST D3DXFLOAT16& x, CONST D3DXFLOAT16& y, CONST D3DXFLOAT16& z, CONST D3DXFLOAT16& w );

    // casting
    operator D3DXFLOAT16* ();
    operator CONST D3DXFLOAT16* () const;

    // binary operators
    BOOL operator == ( CONST D3DXVECTOR4_16F& ) const;
    BOOL operator != ( CONST D3DXVECTOR4_16F& ) const;

public:
#endif //__cplusplus
    D3DXFLOAT16 x, y, z, w;

} D3DXVECTOR4_16F, *LPD3DXVECTOR4_16F;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
