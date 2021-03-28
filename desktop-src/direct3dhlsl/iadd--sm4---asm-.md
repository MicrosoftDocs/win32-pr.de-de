---
title: IAdd (SM4-ASM)
description: Ganzzahlige Addition.
ms.assetid: EF78EA65-DC16-469A-9E45-52844FF4BD93
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b593484aa7c1ef376bb5febf141b144ddef338e0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389574"
---
# <a name="iadd-sm4---asm"></a>IAdd (SM4-ASM)

Ganzzahlige Addition.



| IAdd dest \[ . mask \] , \[ - \] src0 \[ . Swizzle \] , \[ - \] Quelle1 \[ . Swizzle\] |
|------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse des Vorgangs Ergebnisses.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] der Zahl, die zu *Quelle1* hinzugefügt werden soll.<br/>           |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[in \] der Zahl, die zu *src0* hinzugefügt werden soll.<br/>           |



 

## <a name="remarks"></a>Bemerkungen

Komponenten weises Hinzufügen von 32-Bit-Operanden *src0* und *Quelle1*, wobei das korrekte 32-Bit-Ergebnis in *dest* platziert wird. Über die 32-Bit-Werte der einzelnen Komponenten hinaus werden keine übertragen oder Ausleihe durchgeführt, sodass diese Anweisung nicht für die Signierung ihrer Operanden sensibel ist.

Der optionale Negation-Modifizierer für Quell Operanden nimmt die Ergänzung von 2 vor dem Ausführen des Vorgangs an.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



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

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





