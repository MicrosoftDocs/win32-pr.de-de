---
description: Berechnet das Produkt von zwei pherischen Funktionen (f und g). Beide Funktionen haben die Reihenfolge N = 4.
ms.assetid: 05427a18-447e-45d7-a851-e580298c9a1f
title: D3DXSHMultiply4-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply4
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 78305930eb76b3632737c10482768b9db363deae84f14cf5b73f962d265de2a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990010"
---
# <a name="d3dxshmultiply4-function"></a>D3DXSHMultiply4-Funktion

Berechnet das Produkt zweier pherischer Funktionen (*f* und *g*). Beide Funktionen haben die Reihenfolge N = 4.

## <a name="syntax"></a>Syntax


```C++
FLOAT* D3DXSHMultiply4(
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

Zeiger auf die SH-Ausgabekoeffizienten – Die *Basisfunktion Y* lm wird bei l): + *m* + l gespeichert. Die Reihenfolge *N* bestimmt die Länge des Arrays, wobei immer *N 2 Koeffizienten* sein sollten.

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

Das Produkt zweier SH-Funktionen der Reihenfolge N = 4 generiert eine SH-Funktion der Reihenfolge 2 × *N* - 1 = 7, aber die Ergebnisse werden abgeschnitten. Dies bedeutet, dass das Produkt *(f* × *g* g × f ) umständlich ist, aber nicht  =    ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × h ) zugeordnet *wird.*

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
