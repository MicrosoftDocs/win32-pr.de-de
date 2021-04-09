---
description: Beschreibt einen Vektor mit drei Komponenten, einschließlich Operator Überladungen und Typumwandlungen.
ms.assetid: 4d73de4b-82fe-452a-8a1e-17208f172a03
title: D3DXVECTOR3-Struktur (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR3
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 2c49902677999c78737e7dec094c839cd8941f08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050948"
---
# <a name="d3dxvector3-structure-d3dx9mathh"></a>D3DXVECTOR3-Struktur (D3dx9math. h)

Beschreibt einen Vektor mit drei Komponenten, einschließlich Operator Überladungen und Typumwandlungen.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXVECTOR3 {
  FLOAT x;
  FLOAT y;
  FLOAT z;
} D3DXVECTOR3, *LPD3DXVECTOR3;
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

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

### <a name="d3dxvector3-extensions"></a>D3DXVECTOR3-Erweiterungen

D3DXVECTOR3 verfügt über die folgenden C++-Erweiterungen.


```
#ifdef __cplusplus
typedef struct D3DXVECTOR3 : public D3DVECTOR
{
public:
    D3DXVECTOR3() {};
    D3DXVECTOR3( CONST FLOAT * );
    D3DXVECTOR3( CONST D3DVECTOR& );
    D3DXVECTOR3( CONST D3DXFLOAT16 * );
    D3DXVECTOR3( FLOAT x, FLOAT y, FLOAT z );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXVECTOR3& operator += ( CONST D3DXVECTOR3& );
    D3DXVECTOR3& operator -= ( CONST D3DXVECTOR3& );
    D3DXVECTOR3& operator *= ( FLOAT );
    D3DXVECTOR3& operator /= ( FLOAT );

    // unary operators
    D3DXVECTOR3 operator + () const;
    D3DXVECTOR3 operator - () const;

    // binary operators
    D3DXVECTOR3 operator + ( CONST D3DXVECTOR3& ) const;
    D3DXVECTOR3 operator - ( CONST D3DXVECTOR3& ) const;
    D3DXVECTOR3 operator * ( FLOAT ) const;
    D3DXVECTOR3 operator / ( FLOAT ) const;

    friend D3DXVECTOR3 operator * ( FLOAT, CONST struct D3DXVECTOR3& );

    BOOL operator == ( CONST D3DXVECTOR3& ) const;
    BOOL operator != ( CONST D3DXVECTOR3& ) const;

} D3DXVECTOR3, *LPD3DXVECTOR3;

#else //!__cplusplus
typedef struct _D3DVECTOR D3DXVECTOR3, *LPD3DXVECTOR3;
#endif //!__cplusplus

typedef struct D3DXVECTOR3_16F
{
#ifdef __cplusplus
public:
    D3DXVECTOR3_16F() {};
    D3DXVECTOR3_16F( CONST FLOAT * );
    D3DXVECTOR3_16F( CONST D3DVECTOR& );
    D3DXVECTOR3_16F( CONST D3DXFLOAT16 * );
    D3DXVECTOR3_16F( CONST D3DXFLOAT16 &x, CONST D3DXFLOAT16 &y, CONST D3DXFLOAT16 &z );

    // casting
    operator D3DXFLOAT16* ();
    operator CONST D3DXFLOAT16* () const;

    // binary operators
    BOOL operator == ( CONST D3DXVECTOR3_16F& ) const;
    BOOL operator != ( CONST D3DXVECTOR3_16F& ) const;

public:
#endif //__cplusplus
    D3DXFLOAT16 x, y, z;

} D3DXVECTOR3_16F, *LPD3DXVECTOR3_16F;
        
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
