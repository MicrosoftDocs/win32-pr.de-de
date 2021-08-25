---
description: 'D3DXMatrixMultiplyTranspose-Funktion (D3DX10Math.h): Berechnet das transponierte Produkt zweier Matrizen.'
ms.assetid: 3db4138c-407c-47b5-b8b9-04af8771e98e
title: D3DXMatrixMultiplyTranspose-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiplyTranspose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 55bf8dc8eaed13c6bfdc4a8cedacd02b9c5cc5aa11ca0d3e494ed194c8cc9245
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858780"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx10mathh"></a>D3DXMatrixMultiplyTranspose-Funktion (D3DX10Math.h)

Berechnet das transponierte Produkt zweier Matrizen.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pM1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Zeiger auf eine D3DXMATRIX-Quellstruktur (linke Seite).

</dd> <dt>

*pM2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Zeiger auf eine D3DXMATRIX-Quellstruktur (rechte Seite).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf eine D3DXMATRIX-Struktur, die das Produkt zweier Matrizen ist.

## <a name="remarks"></a>Hinweise

Das Ergebnis ist die transponierte des Produkts von zwei Transformationsmatrizen, Out = T(M1 \* M2).

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXMatrixMultiplyTranspose-Funktion als Parameter für eine andere Funktion verwendet werden.

Diese Funktion ist nützlich, um Matrizen als Konstanten für Vertex- und Pixel-Shader festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
