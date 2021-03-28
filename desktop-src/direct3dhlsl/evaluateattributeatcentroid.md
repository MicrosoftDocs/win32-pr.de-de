---
title: Evaluateattributeatcentroid-Funktion
description: Wertet am Pixel Schwerpunkt aus.
ms.assetid: 6735b3f4-765f-4cd9-9f38-326a52709021
keywords:
- Evaluateattributeatcentroid-Funktion HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtCentroid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ee95c7f2f202dfd0065e5e9c30003cc46fd29281
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389181"
---
# <a name="evaluateattributeatcentroid-function"></a>Evaluateattributeatcentroid-Funktion

Wertet am Pixel Schwerpunkt aus.

## <a name="syntax"></a>Syntax

``` syntax
numeric EvaluateAttributeAtCentroid(
  in attrib numeric value
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ in\]
</dt> <dd>

Type: **atzb numeric**

Der Eingabewert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Interpolations Modus kann **linear** oder **linear ( \_ keine \_ Perspektive** ) für die Variable sein. Die Verwendung von " **Schwerpunkt** " oder " **Sample** " wird ignoriert. Attribute mit konstanter Interpolation sind ebenfalls zulässig. in diesem Fall wird der Beispiel Index ignoriert.

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

 

 




