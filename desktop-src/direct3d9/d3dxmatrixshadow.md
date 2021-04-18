---
description: Erstellt eine Matrix, die Geometrie in eine Ebene vereinfacht.
ms.assetid: 8f283ff9-c879-476c-8057-f4fe77a7a9e7
title: D3DXMatrixShadow-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixShadow
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e6bf1639adb7364536cce5c0dead9ef58ae10bea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361203"
---
# <a name="d3dxmatrixshadow-function-d3dx9mathh"></a>D3DXMatrixShadow-Funktion (D3dx9math. h)

Erstellt eine Matrix, die Geometrie in eine Ebene vereinfacht.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixShadow(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR4 *pLight,
  _In_    const D3DXPLANE   *pPlane
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*Notlage* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***

Ein Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die die Position des Lichts beschreibt.

</dd> <dt>

*pplane* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXPLANE**](d3dxplane.md) \***

Ein Zeiger auf die Quell- [**D3DXPLANE**](d3dxplane.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Geometrie in eine Ebene vereinfacht.

## <a name="remarks"></a>Bemerkungen

Die **D3DXMatrixShadow** -Funktion vereinfacht Geometrie in eine Ebene, als wäre ein Schatten von einem Licht dargestellt.

Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXMatrixShadow** -Funktion als Parameter für eine andere Funktion verwendet werden.

Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.


```
P = normalize(Plane);
L = Light;
d = -dot(P, L)
    
P.a * L.x + d  P.a * L.y      P.a * L.z      P.a * L.w  
P.b * L.x      P.b * L.y + d  P.b * L.z      P.b * L.w  
P.c * L.x      P.c * L.y      P.c * L.z + d  P.c * L.w  
P.d * L.x      P.d * L.y      P.d * L.z      P.d * L.w + d
```



Wenn die w-Komponente des Lichts 0 (null) ist, stellt das Strahl vom Ursprung zum Licht ein Direktionales Licht dar. Wenn der Wert 1 ist, ist das Licht ein Punktuelles Licht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




