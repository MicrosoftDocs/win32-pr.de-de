---
title: ps_3_0 Register
description: Dieser Artikel enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von der Pixelshaderversion 3_0 implementiert werden.
ms.assetid: 01bee50a-c1b7-4b15-9df8-1dd52d9ff163
keywords:
- vPos
- Positionsregister, Pixelshader
- Register – ps_3_0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e1cd0173beabc8fbe21ad15e88e23fc1b6e84892
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405493"
---
# <a name="ps_3_0-registers"></a>ps \_ 3 \_ 0 Register

Pixel-Shader sind von Registern abhängig, um Scheitelpunktdaten abzurufen, Pixeldaten auszugeben, temporäre Ergebnisse bei Berechnungen zu speichern und Textursamplingstufen zu identifizieren. Es gibt mehrere Arten von Registern, die jeweils eine eindeutige Funktionalität aufweisen. Dieser Abschnitt enthält Referenzinformationen zu den Eingabe- und Ausgaberegistern, die von Version 3 0 des Pixelshader implementiert \_ werden.

## <a name="new-registers"></a>Neue Register

### <a name="input-register"></a>Eingaberegister

Die Eingaberegister (v \# ) sind jetzt vollständig gleitkomma, und die [Texturkoordinatenregister](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)(t \# ) wurden darin konsolidiert. Die [ \_ dcl-Semantik (sm3 - ps asm)](dcl-usage---ps.md) am oberen Rand des Shaders wird verwendet, um zu beschreiben, was in einem bestimmten Eingaberegister enthalten \_ ist. Für dieses Modell wird eine Semantik für die Pixeltypen eingeführt (analog zur Scheitelpunktseite). Es wird keine Klammer ausgeführt, wenn die Eingaberegister als Farben (z. B. Texturkoordinaten) definiert sind. Die Auswertung der als Farbe definierten Register unterscheidet sich von den Texturkoordinaten beim Multisampling.

### <a name="face-register"></a>Gesichtsregister

Das Gesichtsregister (vFace) ist für dieses Modell neu. Dies ist ein Gleitkomma-Skalarregister, das schließlich den primitiven Bereich enthält. In PS \_ 3 \_ 0 ist jedoch nur das Vorzeichen dieses Registers gültig. Wenn der Wert also kleiner als 0 (das Vorzeichenbit ist negativ festgelegt) ist, ist der Primitive die Rückwand (der Bereich ist negativ, gegen den Uhrzeigersinn). Daher ist es in PS \_ 3 \_ 0 nur sinnvoll, dieses Register mit 0 (> 0 oder < 0) zu vergleichen. Innerhalb des Pixelshader kann die Anwendung entscheiden, welche Beleuchtungstechnik verwendet werden soll. Auf diese Weise kann eine zweiseitige Beleuchtung erreicht werden. Dieses Register erfordert eine Deklaration, sodass nicht deklarierte Nutzung als Fehler gekennzeichnet wird. Für Linien und Punktprimitive ist dieses Register nicht definiert. Das Gesichtsregister kann nur als Bedingung mit den folgenden Anweisungen verwendet werden: [setp \_ comp - ps](setp-comp---ps.md), wenn comp - [ \_ ps](if-comp---ps.md), oder [break comp - \_ ps](break-comp---ps.md).

### <a name="loop-counter-register"></a>Schleifenzählerregister

Das [Schleifenzählerregister (Loop Counter Register,](dx9-graphics-reference-asm-ps-registers-loop-counter.md) aL) ist für dieses Modell neu. Bei jeder Ausführung der [Schleife](loop---ps.md)– ps / [endloop](endloop---ps.md) – ps block – wird sie automatisch erhöht. Sie kann im -Block bei Bedarf für die relative Adressierung verwendet werden. Es ist ungültig, das Schleifenzählerregister außerhalb der Schleife zu verwenden.

### <a name="position-register"></a>Positionsregister

Das Positionsregister (vPos) ist für dieses Modell neu. Sie enthält die aktuellen Pixel (x, y) in den entsprechenden Kanälen. Die Kanäle (z, w) sind nicht definiert. Dieses Register erfordert eine Deklaration, sodass nicht deklarierte Nutzung als Fehler gekennzeichnet wird. Wenn dieses Register deklariert wird, muss es genau eine der folgenden Masken aufweisen: .x, .y, .xy.

## <a name="input-register-types"></a>Eingaberegistertypen



| Registrieren | Name                                                                                      | Anzahl | R/W | \# Leseports | \# Lese-/Inst-Lesefunktionen | Dimension | RelAddr | Standardeinstellungen   | Erfordert DCL |
|----------|-------------------------------------------------------------------------------------------|-------|-----|---------------|---------------|-----------|---------|------------|--------------|
| V\#      | [Eingaberegister](dx9-graphics-reference-asm-ps-registers-input-color.md)                 | 10    | R   | 1             | Unbegrenzt     | 4         | Al      | Keine       | Ja          |
| R\#      | [Temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md)               | 32    | R/W | 3             | Unbegrenzt     | 4         | Nein      | Keine       | Nein           |
| c\#      | [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)     | 224   | R   | 1             | Unbegrenzt     | 4         | Nein      | 0000       | Nein           |
| Ich\#      | [Constant Integer Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md) | 16    | R   | 1             | 1             | 4         | Nein      | 0000       | Nein           |
| b\#      | [Constant Boolean Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md) | 16    | R   | 1             | 1             | 1         | Nein      | FALSE      | Nein           |
| p0       | [Prädikatregister](dx9-graphics-reference-asm-ps-registers-predicate.md)               | 1     | R   | 1             | 1             | 1         | Nein      | Keine       | Nein           |
| s\#      | [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md)        | 16    | R   | 1             | 1             | 4         | Nein      | Siehe Hinweis 1 | Ja          |
| vFace    | \_Gesichtsregister                                                                            | 1     | R   | 1             | Unbegrenzt     | 1         | Nein      | Keine       | Ja          |
| vPos     | \_Positionsregister                                                                        | 1     | R   | 1             | Unbegrenzt     | 4         | Nein      | Keine       | Ja          |
| Al       | \_ \_ Schleifenzählerregister                                                                   | 1     | R   | 1             | Unbegrenzt     | 1         | –     | Keine       | Nein           |



 

Hinweise:

-   Es sind Standardwerte für Samplersuchen vorhanden, die Werte hängen jedoch vom Texturformat ab.

Die Anzahl der Readports ist die Anzahl verschiedener Register (für jeden Registertyp), die in einer einzelnen Anweisung gelesen werden können.

## <a name="output-register-types"></a>Ausgaberegistertypen



| Registrieren | Name                                                                              | Anzahl                                                                             | R/W | Dimension | RelAddr | Standardeinstellungen | Erfordert DCL |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| Oc #     | [Ausgabefarbregister](dx9-graphics-reference-asm-ps-registers-output-color.md) | Weitere [Informationen finden Sie unter Texturen mit mehreren Element (Direct3D 9).](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | Nein      | Keine     | Nein           |
| oDepth   | [Ausgabetiefenregister](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | Nein      | Keine     | Nein           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 