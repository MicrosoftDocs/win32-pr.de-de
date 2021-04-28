---
description: D3DXSHDot-Funktion (D3dx9math.h) – Berechnet das Punktprodukt von zwei SH-Vektoren (PhericalIcalIcal, PhericalIcalIcal).
ms.assetid: 71b7480d-ddac-4b02-bca7-d9318823d03e
title: D3DXSHDot-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87f88c7c7b80871a68084607cb99621199dfcc0a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093928"
---
# <a name="d3dxshdot-function-d3dx9mathh"></a>D3DXSHDot-Funktion (D3dx9math.h)

Berechnet das Punktprodukt von zwei SH-Vektoren (PhericalIcal).

## <a name="syntax"></a>Syntax


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Bestellung* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Reihenfolge der Sh-Auswertung (PhericalIcalIcal). Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen. Die Auswertung generiert Order Koeffizienten. Der Grad der Auswertung ist Order - 1.

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

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

SH-Ausgabekoeffizienten.

## <a name="remarks"></a>Bemerkungen

Jeder Koeffizient der Basisfunktion "Ylm" wird an der Speicherposition "l): + m + l" gespeichert, wobei:

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

 

 
