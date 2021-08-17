---
title: Saturate (HLSL-Referenz)
description: Klammert das Ergebnis einer Gleitkommaarithmetikoperation mit einzelner oder doppelter Genauigkeit auf \ 0,0f... 1,0f\-Bereich.
ms.assetid: ce3e79c7-c3e6-4a2c-910a-2cd568aece50
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 25e771bd53dbb8a4b0d2eaf8162675cd556c071344b249562defe4a06e715f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790743"
---
# <a name="saturate-hlsl-reference"></a>Saturate (HLSL-Referenz)

Klammert das Ergebnis einer arithmetischen Gleitkommaoperation mit einzelner oder doppelter Genauigkeit auf \[ 0,0f... 1,0f-Bereich. \]



| \_Sat |
|-------|



 

Der Ergebnismodifizierer für die **Saturate-Anweisung** führt den folgenden Vorgang für die Ergebniswerte aus einer arithmetischen Gleitkommaoperation aus, die darauf angewendet \_ wurde:

`min(1.0f, max(0.0f, value))`

dabei verhalten sich min() und max() im obigen Ausdruck wie [min,](min--sm4---asm-.md) [max,](max--sm4---asm-.md) [dmin](dmin--sm5---asm-.md)oder [dmax.](dmax--sm5---asm-.md)

`_sat(NaN)` gibt nach den Regeln für min und max 0 zurück.

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Dieser Modifizierer wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungsmodifizierer](instruction-modifiers.md)
</dt> </dl>

 

 




