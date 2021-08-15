---
description: Blendt zwei Farben.
ms.assetid: deff70c7-2359-48b2-ab40-8c418acf5a07
title: D3DXColorModulate-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorModulate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3be2b2174a4f6e76a211e0da43dab85e81c490495173f2d2323caa71a463de79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988710"
---
# <a name="d3dxcolormodulate-function"></a>D3DXColorModulate-Funktion

Blendt zwei Farben.

## <a name="syntax"></a>Syntax


```C++
D3DXCOLOR* D3DXColorModulate(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Zeiger auf eine [**D3DXCOLOR-Struktur,**](d3dxcolor.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pC1* \[ In\]
</dt> <dd>

Typ: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Zeiger auf eine [**D3DXCOLOR-Quellstruktur.**](d3dxcolor.md)

</dd> <dt>

*pC2* \[ In\]
</dt> <dd>

Typ: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Zeiger auf eine [**D3DXCOLOR-Quellstruktur.**](d3dxcolor.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Diese Funktion gibt einen Zeiger auf eine [**D3DXCOLOR-Struktur**](d3dxcolor.md) zurück, die das Ergebnis des Blending-Vorgangs ist.

## <a name="remarks"></a>Hinweise

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXColorModulate-Funktion** als Parameter für eine andere Funktion verwendet werden.

Diese Funktion kombiniert zwei Farben, indem übereinstimmende Farbkomponenten multipliziert werden, wie im folgenden Beispiel gezeigt.


```
pOut->r = pC1->r * pC2->r;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorLerp**](d3dxcolorlerp.md)
</dt> <dt>

[**D3DXColorNegative**](d3dxcolornegative.md)
</dt> <dt>

[**D3DXColorScale**](d3dxcolorscale.md)
</dt> </dl>

 

 




