---
description: 'D3DXColorAdjustContrast-Funktion (D3dx9math.h): Passt den Kontrastwert einer Farbe an.'
ms.assetid: be49c9c7-b625-4cbc-bd63-1d5766ae2dbb
title: D3DXColorAdjustContrast-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustContrast
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dc9bb79d1ebbe536661347d76d13846dead6aa8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115878"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx9mathh"></a>D3DXColorAdjustContrast-Funktion (D3dx9math.h)

Passt den Kontrastwert einer Farbe an.

## <a name="syntax"></a>Syntax


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     c
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

</dd> <dt>

*c* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Kontrastwert. Dieser Parameter interpoliert linear zwischen 15 Prozent Grau und der Farbe pC. Es gibt keine Grenzwerte für den Wert von c. Wenn dieser Parameter 0 (null) ist, ist die zurückgegebene Farbe prozentgrau. Wenn dieser Parameter 1 ist, ist die zurückgegebene Farbe die ursprüngliche Farbe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Diese Funktion gibt einen Zeiger auf eine [**D3DXCOLOR-Struktur**](d3dxcolor.md) zurück, die das Ergebnis der Kontrastanpassung ist.

## <a name="remarks"></a>Bemerkungen

Der Eingabe-Alphakanal wird unverändert in den Alphakanal der Ausgabe kopiert.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann diese Funktion als Parameter für eine andere Funktion verwendet werden.

Diese Funktion interpoliert die Rot-, Grün- und Blaufarbkomponenten einer [**D3DXCOLOR-Struktur**](d3dxcolor.md) zwischen 10 Prozent Grau und einem angegebenen Kontrastwert, wie im folgenden Beispiel gezeigt.


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



Wenn c größer als 0 und kleiner als 1 ist, wird der Kontrast verringert. Wenn c größer als 1 ist, wird der Kontrast erhöht.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorAdjustSaturation**](d3dxcoloradjustsaturation.md)
</dt> </dl>

 

 
