---
title: ddx_coarse-Funktion
description: Berechnet eine partielle Ableitung mit niedriger Genauigkeit in Bezug auf die x-Koordinate des Bildschirm Raums.
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
ms.openlocfilehash: 4f9d4805a1d516a5d8980fcd8209fd6733fe86c4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038123"
---
# <a name="ddx_coarse-function"></a>grobe DDX- \_ Funktion

Berechnet eine partielle Ableitung mit niedriger Genauigkeit in Bezug auf die x-Koordinate des Bildschirm Raums.

## <a name="syntax"></a>Syntax

``` syntax
float ddx_coarse(
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
float2 ddx_coarse(float2 value);
float3 ddx_coarse(float3 value);
float4 ddx_coarse(float4 value);
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

 

 




