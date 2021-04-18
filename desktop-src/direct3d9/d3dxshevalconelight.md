---
description: Wertet ein Licht aus, bei dem es sich um einen Kegel konstanter Intensität handelt.
ms.assetid: 13088e3b-76ae-43ef-886e-686f1f18a31d
title: D3DXSHEvalConeLight-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalConeLight
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2400fe0430e008ea1b704ee4daef51eeee7bd7a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104563274"
---
# <a name="d3dxshevalconelight-function-d3dx9mathh"></a>D3DXSHEvalConeLight-Funktion (D3dx9math. h)

Wertet ein Licht aus, bei dem es sich um einen Kegel konstanter Intensität handelt.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXSHEvalConeLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir,
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

*Reihenfolge* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Reihenfolge der SH-Evaluierung. Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen. Die Auswertung generiert die Koeffizienten der Bestellung. Der Bewertungs Grad ist Order-1.

</dd> <dt>

*pdir* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Ein Zeiger auf den Achsen Richtungsvektor (x, y, z), in dem die sh-Basisfunktionen ausgewertet werden. Siehe Hinweise.

</dd> <dt>

*RADIUS* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der Radius des Kegel im Bogenmaße.

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

*Proxy* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Zeiger auf den Ausgabe-SH-Vektor für die rote Komponente.

</dd> <dt>

*pgout* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Zeiger auf den Ausgabe-SH-Vektor für die grüne Komponente.

</dd> <dt>

*pbout* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Zeiger auf den Ausgabe-SH-Vektor für die blaue Komponente.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert lauten: D3DERR \_ invalidcall.

## <a name="remarks"></a>Bemerkungen

Wertet ein Licht aus, bei dem es sich um einen Kegel konstanter Intensität handelt Der Ausgabe Vektor wird berechnet, sodass die Ausgangs Kraft eines Punkts, der sich direkt unterhalb des Lichts (in der Kegel Richtung eines diffuses Objekts mit einem Albedo-Wert von 1) befindet, 1,0 ist, wenn das Intensität-Verhältnis von R/G/B gleich 1 ist. Dadurch werden drei Spektral Beispiele berechnet. " *Prout* " wird zurückgegeben, während " *pgout* " und " *pbout* " zurückgegeben werden können.

In der Kugel mit Einheiten RADIUS, wie in der folgenden Abbildung gezeigt, kann die Richtung einfach mit der TA angegeben werden, dem Winkel zur z-Achse in der [rechten Hand Richtung](coordinate-systems.md)und dem Phi, dem Winkel von z.

![Abbildung einer Kugel mit Einheiten RADIUS](images/spherical-coordinates.png)

Die folgenden Gleichungen zeigen die Beziehung zwischen kartesischen Koordinaten (x, y, z) und sphärischen Koordinaten (Orta, Phi) in der Einheits Kugel. Der Winkel der Spitze variiert im Bereich von 0 bis 2 PI, während sich der Wert von "0" bis "Pi" unterscheidet.

![Gleichungen der Beziehung zwischen kartesischen und kugelförmigen Koordinaten](images/spherical-coordinates-equations.png)

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

 

 
