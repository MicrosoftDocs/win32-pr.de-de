---
description: 'D3DXVec4Cross-Funktion (D3DX10Math.h): Bestimmt das Kreuzprodukt in vier Dimensionen.'
ms.assetid: 4f728fbd-cf5a-4d2e-ba4f-487616d83f6d
title: D3DXVec4Cross-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Cross
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: e52cc1adb1e48f65599b1bf7179f7953823f1e1c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102948"
---
# <a name="d3dxvec4cross-function-d3dx10mathh"></a>D3DXVec4Cross-Funktion (D3DX10Math.h)

Bestimmt das Kreuzprodukt in vier Dimensionen.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Zeiger auf [**D3DXVECTOR4,**](d3d10-d3dxvector4.md) das das Ergebnis des Vorgangs ist.

</dd> <dt>

*pV1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Zeiger auf eine D3DXVECTOR4-Quellstruktur.

</dd> <dt>

*pV2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Zeiger auf eine D3DXVECTOR4-Quellstruktur.

</dd> <dt>

*pV3* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Zeiger auf eine D3DXVECTOR4-Quellstruktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Zeiger auf eine D3DXVECTOR4-Struktur, die das Kreuzprodukt ist.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXVec4Cross-Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
