---
description: Bestimmt das Kreuz Produkt in vier Dimensionen.
ms.assetid: 10b965c9-7ed7-450c-86a0-114f068c888f
title: D3DXVec4Cross-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Cross
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91e6e5662bff503ba96d96f135f98e60cf15c8fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219552"
---
# <a name="d3dxvec4cross-function-d3dx9mathh"></a>D3DXVec4Cross-Funktion (D3dx9math. h)

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

Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ein Zeiger auf die [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pV1* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.

</dd> <dt>

*pV2* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.

</dd> <dt>

*pV3* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das Kreuz Produkt ist.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXVec4Cross** -Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec4Dot**](d3dxvec4dot.md)
</dt> </dl>

 

 




