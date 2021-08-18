---
title: ddx_fine-Funktion
description: Berechnet eine partielle Ableitung mit hoher Genauigkeit in Bezug auf die x-Koordinate des Bildschirmbereichs. | ddx_fine-Funktion
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
ms.openlocfilehash: 5735d0e2f13a150b730855bc1308cba6e9f2dac795f6c5fc09000e42a607bec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986670"
---
# <a name="ddx_fine-function"></a>ddx \_ fine-Funktion

Berechnet eine partielle Ableitung mit hoher Genauigkeit in Bezug auf die x-Koordinate des Bildschirmbereichs.

## <a name="syntax"></a>Syntax

``` syntax
float ddx_fine(
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

Die partielle Ableitung des *Werts* mit hoher Genauigkeit.

## <a name="remarks"></a>Hinweise

Die folgenden überladenen Versionen sind ebenfalls verfügbar:

``` syntax
float2 ddx_fine(float2 value);
float3 ddx_fine(float3 value);
float4 ddx_fine(float4 value);
```

### <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höhere Shadermodelle | Ja       |



 

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




