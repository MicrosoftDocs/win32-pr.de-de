---
description: Berechnet das Produkt von zwei pherischen Funktionen (f und g). Beide Funktionen haben die Reihenfolge N = 5.
ms.assetid: c72231a1-9db3-4701-b7ad-4509028ce508
title: D3DXSHMultiply5-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply5
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a022fa883a1b1e809f965ec94813741a285447e9f6935c1adca370b5aef6c061
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990770"
---
# <a name="d3dxshmultiply5-function"></a>D3DXSHMultiply5-Funktion

Berechnet das Produkt von zwei pherischen Funktionen (f und g). Beide Funktionen haben die Reihenfolge N = 5.

## <a name="syntax"></a>Syntax


```C++
FLOAT* D3DXSHMultiply5(
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

Zeiger auf die SH-Ausgabekoeffizienten – die *Basisfunktion Y* lm wird bei *l* 2 + *m* + l gespeichert. Die Reihenfolge N bestimmt die Länge des Arrays, wobei immer *N 2 Koeffizienten* sein sollten.

</dd> <dt>

*pF* \[ In\]
</dt> <dd>

Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Eingabe-SH-Koeffizienten für die erste Funktion.

</dd> <dt>

*pG* \[ In\]
</dt> <dd>

Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Zweiter Satz von EINGABE-SH-Koeffizienten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf SH-Ausgabekoeffizienten.

## <a name="remarks"></a>Hinweise

Das Produkt zweier SH-Funktionen der Reihenfolge N = 5 generiert eine SH-Funktion der Reihenfolge 2 × *N* - 1 = 9, aber die Ergebnisse werden abgeschnitten. Dies bedeutet, dass das Produkt *(f* × *g* g × f ) umständlich ist, aber nicht  =   ( *f* × (  *g* × *h* ) ≠ ( *f* × *g* ) × h ) zugeordnet *wird.*

Diese Funktion verwendet die folgende Gleichung:


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



Wobei y \_ i(s) die ITH-SH-Basisfunktion ist und wobei f(s) und g(s) die folgende SH-Funktion verwenden:


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
