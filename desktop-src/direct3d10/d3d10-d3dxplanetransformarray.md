---
description: 'D3DXPlaneTransformArray-Funktion (D3DX10Math.h): Transformiert ein Array von Ebenen durch eine Matrix. Die Vektoren, die jede Ebene beschreiben, müssen normalisiert werden.'
ms.assetid: 9529b06a-0575-4115-8d35-fc35a7bfb0bd
title: D3DXPlaneTransformArray-Funktion (D3DX10Math.h)
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
ms.openlocfilehash: 04cda233d777f05dec44b4fc93537cc33b0369d14d95c104773f0f33ef03498d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070040"
---
# <a name="d3dxplanetransformarray-function-d3dx10mathh"></a>D3DXPlaneTransformArray-Funktion (D3DX10Math.h)

Transformiert ein Array von Ebenen durch eine Matrix. Die Vektoren, die jede Ebene beschreiben, müssen normalisiert werden.

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

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Zeiger auf die [**D3DXPLANE-Struktur,**](d3d10-d3dxplane.md) die die resultierende transformierte Ebene enthält. Siehe Beispiel.

</dd> <dt>

*OutStride* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Der Schritt jeder transformierten Ebene.

</dd> <dt>

*pP* \[ In\]
</dt> <dd>

Typ: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Zeiger auf die D3DXPLANE-Eingabestruktur, die das Array der zu transformierten Ebenen enthält. Der Vektor (a, b, c), der die Ebene beschreibt, muss normalisiert werden, bevor diese Funktion aufgerufen wird. Siehe Beispiel.

</dd> <dt>

*PStride* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Der Schritt jeder nicht transformierten Ebene.

</dd> <dt>

*pM* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Zeiger auf die [**D3DXMATRIX-Quellstruktur,**](d3d10-d3dxmatrix.md) die die umgekehrte Transponierung der Transformationswerte enthält.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der zu transformierenden Ebenen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Zeiger auf eine D3DXPLANE-Struktur, die die transformierte Ebene darstellt. Dies ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird, sodass diese Funktion als Parameter für eine andere Funktion verwendet werden kann.

## <a name="remarks"></a>Hinweise

In diesem Beispiel wird eine Ebene transformiert, indem eine nicht einheitliche Skala angewendet wird.


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



Eine Ebene wird durch ax + by + tg + dw = 0 beschrieben. Die erste Ebene wird mit (a,b,c,d) = (0,1,1,0) erstellt, wobei es sich um eine Ebene handelt, die durch y + z = 0 beschrieben wird. Nach der Skalierung enthält die neue Ebene (a,b,c,d) = (0, 0,353f, 0,235f, 0), die die neue Ebene anzeigt, die durch 0,353y + 0,235z = 0 beschrieben werden soll.

Der Parameter pM enthält die umgekehrte Transponierung der Transformationsmatrix. Die umgekehrte Transponieren ist für diese Methode erforderlich, damit auch der normale Vektor der transformierten Ebene ordnungsgemäß transformiert werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
