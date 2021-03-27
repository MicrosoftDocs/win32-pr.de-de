---
title: ps_3_0 Register
description: Pixel-Shader sind von Registern abhängig, um Vertex-Daten zu erhalten, Pixeldaten auszugeben, temporäre Ergebnisse während der Berechnungen zu speichern und Textur-Samplings zu identifizieren.
ms.assetid: 01bee50a-c1b7-4b15-9df8-1dd52d9ff163
keywords:
- vpos
- Positions Register, Pixel-Shader
- Register-ps_3_0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ef4eef435857968246ab0413841ef072b5391a5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390467"
---
# <a name="ps_3_0-registers"></a>PS \_ 3 \_ 0-Register

Pixel-Shader sind von Registern abhängig, um Vertex-Daten zu erhalten, Pixeldaten auszugeben, temporäre Ergebnisse während der Berechnungen zu speichern und Textur-Samplings zu identifizieren. Es gibt mehrere Arten von Registern, von denen jede über eine eindeutige Funktionalität verfügt. Dieser Abschnitt enthält Referenzinformationen zu den Eingabe-und Ausgabe Registern, die von Pixel Shader Version 3 0 implementiert werden \_ .

## <a name="new-registers"></a>Neue Register

### <a name="input-register"></a>Eingabe Register

Die Eingabe Register (v \# ) sind nun vollständig Gleit Komma und die [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)s (t \# ) wurden in Sie konsolidiert. Die [DCL \_ -Semantik (SM3-PS ASM)](dcl-usage---ps.md) am Anfang des Shaders wird verwendet, um zu beschreiben, was in einem bestimmten Eingabe Register Container enthalten ist \_ . Eine Semantik für die Pixel Typen wird (analog zur Scheitelpunkt Seite) für dieses Modell eingeführt. Es wird keine Klammer ausgeführt, wenn die Eingabe Register als Farben (z. b. Texturkoordinaten) definiert sind. Die Auswertung der als Farbe definierten Register unterscheidet sich von den Texturkoordinaten beim Multisampling.

### <a name="face-register"></a>Gesichts Register

Das Face Register (vface) ist neu für dieses Modell. Dabei handelt es sich um ein Gleit Komma-skalarregister, das schließlich den primitiven Bereich enthalten wird. In PS \_ 3 \_ 0 ist jedoch nur das Vorzeichen dieses Registers gültig. Wenn der Wert also kleiner als 0 (null) ist (das Signier Bit ist auf negativ festgelegt), ist das primitive das hintere Gesicht (der Bereich ist negativ, gegen den Uhrzeigersinn). Daher ist es in PS \_ 3 \_ 0 nur sinnvoll, dieses Register mit 0 (> 0 oder < 0) zu vergleichen. Innerhalb des Pixel-Shaders kann die Anwendung entscheiden, welches Beleuchtungs Verfahren verwendet werden soll. Die zweiseitige Beleuchtung kann auf diese Weise erreicht werden. Dieses Register erfordert eine Deklaration, sodass die nicht deklarierte Verwendung als Fehler gekennzeichnet wird. Für Zeilen und Punkt primitive ist dieses Register nicht definiert. Das Gesichts Register kann nur als Bedingung mit den folgenden Anweisungen verwendet werden: [SETP \_ Comp-PS](setp-comp---ps.md), [if \_ Comp-](if-comp---ps.md)PS oder [break \_ -PS unterbrechen](break-comp---ps.md).

### <a name="loop-counter-register"></a>Schleifen-Counter-Register

Das [Schleifen-Counter-Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al) ist neu für dieses Modell. Sie wird bei jeder Ausführung des [Loop-PS](loop---ps.md)- / [ENDLOOP-PS-](endloop---ps.md) Blocks automatisch inkrementiert. Sie kann bei Bedarf im-Block für die relative Adressierung verwendet werden. Es ist ungültig, das Schleifen Counter-Register außerhalb der-Schleife zu verwenden.

### <a name="position-register"></a>Positions Register

Das Positions Register (vpos) ist neu für dieses Modell. Sie enthält die aktuellen Pixel (x, y) in den entsprechenden Kanälen. Die Kanäle (z, w) sind nicht definiert. Dieses Register erfordert eine Deklaration, sodass die nicht deklarierte Verwendung als Fehler gekennzeichnet wird. Wenn Sie deklariert ist, muss dieses Register genau eine der folgenden Masken aufweisen:. x,. y,. XY.

## <a name="input-register-types"></a>Eingabe Register Typen



| Register | Name                                                                                      | Anzahl | R/W | \# Leseports | \# Lese-/inst- | Dimension | Reladdr | der Arbeitszeittabelle   | Erfordert DCL |
|----------|-------------------------------------------------------------------------------------------|-------|-----|---------------|---------------|-----------|---------|------------|--------------|
| Ramelow\#      | [Eingabe Register](dx9-graphics-reference-asm-ps-registers-input-color.md)                 | 10    | R   | 1             | Unbegrenzt     | 4         | irdische      | Keine       | Ja          |
| r\#      | [Temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md)               | 32    | R/W | 3             | Unbegrenzt     | 4         | Nein      | Keine       | Nein           |
| c\#      | [Konstantes float-Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)     | 224   | R   | 1             | Unbegrenzt     | 4         | Nein      | 0000       | Nein           |
| Ich\#      | [Konstanter ganzzahliges Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md) | 16    | R   | 1             | 1             | 4         | Nein      | 0000       | Nein           |
| b\#      | [Konstantes boolesches Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md) | 16    | R   | 1             | 1             | 1         | Nein      | FALSE      | Nein           |
| P0       | [Prädikat Register](dx9-graphics-reference-asm-ps-registers-predicate.md)               | 1     | R   | 1             | 1             | 1         | Nein      | Keine       | Nein           |
| s\#      | [Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md)        | 16    | R   | 1             | 1             | 4         | Nein      | Siehe Hinweis 1 | Ja          |
| vface    | Gesichts \_ Register                                                                            | 1     | R   | 1             | Unbegrenzt     | 1         | Nein      | Keine       | Ja          |
| vpos     | Positions \_ Register                                                                        | 1     | R   | 1             | Unbegrenzt     | 4         | Nein      | Keine       | Ja          |
| irdische       | Schleifen- \_ counter- \_ Register                                                                   | 1     | R   | 1             | Unbegrenzt     | 1         | –     | Keine       | Nein           |



 

Hinweise:

-   Standardwerte für samplerlookups sind vorhanden, aber die Werte hängen vom Textur Format ab.

Die Anzahl der Schreibvorgänge ist die Anzahl der verschiedenen Register (für jeden Registrierungstyp), die in einer einzelnen Anweisung gelesen werden können.

## <a name="output-register-types"></a>Ausgabe Register Typen



| Register | Name                                                                              | Anzahl                                                                             | R/W | Dimension | Reladdr | der Arbeitszeittabelle | Erfordert DCL |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| d #     | [Ausgabe Farb Register](dx9-graphics-reference-asm-ps-registers-output-color.md) | Siehe [Texturen mit mehreren Elementen (Direct3D 9)](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | Nein      | Keine     | Nein           |
| otiefe   | [Ausgabe tiefen Register](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | Nein      | Keine     | Nein           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 