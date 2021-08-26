---
description: 'D3DXFresnelTerm-Funktion (D3DX10Math.h): Berechnet den Fresnel-Begriff.'
ms.assetid: eaa2e5ea-9b6f-4216-8b48-7be74501124d
title: D3DXFresnelTerm-Funktion (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 862c83fd20e7646defbbaa7b82ad43ce0a384c1dd460d182af60bf8a5b23d88e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028710"
---
# <a name="d3dxfresnelterm-function-d3dx10mathh"></a>D3DXFresnelTerm-Funktion (D3DX10Math.h)

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

## <a name="remarks"></a>Hinweise

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



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
