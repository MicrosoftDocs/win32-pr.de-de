---
title: ddy_coarse-Funktion
description: Berechnet eine partielle Ableitung mit niedriger Genauigkeit in Bezug auf die y-Koordinate für den Bildschirmbereich.
ms.assetid: f6103cd3-f7ee-41c2-b3cf-9e72ca84b25e
keywords:
- ddy_coarse-Funktion HLSL
topic_type:
- apiref
api_name:
- ddy_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b6fef330e919a31e39306742bb03280454d47626
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038122"
---
# <a name="ddy_coarse-function"></a>rauen \_ grobe Funktion

Berechnet eine partielle Ableitung mit niedriger Genauigkeit in Bezug auf die y-Koordinate für den Bildschirmbereich.

## <a name="syntax"></a>Syntax

``` syntax
float ddy_coarse(
  in float value
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ in\]
</dt> <dd>

Typ: **float**

Der Eingabewert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **float**

Die partielle Ableitung mit niedriger Genauigkeit des *Werts*.

## <a name="remarks"></a>Bemerkungen

Außerdem sind die folgenden überladenen Versionen verfügbar:

``` syntax
float2 ddy_coarse(float2 value);
float3 ddy_coarse(float3 value);
float4 ddy_coarse(float4 value);
```

### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Intrinsische Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




