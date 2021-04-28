---
description: 'D3DXPlaneTransformArray-Funktion (D3dx9math.h): Transformiert ein Array von Ebenen durch eine Matrix. Die Vektoren, die jede Ebene beschreiben, müssen normalisiert werden.'
ms.assetid: e82e830b-efbb-4bdc-b370-7bfa4326a669
title: D3DXPlaneTransformArray-Funktion (D3dx9math.h)
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
ms.openlocfilehash: bdbc845eda69d22f6e7097131f71b074a9b53985
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094128"
---
# <a name="d3dxplanetransformarray-function-d3dx9mathh"></a>D3DXPlaneTransformArray-Funktion (D3dx9math.h)

Transformiert ein Array von Ebenen durch eine Matrix. Die Vektoren, die jede Ebene beschreiben, müssen normalisiert werden.

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

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXPLANE**](d3dxplane.md)\***

Zeiger auf die [**D3DXPLANE-Struktur,**](d3dxplane.md) die die resultierende transformierte Ebene enthält. Siehe Beispiel.

</dd> <dt>

*OutStride* \[ out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Der Schritt jeder transformierten Ebene.

</dd> <dt>

*pP* \[ In\]
</dt> <dd>

Typ: **const [**D3DXPLANE**](d3dxplane.md) \***

Zeiger auf die [**D3DXPLANE-Eingabestruktur,**](d3dxplane.md) die das Array der zu transformierten Ebenen enthält. Der Vektor (a,b,c), der die Ebene beschreibt, muss normalisiert werden, bevor diese Funktion aufgerufen wird. Siehe Beispiel.

</dd> <dt>

*PStride* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Der Schritt jeder nicht transformierten Ebene.

</dd> <dt>

*pM* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf die [**D3DXMATRIX-Quellstruktur,**](d3dxmatrix.md) die die umgekehrte Transponierung der Transformationswerte enthält.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der zu transformierenden Ebenen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXPLANE**](d3dxplane.md)\***

Zeiger auf eine [**D3DXPLANE-Struktur,**](d3dxplane.md) die die transformierte Ebene darstellt. Dies ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird, sodass diese Funktion als Parameter für eine andere Funktion verwendet werden kann.

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



Eine Ebene wird durch ax + by + dw + dw = 0 beschrieben. Die erste Ebene wird mit (a,b,c,d) = (0,1,1,0) erstellt. Dies ist eine Ebene, die von y + z = 0 beschrieben wird. Nach der Skalierung enthält die neue Ebene (a,b,c,d) = (0, 0,353f, 0,235f, 0), die die neue Ebene zeigt, die von 0,353y + 0,235z = 0 beschrieben werden soll.

Der Parameter *pM* enthält die umgekehrte Transponierung der Transformationsmatrix. Die umgekehrte Transponierung ist für diese Methode erforderlich, damit auch der normale Vektor der transformierten Ebene ordnungsgemäß transformiert werden kann.

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

 

 
