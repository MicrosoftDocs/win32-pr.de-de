---
description: Erstellt eine 2D-Transformationsmatrix, die Transformationen in der XY-Ebene darstellt. NULL-Argumente werden als Identitäts Transformationen behandelt.
ms.assetid: 671d3d67-b474-4fc1-9913-d21f05d66d9a
title: D3DXMatrixTransformation2D-Funktion (D3dx9math. h)
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
ms.openlocfilehash: ead4d403917b5328776b33563bc477c28983d6ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355184"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx9mathh"></a>D3DXMatrixTransformation2D-Funktion (D3dx9math. h)

Erstellt eine 2D-Transformationsmatrix, die Transformationen in der XY-Ebene darstellt. **Null** -Argumente werden als Identitäts Transformationen behandelt.

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

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis der Transformationen enthält.

</dd> <dt>

*pscalingcenter* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***

Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, ein Punkt, der die Skalierungs Mitte identifiziert. Wenn dieses Argument **null** ist, wird eine identitätsm-<sub>SC</sub> -Matrix auf die Formel in den Hinweisen angewendet.

</dd> <dt>

*pscalingrotation* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der Faktor für die Skalierungs Drehung.

</dd> <dt>

*pscaling* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***

Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, ein Punkt, der die Skala identifiziert. Wenn dieses Argument **null** ist, wird eine Identitäts-MS-Matrix auf die Formel in den Hinweisen angewendet.

</dd> <dt>

*protationcenter* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***

Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, ein Punkt, der das Drehzentrum identifiziert. Wenn dieses Argument **null** ist, wird eine identitätsm <sub>RC</sub> -Matrix auf die Formel in den Hinweisen angewendet.

</dd> <dt>

*Drehung* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der Drehwinkel im Bogenmaße.

</dd> <dt>

*ptranslation* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***

Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die die Übersetzung identifiziert. Wenn dieses Argument **null** ist, wird eine Identity MT-Matrix auf die Formel in den Hinweisen angewendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Transformationsmatrix enthält.

## <a name="remarks"></a>Bemerkungen

Diese Funktion berechnet die Transformationsmatrix mit der folgenden Formel, wobei die Matrix Verkettung in der Reihenfolge von links nach rechts ausgewertet wird:

M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* m<sub>SR</sub> \* m<sub>SC</sub> \* (M<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* M<sub>RC</sub> \* MT

Dabei gilt:

M <sub>out</sub> = Ausgabe Matrix (*Pout*)

M <sub>SC</sub> = Skalierungs Center Matrix (*pscalingcenter*)

M <sub>SR</sub> = Skalierungs Rotations Matrix (*pscalingrotation*)

MS = Skalierungs Matrix (*pscaling*)

M <sub>RC</sub> = Mitte der Rotations Matrix (*protationcenter*)

M <sub>r</sub> = Rotations Matrix (*Drehung*)

MT = Übersetzungs Matrix (*ptranslation*)

Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXMatrixTransformation2D** -Funktion als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie für 3D-Transformationen [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md)
</dt> <dt>

[Transformationen (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
