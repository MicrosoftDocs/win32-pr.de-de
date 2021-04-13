---
description: Wertet ein Direktionales Licht aus und gibt die Daten mit dem Wert "Spectral Kugel Harmonic" zurück
ms.assetid: b5c657f5-d291-4e53-908c-670b29a1888a
title: D3DXSHEvalDirectionalLight-Funktion (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirectionalLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9c6b5c9590132d9fe3d0fc07ae419d442144079a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104561464"
---
# <a name="d3dxshevaldirectionallight-function-d3dx10h"></a>D3DXSHEvalDirectionalLight-Funktion (d3dx10. h)

Wertet ein Direktionales Licht aus und gibt die Daten mit dem Wert "Spectral Kugel Harmonic" zurück

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXSHEvalDirectionalLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Reihenfolge* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Reihenfolge der SH-Evaluierung. Muss im Bereich von D3DXSH \_ minorder bis D3DXSH \_ maxorder (einschließlich) liegen. Die Auswertung generiert die Koeffizienten der Bestellung. Der Bewertungs Grad ist Order-1.

</dd> <dt>

*pdir* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ein Zeiger auf den Achsen Richtungsvektor (x, y, z), in dem die sh-Basisfunktionen ausgewertet werden. Siehe Hinweise.

</dd> <dt>

*Rintensität* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Die rote Intensität des Lichts.

</dd> <dt>

*Gintensity* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Die grüne Intensität des Lichts.

</dd> <dt>

*Bintensity* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Die blaue Intensität des Lichts.

</dd> <dt>

*Proxy* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Zeiger auf den Ausgabe-SH-Vektor für die rote Komponente.

</dd> <dt>

*pgout* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Optionaler Zeiger auf den Ausgabe-SH-Vektor für die grüne Komponente.

</dd> <dt>

*pbout* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Optionaler Zeiger auf den Ausgabe-SH-Vektor für die blaue Komponente.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert lauten: D3DERR \_ invalidcall.

## <a name="remarks"></a>Bemerkungen

Der Ausgabe Vektor wird berechnet, sodass die resultierende Ausgangs Glanz eines Punkts, der sich auf ein diffuses Objekt mit einem Albedo von 1 direkt unter dem Licht für ein diffuses Objekt mit dem Wert 1 ergibt, 1,0 ist, wenn das Intensität-Verhältnis von R/G/B 1 beträgt. Dadurch werden drei Spektral Beispiele berechnet. "Prout" wird zurückgegeben, während "pgout" und "pbout" zurückgegeben werden können.

In der Kugel mit Einheiten RADIUS, wie in der folgenden Abbildung gezeigt, kann die Richtung einfach mit der TA angegeben werden, dem Winkel zur z-Achse in der rechten Hand Richtung und dem Phi, dem Winkel von z.

![Abbildung einer Kugel mit Einheiten RADIUS](images/spherical-coordinates.png)

Die folgenden Gleichungen zeigen die Beziehung zwischen kartesischen Koordinaten (x, y, z) und sphärischen Koordinaten (Orta, Phi) in der Einheits Kugel. Der Winkel der Spitze variiert im Bereich von 0 bis 2 PI, während sich der Wert von "0" bis "Pi" unterscheidet.

![Gleichungen der Beziehung zwischen kartesischen und kugelförmigen Koordinaten](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
