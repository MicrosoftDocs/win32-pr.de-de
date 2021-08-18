---
description: Berechnet das Produkt von zwei Funktionen, die mit SH dargestellt werden (f und g).
ms.assetid: 632400a4-2ac9-438d-85f7-869101f350c8
title: D3DXSHMultiply2-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply2
- D3DXSHMultiply3
- D3DXSHMultiply4
- D3DXSHMultiply5
- D3DXSHMultiply6
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 00219ed1c38105562591b63e6bef64b949b2ab4443aed68e0e6b9d64cb156cc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849690"
---
# <a name="d3dxshmultiply2-function-d3dx9mathh"></a>D3DXSHMultiply2-Funktion (D3dx9math.h)

Berechnet das Produkt von zwei Funktionen, die mit SH dargestellt werden (f und g).

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

*pOut* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf die SH-Ausgabekoeffizienten – Basisfunktion Ylm wird unter l \* l + m+l gespeichert.

</dd> <dt>

*pF* \[ In\]
</dt> <dd>

Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Eingabe-SH-Coeffs für die erste Funktion.

</dd> <dt>

*pG* \[ In\]
</dt> <dd>

Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Zweiter Satz von EINGABE-SH-Coeffs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf SH-Ausgabekoeffizienten.

## <a name="remarks"></a>Hinweise

Die Reihenfolge ist eine Zahl zwischen 2 und einschließlich 6. Diese Seite dokumentiert also mehrere Funktionen: D3DXSHMultiply2, D3DXSHMultiply3, ... D3DXSHMultiply6.

Berechnet das Produkt von zwei Funktionen, die mit SH (f und g) dargestellt werden, wobei *pOut* \[ i = \] int(y \_ \* i(s) \* f(s) g(s)), wobei y \_ i(s) die ITH SH-Basisfunktion ist, f(s) und g(s) SH-Funktionen sind (sum \_ i(y \_ i(s) \* c \_ i)). Die Reihenfolge O bestimmt die Längen der Arrays, wobei immer O^2-Koeffizienten vorhanden sein sollten. Im Allgemeinen generiert das Produkt von zwei SH-Funktionen der Reihenfolge O eine SH-Funktion der Reihenfolge 2 \* O bis 1, aber die Ergebnisse werden abgeschnitten. Dies bedeutet, dass das Produkt (f \* g == g \* f) funktioniert, aber nicht zugeordnet wird (f \* (g \* h) != (f \* g) \* h.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
