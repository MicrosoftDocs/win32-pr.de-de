---
description: Berechnet das Punktprodukt zweier kugelförmiger (SH) Vektoren.
ms.assetid: 30f0e858-4c31-4b25-9979-754d996a7d48
title: D3DXSHDot-Funktion (d3dx10. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 20f0896168dae0e2a779625c683777938c8e2df2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353750"
---
# <a name="d3dxshdot-function-d3dx10h"></a>D3DXSHDot-Funktion (d3dx10. h)

Berechnet das Punktprodukt zweier kugelförmiger (SH) Vektoren.

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

*Reihenfolge* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Reihenfolge der Auswertung der sphärischen Harmonika (SH). Muss im Bereich von D3DXSH \_ minorder bis D3DXSH \_ maxorder (einschließlich) liegen. Die Auswertung generiert die Koeffizienten der Bestellung. Der Bewertungs Grad ist Order-1.

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

Typ: **[ **float**](../winprog/windows-data-types.md)**

SH-Ausgabe Koeffizienten.

## <a name="remarks"></a>Bemerkungen

Jeder Koeffizient der Basis Funktion "ylm" wird am Speicherort l ² + m + l gespeichert, wobei Folgendes gilt:

-   l ist der Grad der Basis Funktion.
-   m ist der Basis Funktions Index für den angegebenen l-Wert und reicht von-l bis l (einschließlich).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
