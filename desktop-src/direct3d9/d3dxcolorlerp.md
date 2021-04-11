---
description: Verwendet die lineare interpolung, um einen Farbwert zu erstellen.
ms.assetid: bf7bf2f4-5fb5-44d3-a7e5-7998640d7d49
title: D3DXColorLerp-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 3521ee9e76aecd486093f903d336c08553e0e4ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870127"
---
# <a name="d3dxcolorlerp-function"></a>D3DXColorLerp-Funktion

Verwendet die lineare interpolung, um einen Farbwert zu erstellen.

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

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pC1* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXCOLOR**](d3dxcolor.md) \***

Zeiger auf eine Quell- [**D3DXCOLOR**](d3dxcolor.md) -Struktur.

</dd> <dt>

*pC2* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXCOLOR**](d3dxcolor.md) \***

Zeiger auf eine Quell- [**D3DXCOLOR**](d3dxcolor.md) -Struktur.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

-Parameter, der linear zwischen den Farben, pC1 und pC2, interpoliert und beide als 4D-Vektoren behandelt. Es gibt keine Einschränkungen für den Wert von s.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Diese Funktion gibt einen Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur zurück, die das Ergebnis der linearen interpolung ist.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXColorLerp** -Funktion als Parameter für eine andere Funktion verwendet werden.

Diese Funktion interpoliert die roten, grünen, blauen und Alpha Komponenten einer [**D3DXCOLOR**](d3dxcolor.md) -Struktur zwischen zwei Farben, wie im folgenden Beispiel gezeigt.


```
   
pOut->r = pC1->r + s * (pC2->r - pC1->r);
```



Wenn Sie eine lineare Interpolation zwischen den Farben A und B durchführen und s 0 (null) ist, ist die resultierende Farbe ein. Wenn s den Wert 1 hat, ist die resultierende Farbe Color B.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorNegative**](d3dxcolornegative.md)
</dt> <dt>

[**D3DXColorScale**](d3dxcolorscale.md)
</dt> </dl>

 

 
