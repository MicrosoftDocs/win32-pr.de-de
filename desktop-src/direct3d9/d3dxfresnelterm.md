---
description: 'D3DXFresnelTerm-Funktion (D3dx9math.h): Berechnet den Fresnel-Begriff.'
ms.assetid: d3d281db-91a1-4100-8a82-028554b5a91d
title: D3DXFresnelTerm-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFresnelTerm
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5472f9839928fd3b4c1830bc309c7f610d487864
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114478"
---
# <a name="d3dxfresnelterm-function-d3dx9mathh"></a>D3DXFresnelTerm-Funktion (D3dx9math.h)

Berechnen Sie den Fresnel-Begriff.

## <a name="syntax"></a>Syntax


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*CosTheta* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Der Wert muss zwischen 0 und 1 liegen.

</dd> <dt>

*RefractionIndex* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Der Refraktionsindex eines Materials. Der Wert muss größer als 1 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Diese Funktion gibt den Fresnel-Begriff für unisiertes Licht zurück. CosTheta ist der Kosinus des Incidentwinkels.

## <a name="remarks"></a>Bemerkungen

So finden Sie den Fresnel-Begriff (F):

Wenn A ein Winkel von 1 und B der Winkel der Refraktion ist, dann


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]
    
Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



Wenn Sie dann mithilfe der Trig-Identitäten erweitern und vereinfachen, erhalten Sie:


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
