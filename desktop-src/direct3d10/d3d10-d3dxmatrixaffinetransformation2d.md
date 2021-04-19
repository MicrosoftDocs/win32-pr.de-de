---
description: Erstellt eine 2D-affine-Transformationsmatrix in der x-y-Ebene. NULL-Argumente werden als Identitäts Transformationen behandelt.
ms.assetid: f46a307c-4566-42c8-8def-fb189116144e
title: D3DXMatrixAffineTransformation2D-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: 223ef5d2d9a68c993553d52f5d4cf63e8b95dd3b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353394"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx10mathh"></a>D3DXMatrixAffineTransformation2D-Funktion (D3DX10Math. h)

Erstellt eine 2D-affine-Transformationsmatrix in der x-y-Ebene. **Null** -Argumente werden als Identitäts Transformationen behandelt.

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

*Pout* \[ in\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf das [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , das das Ergebnis des Vorgangs ist.

</dd> <dt>

*Skalieren* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Skalierungsfaktor.

</dd> <dt>

*protationcenter* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf ein [**D3DXVECTOR2**](d3d10-d3dxvector2.md), ein Punkt, der den Mittelpunkt der Drehung identifiziert. Wenn dieses Argument **null** ist, wird eine identitätsm <sub>RC</sub> -Matrix auf die Formel in den Hinweisen angewendet.

</dd> <dt>

*Drehung* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der Rotationswinkel.

</dd> <dt>

*ptranslation* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf ein [**D3DXVECTOR2**](d3d10-d3dxvector2.md)-Objekt, das die Übersetzung darstellt. Wenn dieses Argument **null** ist, wird eine Identity MT-Matrix auf die Formel in den Hinweisen angewendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf eine D3DXMATRIX-Struktur, die eine affine Transformationsmatrix ist.

## <a name="remarks"></a>Bemerkungen

Diese Funktion berechnet die affine Transformationsmatrix mit der folgenden Formel, wobei die Matrix Verkettung in der Reihenfolge von links nach rechts ausgewertet wird:

M<sub>out</sub> = MS \* (m<sub>RC</sub>)-1 \* M<sub>r</sub> \* m<sub>RC</sub> \* MT

Dabei gilt:

M<sub>out</sub> = Ausgabe Matrix (Pout)

MS = Skalierungs Matrix (Skalierung)

M<sub>RC</sub> = Mitte der Rotations Matrix (protationcenter)

M<sub>r</sub> = Rotations Matrix (Drehung)

MT = Übersetzungs Matrix (ptranslation)

Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXMatrixAffineTransformation2D-Funktion als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie für 3D-affine Transformationen D3DXMatrixAffineTransformation.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
