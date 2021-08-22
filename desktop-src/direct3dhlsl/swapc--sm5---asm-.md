---
title: swapc (sm5 - asm)
description: Führt einen komponentenweisen bedingten Austausch der Werte zwischen zwei Eingaberegistern durch.
ms.assetid: 3DFCEB82-076E-4AFA-915F-47390A355B7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d09d52bd497c7819500c11c4464907e4a7854bb305ed0e31d53b897ba4cf7e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486260"
---
# <a name="swapc-sm5---asm"></a>swapc (sm5 - asm)

Führt einen komponentenweisen bedingten Austausch der Werte zwischen zwei Eingaberegistern durch.



| swapc dest0 \[ .mask \] , dest1 \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle \] , src2 \[ .swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Element                                                               | Beschreibung                                                                                     |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[in \] Register with arbitrary nonempty write masks (Registrieren mit beliebigen nichtmpty-Schreibmasken). Muss sich von *dest1* unterscheiden.<br/> |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[in \] Register with arbitrary nonempty write masks (Registrieren mit beliebigen nichtmpty-Schreibmasken). Muss sich von *dest0* unterscheiden.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[in \] Stellt 4 Bedingungen bereit. Ein ganzzahliger Wert ungleich 0 (null) bedeutet **true.** <br/>               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[in \] einem der Werte, die ausgetauscht werden sollen.<br/>                                              |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/>    | \[in \] einem der Werte, die ausgetauscht werden sollen.<br/>                                              |



 

## <a name="remarks"></a>Hinweise

Die Codierung dieser Anweisung versucht, mehrere parallele bedingte Tausche von Skalarn über zwei Register mit 4 Komponenten hinweg mit geringfügiger Flexibilität bei der Anordnung der Zahlenpaare, die am Austausch beteiligt sind, kompakt auszudrücken.

Die Auswahl von Register und Wert für *src0,* *src1* und *src2* ist in keiner Weise eingeschränkt, z. B. [movc](movc--sm4---asm-.md).

Die Semantik dieser Anweisung kann von den entsprechenden Vorgängen mit der **movc-Anweisung** beschrieben werden. Der schlechteste Fall wird im folgenden Beispiel gezeigt, indem sichergestellt wird, dass Zielregister erst am Ende aktualisiert werden.

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

Sie können auswählen, wie die Aufgabe gelöst werden soll, falls nicht direkt. Der gleiche Effekt kann z. B. durch eine Sequenz von bis zu vier einfachen bedingten Skalaraustauschvorgängen oder wie oben durch zwei **Vektor-Movc-Anweisungen** sowie jeglicher Mehraufwand erreicht werden, um sicherzustellen, dass die Quellwerte nicht durch frühere Vorgänge in der Mitte der Erweiterung vertauscht werden.

Verwenden Sie diese Anweisung zum Sortieren.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





