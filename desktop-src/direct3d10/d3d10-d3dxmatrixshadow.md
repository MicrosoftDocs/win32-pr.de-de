---
description: 'D3DXMatrixShadow-Funktion (D3DX10Math.h): Erstellt eine Matrix, die die Geometrie in eine Ebene vereinfacht.'
ms.assetid: 83c9e7d6-fc6c-48e7-bbf2-6aa10868351d
title: D3DXMatrixShadow-Funktion (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1e9a831eae416986dc4111e9928ffe9c2b09119fb4595119174d745aedbb6ac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118809892"
---
# <a name="d3dxmatrixshadow-function-d3dx10mathh"></a>D3DXMatrixShadow-Funktion (D3DX10Math.h)

Erstellt eine Matrix, die die Geometrie in eine Ebene verflachen kann.

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

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pLight* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Zeiger auf einen [**D3DXVECTOR4,**](d3d10-d3dxvector4.md) der die Position des Lichts beschreibt.

</dd> <dt>

*pPlane* \[ In\]
</dt> <dd>

Typ: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Zeiger auf die [**D3DXPLANE-Quelle.**](d3d10-d3dxplane.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf eine D3DXMATRIX-Struktur, die die Geometrie in eine Ebene vereinfacht.

## <a name="remarks"></a>Hinweise

Die **D3DXMatrixShadow-Funktion** vereinfacht die Geometrie in eine Ebene, als ob ein Schatten aus einem Licht werfen würde.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXMatrixShadow-Funktion** als Parameter für eine andere Funktion verwendet werden.

Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.


```
P = normalize(Plane);
L = Light;
d = dot(P, L)
    
P.a * L.x + d  P.a * L.y      P.a * L.z      P.a * L.w  
P.b * L.x      P.b * L.y + d  P.b * L.z      P.b * L.w  
P.c * L.x      P.c * L.y      P.c * L.z + d  P.c * L.w  
P.d * L.x      P.d * L.y      P.d * L.z      P.d * L.w + d
```



Wenn die w-Komponente des Lichts 0 ist, stellt der Strahl vom Ursprung zum Licht ein gerichtetes Licht dar. Wenn es 1 ist, ist das Licht ein Punktlicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
