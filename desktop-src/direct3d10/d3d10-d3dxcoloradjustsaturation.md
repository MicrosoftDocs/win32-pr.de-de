---
description: Passt den Sättigungswert einer Farbe an.
ms.assetid: a7ca64b4-2198-4116-8e9f-79d6c922fd09
title: D3DXColorAdjustSaturation-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: e6cfa4dd2af6e4a4ac3772af80ba11b8189405f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961704"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx10mathh"></a>D3DXColorAdjustSaturation-Funktion (D3DX10Math. h)

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

*Pout* \[ in\]
</dt> <dd>

Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Zeiger auf ein [**D3DXCOLOR**](d3d10-d3dxcolor.md) -Ergebnis, das das Ergebnis des Vorgangs ist.

</dd> <dt>

*PC* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***

Zeiger auf eine Quell-D3DXCOLOR-Struktur.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Sättigungswert. Dieser Parameter interpoliert eine lineare Interpolation zwischen der Farbe, die in Graustufen konvertiert wurde, und der ursprünglichen Farbe, dem PC. Es gibt keine Einschränkungen für den Wert von s. Wenn s 0 ist, ist die zurückgegebene Farbe die Graustufen Farbe. Wenn s den Wert 1 hat, ist die zurückgegebene Farbe die ursprüngliche Farbe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Diese Funktion gibt einen Zeiger auf eine D3DXCOLOR-Struktur zurück, die das Ergebnis der Sättigungs Anpassung ist.

## <a name="remarks"></a>Bemerkungen

Der Alphakanal für die Eingabe wird unverändert in den Alpha-Ausgabekanal kopiert.

Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird. Auf diese Weise kann diese Funktion als Parameter für eine andere Funktion verwendet werden.

Diese Funktion interpoliert die roten, grünen und blauen Farbkomponenten einer D3DXCOLOR-Struktur zwischen einer ungesättigten Farbe und einer Farbe, wie im folgenden Beispiel gezeigt.


```
//Approximate values for each component's contribution to luminance.
//Based upon the NTSC standard described in ITU-R Recommendation BT.709.
FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;

pOut->r = grey + s * (pC->r - grey);
```



Wenn s größer als 0 und kleiner als 1 ist, wird die Sättigung verringert. Wenn s größer als 1 ist, wird die Sättigung angehoben.

Die Graustufen Farbe wird wie folgt berechnet:


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
