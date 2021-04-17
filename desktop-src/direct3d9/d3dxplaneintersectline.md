---
description: Sucht die Schnittmenge zwischen einer Ebene und einer Linie.
ms.assetid: 2723cd3e-fdc3-4aab-a089-0089e5b14e3e
title: D3DXPlaneIntersectLine-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b4a91a4592d039510e11147ffb680c880c43ccec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219433"
---
# <a name="d3dxplaneintersectline-function-d3dx9mathh"></a>D3DXPlaneIntersectLine-Funktion (D3dx9math. h)

Sucht die Schnittmenge zwischen einer Ebene und einer Linie.

## <a name="syntax"></a>Syntax


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Schnittmenge zwischen der angegebenen Ebene und der angegebenen Zeile identifiziert.

</dd> <dt>

*PP* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXPLANE**](d3dxplane.md) \***

Ein Zeiger auf die Quell- [**D3DXPLANE**](d3dxplane.md) -Struktur.

</dd> <dt>

*pV1* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die einen Zeilen Startpunkt definiert.

</dd> <dt>

*pV2* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die einen Zeilen Endpunkt definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Schnittmenge zwischen der angegebenen Ebene und der angegebenen Zeile ist.

## <a name="remarks"></a>Bemerkungen

Wenn die Zeile parallel zur Ebene ist, wird **null** zurückgegeben.

Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXPlaneIntersectLine** -Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




