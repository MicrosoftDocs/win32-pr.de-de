---
description: Passt den Kontrastwert einer Farbe an.
ms.assetid: c111d3c7-19c6-4a6b-af0d-a9e1bc0bb7d9
title: D3DXColorAdjustContrast-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: 24586b2a8d2206d6818e00af9ea86e4c5e9758fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364378"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx10mathh"></a>D3DXColorAdjustContrast-Funktion (D3DX10Math. h)

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

*Pout* \[ in\]
</dt> <dd>

Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

\[in, out- \] Zeiger auf ein [**D3DXCOLOR**](d3d10-d3dxcolor.md) , das das Ergebnis des Vorgangs ist.

</dd> <dt>

*PC* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***

Zeiger auf eine Quell-D3DXCOLOR-Struktur.

</dd> <dt>

*c* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Kontrastwert. Dieser Parameter interpoliert eine lineare Interpolation zwischen 50 Prozent grau und der Farbe "PC". Es gibt keine Einschränkungen für den Wert von c. Wenn dieser Parameter 0 (null) ist, ist die zurückgegebene Farbe 50 Prozent grau. Wenn dieser Parameter 1 ist, entspricht die zurückgegebene Farbe der ursprünglichen Farbe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Diese Funktion gibt einen Zeiger auf eine D3DXCOLOR-Struktur zurück, die das Ergebnis der Kontrast Anpassung ist.

## <a name="remarks"></a>Bemerkungen

Der Alphakanal für die Eingabe wird unverändert in den Alpha-Ausgabekanal kopiert.

Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird. Auf diese Weise kann diese Funktion als Parameter für eine andere Funktion verwendet werden.

Diese Funktion interpoliert die roten, grünen und blauen Farbkomponenten einer D3DXCOLOR-Struktur zwischen 50 Prozent grau und einem angegebenen Kontrastwert, wie im folgenden Beispiel gezeigt.


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



Wenn c größer als 0 und kleiner als 1 ist, wird der Kontrast verringert. Wenn c größer als 1 ist, wird der Kontrast erweitert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
