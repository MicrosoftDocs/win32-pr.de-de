---
description: 'D3DXPlaneNormalize-Funktion (D3DX10Math.h): Normalisiert die Ebenenkoeffizienten so, dass die Normalebene die Einheitslänge aufwies.'
ms.assetid: 52ae36a7-e37b-457a-9832-e62900a85bde
title: D3DXPlaneNormalize-Funktion (D3DX10Math.h)
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
ms.openlocfilehash: 8b3499297a008b0d8f5dc705080bbd1d5bbe3af4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103308"
---
# <a name="d3dxplanenormalize-function-d3dx10mathh"></a>D3DXPlaneNormalize-Funktion (D3DX10Math.h)

Normalisiert die Ebenenkoeffizienten so, dass der Ebenennormar die Einheitslänge aufwies.

## <a name="syntax"></a>Syntax


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Zeiger auf die [**D3DXPLANE,**](d3d10-d3dxplane.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pP* \[ In\]
</dt> <dd>

Typ: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Zeiger auf die D3DXPLANE-Quellstruktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Zeiger auf eine D3DXPLANE-Struktur, die die Normalität der Ebene darstellt.

## <a name="remarks"></a>Bemerkungen

Diese Funktion normalisiert eine Ebene so, dass \| a,b,c \| == 1.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann diese Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
