---
description: Erstellt den negativen Farbwert eines Farbwerts.
ms.assetid: 74143126-93f8-49fa-abe3-fd730b644d87
title: D3DXColorNegative-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorNegative
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6d4d8559e64580897aec5261c450dc739496e75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355018"
---
# <a name="d3dxcolornegative-function"></a>D3DXColorNegative-Funktion

Erstellt den negativen Farbwert eines Farbwerts.

## <a name="syntax"></a>Syntax


```C++
D3DXCOLOR* D3DXColorNegative(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*PC* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXCOLOR**](d3dxcolor.md) \***

Zeiger auf eine Quell- [**D3DXCOLOR**](d3dxcolor.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Diese Funktion gibt einen Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur zurück, die der negative Farbwert des Farbwerts ist.

## <a name="remarks"></a>Bemerkungen

Der Alphakanal für die Eingabe wird unverändert in den Alpha-Ausgabekanal kopiert.

Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXColorNegative** -Funktion als Parameter für eine andere Funktion verwendet werden.

Diese Funktion gibt den negativen Farbwert zurück, indem Sie 1,0 von den Farbkomponenten der [**D3DXCOLOR**](d3dxcolor.md) -Struktur subtrahieren, wie im folgenden Beispiel gezeigt.


```
pOut->r = 1.0f - pC->r;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorLerp**](d3dxcolorlerp.md)
</dt> <dt>

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorScale**](d3dxcolorscale.md)
</dt> </dl>

 

 




