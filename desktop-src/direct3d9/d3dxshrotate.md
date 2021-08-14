---
description: 'D3DXSHRotate-Funktion (D3dx9math.h): Rotiert den SH-Vektor (Pherical Rotation) um die gegebene Matrix.'
ms.assetid: 9e319725-6cbb-441e-b996-ec2c6f66e5df
title: D3DXSHRotate-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 26505e768a0f8ad48b069cee2cc83876976e0134d8a60a2f93b17b0cb2aad323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298279"
---
# <a name="d3dxshrotate-function-d3dx9mathh"></a>D3DXSHRotate-Funktion (D3dx9math.h)

Dreht den SH-Vektor (Pherical Rotation) um die gegebene Matrix.

## <a name="syntax"></a>Syntax


```C++
FLOAT* D3DXSHRotate(
  _Out_       FLOAT      *pOut,
  _In_        UINT       Order,
  _In_  const D3DXMATRIX *pMatrix,
  _In_  const FLOAT      *pIn
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf SH-Ausgabekoeffizienten (Spherical- oder Pherical-Rumpf). Die Auswertung generiert Order Koeffizienten. Dieser Zeiger sollte keinen Alias mit *pIn verwenden.* Siehe Hinweise.

</dd> <dt>

*Bestellung* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Reihenfolge der SH-Auswertung. Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen. Die Auswertung generiert Order Koeffizienten. Der Grad der Auswertung ist Order - 1.

</dd> <dt>

*pMatrix* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf die Rotationsmatrix. Die Rotationsuntermatrix muss orthogonal sein, mit einer Einheitsdetermination.

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

Jeder Koeffizient der Basisfunktion "Ylm" wird an der Speicherposition "l): + m + l" gespeichert, wobei:

-   l ist der Grad der Basisfunktion.
-   m ist der Basisfunktionsindex für den angegebenen l-Wert und reicht von -l bis einschließlich l.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Vorausberechnungsübertragung der Radiance (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
