---
description: 'D3DXPlaneTransform-Funktion (D3DX10Math.h): Transformiert eine Ebene durch eine Matrix. Die Eingabematrix ist die umgekehrte Transponieren der tatsächlichen Transformation.'
ms.assetid: ded06eac-4086-47e8-bc55-c37959afc22d
title: D3DXPlaneTransform-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransform
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9b1d16ba2a29d42614c388a6207503ad32dd5e0f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108788"
---
# <a name="d3dxplanetransform-function-d3dx10mathh"></a>D3DXPlaneTransform-Funktion (D3DX10Math.h)

Transformiert eine Ebene durch eine Matrix. Die Eingabematrix ist die umgekehrte Transponieren der tatsächlichen Transformation.

## <a name="syntax"></a>Syntax


```C++
D3DXPLANE* D3DXPlaneTransform(
  _Inout_       D3DXPLANE  *pOut,
  _In_    const D3DXPLANE  *pP,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Zeiger auf die [**D3DXPLANE,die**](d3d10-d3dxplane.md) die resultierende transformierte Ebene enthält. Weitere Informationen sind im Beispiel enthalten.

</dd> <dt>

*pP* \[ In\]
</dt> <dd>

Typ: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Zeiger auf die D3DXPLANE-Eingabestruktur, die die ebene enthält, die transformiert wird. Der Vektor (a,b,c), der die Ebene beschreibt, muss normalisiert werden, bevor diese Funktion aufgerufen wird. Weitere Informationen sind im Beispiel enthalten.

</dd> <dt>

*pM* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Zeiger auf die [**D3DXMATRIX-Quellstruktur,**](d3d10-d3dxmatrix.md) die die Transformationswerte enthält. Diese Matrix muss die umgekehrte Transponieren der Transformationswerte enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Zeiger auf eine D3DXPLANE-Struktur, die die transformierte Ebene darstellt. Dies ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird, sodass diese Funktion als Parameter für eine andere Funktion verwendet werden kann.

## <a name="remarks"></a>Bemerkungen

### <a name="examples"></a>Beispiele

In diesem Beispiel wird eine Ebene transformiert, indem eine nicht einheitliche Skala angewendet wird.


```
D3DXPLANE   planeNew;
D3DXPLANE   plane(0,1,1,0);
D3DXPlaneNormalize(&plane, &plane);

D3DXMATRIX  matrix;
D3DXMatrixScaling(&matrix, 1.0f,2.0f,3.0f); 
D3DXMatrixInverse(&matrix, NULL, &matrix);
D3DXMatrixTranspose(&matrix, &matrix);
D3DXPlaneTransform(&planeNew, &plane, &matrix);
```



Eine Ebene wird durch ax + by + soll + dw = 0 beschrieben werden. Die erste Ebene wird mit (a,b,c,d) = (0,1,1,0) erstellt. Dabei handelt es sich um eine Ebene, die durch y + z = 0 beschrieben wird. Nach der Skalierung enthält die neue Ebene (a,b,c,d) = (0, 0,353f, 0,235f, 0), die die neue Ebene anzeigt, die durch 0,353y + 0,235z = 0 beschrieben werden soll.

Der Parameter pM enthält die umgekehrte Transponierung der Transformationsmatrix. Die umgekehrte Transponieren ist für diese Methode erforderlich, damit auch der normale Vektor der transformierten Ebene ordnungsgemäß transformiert werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
