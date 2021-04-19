---
description: Erstellt eine 2D-affine-Transformationsmatrix in der XY-Ebene. NULL-Argumente werden als Identitäts Transformationen behandelt.
ms.assetid: 335de919-ae4d-405d-b6bb-ca6bdc2d568a
title: D3DXMatrixAffineTransformation2D-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation2D
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6edd0658eb80ec53d19b6c136a672cb78a2087b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366453"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx9mathh"></a>D3DXMatrixAffineTransformation2D-Funktion (D3dx9math. h)

Erstellt eine 2D-affine-Transformationsmatrix in der XY-Ebene. **Null** -Argumente werden als Identitäts Transformationen behandelt.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_          FLOAT       Scaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*Skalieren* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Skalierungsfaktor.

</dd> <dt>

*protationcenter* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***

Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, ein Punkt, der den Mittelpunkt der Drehung identifiziert. Wenn dieses Argument **null** ist, wird eine identitätsm <sub>RC</sub> -Matrix auf die Formel in den Hinweisen angewendet.

</dd> <dt>

*Drehung* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der Rotationswinkel.

</dd> <dt>

*ptranslation* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***

Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die die Übersetzung darstellt. Wenn dieses Argument **null** ist, wird eine Identity MT-Matrix auf die Formel in den Hinweisen angewendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die eine affine Transformationsmatrix ist.

## <a name="remarks"></a>Bemerkungen

Diese Funktion berechnet die affine Transformationsmatrix mit der folgenden Formel, wobei die Matrix Verkettung in der Reihenfolge von links nach rechts ausgewertet wird:

M<sub>out</sub> = MS \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* M<sub>RC</sub> \* MT

Dabei gilt:

M <sub>out</sub> = Ausgabe Matrix (*Pout*)

MS = Skalierungs Matrix (*Skalierung*)

M <sub>RC</sub> = Mitte der Rotations Matrix (*protationcenter*)

M <sub>r</sub> = Rotations Matrix (*Drehung*)

MT = Übersetzungs Matrix (*ptranslation*)

Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXMatrixAffineTransformation2D** -Funktion als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie für 3D-affine Transformationen [**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md)
</dt> <dt>

[Transformationen (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
