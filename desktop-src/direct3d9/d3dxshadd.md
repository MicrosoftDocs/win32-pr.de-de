---
description: 'Fügt zwei kugelförmige (SH) Vektoren hinzu. Anders ausgedrückt: Pout \[ i \] = PA \[ i \] + PB \[ i \] .'
ms.assetid: 12775c90-ed9d-4931-a449-2571816dd079
title: D3DXSHAdd-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 6b8f65a14cf745e8b378728d4fa6e0a234284d2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361856"
---
# <a name="d3dxshadd-function-d3dx9mathh"></a>D3DXSHAdd-Funktion (D3dx9math. h)

Fügt zwei kugelförmige (SH) Vektoren hinzu. Anders ausgedrückt: Pout \[ i \] = PA \[ i \] + PB \[ i \] .

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

*Pout* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Zeiger auf SH-Ausgabe Koeffizienten. Die Auswertung generiert die Koeffizienten der Bestellung. Siehe Hinweise.

</dd> <dt>

*Reihenfolge* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Reihenfolge der SH-Evaluierung. Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen. Die Auswertung generiert die Koeffizienten der Bestellung. Der Bewertungs Grad ist Order-1.

</dd> <dt>

*PA* \[ in\]
</dt> <dd>

Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***

Zeiger zum ersten SH-Vektor.

</dd> <dt>

*PB* \[ in\]
</dt> <dd>

Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***

Zeiger auf den zweiten SH-Vektor.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Zeiger auf SH-Ausgabe Koeffizienten.

## <a name="remarks"></a>Bemerkungen

Jeder Koeffizient der Basis Funktion "ylm" wird am Speicherort l ² + m + l gespeichert, wobei Folgendes gilt:

-   l ist der Grad der Basis Funktion.
-   m ist der Basis Funktions Index für den angegebenen l-Wert und reicht von-l bis l (einschließlich).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Voraus berechnete Strahlungs Übertragung (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
