---
title: Negate
description: Flippt das Vorzeichen des Werts eines Quell Operanden, der in einer arithmetischen Operation verwendet wird.
ms.assetid: 83ef3f61-7b0b-4033-8f7b-5345b205c441
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cc2637a76b52b28eefcfb3637cc8b2d406c02c06
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038320"
---
# <a name="negate"></a>Negate

Flippt das Vorzeichen des Werts eines Quell Operanden, der in einer arithmetischen Operation verwendet wird.



| \-  |
|-----|



 

Für Gleit Komma-und-Anweisungen mit einfacher und doppelter Genauigkeit flippt der Negation-Modifizierer das Vorzeichen der Zahl (n) im Quell Operanden, einschließlich der INF-Werte. Das Anwenden von **Negation** auf NaN behält Nan bei, obwohl das betreffende Nan-Bitmuster nicht definiert ist.

Für ganzzahlige Anweisungen nimmt der **Negation-Modifizierer** das 2-Komplement der Zahl (n) im Quell Operanden an.

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

 

 




