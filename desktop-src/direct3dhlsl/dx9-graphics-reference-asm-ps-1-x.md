---
title: ps_1_1, ps_1_2, ps_1_3, ps_1_4
description: Der Pixel-Shader-Assembler besteht aus einer Reihe von Anweisungen, die mit Pixeldaten arbeiten, die in Registern enthalten sind.
ms.assetid: 51b59f98-2fa8-4280-bc36-f4328a646168
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3e10e4eee48490e7ae998e39d71265aef74339c1979112e2fcf0e47e5b07cda7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512941"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4"></a>ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ 1 \_ 3, ps \_ 1 \_ 4

Der Pixel-Shader-Assembler besteht aus einer Reihe von Anweisungen, die mit Pixeldaten arbeiten, die in Registern enthalten sind. Vorgänge werden als Anweisungen ausgedrückt, die aus einem Operator und mindestens einem Operanden bestehen. Anweisungen verwenden Register, um Daten in und aus der Pixel-Shader-ALU zu übertragen. Register können auch von einigen Anweisungen verwendet werden, um temporäre Ergebnisse zu enthalten.

> [!Note]  
> HLSL-Unterstützung für Pixel-Shader 1.x ist veraltet.

 

## <a name="instructions"></a>Anweisungen

Es gibt zwei Hauptkategorien von Anweisungen für Pixel-Shader: arithmetische Anweisungen und Anweisungen zur Textur adressierung. Arithmetische Anweisungen ändern Farbdaten. Textur adressierungsvorgänge verarbeiten Texturkoordinatendaten und in den meisten Fällen Stichproben einer Textur. Anweisungen für Den Pixel-Shader werden auf Pixelbasis ausgeführt. Das heißt, sie haben keine Kenntnis von anderen Pixeln in der Pipeline.

Textur-Adressierungsanweisungen verbrauchen jeweils einen Slot, aber arithmetische Anweisungen können gekoppelt werden, um sowohl Farbkomponenten (RGB) als auch eine Alphakomponentenanweisung in einem einzelnen Slot zu aktivieren.

[ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ 1 \_ 3, ps \_ 1 \_ 4 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) enthält eine Liste der verfügbaren Anweisungen.

Wenn Multisampling aktiviert ist, werden Pixel-Shader nur einmal pro Pixel ausgeführt, nicht einmal für jedes Subpixel. Multisampling erhöht nur die Auflösung von Polygonrändern sowie Tiefen- und Schablonentests. Wenn z. B. 3x3 Multisampling aktiviert ist und ein rasterfähiges Dreieck fünf der neun Subpixel für ein bestimmtes Pixel abdecken kann, wird der Pixelschattenr einmal ausgeführt, und das gleiche Farbergebnis wird auf alle fünf Subpixel angewendet.

## <a name="registers"></a>Register

[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Register listet](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) die verschiedenen Register auf, die vom Shader ALU verwendet werden.

## <a name="modifiers"></a>Modifizierer

[Modifizierer für ps \_ 1 \_ X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) können verwendet werden, um die Funktionalität einer Anweisung oder die aus einem Register gelesenen oder in ein Register geschriebenen Daten zu ändern.

Direct3D 9 erfordert Zwischenberechnungen, um für alle Oberflächenformate eine Genauigkeit von mindestens 8 Bit zu erhalten. Sowohl eine höhere Genauigkeit (12-Bit) für die In-Stage-Mathematik als auch eine Sättigung von 8 Bits zwischen Texturstufen werden empfohlen. Änderbare Rundungsmodi oder Ausnahmen werden nicht unterstützt. Multiplikation sollte mit einer Genauigkeit von Rund-zu-Nächste unterstützt werden, um den Genauigkeitsverlust auf ein Minimum zu beschränken.

## <a name="sampler-count"></a>Sampleranzahl

Die Anzahl der verfügbaren Texturs sampler ist:

-   Für ps \_ 1 \_ 0 - ps \_ 1 \_ 3 beträgt der Höchstwert 4.
-   Für ps \_ 1 \_ 4 beträgt der Höchstwert 6.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel-Shader](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




