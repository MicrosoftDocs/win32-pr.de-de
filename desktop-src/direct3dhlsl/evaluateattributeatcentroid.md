---
title: EvaluateAttributeAtCentroid-Funktion
description: Wertet am Pixelschwerpunkt aus.
ms.assetid: 6735b3f4-765f-4cd9-9f38-326a52709021
keywords:
- EvaluateAttributeAtCentroid-Funktion HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtCentroid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 867f7dadc2ccf7d86eed602dd9e65d07be7558f0a8a00426e3a45bc1c2c97a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744040"
---
# <a name="evaluateattributeatcentroid-function"></a>EvaluateAttributeAtCentroid-Funktion

Wertet am Pixelschwerpunkt aus.

## <a name="syntax"></a>Syntax

``` syntax
numeric EvaluateAttributeAtCentroid(
  in attrib numeric value
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ In\]
</dt> <dd>

Typ: **attrib numeric**

Der Eingabewert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Interpolationsmodus kann **linear oder linear** **\_ sein, keine Perspektive \_ auf** die Variable. Die Verwendung **von Schwerpunkten** **oder Stichproben** wird ignoriert. Attribute mit konstanter Interpolation sind ebenfalls zulässig. In diesem Fall wird der Beispielindex ignoriert.

### <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher– Shadermodelle | Ja       |



 

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

 

 




