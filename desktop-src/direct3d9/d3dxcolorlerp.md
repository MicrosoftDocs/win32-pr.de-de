---
description: Verwendet lineare Interpolation, um einen Farbwert zu erstellen.
ms.assetid: bf7bf2f4-5fb5-44d3-a7e5-7998640d7d49
title: D3DXColorLerp-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorLerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fa0134ca1c3cf88e0e25f253cca4ebeb16a89b5bdaa982cf4e9e96e85bfb1d35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988700"
---
# <a name="d3dxcolorlerp-function"></a>D3DXColorLerp-Funktion

Verwendet lineare Interpolation, um einen Farbwert zu erstellen.

## <a name="syntax"></a>Syntax


```C++
D3DXCOLOR* D3DXColorLerp(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2,
  _In_          FLOAT     s
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

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Parameter, der linear zwischen den Farben pC1 und pC2 interpoliert und beide als 4D-Vektoren behandelt. Es gibt keine Grenzwerte für den Wert von s.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Diese Funktion gibt einen Zeiger auf eine [**D3DXCOLOR-Struktur**](d3dxcolor.md) zurück, die das Ergebnis der linearen Interpolation ist.

## <a name="remarks"></a>Hinweise

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXColorLerp-Funktion** als Parameter für eine andere Funktion verwendet werden.

Diese Funktion interpoliert die Rot-, Grün-, Blau- und Alphakomponenten einer [**D3DXCOLOR-Struktur**](d3dxcolor.md) zwischen zwei Farben, wie im folgenden Beispiel gezeigt.


```
   
pOut->r = pC1->r + s * (pC2->r - pC1->r);
```



Wenn Sie linear zwischen den Farben A und B interpolieren und s gleich 0 ist, ist die resultierende Farbe A. Wenn s 1 ist, ist die resultierende Farbe Farbe B.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorNegative**](d3dxcolornegative.md)
</dt> <dt>

[**D3DXColorScale**](d3dxcolorscale.md)
</dt> </dl>

 

 
