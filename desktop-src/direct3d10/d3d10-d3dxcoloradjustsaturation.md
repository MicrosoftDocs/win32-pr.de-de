---
description: 'D3DXColorAdjustSaturation-Funktion (D3DX10Math.h): Passt den Sättigungswert einer Farbe an.'
ms.assetid: a7ca64b4-2198-4116-8e9f-79d6c922fd09
title: D3DXColorAdjustSaturation-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustSaturation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9e9ae91f5c898dae8ff922616bc02846732c760a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103538"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx10mathh"></a>D3DXColorAdjustSaturation-Funktion (D3DX10Math.h)

Passt den Sättigungswert einer Farbe an.

## <a name="syntax"></a>Syntax


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     s
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ In\]
</dt> <dd>

Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Zeiger auf eine [**D3DXCOLOR,**](d3d10-d3dxcolor.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pC* \[ In\]
</dt> <dd>

Typ: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***

Zeiger auf eine D3DXCOLOR-Quellstruktur.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Sättigungswert. Dieser Parameter interpoliert linear zwischen der in Graustufen konvertierten Farbe und der ursprünglichen Farbe pC. Es gibt keine Grenzwerte für den Wert von s. Wenn s 0 ist, ist die zurückgegebene Farbe die Graustufenfarbe. Wenn s 1 ist, ist die zurückgegebene Farbe die ursprüngliche Farbe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Diese Funktion gibt einen Zeiger auf eine D3DXCOLOR-Struktur zurück, die das Ergebnis der Anpassung der Sättigung ist.

## <a name="remarks"></a>Bemerkungen

Der Alpha-Eingabekanal wird unverändert in den Alphaausgabekanal kopiert.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann diese Funktion als Parameter für eine andere Funktion verwendet werden.

Diese Funktion interpoliert die Rot-, Grün- und Blau-Farbkomponenten einer D3DXCOLOR-Struktur zwischen einer nicht überlasteten Farbe und einer Farbe, wie im folgenden Beispiel gezeigt.


```
//Approximate values for each component's contribution to luminance.
//Based upon the NTSC standard described in ITU-R Recommendation BT.709.
FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;

pOut->r = grey + s * (pC->r - grey);
```



Wenn s größer als 0 und kleiner als 1 ist, wird die Sättigung verringert. Wenn s größer als 1 ist, wird die Sättigung erhöht.

Die Graustufenfarbe wird wie die folgende berechnet:


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b;
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
