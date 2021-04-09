---
description: Erstellt eine Transformationsmatrix. NULL-Argumente werden als Identitäts Transformationen behandelt.
ms.assetid: 39042fc6-f489-4e44-ad3f-858ca395575d
title: D3DXMatrixTransformation-Funktion (D3dx9math. h)
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
ms.openlocfilehash: f2174329e01e3e624ef27608ca56b33181b770db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050834"
---
# <a name="d3dxmatrixtransformation-function-d3dx9mathh"></a>D3DXMatrixTransformation-Funktion (D3dx9math. h)

Erstellt eine Transformationsmatrix. **Null** -Argumente werden als Identitäts Transformationen behandelt.

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

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pscalingcenter* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die den Skalierungs Mittelpunkt identifiziert. Wenn dieses Argument **null** ist, wird eine identitätsm-<sub>SC</sub> -Matrix auf die Formel in den Hinweisen angewendet.

</dd> <dt>

*pscalingrotation* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf eine [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die die Skalierungs Drehung angibt. Wenn dieses Argument **null** ist, wird in den Hinweisen eine identitätsm <sub>SR</sub> -Matrix auf die Formel angewendet.

</dd> <dt>

*pscaling* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, den Skalierungs Vektor. Wenn dieses Argument **null** ist, wird eine Identitäts-MS-Matrix auf die Formel in den Hinweisen angewendet.

</dd> <dt>

*protationcenter* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, ein Punkt, der den Mittelpunkt der Drehung bezeichnet. Wenn dieses Argument **null** ist, wird eine identitätsm <sub>RC</sub> -Matrix auf die Formel in den Hinweisen angewendet.

</dd> <dt>

*protation* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf eine [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die die Drehung angibt. Wenn dieses Argument **null** ist, wird eine M <sub>r</sub> -Identitätsmatrix auf die Formel in den Hinweisen angewendet.

</dd> <dt>

*ptranslation* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Übersetzung darstellt. Wenn dieses Argument **null** ist, wird eine Identity MT-Matrix auf die Formel in den Hinweisen angewendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Transformationsmatrix ist.

## <a name="remarks"></a>Bemerkungen

Diese Funktion berechnet die Transformationsmatrix mit der folgenden Formel, wobei die Matrix Verkettung in der Reihenfolge von links nach rechts ausgewertet wird:

M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* m<sub>SR</sub> \* m<sub>SC</sub> \* (M<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* M<sub>RC</sub> \* MT

Dabei gilt:

M <sub>out</sub> = Ausgabe Matrix (*Pout*)

M <sub>SC</sub> = Skalierungs Center Matrix (*pscalingcenter*)

M <sub>SR</sub> = Skalierungs Rotations Matrix (*pscalingrotation*)

MS = Skalierungs Matrix (*pscaling*)

M <sub>RC</sub> = Mitte der Rotations Matrix (*protationcenter*)

M <sub>r</sub> = Rotations Matrix (*protation*)

MT = Übersetzungs Matrix (*ptranslation*)

Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXMatrixTransformation** -Funktion als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md)für 2D-Transformationen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md)
</dt> <dt>

[Transformationen (Direct3D 9)](transforms.md)
</dt> </dl>

 

 




