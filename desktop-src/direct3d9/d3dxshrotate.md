---
description: Dreht den sphärischen harmonischen (SH) Vektor um die angegebene Matrix.
ms.assetid: 9e319725-6cbb-441e-b996-ec2c6f66e5df
title: D3DXSHRotate-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 606ef1909237fd9c0277c5d7112284f6b7018e0e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351946"
---
# <a name="d3dxshrotate-function-d3dx9mathh"></a>D3DXSHRotate-Funktion (D3dx9math. h)

Dreht den sphärischen harmonischen (SH) Vektor um die angegebene Matrix.

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

*Pout* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Zeiger auf Ausgabe Koeffizienten für die sphärischen (SH). Die Auswertung generiert die Koeffizienten der Bestellung. Dieser Zeiger sollte nicht mit *pIn* Alias sein. Siehe Hinweise.

</dd> <dt>

*Reihenfolge* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Reihenfolge der SH-Evaluierung. Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen. Die Auswertung generiert die Koeffizienten der Bestellung. Der Bewertungs Grad ist Order-1.

</dd> <dt>

*pmatrix* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf die Rotations Matrix. Die Rotations Teil Matrix muss orthogonal und eine Maßeinheit sein.

</dd> <dt>

*pIn* \[ in\]
</dt> <dd>

Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***

Zeiger auf gedrehte SH-Koeffizienten.

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

 

 
