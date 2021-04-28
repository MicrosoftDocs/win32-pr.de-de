---
description: 'D3DXPlaneTransform-Funktion (D3dx9math.h): Transformiert eine Ebene durch eine Matrix. Die Eingabematrix ist die umgekehrte Transponierung der tatsächlichen Transformation.'
ms.assetid: 3581b397-cbd8-4aed-80dd-1841f331a367
title: D3DXPlaneTransform-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1f1f6ffc45098ba8f8b689e6f6212e5bec4fd679
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098018"
---
# <a name="d3dxplanetransform-function-d3dx9mathh"></a>D3DXPlaneTransform-Funktion (D3dx9math.h)

Transformiert eine Ebene durch eine Matrix. Die Eingabematrix ist die umgekehrte Transponierung der tatsächlichen Transformation.

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

Typ: **[ **D3DXPLANE**](d3dxplane.md)\***

Zeiger auf die [**D3DXPLANE-Struktur,**](d3dxplane.md) die die resultierende transformierte Ebene enthält. Weitere Informationen sind im Beispiel enthalten.

</dd> <dt>

*pP* \[ In\]
</dt> <dd>

Typ: **const [**D3DXPLANE**](d3dxplane.md) \***

Zeiger auf die [**D3DXPLANE-Eingabestruktur,**](d3dxplane.md) die die ebene enthält, die transformiert wird. Der Vektor (a,b,c), der die Ebene beschreibt, muss normalisiert werden, bevor diese Funktion aufgerufen wird. Weitere Informationen sind im Beispiel enthalten.

</dd> <dt>

*pM* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf die [**D3DXMATRIX-Quellstruktur,**](d3dxmatrix.md) die die Transformationswerte enthält. Diese Matrix muss die umgekehrte Transponierung der Transformationswerte enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXPLANE**](d3dxplane.md)\***

Zeiger auf eine [**D3DXPLANE-Struktur,**](d3dxplane.md) die die transformierte Ebene darstellt. Dies ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird, sodass diese Funktion als Parameter für eine andere Funktion verwendet werden kann.

## <a name="remarks"></a>Bemerkungen

### <a name="examples"></a>Beispiele

In diesem Beispiel wird eine Ebene durch Anwenden einer nicht einheitlichen Skala transformiert.


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



Eine Ebene wird durch ax + by + dw + dw = 0 beschrieben. Die erste Ebene wird mit (a,b,c,d) = (0,1,1,0) erstellt. Dies ist eine Ebene, die von y + z = 0 beschrieben wird. Nach der Skalierung enthält die neue Ebene (a,b,c,d) = (0, 0,353f, 0,235f, 0), die die neue Ebene zeigt, die von 0,353y + 0,235z = 0 beschrieben werden soll.

Der Parameter pM enthält die umgekehrte Transponierung der Transformationsmatrix. Die umgekehrte Transponierung ist für diese Methode erforderlich, damit auch der normale Vektor der transformierten Ebene ordnungsgemäß transformiert werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneNormalize**](d3dxplanenormalize.md)
</dt> <dt>

[**D3DXMatrixRotationX**](d3dxmatrixrotationx.md)
</dt> <dt>

[**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)
</dt> <dt>

[**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md)
</dt> <dt>

[**D3DXMatrixInverse**](d3dxmatrixinverse.md)
</dt> <dt>

[**D3DXMatrixTranspose**](d3dxmatrixtranspose.md)
</dt> </dl>

 

 




