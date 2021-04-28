---
description: 'D3DXMatrixTransformation2D-Funktion (D3dx9math.h): Erstellt eine 2D-Transformationsmatrix, die Transformationen in der XY-Ebene darstellt. NULL-Argumente werden als Identitätstransformationen behandelt.'
ms.assetid: 671d3d67-b474-4fc1-9913-d21f05d66d9a
title: D3DXMatrixTransformation2D-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b92a5489569765ef059af9b1023b40fc681b5d0c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098118"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx9mathh"></a>D3DXMatrixTransformation2D-Funktion (D3dx9math.h)

Erstellt eine 2D-Transformationsmatrix, die Transformationen in der XY-Ebene darstellt. **NULL-Argumente** werden als Identitätstransformationen behandelt.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       pScalingRotation,
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

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis der Transformationen enthält.

</dd> <dt>

*pScalingCenter* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Zeiger auf eine [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) ein Punkt, der das Skalierungscenter identifiziert. Wenn dieses Argument **NULL ist,** wird eine M <sub>sc-Matrix</sub> der Identität auf die Formel in "Hinweise" angewendet.

</dd> <dt>

*pScalingRotation* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Der Skalierungsrotationsfaktor.

</dd> <dt>

*pScaling* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Zeiger auf eine [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) ein Punkt, der die Skala identifiziert. Wenn dieses Argument **NULL ist,** wird eine Ms-Identitätsmatrix auf die Formel in "Hinweise" angewendet.

</dd> <dt>

*pRotationCenter* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Zeiger auf eine [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) ein Punkt, der den Drehmittelpunkt identifiziert. Wenn dieses Argument **NULL** ist, wird eine Rc-Matrix <sub></sub> für identität M auf die Formel in "Hinweise" angewendet.

</dd> <dt>

*Drehung* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Der Drehwinkel im Bogenmaß.

</dd> <dt>

*pTranslation* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Zeiger auf eine [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) die die Übersetzung identifiziert. Wenn dieses Argument **NULL** ist, wird eine Mt-Identitätsmatrix auf die Formel in "Hinweise" angewendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Transformationsmatrix enthält.

## <a name="remarks"></a>Bemerkungen

Diese Funktion berechnet die Transformationsmatrix mit der folgenden Formel, wobei die Matrixverkettung in der Reihenfolge von links nach rechts ausgewertet wird:

M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹ \* Ms \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt

Dabei gilt:

M <sub>out</sub> = Ausgabematrix (*pOut*)

M <sub>sc</sub> = Skalierungscentermatrix (*pScalingCenter*)

M <sub>sr</sub> = Skalierungsrotationsmatrix (*pScalingRotation*)

Ms =*Skalierungsmatrix ( pScaling*)

M <sub>rc</sub> = Mittelpunkt der Rotationsmatrix (*pRotationCenter*)

M <sub>r</sub> = Drehungsmatrix (*Drehung*)

Mt = Übersetzungsmatrix (*pTranslation*)

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXMatrixTransformation2D-Funktion** als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie für 3D-Transformationen [**D3DXMatrixTransformation.**](d3dxmatrixtransformation.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md)
</dt> <dt>

[Transformationen (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
