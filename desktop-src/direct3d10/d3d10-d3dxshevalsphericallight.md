---
description: D3DXSHEvalSphericalLight-Funktion (D3DX10.h) – Wertet ein sphärisches Licht aus und gibt shherische (Spherical)-Daten zurück.
ms.assetid: e2a2b998-285a-46ef-99fe-ccc923013e9a
title: D3DXSHEvalSphericalLight-Funktion (D3DX10.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e1e509ea4695f143bd5399cbda004bcba53f514c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108558"
---
# <a name="d3dxshevalsphericallight-function-d3dx10h"></a>D3DXSHEvalSphericalLight-Funktion (D3DX10.h)

Wertet ein sphärisches Licht aus und gibt sh-Daten zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXSHEvalSphericalLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pPos,
  _In_       FLOAT       Radius,
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

*Bestellung* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Reihenfolge der SH-Auswertung. Muss im Bereich von D3DXSH \_ MINORDER bis D3DXSH \_ MAXORDER (einschließlich) liegen. Die Auswertung generiert Order²-Koeffizienten. Der Grad der Auswertung ist "Order - 1".

</dd> <dt>

*pPos* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf die helle Position.

</dd> <dt>

*Radius* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Radius der sphärischen Lichtquelle.

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

Wertet ein pherisches Licht aus und gibt sh-Daten zurück. Es gibt keine Normalisierung der Intensität des Lichts wie bei direktionalen Licht, daher muss bei der Angabe der Intensitäten vorsichtssam vorgesamst werden. Dadurch werden drei Beispielbeispiele berechnet. pROut wird zurückgegeben, während pGOut und pBOut zurückgegeben werden können.

Auf der Kugel mit Einheitenradius kann die Richtung wie in der folgenden Abbildung dargestellt einfach mit theta, dem Winkel um die Z-Achse in der rechtshändigen Richtung und phi, dem Winkel von z, angegeben werden.

![Abbildung einer Kugel mit Einheitenradius](images/spherical-coordinates.png)

Die folgenden Gleichungen zeigen die Beziehung zwischen kartesischen (x, y, z) und sphärischen Koordinaten (Theta, Phi) auf der Einheitenkugel. Der Winkel theta variiert im Bereich von 0 bis 2 Pi, während phi von 0 bis Pi variiert.

![Gleichungen der Beziehung zwischen kartesischen und sphärischen Koordinaten](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
