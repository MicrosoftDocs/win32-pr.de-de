---
title: ddx_coarse-Funktion
description: Berechnet eine partielle Ableitung mit niedriger Genauigkeit in Bezug auf die X-Koordinate des Bildschirmraums.
ms.assetid: 5719f45d-b2ae-4916-8f31-c2797b661814
keywords:
- ddx_coarse-Funktion HLSL
topic_type:
- apiref
api_name:
- ddx_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d5521da56804156485fcacb37b43cbf27d8d4b3659cbced918eaea2c12b308ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855370"
---
# <a name="ddx_coarse-function"></a>DDX-Funktion \_ "coarse"

Berechnet eine partielle Ableitung mit niedriger Genauigkeit in Bezug auf die X-Koordinate des Bildschirmraums.

## <a name="syntax"></a>Syntax

``` syntax
float ddx_coarse(
  in float value
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ In\]
</dt> <dd>

Typ: **float**

Der Eingabewert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **float**

Die partielle Ableitung des Werts mit niedriger *Genauigkeit.*

## <a name="remarks"></a>Hinweise

Die folgenden überladenen Versionen sind ebenfalls verfügbar:

``` syntax
float2 ddx_coarse(float2 value);
float3 ddx_coarse(float3 value);
float4 ddx_coarse(float4 value);
```

### <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher– Shadermodelle | Ja       |



 

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




