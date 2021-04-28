---
description: 'D3DXMatrixAffineTransformation-Funktion (D3DX10Math.h): Erstellt eine 3D-affine Transformationsmatrix. NULL-Argumente werden als Identitätstransformationen behandelt.'
ms.assetid: 36044272-a8ce-47db-8f52-30dc680f8174
title: D3DXMatrixAffineTransformation-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 01c6b3c3ffe2de9b7c7003b78f1b07a0f35cc3a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113178"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx10mathh"></a>D3DXMatrixAffineTransformation-Funktion (D3DX10Math.h)

Erstellt eine 3D-affine Transformationsmatrix. **NULL-Argumente** werden als Identitätstransformationen behandelt.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _In_       D3DXMATRIX     *pOut,
  _In_       FLOAT          Scaling,
  _In_ const D3DXVECTOR3    *pRotationCenter,
  _In_ const D3DXQUATERNION *pRotation,
  _In_ const D3DXVECTOR3    *pTranslation
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

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf ein [**D3DXVECTOR3**](d3d10-d3dxvector3.md), ein Punkt, der den Mittelpunkt der Drehung identifiziert. Wenn dieses Argument **NULL** ist, wird eine Rc-Matrix <sub></sub> für identität M auf die Formel in "Hinweise" angewendet.

</dd> <dt>

*pRotation* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf ein [**D3DXQUATERNION-Element,**](d3d10-d3dxquaternion.md) das die Drehung angibt. Wenn dieses Argument **NULL** ist, wird eine M <sub>r-Identitätsmatrix</sub> auf die Formel in "Hinweise" angewendet.

</dd> <dt>

*pTranslation* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine D3DXVECTOR3-Struktur, die die Übersetzung darstellt. Wenn dieses Argument **NULL ist,** wird eine Identitäts-Mt-Matrix auf die Formel in "Hinweise" angewendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf eine D3DXMATRIX-Struktur, die eine affine Transformationsmatrix ist.

## <a name="remarks"></a>Bemerkungen

Diese Funktion berechnet die affine Transformationsmatrix mit der folgenden Formel, bei der die Matrixverkettung in der Reihenfolge von links nach rechts ausgewertet wird:

M<sub>out</sub> = Ms \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt

Dabei gilt:

M<sub>out</sub> = Ausgabematrix (pOut)

Ms = Skalierungsmatrix (Skalierung)

M<sub>rc</sub> = Mitte der Rotationsmatrix (pRotationCenter)

M<sub>r</sub> = Rotationsmatrix (pRotation)

Mt = Übersetzungsmatrix (pTranslation)

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXMatrixAffineTransformation-Funktion als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie für 2D-affine Transformationen D3DXMatrixAffineTransformation2D.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
