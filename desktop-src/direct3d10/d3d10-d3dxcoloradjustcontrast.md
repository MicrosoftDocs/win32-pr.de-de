---
description: 'D3DXColorAdjustContrast-Funktion (D3DX10Math.h): Passt den Kontrastwert einer Farbe an.'
ms.assetid: c111d3c7-19c6-4a6b-af0d-a9e1bc0bb7d9
title: D3DXColorAdjustContrast-Funktion (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 09781c5c11560c3497a5af57528cf478f6259816
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113328"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx10mathh"></a>D3DXColorAdjustContrast-Funktion (D3DX10Math.h)

Passt den Kontrastwert einer Farbe an.

## <a name="syntax"></a>Syntax


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     c
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ In\]
</dt> <dd>

Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

\[in, out \] Zeiger auf eine [**D3DXCOLOR,**](d3d10-d3dxcolor.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pC* \[ In\]
</dt> <dd>

Typ: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***

Zeiger auf eine D3DXCOLOR-Quellstruktur.

</dd> <dt>

*c* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Kontrastwert. Dieser Parameter interpoliert linear zwischen 15 Prozent Grau und der Farbe pC. Es gibt keine Grenzwerte für den Wert von c. Wenn dieser Parameter 0 (null) ist, ist die zurückgegebene Farbe prozentgrau. Wenn dieser Parameter 1 ist, ist die zurückgegebene Farbe die ursprüngliche Farbe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Diese Funktion gibt einen Zeiger auf eine D3DXCOLOR-Struktur zurück, die das Ergebnis der Kontrastanpassung ist.

## <a name="remarks"></a>Bemerkungen

Der Eingabe-Alphakanal wird unverändert in den Alphakanal der Ausgabe kopiert.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann diese Funktion als Parameter für eine andere Funktion verwendet werden.

Diese Funktion interpoliert die Rot-, Grün- und Blau-Farbkomponenten einer D3DXCOLOR-Struktur zwischen 50 Prozent Grau und einem angegebenen Kontrastwert, wie im folgenden Beispiel gezeigt.


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



Wenn c größer als 0 und kleiner als 1 ist, wird der Kontrast verringert. Wenn c größer als 1 ist, wird der Kontrast erhöht.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
