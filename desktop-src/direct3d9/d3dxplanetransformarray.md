---
description: Transformiert ein Array von Ebenen durch eine Matrix. Die Vektoren, die die einzelnen Ebenen beschreiben, müssen normalisiert werden.
ms.assetid: e82e830b-efbb-4bdc-b370-7bfa4326a669
title: D3DXPlaneTransformArray-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a9a213b17aca9999ef0028fdceb4bb4321d47660
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354346"
---
# <a name="d3dxplanetransformarray-function-d3dx9mathh"></a>D3DXPlaneTransformArray-Funktion (D3dx9math. h)

Transformiert ein Array von Ebenen durch eine Matrix. Die Vektoren, die die einzelnen Ebenen beschreiben, müssen normalisiert werden.

## <a name="syntax"></a>Syntax


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _Out_         UINT       OutStride,
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

Typ: **[ **D3DXPLANE**](d3dxplane.md)\***

Ein Zeiger auf die [**D3DXPLANE**](d3dxplane.md) -Struktur, die die resultierende transformierte Ebene enthält. Siehe Beispiel.

</dd> <dt>

*Outstride* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der Schritt der einzelnen transformierten Ebenen.

</dd> <dt>

*PP* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXPLANE**](d3dxplane.md) \***

Ein Zeiger auf die [**D3DXPLANE**](d3dxplane.md) -Eingabe Struktur, die das zu transformierenden Array von Ebenen enthält. Der Vektor (a, b, c), der die Ebene beschreibt, muss normalisiert werden, bevor diese Funktion aufgerufen wird. Siehe Beispiel.

</dd> <dt>

*Pstride* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der Stride der einzelnen nicht transformierten Ebenen.

</dd> <dt>

*pm* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***

Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die umgekehrte Umwandlung der Transformations Werte enthält.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Anzahl der zu transformierenden Ebenen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXPLANE**](d3dxplane.md)\***

Zeiger auf eine [**D3DXPLANE**](d3dxplane.md) -Struktur, die die transformierte Ebene darstellt. Dabei handelt es sich um denselben Wert, der im *Pout* -Parameter zurückgegeben wird, sodass diese Funktion als Parameter für eine andere Funktion verwendet werden kann.

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

Der-Parameter *pm* enthält die umgekehrte Umwandlung der Transformationsmatrix. Die umgekehrte Umwandlung ist für diese Methode erforderlich, damit der normale Vektor der transformierten Ebene ebenfalls ordnungsgemäß transformiert werden kann.

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

 

 
