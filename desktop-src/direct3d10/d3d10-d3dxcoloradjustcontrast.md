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
ms.openlocfilehash: 90c36ee9c414b6ae34058b255ad2e7a642f13ef49ee91b586ca974009d4e6b7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498490"
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

## <a name="remarks"></a>Hinweise

Der Eingabe-Alphakanal wird unverändert in den Alphakanal der Ausgabe kopiert.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann diese Funktion als Parameter für eine andere Funktion verwendet werden.

Diese Funktion interpoliert die Rot-, Grün- und Blau-Farbkomponenten einer D3DXCOLOR-Struktur zwischen 10 Prozent Grau und einem angegebenen Kontrastwert, wie im folgenden Beispiel gezeigt.


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



Wenn c größer als 0 und kleiner als 1 ist, wird der Kontrast verringert. Wenn c größer als 1 ist, wird der Kontrast erhöht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
