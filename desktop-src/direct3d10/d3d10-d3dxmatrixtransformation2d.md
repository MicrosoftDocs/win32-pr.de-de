---
description: 'D3DXMatrixTransformation2D-Funktion (D3DX10Math.h): Erstellt eine 2D-Transformationsmatrix, die Transformationen in der XY-Ebene darstellt. NULL-Argumente werden als Identitätstransformationen behandelt.'
ms.assetid: 5b894c3b-a532-458a-bcbc-48fcd5c73c34
title: D3DXMatrixTransformation2D-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation2D
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 754e755b0ee6e03692bf7eabeb4e751284478621f47c912d399eb101adfd98e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754290"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx10mathh"></a>D3DXMatrixTransformation2D-Funktion (D3DX10Math.h)

Erstellt eine 2D-Transformationsmatrix, die Transformationen in der XY-Ebene darstellt. **NULL-Argumente** werden als Identitätstransformationen behandelt.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       ScalingRotation,
  _In_    const D3DXVECTOR2 *pScaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis der Transformationen enthält.

</dd> <dt>

*pScalingCenter* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf einen [**D3DXVECTOR2,**](d3d10-d3dxvector2.md)ein Punkt, der das Skalierungscenter identifiziert. Wenn dieses Argument **NULL ist,** wird eine M <sub>sc-Matrix</sub> der Identität auf die Formel in "Hinweise" angewendet.

</dd> <dt>

*ScalingRotation* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Zeiger auf den Skalierungsrotationsfaktor.

</dd> <dt>

*pScaling* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf eine D3DXVECTOR2-Struktur, ein Punkt, der die Skala identifiziert. Wenn dieses Argument **NULL ist,** wird eine Ms-Identitätsmatrix auf die Formel in "Hinweise" angewendet.

</dd> <dt>

*pRotationCenter* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf eine D3DXVECTOR2-Struktur, ein Punkt, der den Drehmittelpunkt identifiziert. Wenn dieses Argument **NULL ist,** wird eine M <sub>RC-Matrix</sub> der Identität auf die Formel in "Hinweise" angewendet.

</dd> <dt>

*Drehung* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Der Drehwinkel im Bogenmaß.

</dd> <dt>

*pTranslation* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf eine D3DXVECTOR2-Struktur, die die Übersetzung identifiziert. Wenn dieses Argument **NULL ist,** wird eine Identitäts-Mt-Matrix auf die Formel in "Hinweise" angewendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf eine D3DXMATRIX-Struktur, die die Transformationsmatrix enthält.

## <a name="remarks"></a>Hinweise

Diese Funktion berechnet die Transformationsmatrix mit der folgenden Formel, bei der die Matrixverkettung in der Reihenfolge von links nach rechts ausgewertet wird:

M<sub>out</sub> = (M<sub>sc</sub>)⁻. \* (M<sub>sr</sub>)⁻. Ms \* M \* <sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻. \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt

Dabei gilt:

M<sub>out</sub> = Ausgabematrix (pOut)

M<sub>sc</sub> = Skalierungscentermatrix (pScalingCenter)

M<sub>sr</sub> = Skalierungsrotationsmatrix (pScalingRotation)

Ms = Skalierungsmatrix (pScaling)

M<sub>rc</sub> = Mittelpunkt der Rotationsmatrix (pRotationCenter)

M<sub>r</sub> = Rotationsmatrix (Drehung)

Mt = Übersetzungsmatrix (pTranslation)

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXMatrixTransformation2D-Funktion als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie für 3D-Transformationen [**D3DXMatrixTransformation**](d3d10-d3dxmatrixtransformation.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
