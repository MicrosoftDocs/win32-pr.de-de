---
description: 'D3DXSHEvalDirection-Funktion (D3dx9math.h): Wertet die SH-Basisfunktionen (Spherical Vector) aus einem Eingaberichtungsvektor aus.'
ms.assetid: f30ba32c-d6b0-4e4e-b5cd-839ed7821855
title: D3DXSHEvalDirection-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirection
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e02f0f3d8770b4b703f275de3225eacb301a7843
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093961"
---
# <a name="d3dxshevaldirection-function-d3dx9mathh"></a>D3DXSHEvalDirection-Funktion (D3dx9math.h)

Wertet die SH-Basisfunktionen (Spherical Vector) aus einem Eingaberichtungsvektor aus.

## <a name="syntax"></a>Syntax


```C++
FLOAT* D3DXSHEvalDirection(
  _Out_       FLOAT       *pOut,
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf SH-Ausgabekoeffizienten (Spherical veralten). Die Auswertung generiert Order²-Koeffizienten. Siehe Hinweise.

</dd> <dt>

*Bestellung* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Reihenfolge der SH-Auswertung. Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen. Die Auswertung generiert Order²-Koeffizienten. Der Grad der Auswertung ist "Order - 1".

</dd> <dt>

*pDir* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

(x, y, z) Richtungsvektor, in dem die SH-Basisfunktionen ausgewertet werden sollen. Muss normalisiert werden. Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf SH-Ausgabekoeffizienten. Siehe Hinweise.

## <a name="remarks"></a>Bemerkungen

Jeder Koeffizient der Basisfunktion "Ylm" wird an der Speicherposition "l): + m + l" gespeichert, wobei:

-   l ist der Grad der Basisfunktion.
-   m ist der Basisfunktionsindex für den angegebenen l-Wert und reicht von -l bis einschließlich l.

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

[Vorausberechnungsübertragung der Radiance (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
