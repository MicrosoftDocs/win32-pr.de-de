---
title: Absoluter Wert
description: Verwenden Sie den absoluten Wert eines Quell Operanden, der in einer arithmetischen Operation verwendet wird.
ms.assetid: FD2ACE91-0AF6-43E8-80C5-849488E39BEF
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27ceefa2c4b4ee2eb890b0692a33266e89a18cfb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313740"
---
# <a name="absolute-value"></a>Absoluter Wert

Verwenden Sie den absoluten Wert eines Quell Operanden, der in einer arithmetischen Operation verwendet wird.



| \_Stäbchen |
|-------|



 

Dieser Modifizierer wird für Gleit Komma-und Gleit Komma Zahlen mit doppelter Genauigkeit und nur Anweisungen verwendet. Der **\_ ABS** -Modifizierer erzwingt das Vorzeichen der Zahl (en) im Quell Operanden, einschließlich der INF-Werte.

Das Anwenden von **\_ ABS** auf NaN behält Nan bei, obwohl das betreffende Nan-Bitmuster nicht definiert ist.

Wenn \_ ABS mit dem [Negation-Modifizierer](negate.md) kombiniert wird, erzwingt die Kombination das Vorzeichen, dass das Vorzeichen negativ ist, als wenn der **\_ ABS** - **Modifizierer** zuerst angewendet wird, dann die Negation.

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

 

 




