---
title: Precise (Genau)
description: Die pro-Anweisung-Deaktivierung des arithmetischen refactorings.
ms.assetid: A26E569A-32EA-4AED-83C2-4F937AD3829E
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03f288fb5dafee0e29c8c11cab72156f7ad3d569
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516478"
---
# <a name="precise"></a>Precise (Genau)

Die pro-Anweisung-Deaktivierung des arithmetischen refactorings.



| präzise (Komponenten Maske) |
|--------------------------|



 

Dieser Modifizierer erfordert das globale shaderflag "Refactoring \_ zugelassen". Wenn das Refactoring \_ zulässig ist, können einzelne Komponenten Ergebnisse einzelner Anweisungen erzwungen werden, damit Sie durch Compiler oder Treiber präzise oder nicht umgestaltbar bleiben. Wenn die Komponenten einer [**Mad**](mad--sm4---asm-.md) -Anweisung als **präzise** gekennzeichnet sind, muss die Hardware eine **Mad** -Anweisung oder die exakte Entsprechung ausführen, und Sie kann Sie nicht in ein multiplizieren, gefolgt von einem Add-Wert, aufteilen. Umgekehrt kann ein multiplizieren, gefolgt von einem Add-in, bei dem entweder oder beide als **genau** gekennzeichnet sind, nicht mit einem gemergten **Mad** zusammengeführt werden.

Wenn Refactoring \_ zugelassen nicht angegeben wurde, ist der **exakte** Modifizierer nicht zulässig. Er ist nicht erforderlich, da alles präzise ist. Der **genaue** Modifizierer wirkt sich auf jeden Vorgang aus, nicht nur auf Arithmetik.

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Dieser Modifizierer wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Anweisungs modifiziererer](shader-model-5-instruction-modifiers.md)
</dt> </dl>

 

 




