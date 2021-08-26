---
description: Erstellt den negativen Farbwert eines Farbwerts.
ms.assetid: 74143126-93f8-49fa-abe3-fd730b644d87
title: D3DXColorNegative-Funktion (D3dx9math.h)
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
ms.openlocfilehash: c046702b81ce60f2e50817cb98c04686d9a35e964a141d88fd70dd05654e3067
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069330"
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

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Zeiger auf eine [**D3DXCOLOR-Struktur,**](d3dxcolor.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pC* \[ In\]
</dt> <dd>

Typ: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Zeiger auf eine [**D3DXCOLOR-Quellstruktur.**](d3dxcolor.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Diese Funktion gibt einen Zeiger auf eine [**D3DXCOLOR-Struktur**](d3dxcolor.md) zurück, bei der es sich um den negativen Farbwert des Farbwerts handelt.

## <a name="remarks"></a>Hinweise

Der Eingabe-Alphakanal wird unverändert in den Alphakanal der Ausgabe kopiert.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXColorNegative-Funktion** als Parameter für eine andere Funktion verwendet werden.

Diese Funktion gibt den negativen Farbwert zurück, indem 1,0 von den Farbkomponenten der [**D3DXCOLOR-Struktur**](d3dxcolor.md) subtrahiert wird, wie im folgenden Beispiel gezeigt.


```
pOut->r = 1.0f - pC->r;
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

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorScale**](d3dxcolorscale.md)
</dt> </dl>

 

 




