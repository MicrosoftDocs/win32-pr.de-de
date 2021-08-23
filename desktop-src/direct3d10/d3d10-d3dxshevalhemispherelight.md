---
description: 'D3DXSHEvalChemisphereLight-Funktion (D3DX10.h): Wertet ein Licht aus, das eine lineare Interpolation zwischen zwei Farben über der Kugel ist.'
ms.assetid: 7523ff42-c81d-4857-a50d-7efa213214b8
title: D3DXSHEvalChemisphereLight-Funktion (D3DX10.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e32221167e2a736e46b847c88300221c3bd8b1675973604703600bb8e36549a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497910"
---
# <a name="d3dxshevalhemispherelight-function-d3dx10h"></a>D3DXSHEvalChemisphereLight-Funktion (D3DX10.h)

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

Die Reihenfolge der SH-Auswertung (SphericalLips). Muss im Bereich von D3DXSH \_ MINORDER bis D3DXSH \_ MAXORDER (einschließlich) liegen. Die Auswertung generiert Order²-Koeffizienten. Der Grad der Auswertung ist "Order - 1".

</dd> <dt>

*pDir* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf den Achsenrichtungsvektor (x, y, z), in dem die SH-Basisfunktionen ausgewertet werden sollen. Siehe Hinweise.

</dd> <dt>

*Top* \[ In\]
</dt> <dd>

Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

Die Sky-Farbe.

</dd> <dt>

*Unten* \[ In\]
</dt> <dd>

Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

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

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Die Interpolation erfolgt linear zwischen den beiden Punkten, nicht über der Oberfläche der Kugel (d. b. wenn die Achse (0,0,1) war, ist sie linear in Z, nicht im azizimalen Winkel. Die resultierende sphärische Beleuchtungsfunktion wird normalisiert, sodass ein Punkt auf einer perfekt diffusen Oberfläche ohne Schatten und ein normaler Punkt, der in Richtung pDir gezeigt wird, zu einer Ausgangslichtung mit dem Wert 1 führen würde (wenn die obere Farbe weiß und die untere Farbe schwarz wäre). Dies ist ein sehr einfaches Modell, bei dem Top die Intensität des "Sky" und Bottom die Intensität des "Bodens" darstellt.

Auf der Kugel mit Einheitenradius kann die Richtung wie in der folgenden Abbildung dargestellt einfach mit theta, dem Winkel um die Z-Achse in der rechtshändigen Richtung und phi, dem Winkel von z, angegeben werden.

![Abbildung einer Kugel mit Einheitenradius](images/spherical-coordinates.png)

Die folgenden Gleichungen zeigen die Beziehung zwischen kartesischen Koordinaten (x, y, z) und sphärischen Koordinaten (Theta, Phi) auf der Einheitenkugel. Der Winkel theta variiert über den Bereich von 0 bis 2 Pi, während phi von 0 bis pi variiert.

![Gleichungen der Beziehung zwischen kartesischen und sphärischen Koordinaten](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
