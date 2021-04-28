---
description: 'D3DXVec2TransformNormalArray-Funktion (D3DX10Math.h): Transformiert ein Array (x, y, 0, 0) durch eine bestimmte Matrix.'
ms.assetid: a53f998a-f2a5-4e4b-bc1c-c1f46284d78b
title: D3DXVec2TransformNormalArray-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormalArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b4e18fc2bb8c62bb86947b9eab35daae9d0242ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108278"
---
# <a name="d3dxvec2transformnormalarray-function-d3dx10mathh"></a>D3DXVec2TransformNormalArray-Funktion (D3DX10Math.h)

Transformiert ein Array (x, y, 0, 0) durch eine bestimmte Matrix.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR2* D3DXVec2TransformNormalArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Zeiger auf den [**D3DXVECTOR2,**](d3d10-d3dxvector2.md) der das Ergebnis des Vorgangs ist.

</dd> <dt>

*OutStride* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Stride zwischen Vektoren im Ausgabedatenstrom.

</dd> <dt>

*pV* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf das D3DXVECTOR2-Quellarray.

</dd> <dt>

*VStride* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Stride zwischen Vektoren im Eingabedatenstrom.

</dd> <dt>

*pM* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3d10-d3dxmatrix.md)

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Elemente im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Zeiger auf eine D3DXVECTOR2-Struktur, die das transformierte Array ist.

## <a name="remarks"></a>Bemerkungen

Diese Funktion transformiert den Vektor (pV->x, pV->y, 0, 0) durch die Matrix, auf die pM zeigt.

Wenn Sie einen normalen transformieren möchten, sollte die Matrix, die Sie an diese Funktion übergeben, die Transponieren der Umkehrung der Matrix sein, die Sie zum Transformieren eines Punkts verwenden würden.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXVec2TransformNormalArray-Funktion** als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
