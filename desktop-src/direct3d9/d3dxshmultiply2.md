---
description: Berechnet das Produkt von zwei Funktionen, die mit sh (f und g) dargestellt werden.
ms.assetid: 632400a4-2ac9-438d-85f7-869101f350c8
title: D3DXSHMultiply2-Funktion (D3dx9math. h)
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
ms.openlocfilehash: f7b9adaf5caf7b4b2d35035fd5c2a916298b0c8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355800"
---
# <a name="d3dxshmultiply2-function-d3dx9mathh"></a>D3DXSHMultiply2-Funktion (D3dx9math. h)

Berechnet das Produkt von zwei Funktionen, die mit sh (f und g) dargestellt werden.

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

Ein Zeiger auf die Ausgabe-SH-Basis Funktion "ylm" wird in l \* l + m + l gespeichert.

</dd> <dt>

*PF* \[ in\]
</dt> <dd>

Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***

Geben Sie sh coeffs als erste Funktion ein.

</dd> <dt>

*PG* \[ in\]
</dt> <dd>

Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***

Der zweite Satz von Eingabe-SH-coeffs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Zeiger auf SH-Ausgabe Koeffizienten.

## <a name="remarks"></a>Bemerkungen

Die Reihenfolge ist eine Zahl zwischen 2 und einschließlich 6. Auf dieser Seite werden also mehrere Funktionen dokumentiert: D3DXSHMultiply2, D3DXSHMultiply3,... D3DXSHMultiply6.

Berechnet das Produkt von zwei Funktionen, die mit sh (f und g) dargestellt werden, wobei *Pout* \[ i \] = int (y i (s) f (s) \_ g (s)) ist \* \* , wobei y \_ i (s) die ITH-Basis Funktion ist, f (s) und g (s) SH Functions (Sum \_ i (y \_ i (s) \* c \_ i)). Die Reihenfolge o bestimmt die Längen der Arrays, bei denen immer O ^ 2-Koeffizienten vorhanden sein sollten. Im allgemeinen generiert das Produkt von zwei SH-Funktionen von Order O eine sh-Funktion von Order 2 \* O-1, aber die Ergebnisse werden abgeschnitten. Dies bedeutet, dass das Produkt sich (f \* g = = g \* f), aber nicht zuordnen lässt (f \* (g \* h)! = (f \* g) \* h.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
