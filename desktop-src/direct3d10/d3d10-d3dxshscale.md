---
description: 'D3DXSHScale-Funktion (D3DX10.h): Skaliert einen pherischen Vektor (SH) anders ausgedrückt: pOut \[ i \] = pA i \[ \] \* Scale.'
ms.assetid: e323d238-f635-4780-982d-8798ba178f31
title: D3DXSHScale-Funktion (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHScale
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0fab96575e5542eaaed725a88f9ba52c3289a4ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108498"
---
# <a name="d3dxshscale-function-d3dx10h"></a>D3DXSHScale-Funktion (D3DX10.h)

Skaliert einen Sh-Vektor (PhericalIcal). anders ausgedrückt: pOut \[ i \] = pA i \[ \] \* Scale.

## <a name="syntax"></a>Syntax


```C++
FLOAT* D3DXSHScale(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pIn,
  _In_ const FLOAT Scale
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf SH-Ausgabekoeffizienten (Spherical- und Pherical-Rumpf). Die Auswertung generiert Order Koeffizienten. Siehe Hinweise.

</dd> <dt>

*Bestellung* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Reihenfolge der SH-Auswertung. Muss im Bereich von D3DXSH \_ MINORDER bis D3DXSH \_ MAXORDER (einschließlich) liegen. Die Auswertung generiert Order Koeffizienten. Der Grad der Auswertung ist Order - 1.

</dd> <dt>

*pIn* \[ In\]
</dt> <dd>

Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Zeiger auf den zu skalierenden SH-Vektor.

</dd> <dt>

*Skalieren* \[ In\]
</dt> <dd>

Typ: **const [**FLOAT**](../winprog/windows-data-types.md)**

Zeiger auf den Skalierungswert.

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
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
