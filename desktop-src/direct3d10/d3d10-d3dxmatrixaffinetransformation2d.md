---
description: Erstellt eine 2D-affine Transformationsmatrix in der x-y-Ebene. NULL-Argumente werden als Identitätstransformationen behandelt.
ms.assetid: f46a307c-4566-42c8-8def-fb189116144e
title: D3DXMatrixAffineTransformation2D-Funktion (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 40666e4fc74f834d6333259636f9953281d534570eedabf37a3d99590ec2e1ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070160"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx10mathh"></a>D3DXMatrixAffineTransformation2D-Funktion (D3DX10Math.h)

Erstellt eine 2D-affine Transformationsmatrix in der x-y-Ebene. **NULL-Argumente** werden als Identitätstransformationen behandelt.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation2D(
  _In_       D3DXMATRIX  *pOut,
  _In_       FLOAT       Scaling,
  _In_ const D3DXVECTOR2 *pRotationCenter,
  _In_       FLOAT       Rotation,
  _In_ const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ In\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf die [**D3DXMATRIX,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*Skalierung* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Skalierungsfaktor.

</dd> <dt>

*pRotationCenter* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf einen [**D3DXVECTOR2,**](d3d10-d3dxvector2.md)ein Punkt, der den Mittelpunkt der Drehung identifiziert. Wenn dieses Argument **NULL ist,** wird eine M <sub>RC-Matrix</sub> der Identität auf die Formel in "Hinweise" angewendet.

</dd> <dt>

*Drehung* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Der Rotationswinkel.

</dd> <dt>

*pTranslation* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf einen [**D3DXVECTOR2,**](d3d10-d3dxvector2.md)der die Übersetzung darstellt. Wenn dieses Argument **NULL ist,** wird eine Identitäts-Mt-Matrix auf die Formel in "Hinweise" angewendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf eine D3DXMATRIX-Struktur, die eine affine Transformationsmatrix ist.

## <a name="remarks"></a>Hinweise

Diese Funktion berechnet die affine Transformationsmatrix mit der folgenden Formel, bei der die Matrixverkettung in der Reihenfolge von links nach rechts ausgewertet wird:

M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ

Dabei gilt:

M<sub>out</sub> = Ausgabematrix (pOut)

Ms = Skalierungsmatrix (Skalierung)

M<sub>rc</sub> = Mitte der Rotationsmatrix (pRotationCenter)

M<sub>r</sub> = Rotationsmatrix (Drehung)

Mt = Übersetzungsmatrix (pTranslation)

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXMatrixAffineTransformation2D-Funktion als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie für 3D-affine Transformationen D3DXMatrixAffineTransformation.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
