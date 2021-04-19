---
description: Bestimmt das Kreuz Produkt in vier Dimensionen.
ms.assetid: 4f728fbd-cf5a-4d2e-ba4f-487616d83f6d
title: D3DXVec4Cross-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: 8e3e2a612740a207ea4dc44243ce24ebbab7fc08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363163"
---
# <a name="d3dxvec4cross-function-d3dx10mathh"></a>D3DXVec4Cross-Funktion (D3DX10Math. h)

Bestimmt das Kreuz Produkt in vier Dimensionen.

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

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Zeiger auf das [**D3DXVECTOR4**](d3d10-d3dxvector4.md) , das das Ergebnis des Vorgangs ist.

</dd> <dt>

*pV1* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Zeiger auf eine Quell-D3DXVECTOR4-Struktur.

</dd> <dt>

*pV2* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Zeiger auf eine Quell-D3DXVECTOR4-Struktur.

</dd> <dt>

*pV3* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Zeiger auf eine Quell-D3DXVECTOR4-Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Zeiger auf eine D3DXVECTOR4-Struktur, die das Kreuz Produkt ist.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXVec4Cross-Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
