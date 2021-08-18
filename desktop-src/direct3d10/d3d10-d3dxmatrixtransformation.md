---
description: 'D3DXMatrixTransformation-Funktion (D3DX10Math.h): Erstellt eine Transformationsmatrix. NULL-Argumente werden als Identitätstransformationen behandelt.'
ms.assetid: 99c75ce9-3683-4753-b635-760eb8aaf46e
title: D3DXMatrixTransformation-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a9f9b6679093ef1defb98289bbc1c0f70410a7ab6b1f4c7a5107012e16976a2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754310"
---
# <a name="d3dxmatrixtransformation-function-d3dx10mathh"></a>D3DXMatrixTransformation-Funktion (D3DX10Math.h)

Erstellt eine Transformationsmatrix. **NULL-Argumente** werden als Identitätstransformationen behandelt.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXVECTOR3    *pScalingCenter,
  _In_    const D3DXQUATERNION *pScalingRotation,
  _In_    const D3DXVECTOR3    *pScaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pScalingCenter* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf einen [**D3DXVECTOR3,**](d3d10-d3dxvector3.md)der den Mittelpunkt der Skalierung identifiziert. Wenn dieses Argument **NULL** ist, wird eine M <sub>sc-Identitätsmatrix</sub> auf die Formel in "Hinweise" angewendet.

</dd> <dt>

*pScalingRotation* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf ein [**D3DXQUATERNION,das**](d3d10-d3dxquaternion.md) die Skalierungsrotation angibt. Wenn dieses Argument **NULL** ist, wird eine M <sub>SR-Identitätsmatrix</sub> auf die Formel in "Hinweise" angewendet.

</dd> <dt>

*pScaling* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine D3DXVECTOR3-Struktur, den Skalierungsvektor. Wenn dieses Argument **NULL** ist, wird eine Ms-Identitätsmatrix auf die Formel in "Hinweise" angewendet.

</dd> <dt>

*pRotationCenter* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine D3DXVECTOR3-Struktur, ein Punkt, der den Mittelpunkt der Drehung identifiziert. Wenn dieses Argument **NULL** ist, wird eine Identity M <sub>rc-Matrix</sub> auf die Formel in "Remarks" angewendet.

</dd> <dt>

*pRotation* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf eine D3DXQUATERNION-Struktur, die die Drehung angibt. Wenn dieses Argument **NULL** ist, wird eine M <sub>r-Identitätsmatrix</sub> auf die Formel in "Hinweise" angewendet.

</dd> <dt>

*pTranslation* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine D3DXVECTOR3-Struktur, die die Übersetzung darstellt. Wenn dieses Argument **NULL** ist, wird eine Mt-Identitätsmatrix auf die Formel in "Hinweise" angewendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf eine D3DXMATRIX-Struktur, die die Transformationsmatrix ist.

## <a name="remarks"></a>Hinweise

Diese Funktion berechnet die Transformationsmatrix mit der folgenden Formel, wobei die Matrixverkettung in der Reihenfolge von links nach rechts ausgewertet wird:

M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹ \* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt

Dabei gilt:

M<sub>out</sub> = Ausgabematrix (pOut)

M<sub>sc</sub> = Skalierungscentermatrix (pScalingCenter)

M<sub>sr</sub> = Skalierungsrotationsmatrix (pScalingRotation)

Ms = Skalierungsmatrix (pScaling)

M<sub>rc</sub> = Mittelpunkt der Rotationsmatrix (pRotationCenter)

M<sub>r</sub> = Rotationsmatrix (pRotation)

Mt = Übersetzungsmatrix (pTranslation)

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXMatrixTransformation-Funktion als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie für 2D-Transformationen [**D3DXMatrixTransformation2D.**](d3d10-d3dxmatrixtransformation2d.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
