---
description: 'D3DXSHAdd-Funktion (D3dx9math.h) – Fügt zwei SH-Vektoren (PhericalIcalIcal, Pherical- Enzyprischen) hinzu; anders ausgedrückt: pOut \[ i \] = pA i + \[ \] pB i \[ \] .'
ms.assetid: 12775c90-ed9d-4931-a449-2571816dd079
title: D3DXSHAdd-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7333d1803b9f7ea7b056ff78ffd053bd6086184b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117958"
---
# <a name="d3dxshadd-function-d3dx9mathh"></a>D3DXSHAdd-Funktion (D3dx9math.h)

Fügt zwei SH-Vektoren (PhericalIcal) hinzu. anders ausgedrückt: pOut \[ i \] = pA i + \[ \] pB i \[ \] .

## <a name="syntax"></a>Syntax


```C++
FLOAT* D3DXSHAdd(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pA,
  _In_  const FLOAT *pB
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf SH-Ausgabekoeffizienten. Die Auswertung generiert Order Koeffizienten. Siehe Hinweise.

</dd> <dt>

*Bestellung* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Reihenfolge der SH-Auswertung. Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen. Die Auswertung generiert Order Koeffizienten. Der Grad der Auswertung ist Order - 1.

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

## <a name="remarks"></a>Bemerkungen

Jeder Koeffizient der Basisfunktion "Ylm" wird an der Speicherposition ljs + m + l gespeichert, wobei Folgendes gilt:

-   l ist der Grad der Basisfunktion.
-   m ist der Basisfunktionsindex für den angegebenen l-Wert und reicht von -l bis l einschließlich.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Vorausberechnen der Übertragungsstärke (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
