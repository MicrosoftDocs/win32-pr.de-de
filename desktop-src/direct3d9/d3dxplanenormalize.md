---
description: Normalisiert die ebenenkoeffizienten, sodass die Ebene normal über eine Einheitslänge verfügt.
ms.assetid: 9c595986-e1f8-4153-ba23-1fa6e583a050
title: D3DXPlaneNormalize-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneNormalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0f0c87028d3b37f785005725e7510f689cf56d61
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366434"
---
# <a name="d3dxplanenormalize-function-d3dx9mathh"></a>D3DXPlaneNormalize-Funktion (D3dx9math. h)

Normalisiert die ebenenkoeffizienten, sodass die Ebene normal über eine Einheitslänge verfügt.

## <a name="syntax"></a>Syntax


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXPLANE**](d3dxplane.md)\***

Ein Zeiger auf die [**D3DXPLANE**](d3dxplane.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*PP* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXPLANE**](d3dxplane.md) \***

Ein Zeiger auf die Quell- [**D3DXPLANE**](d3dxplane.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXPLANE**](d3dxplane.md)\***

Zeiger auf eine [**D3DXPLANE**](d3dxplane.md) -Struktur, die die normale der Ebene darstellt.

## <a name="remarks"></a>Bemerkungen

Diese Funktion normalisiert eine Ebene, sodass \| a, b, c \| = = 1 ist.

Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird. Auf diese Weise kann diese Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




