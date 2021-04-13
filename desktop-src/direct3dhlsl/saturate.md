---
title: Sätftigen (HLSL-Referenz)
description: Bindet das Ergebnis einer arithmetischen Operation mit einer Gleit Komma Zahl oder einer Gleit Komma Zahl mit doppelter Genauigkeit in \ 0,0 f... 1.0 f \ Bereich.
ms.assetid: ce3e79c7-c3e6-4a2c-910a-2cd568aece50
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05b6048777ac7b6ecd2c4b59ff3c9e0287380949
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104389632"
---
# <a name="saturate-hlsl-reference"></a>Sätftigen (HLSL-Referenz)

Bindet das Ergebnis einer arithmetischen Operation mit einer Gleit Komma Zahl oder einer Gleit Komma Zahl mit doppelter Genauigkeit auf \[ 0,0 f... 1.0 f \] Bereich.



| \_gesetzt |
|-------|



 

Der **ergebnismodifizierer** "Bezeichner" führt die folgenden Vorgänge für die Ergebnis Werte aus einer arithmetischen Operation für Gleit Komma Operationen aus, auf die festgelegt wurde \_ :

`min(1.0f, max(0.0f, value))`

Dabei verhalten sich "min ()" und "Max ()" im obigen Ausdruck in der Art und Weise, wie [Min](min--sm4---asm-.md), [Max](max--sm4---asm-.md), [DMin](dmin--sm5---asm-.md)oder [DMax](dmax--sm5---asm-.md) betrieben werden.

`_sat(NaN)` gibt 0 zurück, durch die Regeln für min und Max.

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Dieser Modifizierer wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungs Modifizierer](instruction-modifiers.md)
</dt> </dl>

 

 




