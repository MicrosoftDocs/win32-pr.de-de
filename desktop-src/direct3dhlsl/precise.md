---
title: Precise (Genau)
description: 'Pro-Anweisung: Deaktivieren des arithmetischen Refactorings.'
ms.assetid: A26E569A-32EA-4AED-83C2-4F937AD3829E
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c7929a7ebab01b17aca3e11cb98de8796bf568cd08a3a7b04d8f3395f531d72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067910"
---
# <a name="precise"></a>Precise (Genau)

Pro-Anweisung: Deaktivieren des arithmetischen Refactorings.



| precise (Komponentenmaske) |
|--------------------------|



 

Dieser Modifizierer erfordert das globale Shaderflag "REFACTORING \_ ALLOWED". Wenn REFACTORING \_ ALLOWED vorhanden ist, können einzelne Komponentenergebnisse einzelner Anweisungen gezwungen werden, präzise zu bleiben oder von Compilern oder Treibern nicht umgestaltbar zu bleiben. Wenn Komponenten einer [**"toll"-Anweisung**](mad--sm4---asm-.md) als **präzise** gekennzeichnet werden, muss die Hardware eine **"toll"-Anweisung** oder die genaue Entsprechung ausführen und kann sie nicht in eine Multiplikation aufteilen, auf die ein Add folgt. Umgekehrt kann eine Multiplikation gefolgt von einem Add,bei dem entweder oder beide als **präzise** gekennzeichnet sind, nicht in einem fused-toll zusammengeführt werden. 

Wenn REFACTORING \_ ALLOWED nicht angegeben wurde, ist der **genaue** Modifizierer nicht zulässig. Sie ist nicht erforderlich, da alles präzise ist. Der **genaue** Modifizierer wirkt sich auf alle Vorgänge aus, nicht nur auf arithmetische Vorgänge.

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Dieser Modifizierer wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 5-Anweisungsmodifizierer](shader-model-5-instruction-modifiers.md)
</dt> </dl>

 

 




