---
description: 'D3DXSHAdd-Funktion (D3DX10.h): Fügt zwei SH-Vektoren (PhericalIcalIcal, Förmige Förmiges) hinzu; anders ausgedrückt: pOut \[ i \] = pA i + \[ \] pB i \[ \] .'
ms.assetid: dbfea12b-c110-42a7-84b6-0dff3d958032
title: D3DXSHAdd-Funktion (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHAdd
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f59d0d83424039af6d2ca5d4ea6ca25702d6fc50039502fb0af0eae3ab782ec3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990930"
---
# <a name="d3dxshadd-function-d3dx10h"></a>D3DXSHAdd-Funktion (D3DX10.h)

Fügt zwei SH-Vektoren (PhericalIcal) hinzu. anders ausgedrückt: pOut \[ i \] = pA i + \[ \] pB i \[ \] .

## <a name="syntax"></a>Syntax


```C++
FLOAT* D3DXSHAdd(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf SH-Ausgabekoeffizienten. Die Auswertung generiert Order Koeffizienten. Siehe Hinweise.

</dd> <dt>

*Bestellung* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Reihenfolge der SH-Auswertung. Muss im Bereich von D3DXSH \_ MINORDER bis D3DXSH \_ MAXORDER (einschließlich) liegen. Die Auswertung generiert Order Koeffizienten. Der Grad der Auswertung ist Order - 1.

</dd> <dt>

*pA* \[ In\]
</dt> <dd>

Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Zeiger auf den ersten SH-Vektor.

</dd> <dt>

*pB* \[ In\]
</dt> <dd>

Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Zeiger auf den zweiten SH-Vektor.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf SH-Ausgabekoeffizienten.

## <a name="remarks"></a>Hinweise

Jeder Koeffizient der Basisfunktion "Ylm" wird an der Speicherposition "l): + m + l" gespeichert, wobei:

-   l ist der Grad der Basisfunktion.
-   m ist der Basisfunktionsindex für den angegebenen l-Wert und reicht von -l bis einschließlich l.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
