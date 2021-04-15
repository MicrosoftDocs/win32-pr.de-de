---
title: Imad (SM4-ASM)
description: Ganze Zahl mit Vorzeichen multiplizieren und hinzufügen.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90db4cb0a36b0d3951e8b0490bb3ca08db8d5354
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104992983"
---
# <a name="imad-sm4---asm"></a>Imad (SM4-ASM)

Ganze Zahl mit Vorzeichen multiplizieren und hinzufügen.



| Imad dest \[ . mask \] , \[ - \] src0 \[ . Swizzle \] , \[ - \] Quelle1 \[ . Swizzle \] , \[ - \] Quelle2 \[ . Swizzle |
|---------------------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[im \] Ergebnis des Vorgangs.<br/>                      |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[unter \] Wert, der mit *Quelle1* multipliziert werden soll.<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[unter \] Wert, der mit *src0* multipliziert werden soll.<br/>                    |
| <span id="src2"></span><span id="SRC2"></span>*Quelle2*<br/> | \[unter \] Wert, der dem Produkt von *src0* und *Quelle1* hinzugefügt werden soll.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Komponenten Weise [imul](imul--sm4---asm-.md) der 32-Bit-Operanden *src0* und *Quelle1* (signiert), wobei die niedrigen 32 Bits (pro Komponente) des Ergebnisses, gefolgt von einem [IAdd](iadd--sm4---asm-.md) -Wert von *Quelle2*, generiert werden, wodurch das korrekte niedrige 32-Bit-Ergebnis (pro Komponente) erzeugt wird. Die 32-Bit-Ergebnisse werden in *dest* platziert.

Der optionale Negation-Modifizierer für Quell Operanden nimmt vor dem Ausführen arithmetischer Operationen eine Ergänzung von 2.

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

 

 





