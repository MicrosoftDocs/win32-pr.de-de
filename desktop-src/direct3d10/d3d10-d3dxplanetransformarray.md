---
description: Transformiert ein Array von Ebenen durch eine Matrix. Die Vektoren, die die einzelnen Ebenen beschreiben, müssen normalisiert werden.
ms.assetid: 9529b06a-0575-4115-8d35-fc35a7bfb0bd
title: D3DXPlaneTransformArray-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 128b9c8c73db81faa877295e993504a7a510cd4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050894"
---
# <a name="d3dxplanetransformarray-function-d3dx10mathh"></a>D3DXPlaneTransformArray-Funktion (D3DX10Math. h)

Transformiert ein Array von Ebenen durch eine Matrix. Die Vektoren, die die einzelnen Ebenen beschreiben, müssen normalisiert werden.

## <a name="syntax"></a>Syntax


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _In_          UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Ein Zeiger auf die [**D3DXPLANE**](d3d10-d3dxplane.md) -Struktur, die die resultierende transformierte Ebene enthält. Siehe Beispiel.

</dd> <dt>

*Outstride* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der Schritt der einzelnen transformierten Ebenen.

</dd> <dt>

*PP* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Ein Zeiger auf die D3DXPLANE-Eingabe Struktur, die das zu transformierenden Array von Ebenen enthält. Der Vektor (a, b, c), der die Ebene beschreibt, muss normalisiert werden, bevor diese Funktion aufgerufen wird. Siehe Beispiel.

</dd> <dt>

*Pstride* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der Stride der einzelnen nicht transformierten Ebenen.

</dd> <dt>

*pm* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur, die die umgekehrte Umwandlung der Transformations Werte enthält.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Anzahl der zu transformierenden Ebenen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Zeiger auf eine D3DXPLANE-Struktur, die die transformierte Ebene darstellt. Dabei handelt es sich um denselben Wert, der im Pout-Parameter zurückgegeben wird, sodass diese Funktion als Parameter für eine andere Funktion verwendet werden kann.

## <a name="remarks"></a>Bemerkungen

In diesem Beispiel wird eine Ebene durch Anwenden einer nicht einheitlichen Skala transformiert.


```
#define ARRAYSIZE 4
D3DXPLANE planeNew[ARRAYSIZE];
D3DXPLANE plane[ARRAYSIZE];

for(int i = 0; i < ARRAYSIZE; i++)
{
    plane = D3DXPLANE( 0.0f, 1.0f, 1.0f, 0.0f );
    D3DXPlaneNormalize( &plane[i], &plane[i] );
}

D3DXMATRIX  matrix;
D3DXMatrixScaling( &matrix, 1.0f, 2.0f, 3.0f ); 
D3DXMatrixInverse( &matrix, NULL, &matrix );
D3DXMatrixTranspose( &matrix, &matrix );
D3DXPlaneTransformArray( &planeNew, sizeof (D3DXPLANE), &plane, 
                         sizeof (D3DXPLANE), &matrix, ARRAYSIZE );
```



Eine Ebene wird von AX + by + CZ + DW = 0 beschrieben. Die erste Ebene wird mit (a, b, c, d) = (0, 1, 1, 0) erstellt. Dies ist eine Ebene, die von y + z = 0 beschrieben wird. Nach dem Skalieren enthält die neue Ebene (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), die die neue Ebene anzeigt, die von 0.353 y + 0.235 z = 0 beschrieben wird.

Der-Parameter pm enthält die umgekehrte Umwandlung der Transformationsmatrix. Die umgekehrte Umwandlung ist für diese Methode erforderlich, damit der normale Vektor der transformierten Ebene ebenfalls ordnungsgemäß transformiert werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
