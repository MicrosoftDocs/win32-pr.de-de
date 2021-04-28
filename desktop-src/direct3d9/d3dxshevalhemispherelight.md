---
description: 'D3DXSHEvalChemisphereLight-Funktion (D3dx9math.h): Wertet ein Licht aus, das eine lineare Interpolation zwischen zwei Farben über der Kugel ist.'
ms.assetid: c5815f12-f706-40f6-bf5e-78a211cfbbea
title: D3DXSHEvalChemisphereLight-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalHemisphereLight
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7bc06dcf866c21cc5dcb96b23dea5a4640293fef
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093965"
---
# <a name="d3dxshevalhemispherelight-function-d3dx9mathh"></a>D3DXSHEvalChemisphereLight-Funktion (D3dx9math.h)

Wertet ein Licht aus, das eine lineare Interpolation zwischen zwei Farben über der Kugel ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXSHEvalHemisphereLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       D3DXCOLOR   Top,
  _In_       D3DXCOLOR   Bottom,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Bestellung* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Reihenfolge der SH-Auswertung (SphericalLips). Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen. Die Auswertung generiert Order²-Koeffizienten. Der Grad der Auswertung ist "Order - 1".

</dd> <dt>

*pDir* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf den Hemisphärenrichtungsvektor (x, y, z), in dem die SH-Basisfunktionen ausgewertet werden sollen. Siehe Hinweise.

</dd> <dt>

*Top* \[ In\]
</dt> <dd>

Typ: **[ **D3DXCOLOR**](d3dxcolor.md)**

Die Sky-Farbe.

</dd> <dt>

*Unten* \[ In\]
</dt> <dd>

Typ: **[ **D3DXCOLOR**](d3dxcolor.md)**

Die Bodenfarbe.

</dd> <dt>

*pROut* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf den SH-Ausgabevektor für die rote Komponente.

</dd> <dt>

*pGOut* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf den SH-Ausgabevektor für die grüne Komponente.

</dd> <dt>

*pBOut* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf den SH-Ausgabevektor für die blaue Komponente.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Bemerkungen

Die Interpolation erfolgt linear zwischen den beiden Punkten, nicht über der Oberfläche der Kugel (d. h., wenn die Achse (0,0,1) war, ist sie linear in Z, nicht im winkelförmigen Winkel. Die resultierende pherische Beleuchtungsfunktion wird normalisiert, sodass ein Punkt auf einer perfekt diffusen Oberfläche ohne Schatten und ein normaler Punkt, der in die Richtung *pDir* zeigt, zu einer Beendigungsfläche mit dem Wert 1 führen würde (wenn die obere Farbe weiß und die untere Farbe schwarz ist). Dies ist ein sehr einfaches Modell, bei dem *Top* die Intensität des "Sky" und *Bottom* die Intensität des "Bodens" darstellt.

Auf der Kugel mit Einheitenradius, wie in der folgenden Abbildung dargestellt, kann die Richtung einfach mit theta, dem Winkel um die Z-Achse in der rechtshändigen Richtung und phi, dem Winkel von z, angegeben [werden.](coordinate-systems.md)

![Abbildung einer Kugel mit Einheitenradius](images/spherical-coordinates.png)

Die folgenden Gleichungen zeigen die Beziehung zwischen kartesischen Koordinaten (x, y, z) und pherischen Koordinaten (Theta, phi) auf der Einheitenkugel. Der Winkel theta variiert im Bereich von 0 bis 2 Pi, während phi von 0 bis pi variiert.

![Gleichungen der Beziehung zwischen kartesischen und pherischen Koordinaten](images/spherical-coordinates-equations.png)

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

 

 
