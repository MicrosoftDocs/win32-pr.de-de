---
description: Erstellt eine 3D-affine-Transformationsmatrix. NULL-Argumente werden als Identitäts Transformationen behandelt.
ms.assetid: 36044272-a8ce-47db-8f52-30dc680f8174
title: D3DXMatrixAffineTransformation-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: 27fee5a620d75c3930b1bc2f8a85415db1320a47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350723"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx10mathh"></a>D3DXMatrixAffineTransformation-Funktion (D3DX10Math. h)

Erstellt eine 3D-affine-Transformationsmatrix. **Null** -Argumente werden als Identitäts Transformationen behandelt.

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

Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf ein [**D3DXVECTOR3**](d3d10-d3dxvector3.md), ein Punkt, der den Mittelpunkt der Drehung identifiziert. Wenn dieses Argument **null** ist, wird eine identitätsm <sub>RC</sub> -Matrix auf die Formel in den Hinweisen angewendet.

</dd> <dt>

*protation* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf ein [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) -Wert, der die Drehung angibt. Wenn dieses Argument **null** ist, wird eine M <sub>r</sub> -Identitätsmatrix auf die Formel in den Hinweisen angewendet.

</dd> <dt>

*ptranslation* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine D3DXVECTOR3-Struktur, die die Übersetzung darstellt. Wenn dieses Argument **null** ist, wird eine Identity MT-Matrix auf die Formel in den Hinweisen angewendet.

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

M<sub>r</sub> = Rotations Matrix (protation)

MT = Übersetzungs Matrix (ptranslation)

Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXMatrixAffineTransformation-Funktion als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie für 2D-affine Transformationen D3DXMatrixAffineTransformation2D.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
