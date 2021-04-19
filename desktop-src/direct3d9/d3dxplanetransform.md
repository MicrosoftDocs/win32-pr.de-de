---
description: Transformiert eine Ebene um eine Matrix. Die Eingabe Matrix ist die umgekehrte Umwandlung der eigentlichen Transformation.
ms.assetid: 3581b397-cbd8-4aed-80dd-1841f331a367
title: D3DXPlaneTransform-Funktion (D3dx9math. h)
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
ms.openlocfilehash: fd82478d9fb1f08bb0320a8c84357efcdf20be26
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370397"
---
# <a name="d3dxplanetransform-function-d3dx9mathh"></a>D3DXPlaneTransform-Funktion (D3dx9math. h)

Transformiert eine Ebene um eine Matrix. Die Eingabe Matrix ist die umgekehrte Umwandlung der eigentlichen Transformation.

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

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXPLANE**](d3dxplane.md)\***

Ein Zeiger auf die [**D3DXPLANE**](d3dxplane.md) -Struktur, die die resultierende transformierte Ebene enthält. Weitere Informationen sind im Beispiel enthalten.

</dd> <dt>

*PP* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXPLANE**](d3dxplane.md) \***

Ein Zeiger auf die Eingabe [**D3DXPLANE**](d3dxplane.md) -Struktur, die die zu transformierende Ebene enthält. Der Vektor (a, b, c), der die Ebene beschreibt, muss normalisiert werden, bevor diese Funktion aufgerufen wird. Weitere Informationen sind im Beispiel enthalten.

</dd> <dt>

*pm* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***

Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Transformations Werte enthält. Diese Matrix muss die umgekehrte Umwandlung der Transformations Werte enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXPLANE**](d3dxplane.md)\***

Zeiger auf eine [**D3DXPLANE**](d3dxplane.md) -Struktur, die die transformierte Ebene darstellt. Dabei handelt es sich um denselben Wert, der im Pout-Parameter zurückgegeben wird, sodass diese Funktion als Parameter für eine andere Funktion verwendet werden kann.

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



Eine Ebene wird von AX + by + CZ + DW = 0 beschrieben. Die erste Ebene wird mit (a, b, c, d) = (0, 1, 1, 0) erstellt. Dies ist eine Ebene, die von y + z = 0 beschrieben wird. Nach dem Skalieren enthält die neue Ebene (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), die die neue Ebene anzeigt, die von 0.353 y + 0.235 z = 0 beschrieben wird.

Der-Parameter pm enthält die umgekehrte Umwandlung der Transformationsmatrix. Die umgekehrte Umwandlung ist für diese Methode erforderlich, damit der normale Vektor der transformierten Ebene ebenfalls ordnungsgemäß transformiert werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

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

 

 




