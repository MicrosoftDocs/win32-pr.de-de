---
title: Swap (SM5-ASM)
description: Führt einen Komponenten bezogenen bedingten Austausch der Werte zwischen zwei Eingabe Registern aus.
ms.assetid: 3DFCEB82-076E-4AFA-915F-47390A355B7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d2ee674a1cb1067594b0e96c739ff8df73b152
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993087"
---
# <a name="swapc-sm5---asm"></a>Swap (SM5-ASM)

Führt einen Komponenten bezogenen bedingten Austausch der Werte zwischen zwei Eingabe Registern aus.



| "dest0. \[ Mask" \] , "dest1 \[ . Mask" \] , "src0 \[ . Swizzle" \] , "Quelle1 \[ . Swizzle" \] , "Quelle2 \[ . Swizzle"\] |
|--------------------------------------------------------------------------------------------|



 



| Element                                                               | BESCHREIBUNG                                                                                     |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[in registrieren Sie sich für \] beliebige nicht leere Schreib Masken. Muss sich von *dest1* unterscheiden.<br/> |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[in registrieren Sie sich für \] beliebige nicht leere Schreib Masken. Muss sich von *dest0* unterscheiden.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[in werden \] vier Bedingungen bereitstellt. Ein ganzzahliger Wert ungleich 0 bedeutet **true**. <br/>               |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/>    | \[in \] einem der Werte, die ausgetauscht werden sollen.<br/>                                              |
| <span id="src2"></span><span id="SRC2"></span>*Quelle2*<br/>    | \[in \] einem der Werte, die ausgetauscht werden sollen.<br/>                                              |



 

## <a name="remarks"></a>Bemerkungen

Die Codierung dieser Anweisung versucht, mehrere parallele bedingte Austausch Vorgänge von skalaren in 2 4-Komponenten Registern zu Ausdrücken, wobei die Anordnung der Paare von Zahlen, die an dem Austausch beteiligt sind, geringfügig flexibel ist.

Die Auswahl von Register und Wert für *src0*, *Quelle1* und *Quelle2* ist in keiner Weise eingeschränkt, wie z. b. in der Art von " [muvc](movc--sm4---asm-.md)".

Die Semantik dieser Anweisung kann durch die entsprechenden Vorgänge mit der Anweisung " **muvc** " beschrieben werden. Der schlimmste Fall wird im folgenden Beispiel gezeigt, um sicherzustellen, dass die Ziel Register bis zum Ende nicht aktualisiert werden.

``` syntax
                swapc dest0[.mask], 
                      dest1[.mask],
                      src0[.swizzle],
                      src1[.swizzle],
                      src2[.swizzle]

                expands to:

                movc temp[dest0 s mask], 
                     src0[.swizzle], 
                     src2[.swizzle], src1[.swizzle]

                movc dest1[.mask], 
                     src0[.swizzle], 
                     src1[.swizzle], src2[.swizzle]

                mov  dest0.mask, temp
```

Sie können auswählen, wie der Task angegangen werden soll, wenn nicht direkt. Der gleiche Effekt kann z. b. durch eine Sequenz von bis zu 4 einfachen skalarbedingtem Austausch Vorgängen oder wie oben beschrieben werden, und zwar mit zwei Vektor- **muvc** -Anweisungen, zuzüglich des Aufwands, um sicherzustellen, dass die Quell Werte nicht durch frühere Vorgänge in der Mitte der Erweiterung geclot werden.

Verwenden Sie diese Anweisung zum Sortieren.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Anweisung wird in den folgenden shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





