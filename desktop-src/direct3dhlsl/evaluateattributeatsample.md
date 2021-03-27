---
title: Evaluateattributeatsample-Funktion
description: Wertet an der indizierten Stichproben Position aus.
ms.assetid: b5886004-5960-461d-a0d2-f4c3b0d09d94
keywords:
- Evaluateattributeatsample-Funktion HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtSample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b183f86599d08a6892e33c169b938dc09a2b55de
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718143"
---
# <a name="evaluateattributeatsample-function"></a>Evaluateattributeatsample-Funktion

Wertet an der indizierten Stichproben Position aus.

## <a name="syntax"></a>Syntax

``` syntax
numeric EvaluateAttributeAtSample(
  in attrib numeric value,
  in uint sampleindex
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ in\]
</dt> <dd>

Type: **atzb numeric**

Der Eingabewert.

</dd> <dt>

*sampleingedex* \[ in\]
</dt> <dd>

Typ: **uint**

Der Beispiel Speicherort.

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

 

 




