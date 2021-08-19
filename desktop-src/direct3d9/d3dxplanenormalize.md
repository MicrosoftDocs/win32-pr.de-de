---
description: 'D3DXPlaneNormalize-Funktion (D3dx9math.h): Normalisiert die Ebenenkoeffizienten so, dass die Normalebene die Einheitslänge hat.'
ms.assetid: 9c595986-e1f8-4153-ba23-1fa6e583a050
title: D3DXPlaneNormalize-Funktion (D3dx9math.h)
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
ms.openlocfilehash: a8a5a80526e013c85caf59b3a6a3d6c595a3c10a6e29687882c7789765368d06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952310"
---
# <a name="d3dxplanenormalize-function-d3dx9mathh"></a>D3DXPlaneNormalize-Funktion (D3dx9math.h)

Normalisiert die Ebenenkoeffizienten so, dass der Ebenennorm normal die Einheitslänge aufwies.

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

Typ: **[ **D3DXPLANE**](d3dxplane.md)\***

Zeiger auf die [**D3DXPLANE-Struktur,**](d3dxplane.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pP* \[ In\]
</dt> <dd>

Typ: **const [**D3DXPLANE**](d3dxplane.md) \***

Zeiger auf die [**D3DXPLANE-Quellstruktur.**](d3dxplane.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXPLANE**](d3dxplane.md)\***

Zeiger auf eine [**D3DXPLANE-Struktur,**](d3dxplane.md) die die Normalität der Ebene darstellt.

## <a name="remarks"></a>Hinweise

Diese Funktion normalisiert eine Ebene so, dass \| a,b,c \| == 1.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird. Auf diese Weise kann diese Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




