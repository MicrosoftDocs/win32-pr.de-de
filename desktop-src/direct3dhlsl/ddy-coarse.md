---
title: ddy_coarse-Funktion
description: Berechnet eine partielle Ableitung mit niedriger Genauigkeit in Bezug auf die Bildschirmraum-y-Koordinate.
ms.assetid: f6103cd3-f7ee-41c2-b3cf-9e72ca84b25e
keywords:
- ddy_coarse HlSL-Funktion
topic_type:
- apiref
api_name:
- ddy_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 997b17d486d5e0a396e420bdc7b36da9d7ef83366a0d5c290110cf1cf2098c25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490640"
---
# <a name="ddy_coarse-function"></a>ddy \_ coarse-Funktion

Berechnet eine partielle Ableitung mit niedriger Genauigkeit in Bezug auf die Bildschirmraum-y-Koordinate.

## <a name="syntax"></a>Syntax

``` syntax
float ddy_coarse(
  in float value
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ In\]
</dt> <dd>

Typ: **float**

Der Eingabewert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **float**

Die partielle Ableitung des *Werts* mit niedriger Genauigkeit.

## <a name="remarks"></a>Hinweise

Die folgenden überladenen Versionen sind ebenfalls verfügbar:

``` syntax
float2 ddy_coarse(float2 value);
float3 ddy_coarse(float3 value);
float4 ddy_coarse(float4 value);
```

### <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höhere Shadermodelle | Ja       |



 

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

 

 




