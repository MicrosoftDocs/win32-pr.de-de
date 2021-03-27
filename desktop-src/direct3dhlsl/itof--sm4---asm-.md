---
title: itof (SM4-ASM)
description: Ganzzahl mit Vorzeichen für Gleit Komma Konvertierung.
ms.assetid: 60652168-25FA-4084-8CC1-73F12984ECED
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f9d262f65801cd2caa0e6432b335ce32fff0d4e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857783"
---
# <a name="itof-sm4---asm"></a>itof (SM4-ASM)

Ganzzahl mit Vorzeichen für Gleit Komma Konvertierung.



| itof dest \[ . mask \] , \[ - \] src0 \[ . Swizzle\] |
|-------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] enthält das Ergebnis des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] enthält den zu konvertierenden Wert.<br/>        |



 

## <a name="remarks"></a>Bemerkungen

Diese Konvertierungs Anweisung mit Vorzeichen unter Vorzeichen setzt voraus, dass *src0* 32 eine ganze Zahl mit Vorzeichen und 4-Tupel mit Vorzeichen enthält. Nachdem die Anweisung ausgeführt wurde, enthält " *dest* " ein 4-Tupel mit Gleit Komma Wert.

Die Konvertierung erfolgt pro Komponente.

Wenn ein ganzzahliger Eingabe Wert zu groß ist, um genau im Gleit Komma Format dargestellt zu werden, wird die Rundung auf den nächstgelegenen geraden Modus dringend empfohlen, ist aber nicht erforderlich.

Der optionale Negation-Modifizierer für den Quell Operanden nimmt vor dem Durchführen einer arithmetischen Operation eine Ergänzung von 2.

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

 

 





