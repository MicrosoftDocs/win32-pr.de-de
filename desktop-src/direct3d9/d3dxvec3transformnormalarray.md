---
description: 'D3DXVec3TransformNormalArray-Funktion (D3dx9math.h): Transformiert ein Array (x, y, z, 0) durch eine bestimmte Matrix.'
ms.assetid: c12fad52-d541-483f-a919-e6031aa4f761
title: D3DXVec3TransformNormalArray-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormalArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f90521b51c9c939d459fb10bcf2badd7e551b80e5e9f134d5dfd38b5ec8e18aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730819"
---
# <a name="d3dxvec3transformnormalarray-function-d3dx9mathh"></a>D3DXVec3TransformNormalArray-Funktion (D3dx9math.h)

Transformiert ein Array (x, y, z, 0) durch eine bestimmte Matrix.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR3* D3DXVec3TransformNormalArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf das [**D3DXVECTOR3-Array,**](d3dxvector3.md) das das Ergebnis des Vorgangs ist.

</dd> <dt>

*OutStride* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Stride zwischen Vektoren im Ausgabedatenstrom.

</dd> <dt>

*pV* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf das [**D3DXVECTOR3-Quellarray.**](d3dxvector3.md)

</dd> <dt>

*VStride* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Stride zwischen Vektoren im Eingabedatenstrom.

</dd> <dt>

*pM* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Elemente im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf ein [**D3DXVECTOR3-Array,**](d3dxvector3.md) das das transformierte Array ist.

## <a name="remarks"></a>Hinweise

Diese Funktion transformiert den Vektor (*pV*->x, *pV*->y, *pV*->z, 0) durch die Matrix, auf die *pM* zeigt.

Wenn Sie einen Normalen transformieren möchten, sollte die Matrix, die Sie an diese Funktion übergeben, die Transponieren der Umkehrung der Matrix sein, die Sie zum Transformieren eines Punkts verwenden würden.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird. Auf diese Weise kann die **D3DXVec3TransformNormalArray-Funktion** als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
