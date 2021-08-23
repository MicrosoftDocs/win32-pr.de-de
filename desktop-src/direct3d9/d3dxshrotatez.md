---
description: 'D3DXSHRotateZ-Funktion (D3dx9math.h): Rotiert den SH-Vektor (Spherical Vector) in der Z-Achse um den angegebenen Winkel.'
ms.assetid: 1f471183-4c8e-4fa8-9a42-f6cc2bb1b0f2
title: D3DXSHRotateZ-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotateZ
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ccc1d85ff1fda2bc2a67744a2e9ef75ad99839d63ee8b9e332660a2bd36a30fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630760"
---
# <a name="d3dxshrotatez-function-d3dx9mathh"></a>D3DXSHRotateZ-Funktion (D3dx9math.h)

Rotiert den SH-Vektor (Spherical Vector) in der Z-Achse um den angegebenen Winkel.

## <a name="syntax"></a>Syntax


```C++
FLOAT* D3DXSHRotateZ(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_        FLOAT Angle,
  _In_  const FLOAT *pIn
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf SH-Ausgabekoeffizienten (Spherical Veralten). Die Auswertung generiert Order²-Koeffizienten. Dieser Zeiger sollte keinen Alias mit *pIn* verwenden. Siehe Hinweise.

</dd> <dt>

*Bestellung* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Reihenfolge der SH-Auswertung. Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen. Die Auswertung generiert Order²-Koeffizienten. Der Grad der Auswertung ist "Order - 1".

</dd> <dt>

*Winkel* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Drehwinkel im Bogenmaß. Die Drehung erfolgt um die Z-Achse.

</dd> <dt>

*pIn* \[ In\]
</dt> <dd>

Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Zeiger auf gedrehte SH-Koeffizienten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf SH-Ausgabekoeffizienten.

## <a name="remarks"></a>Hinweise

Jeder Koeffizient der Basisfunktion "Ylm" wird an der Speicherposition ljs + m + l gespeichert, wobei Folgendes gilt:

-   l ist der Grad der Basisfunktion.
-   m ist der Basisfunktionsindex für den angegebenen l-Wert und reicht von -l bis l einschließlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Vorausberechnen der Übertragungsstärke (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
