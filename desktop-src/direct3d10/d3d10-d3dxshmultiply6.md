---
description: Berechnet das Produkt von zwei sphärischen Funktionen (f und g). Beide Funktionen haben die Reihenfolge N = 6.
ms.assetid: 3b68b238-c1ae-4ab8-89ed-bdf815463143
title: D3DXSHMultiply6-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply6
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b442d6d8c64d7c1ef0b202bd2cfa5d6d625280eb7320609a11ea89420c2bc215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990000"
---
# <a name="d3dxshmultiply6-function"></a>D3DXSHMultiply6-Funktion

Berechnet das Produkt von zwei sphärischen Funktionen (f und g). Beide Funktionen haben die Reihenfolge N = 6.

## <a name="syntax"></a>Syntax


```C++
FLOAT* D3DXSHMultiply6(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf die AUSGABE-SH-Koeffizienten: Die Basisfunktion *Y* lm wird bei l² + *m* + l gespeichert. Die Reihenfolge *N* bestimmt die Länge des Arrays, wobei immer *N ²-Koeffizienten* vorhanden sein sollten.

</dd> <dt>

*pF* \[ In\]
</dt> <dd>

Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Eingabe-SH-Koeffizienten für die erste Funktion.

</dd> <dt>

*pG* \[ In\]
</dt> <dd>

Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Zweiter Satz von SH-Eingabekoeffizienten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf SH-Ausgabekoeffizienten.

## <a name="remarks"></a>Hinweise

Das Produkt von zwei SH-Funktionen der Reihenfolge N = 6 generiert eine SH-Funktion der Reihenfolge 2 × *N* - 1 = 11, aber die Ergebnisse werden abgeschnitten. Dies bedeutet, dass das Produkt ( *f* × *g*  =  *g* × *f* ) kommutiert, aber nicht ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ) zuordt.

Diese Funktion verwendet die folgende Gleichung:


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



wobei y \_ i(s) die ith SH-Basisfunktion ist und wobei f(s) und g(s) die folgende SH-Funktion verwenden:


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
