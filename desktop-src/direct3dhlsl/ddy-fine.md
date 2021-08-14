---
title: ddy_fine-Funktion
description: Berechnet eine partielle Ableitung mit hoher Genauigkeit in Bezug auf die x-Koordinate des Bildschirmbereichs. | ddy_fine-Funktion
ms.assetid: 29fcdbc9-470b-4b5b-b18c-f75dd2c87920
keywords:
- ddy_fine-Funktion HLSL
topic_type:
- apiref
api_name:
- ddy_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b59f7ac500658570b19bf932e3abb042f9ecd8e27b63458c25032704c9ba4e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285883"
---
# <a name="ddy_fine-function"></a>ddy \_ fine-Funktion

Berechnet eine partielle Ableitung mit hoher Genauigkeit in Bezug auf die x-Koordinate des Bildschirmbereichs.

## <a name="syntax"></a>Syntax

``` syntax
float ddy_fine(
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
float2 ddy_fine(float2 value);
float3 ddy_fine(float3 value);
float4 ddy_fine(float4 value);  
```

### <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höhere Shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | w     |         |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




