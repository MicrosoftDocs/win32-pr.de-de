---
description: Normalisiert die ebenenkoeffizienten, sodass die Ebene normal über eine Einheitslänge verfügt.
ms.assetid: 52ae36a7-e37b-457a-9832-e62900a85bde
title: D3DXPlaneNormalize-Funktion (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 44d5e9d810653b2cdae233dec803383c74563d08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367392"
---
# <a name="d3dxplanenormalize-function-d3dx10mathh"></a>D3DXPlaneNormalize-Funktion (D3DX10Math. h)

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

Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Zeiger auf das [**D3DXPLANE**](d3d10-d3dxplane.md) , das das Ergebnis des Vorgangs ist.

</dd> <dt>

*PP* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Ein Zeiger auf die Quell-D3DXPLANE-Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Zeiger auf eine D3DXPLANE-Struktur, die die normale der Ebene darstellt.

## <a name="remarks"></a>Bemerkungen

Diese Funktion normalisiert eine Ebene, sodass \| a, b, c \| = = 1 ist.

Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird. Auf diese Weise kann diese Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
