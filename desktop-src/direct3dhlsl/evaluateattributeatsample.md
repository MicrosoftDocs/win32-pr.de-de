---
title: EvaluateAttributeAtSample-Funktion
description: Wertet am indexierten Beispielspeicherort aus.
ms.assetid: b5886004-5960-461d-a0d2-f4c3b0d09d94
keywords:
- EvaluateAttributeAtSample-Funktion HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtSample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 29191a3790afee2d37fee3d2ee8fb58673ff487af178bd8b1e2b33f26f1ec44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982480"
---
# <a name="evaluateattributeatsample-function"></a>EvaluateAttributeAtSample-Funktion

Wertet am indexierten Beispielspeicherort aus.

## <a name="syntax"></a>Syntax

``` syntax
numeric EvaluateAttributeAtSample(
  in attrib numeric value,
  in uint sampleindex
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ In\]
</dt> <dd>

Typ: **attrib numeric**

Der Eingabewert.

</dd> <dt>

*sampleindex* \[ In\]
</dt> <dd>

Typ: **uint**

Der Beispielspeicherort.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Interpolationsmodus kann linear oder **linear** sein, **ohne \_ \_ Perspektive** auf die Variable. Die Verwendung von **Schwerpunkt** oder **Beispiel** wird ignoriert. Attribute mit konstanter Interpolation sind ebenfalls zulässig. In diesem Fall wird der Beispielindex ignoriert.

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

 

 




