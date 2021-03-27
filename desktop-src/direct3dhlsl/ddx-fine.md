---
title: ddx_fine-Funktion
description: Berechnet eine partielle Ableitung mit hoher Genauigkeit in Bezug auf die x-Koordinate des Bildschirm Raums. | ddx_fine-Funktion
ms.assetid: 41062d6f-2b7f-4594-a6de-da37ded5d444
keywords:
- ddx_fine-Funktion HLSL
topic_type:
- apiref
api_name:
- ddx_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c1a579ba5899cf4d3ac3f25ef5a40337f6291977
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982083"
---
# <a name="ddx_fine-function"></a>DDX- \_ Funktion (fein)

Berechnet eine partielle Ableitung mit hoher Genauigkeit in Bezug auf die x-Koordinate des Bildschirm Raums.

## <a name="syntax"></a>Syntax

``` syntax
float ddx_fine(
  in float value
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

Die partielle Ableitung mit hoher Genauigkeit des- *Werts*.

## <a name="remarks"></a>Bemerkungen

Außerdem sind die folgenden überladenen Versionen verfügbar:

``` syntax
float2 ddx_fine(float2 value);
float3 ddx_fine(float3 value);
float4 ddx_fine(float4 value);
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

 

 




