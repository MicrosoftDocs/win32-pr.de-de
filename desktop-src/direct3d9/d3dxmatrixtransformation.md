---
description: 'D3DXMatrixTransformation-Funktion (D3dx9math.h): Erstellt eine Transformationsmatrix. NULL-Argumente werden als Identitätstransformationen behandelt.'
ms.assetid: 39042fc6-f489-4e44-ad3f-858ca395575d
title: D3DXMatrixTransformation-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc3b6502a8015564207f208166cec15227d3b18a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098128"
---
# <a name="d3dxmatrixtransformation-function-d3dx9mathh"></a>D3DXMatrixTransformation-Funktion (D3dx9math.h)

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

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pScalingCenter* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die den Skalierungsmittelpunkt identifiziert. Wenn dieses Argument **NULL ist,** wird eine M <sub>sc-Matrix</sub> der Identität auf die Formel in "Hinweise" angewendet.

</dd> <dt>

*pScalingRotation* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf eine [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die die Skalierungsrotation angibt. Wenn dieses Argument **NULL ist,** wird eine M <sub>sr-Matrix der</sub> Identität auf die Formel in "Hinweise" angewendet.

</dd> <dt>

*pScaling* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) den Skalierungsvektor. Wenn dieses Argument **NULL** ist, wird eine Ms-Identitätsmatrix auf die Formel in "Hinweise" angewendet.

</dd> <dt>

*pRotationCenter* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) ein Punkt, der den Mittelpunkt der Drehung identifiziert. Wenn dieses Argument **NULL** ist, wird eine M <sub>RC-Matrix</sub> der Identität auf die Formel in "Hinweise" angewendet.

</dd> <dt>

*pRotation* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf eine [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die die Drehung angibt. Wenn dieses Argument **NULL** ist, wird eine M <sub>r-Identitätsmatrix</sub> auf die Formel in "Hinweise" angewendet.

</dd> <dt>

*pTranslation* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die Übersetzung darstellt. Wenn dieses Argument **NULL** ist, wird eine Mt-Identitätsmatrix auf die Formel in "Hinweise" angewendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Transformationsmatrix ist.

## <a name="remarks"></a>Bemerkungen

Diese Funktion berechnet die Transformationsmatrix mit der folgenden Formel, wobei die Matrixverkettung in der Reihenfolge von links nach rechts ausgewertet wird:

M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹ \* Ms \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt

Dabei gilt:

M <sub>out</sub> = Ausgabematrix (*pOut*)

M <sub>sc</sub> = Skalierungscentermatrix (*pScalingCenter*)

M <sub>sr</sub> = Skalierungsrotationsmatrix (*pScalingRotation*)

Ms =*Skalierungsmatrix ( pScaling*)

M <sub>rc</sub> = Mittelpunkt der Rotationsmatrix (*pRotationCenter*)

M <sub>r</sub> = Drehungsmatrix (*pRotation*)

Mt = Übersetzungsmatrix (*pTranslation*)

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird. Auf diese Weise kann die **D3DXMatrixTransformation-Funktion** als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie für 2D-Transformationen [**D3DXMatrixTransformation2D.**](d3dxmatrixtransformation2d.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md)
</dt> <dt>

[Transformationen (Direct3D 9)](transforms.md)
</dt> </dl>

 

 




