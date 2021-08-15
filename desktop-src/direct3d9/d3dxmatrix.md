---
description: 'D3DXMATRIX-Struktur (D3dx9math.h): Eine 4x4-Matrix, die Methoden und Operatorüberladungen enthält.'
ms.assetid: 0911088b-50cf-4c4a-996e-351386fc359b
title: D3DXMATRIX-Struktur (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIX
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 7390b31aa2cc2c81d3d56656efb3c9ff3b6c1de81bf3e5d4de471fd1f7058553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525331"
---
# <a name="d3dxmatrix-structure-d3dx9mathh"></a>D3DXMATRIX-Struktur (D3dx9math.h)

Eine 4x4-Matrix, die Methoden und Operatorüberladungen enthält.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXMATRIX {
  FLOAT _ij;
} D3DXMATRIX, *LPD3DXMATRIX;
```



## <a name="members"></a>Member

<dl> <dt>

**\_Ij**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Komponente (i, j) der Matrix, wobei i die Zeilennummer und j die Spaltennummer ist. 34 bedeutet z. B. dasselbe wie a₃₄ , die Komponente in der \_ dritten Zeile und vierten \[ \] Spalte.

</dd> </dl>

## <a name="remarks"></a>Hinweise

C-Programmierer können die D3DXMATRIX-Struktur nicht verwenden. Sie müssen die [**D3DMATRIX-Struktur**](d3dmatrix.md) verwenden. C++-Programmierer können überladene Konstruktoren und Zuweisungsoperatoren, unäre operatoren und binäre Operatoren (einschließlich Gleichheit) nutzen.

In D3DX darf \_ das 34-Element einer Projektionsmatrix keine negative Zahl sein. Wenn Ihre Anwendung an dieser Position einen negativen Wert verwenden muss, sollte sie stattdessen die gesamte Projektionsmatrix um -1 skalieren.

### <a name="d3dxmatrix-extensions"></a>D3DXMATRIX-Erweiterungen

**D3DXMATRIX verfügt** über die folgenden C++-Erweiterungen.


```
#ifdef __cplusplus
typedef struct D3DXMATRIX : public D3DMATRIX
{
public:
    D3DXMATRIX() {};
    D3DXMATRIX( CONST FLOAT * );
    D3DXMATRIX( CONST D3DMATRIX& );
    D3DXMATRIX( CONST D3DXFLOAT16 * );
    D3DXMATRIX( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );


    // access grants
    FLOAT& operator () ( UINT Row, UINT Col );
    FLOAT  operator () ( UINT Row, UINT Col ) const;

    // casting operators
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXMATRIX& operator *= ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator += ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator -= ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator *= ( FLOAT );
    D3DXMATRIX& operator /= ( FLOAT );

    // unary operators
    D3DXMATRIX operator + () const;
    D3DXMATRIX operator - () const;

    // binary operators
    D3DXMATRIX operator * ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator + ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator - ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator * ( FLOAT ) const;
    D3DXMATRIX operator / ( FLOAT ) const;

    friend D3DXMATRIX operator * ( FLOAT, CONST D3DXMATRIX& );

    BOOL operator == ( CONST D3DXMATRIX& ) const;
    BOOL operator != ( CONST D3DXMATRIX& ) const;

} D3DXMATRIX, *LPD3DXMATRIX;

#else //!__cplusplus
typedef struct _D3DMATRIX D3DXMATRIX, *LPD3DXMATRIX;
#endif //!__cplusplus
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DMATRIX**](d3dmatrix.md)
</dt> </dl>

 

 
