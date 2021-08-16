---
description: 'D3DXSHEvalConeLight-Funktion (D3dx9math.h): Wertet ein Licht aus, das ein Kegel konstanter Intensität ist und shherische (Sh)-Daten zurückgibt.'
ms.assetid: 13088e3b-76ae-43ef-886e-686f1f18a31d
title: D3DXSHEvalConeLight-Funktion (D3dx9math.h)
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
ms.openlocfilehash: a3904ee079399a2a3b7152e04a0101bfdef6f1eee393822465bf072271749cba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122759"
---
# <a name="d3dxshevalconelight-function-d3dx9mathh"></a>D3DXSHEvalConeLight-Funktion (D3dx9math.h)

Wertet ein Licht aus, das ein Kegel konstanter Intensität ist, und gibt SH-Daten zurück.

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

*Bestellung* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Reihenfolge der SH-Auswertung. Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen. Die Auswertung generiert Order²-Koeffizienten. Der Grad der Auswertung ist "Order - 1".

</dd> <dt>

*pDir* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf den Hemisphärenrichtungsvektor (x, y, z), in dem die SH-Basisfunktionen ausgewertet werden sollen. Siehe Hinweise.

</dd> <dt>

*Radius* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Kegelradius im Bogenmaß.

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

## <a name="remarks"></a>Hinweise

Wertet ein Licht aus, bei dem es sich um einen Kegel konstanter Intensität handelt, und gibt rekonsistente SH-Daten zurück. Der Ausgabevektor wird so berechnet, dass bei einem Intensitätsverhältnis von R/G/B gleich 1 die Ausgangsstärke eines Punkts direkt unter dem Licht (in Kegelrichtung an einem diffusen Objekt mit einem Albedo von 1 ausgerichtet) 1,0 wäre. Dadurch werden drei Testbeispiele berechnet: *pROut* wird zurückgegeben, während *pGOut* und *pBOut* zurückgegeben werden können.

Auf der Kugel mit Einheitenradius kann die Richtung wie in der folgenden Abbildung dargestellt einfach mit theta, dem Winkel um die [Z-Achse in rechtshändiger Richtung](coordinate-systems.md)und phi, dem Winkel von z, angegeben werden.

![Abbildung einer Kugel mit Einheitenradius](images/spherical-coordinates.png)

Die folgenden Gleichungen zeigen die Beziehung zwischen kartesischen Koordinaten (x, y, z) und sphärischen Koordinaten (Theta, Phi) auf der Einheitenkugel. Der Winkel theta variiert über den Bereich von 0 bis 2 Pi, während phi von 0 bis pi variiert.

![Gleichungen der Beziehung zwischen kartesischen und sphärischen Koordinaten](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Vorausberechnen der Übertragungsstärke (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
