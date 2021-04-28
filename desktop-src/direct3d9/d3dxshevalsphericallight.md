---
description: D3DXSHEvalSphericalLight-Funktion (D3dx9math.h) – Wertet ein pherisches Licht aus und gibt SH-Daten (Pherical Imaging) zurück.
ms.assetid: aa46c162-9c2d-49c0-925c-d0c06456f918
title: D3DXSHEvalSphericalLight-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalSphericalLight
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: db671d58806d999e07b1aac1e8e4da2fb38acc6f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117888"
---
# <a name="d3dxshevalsphericallight-function-d3dx9mathh"></a>D3DXSHEvalSphericalLight-Funktion (D3dx9math.h)

Wertet ein pherisches Licht aus und gibt SH-Daten (PhericalIcalIcals) zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXSHEvalSphericalLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pPos,
  _In_        FLOAT       Radius,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Bestellung* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Reihenfolge der SH-Auswertung. Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen. Die Auswertung generiert Order Koeffizienten. Der Grad der Auswertung ist Order - 1.

</dd> <dt>

*pPos* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf die Lichtposition.

</dd> <dt>

*Radius* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Radius der pherischen Glühbirnenquelle.

</dd> <dt>

*RIntensity* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Die rote Intensität des Lichts.

</dd> <dt>

*GIntensity* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Die grüne Intensität des Lichts.

</dd> <dt>

*BIntensity* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Die blaue Intensität des Lichts.

</dd> <dt>

*pROut* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf den SH-Ausgabevektor für die rote Komponente.

</dd> <dt>

*pGOut* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf den SH-Ausgabevektor für die grüne Komponente.

</dd> <dt>

*pBOut* \[ out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf den SH-Ausgabevektor für die blaue Komponente.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Bemerkungen

Wertet ein sphärisches Licht aus und gibt unerklärliche SH-Daten zurück. Es gibt keine Normalisierung der Intensität des Lichts, wie es für [gerichtete Beleuchtungen](light-types.md)gibt. Daher muss beim Angeben der Intensitäten sorgfältig vorgegangen werden. Dadurch werden drei Testbeispiele berechnet: *pROut* wird zurückgegeben, während *pGOut* und *pBOut* zurückgegeben werden können.

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

 

 
