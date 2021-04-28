---
description: 'D3DXMatrixReflect-Funktion (D3DX10Math.h): Erstellt eine Matrix, die das Koordinatensystem einer Ebene widerspiegelt.'
ms.assetid: bd2c5905-780e-4fac-a848-d7dbcfc390c6
title: D3DXMatrixReflect-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixReflect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f96224c881dcd5db2cc1c356003ab96e8a626900
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103408"
---
# <a name="d3dxmatrixreflect-function-d3dx10mathh"></a>D3DXMatrixReflect-Funktion (D3DX10Math.h)

Erstellt eine Matrix, die das Koordinatensystem einer Ebene widerspiegelt.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixReflect(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXPLANE  *pPlane
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pPlane* \[ In\]
</dt> <dd>

Typ: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Zeiger auf die [**D3DXPLANE-Quelldatei.**](d3d10-d3dxplane.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf eine D3DXMATRIX-Struktur, die das Koordinatensystem der Quellebene widerspiegelt.

## <a name="remarks"></a>Bemerkungen

Diese Funktion normalisiert die Ebenengleichung, bevor sie die reflektierte Matrix erstellt.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXMatrixReflect-Funktion als Parameter für eine andere Funktion verwendet werden.

Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.


```
P = normalize(Plane);
    
-2 * P.a * P.a + 1  -2 * P.b * P.a      -2 * P.c * P.a        0
-2 * P.a * P.b      -2 * P.b * P.b + 1  -2 * P.c * P.b        0
-2 * P.a * P.c      -2 * P.b * P.c      -2 * P.c * P.c + 1    0
-2 * P.a * P.d      -2 * P.b * P.d      -2 * P.c * P.d        1
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
