---
description: Berechnet das Produkt von zwei sphärischen Oberschwingungen-Funktionen (f und g). Beide Funktionen sind in der Reihenfolge N = 2.
ms.assetid: 9e0942ce-e39d-4147-9472-cda8a97fd390
title: D3DXSHMultiply2-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply2
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a72cdf7eb28b06e11b4901ebd048af143dfbdb5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365329"
---
# <a name="d3dxshmultiply2-function-d3dx10mathh"></a>D3DXSHMultiply2-Funktion (D3DX10Math. h)

Berechnet das Produkt von zwei sphärischen Oberschwingungen-Funktionen (*f* und *g*). Beide Funktionen sind in der Reihenfolge N = 2.

## <a name="syntax"></a>Syntax


```C++
FLOAT* D3DXSHMultiply2(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Zeiger auf die Ausgabe-SH-Koeffizienten – die Basis Funktion *Y* LM wird in l ² + *m* + l gespeichert. Die Reihenfolge *n* bestimmt die Länge des Arrays, bei der immer *N*² Koeffizienten vorhanden sein sollten.

</dd> <dt>

*PF* \[ in\]
</dt> <dd>

Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***

Geben Sie SH Koeffizienten für die erste Funktion ein.

</dd> <dt>

*PG* \[ in\]
</dt> <dd>

Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***

Zweiter Satz von Eingabe-SH-Koeffizienten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Zeiger auf SH-Ausgabe Koeffizienten.

## <a name="remarks"></a>Bemerkungen

Das Produkt der beiden SH-Funktionen von Order N = 2 generiert eine sh-Funktion der Reihenfolge 2 × *N* -1 = 3, die Ergebnisse werden jedoch abgeschnitten. Dies bedeutet, dass das Produkt sich ( *f* × *g*  =   × × *f* ), aber nicht zuordnen lässt ( *f* × (*g* × *h*) ≠ ( *f* × *g*) × *h* ).

Diese Funktion verwendet die folgende Gleichung:


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



dabei \_ ist y i (s) die Funktion "ITH sh", und f (s) und g (s) verwenden die folgende sh-Funktion:


```
sum_i(y_i(s)*c_i)
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

 

 
