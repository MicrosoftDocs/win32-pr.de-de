---
description: Stellt die folgenden Operator Überladungen und Typumwandlungen für D3DXCOLOR-Strukturen bereit.
ms.assetid: 89780c6f-c78b-4ebe-876a-6dbc37b598ef
title: D3DXCOLOR Extensions (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 7f457332f371b2c452a465c5b831774488301c6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870147"
---
# <a name="d3dxcolor-extensions"></a>D3DXCOLOR-Erweiterungen

Stellt die folgenden Operator Überladungen und Typumwandlungen für [**D3DXCOLOR**](d3dxcolor.md) -Strukturen bereit.

``` syntax
typedef struct D3DXCOLOR
{
#ifdef __cplusplus
public:
    D3DXCOLOR() {}
    D3DXCOLOR( DWORD argb );
    D3DXCOLOR( CONST FLOAT * );
    D3DXCOLOR( CONST D3DXFLOAT16 * );
    D3DXCOLOR( CONST D3DCOLORVALUE& );
    D3DXCOLOR( FLOAT r, FLOAT g, FLOAT b, FLOAT a );

    // casting
    operator DWORD () const;

    operator FLOAT* ();
    operator CONST FLOAT* () const;

    operator D3DCOLORVALUE* ();
    operator CONST D3DCOLORVALUE* () const;

    operator D3DCOLORVALUE& ();
    operator CONST D3DCOLORVALUE& () const;

    // assignment operators
    D3DXCOLOR& operator += ( CONST D3DXCOLOR& );
    D3DXCOLOR& operator -= ( CONST D3DXCOLOR& );
    D3DXCOLOR& operator *= ( FLOAT );
    D3DXCOLOR& operator /= ( FLOAT );

    // unary operators
    D3DXCOLOR operator + () const;
    D3DXCOLOR operator - () const;

    // binary operators
    D3DXCOLOR operator + ( CONST D3DXCOLOR& ) const;
    D3DXCOLOR operator - ( CONST D3DXCOLOR& ) const;
    D3DXCOLOR operator * ( FLOAT ) const;
    D3DXCOLOR operator / ( FLOAT ) const;

    friend D3DXCOLOR operator * ( FLOAT, CONST D3DXCOLOR& );

    BOOL operator == ( CONST D3DXCOLOR& ) const;
    BOOL operator != ( CONST D3DXCOLOR& ) const;

#endif //__cplusplus
    FLOAT r, g, b, a;
} D3DXCOLOR, *LPD3DXCOLOR;
```

Abgeleitete Typen: \* LPD3DXCOLOR

## <a name="members"></a>Member

Weitere Informationen zu Strukturmembern finden Sie unter [**D3DXCOLOR**](d3dxcolor.md).

## <a name="remarks"></a>Bemerkungen

Operator Überladungen und Typumwandlungen für diese Struktur werden in d3dx9math. INL implementiert.

> [!Note]  
> Der D3DXCOLOR ()-Konstruktor stürzt zur Laufzeit ab, wenn Sie ihn in Microsoft Visual Studio 2010 mit der [Compileroption Lauf Zeit Fehlerüberprüfungen (/RTCc)](/previous-versions/visualstudio/visual-studio-2010/8wtf2dfz(v=vs.100)) im Debugmodus ausführen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
