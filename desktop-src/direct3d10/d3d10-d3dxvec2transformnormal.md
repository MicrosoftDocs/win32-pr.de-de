---
description: 'D3DXVec2TransformNormal-Funktion (D3DX10Math.h): Transformiert den 2D-Vektor normal durch die gegebene Matrix.'
ms.assetid: fc238bb1-155f-4018-9c92-16352726920d
title: D3DXVec2TransformNormal-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormal
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 403562ab779ebf532e1c1ebcec4ce21a2beadd7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108298"
---
# <a name="d3dxvec2transformnormal-function-d3dx10mathh"></a>D3DXVec2TransformNormal-Funktion (D3DX10Math.h)

Transformiert den 2D-Vektor normal durch die gegebene Matrix.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Zeiger auf den [**D3DXVECTOR2,**](d3d10-d3dxvector2.md) der das Ergebnis des Vorgangs ist.

</dd> <dt>

*pV* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Zeiger auf die D3DXVECTOR2-Quellstruktur.

</dd> <dt>

*pM* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3d10-d3dxmatrix.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Zeiger auf eine D3DXVECTOR2-Struktur, die der transformierte Vektor ist.

## <a name="remarks"></a>Bemerkungen

Diese Funktion transformiert den Vektor (pV->x, pV->y, 0, 0) durch die Matrix, auf die pM zeigt.

Wenn Sie einen Normalen transformieren möchten, sollte die Matrix, die Sie an diese Funktion übergeben, die Transponieren der Umkehrung der Matrix sein, die Sie zum Transformieren eines Punkts verwenden würden.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXVec2TransformNormal-Funktion** als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
