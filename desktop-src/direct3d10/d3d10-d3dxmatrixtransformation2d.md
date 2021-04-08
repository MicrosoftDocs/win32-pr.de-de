---
description: Erstellt eine 2D-Transformationsmatrix, die Transformationen in der XY-Ebene darstellt. NULL-Argumente werden als Identitäts Transformationen behandelt.
ms.assetid: 5b894c3b-a532-458a-bcbc-48fcd5c73c34
title: D3DXMatrixTransformation2D-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: b41d8234dcd9dda1b3735c83460a20c7109e63d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762273"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx10mathh"></a>D3DXMatrixTransformation2D-Funktion (D3DX10Math. h)

Erstellt eine 2D-Transformationsmatrix, die Transformationen in der XY-Ebene darstellt. **Null** -Argumente werden als Identitäts Transformationen behandelt.

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

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ein Zeiger auf die [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur, die das Ergebnis der Transformationen enthält.

</dd> <dt>

*pscalingcenter* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf ein [**D3DXVECTOR2**](d3d10-d3dxvector2.md), ein Punkt, der das Skalierungs Center identifiziert. Wenn dieses Argument **null** ist, wird eine identitätsm-<sub>SC</sub> -Matrix auf die Formel in den Hinweisen angewendet.

</dd> <dt>

*Skalierung* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Zeiger zum Skalierungsfaktor für die Skalierung.

</dd> <dt>

*pscaling* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf eine D3DXVECTOR2-Struktur, ein Punkt, der die Skala identifiziert. Wenn dieses Argument **null** ist, wird eine Identitäts-MS-Matrix auf die Formel in den Hinweisen angewendet.

</dd> <dt>

*protationcenter* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf eine D3DXVECTOR2-Struktur, ein Punkt, der das Drehzentrum identifiziert. Wenn dieses Argument **null** ist, wird eine identitätsm <sub>RC</sub> -Matrix auf die Formel in den Hinweisen angewendet.

</dd> <dt>

*Drehung* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der Drehwinkel im Bogenmaße.

</dd> <dt>

*ptranslation* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf eine D3DXVECTOR2-Struktur, die die Übersetzung identifiziert. Wenn dieses Argument **null** ist, wird eine Identity MT-Matrix auf die Formel in den Hinweisen angewendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf eine D3DXMATRIX-Struktur, die die Transformationsmatrix enthält.

## <a name="remarks"></a>Bemerkungen

Diese Funktion berechnet die Transformationsmatrix mit der folgenden Formel, wobei die Matrix Verkettung in der Reihenfolge von links nach rechts ausgewertet wird:

M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* m<sub>SR</sub> \* m<sub>SC</sub> \* (M<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* M<sub>RC</sub> \* MT

Dabei gilt:

M<sub>out</sub> = Ausgabe Matrix (Pout)

M<sub>SC</sub> = Skalierungs Center Matrix (pscalingcenter)

M<sub>SR</sub> = Skalierungs Rotations Matrix (pscalingrotation)

MS = Skalierungs Matrix (pscaling)

M<sub>RC</sub> = Mitte der Rotations Matrix (protationcenter)

M<sub>r</sub> = Rotations Matrix (Drehung)

MT = Übersetzungs Matrix (ptranslation)

Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXMatrixTransformation2D-Funktion als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie für 3D-Transformationen [**D3DXMatrixTransformation**](d3d10-d3dxmatrixtransformation.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
