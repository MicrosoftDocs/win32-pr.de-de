---
description: 'D3DXMatrixAffineTransformation-Funktion (D3dx9math.h): Erstellt eine 3D-affine Transformationsmatrix. NULL-Argumente werden als Identitätstransformationen behandelt.'
ms.assetid: 54eac78f-57be-4a24-8dfb-0b519e97d6ca
title: D3DXMatrixAffineTransformation-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7329ffbffe5ffd89ed64e5386246f39699618960
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094168"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx9mathh"></a>D3DXMatrixAffineTransformation-Funktion (D3dx9math.h)

Erstellt eine 3D-affine Transformationsmatrix. **NULL-Argumente** werden als Identitätstransformationen behandelt.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_          FLOAT          Scaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*Skalierung* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Skalierungsfaktor.

</dd> <dt>

*pRotationCenter* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) ein Punkt, der den Mittelpunkt der Drehung identifiziert. Wenn dieses Argument **NULL** ist, wird eine Rc-Matrix <sub></sub> für identität M auf die Formel in "Hinweise" angewendet.

</dd> <dt>

*pRotation* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf eine [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die die Drehung angibt. Wenn dieses Argument **NULL** ist, wird eine M <sub>r-Identitätsmatrix</sub> auf die Formel in "Hinweise" angewendet.

</dd> <dt>

*pTranslation* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die Übersetzung darstellt. Wenn dieses Argument **NULL ist,** wird eine Identitäts-Mt-Matrix auf die Formel in "Hinweise" angewendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die eine affine Transformationsmatrix ist.

## <a name="remarks"></a>Bemerkungen

Diese Funktion berechnet die affine Transformationsmatrix mit der folgenden Formel, bei der die Matrixverkettung in der Reihenfolge von links nach rechts ausgewertet wird:

M<sub>out</sub> = Ms \* (M<sub>rc</sub>)⁻. \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt

Dabei gilt:

M <sub>out</sub> = Ausgabematrix (*pOut*)

Ms = Skalierungsmatrix (*Skalierung*)

M <sub>rc</sub> = Mitte der Rotationsmatrix (*pRotationCenter*)

M <sub>r</sub> = Rotationsmatrix (*pRotation*)

Mt = Übersetzungsmatrix (*pTranslation*)

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXMatrixAffineTransformation-Funktion** als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie für 2D-affine Transformationen [**D3DXMatrixAffineTransformation2D.**](d3dxmatrixaffinetransformation2d.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixTransformation**](d3dxmatrixtransformation.md)
</dt> <dt>

[Transformationen (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
