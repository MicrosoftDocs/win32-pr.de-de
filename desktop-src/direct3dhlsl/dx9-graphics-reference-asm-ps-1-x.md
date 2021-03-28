---
title: ps_1_1, ps_1_2 ps_1_3, ps_1_4
description: Der Pixelshader-Assembler besteht aus einer Reihe von Anweisungen, die auf Pixeldaten in Registern angewendet werden.
ms.assetid: 51b59f98-2fa8-4280-bc36-f4328a646168
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 761721a4de64e8a9168bcfea49ce7adf567ea7ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206226"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4"></a>PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4

Der Pixelshader-Assembler besteht aus einer Reihe von Anweisungen, die auf Pixeldaten in Registern angewendet werden. Vorgänge werden als Anweisungen ausgedrückt, die aus einem Operator und einem oder mehreren Operanden bestehen. In den Anweisungen werden Register zum Übertragen von Daten in den und aus dem Pixelshader Alu verwendet. Register können auch in einigen Anweisungen verwendet werden, um temporäre Ergebnisse zu speichern.

> [!Note]  
> Die HLSL-Unterstützung für Pixel Shader 1. x ist veraltet.

 

## <a name="instructions"></a>Instructions

Es gibt zwei Hauptkategorien von pixelshaderanweisungen: arithmetische Anweisungen und Anweisungen zur Textur Adressierung. Arithmetische Anweisungen ändern von Farbdaten. Textur Adressierungs Vorgänge verarbeiten Texturkoordinaten Daten und in den meisten Fällen eine Textur. Pixelshaderanweisungen werden pro Pixel ausgeführt. Das heißt, Sie haben keine Kenntnis von anderen Pixeln in der Pipeline.

Textur Adressierungs Anweisungen verwenden jeweils einen Slot, aber arithmetische Anweisungen können kombiniert werden, um sowohl Farbkomponenten (RGB) als auch eine Alpha Komponenten Anweisung in einem einzelnen Slot zu aktivieren.

[PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4 Anweisungen](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) enthalten eine Liste der verfügbaren Anweisungen.

Wenn die multisamplinggrad-Funktion aktiviert ist, werden Pixel-Shader nur einmal pro Pixel und nicht einmal für jedes Subpixel ausgeführt. Multisampling erhöht nur die Auflösung von Polygon Rändern sowie tiefen-und Schablonen Tests. Wenn z. b. 3X3-multisamplinggrad aktiviert ist und ein Dreieck, das rasterisiert wird, fünf der neun Subpixel für ein bestimmtes Pixel abdeckt, wird der Pixelshader einmal ausgeführt, und das gleiche Farbergebnis wird auf alle fünf Subpixel angewendet.

## <a name="registers"></a>Register

[PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 Register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) listet die verschiedenen Register auf, die von Shader Alu verwendet werden.

## <a name="modifiers"></a>Modifizierer

[Modifiziererer für PS \_ 1 \_ X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) können verwendet werden, um die Funktionalität einer Anweisung oder die aus einem Register gelesenen oder geschriebenen Daten zu ändern.

Direct3D 9 erfordert Zwischenberechnungen, um mindestens eine 8-Bit-Genauigkeit für alle Oberflächen Formate beizubehalten. Es wird empfohlen, eine höhere Genauigkeit (12-Bit) für in-Stage-Mathematik und eine Sättigung von 8 Bits zwischen Textur Phasen zu erhalten. Es werden keine änderbaren Rundungs Modi oder Ausnahmen unterstützt. Multiplikation sollte mit einer Round-to-Next-Genauigkeit unterstützt werden, um den Genauigkeits Verlust minimal zu halten.

## <a name="sampler-count"></a>Sampleranzahl

Die Anzahl der verfügbaren Textur-Samplern ist:

-   Für PS \_ 1 \_ 0-PS \_ 1 \_ 3 beträgt der Höchstwert 4.
-   Für PS \_ 1 \_ 4 ist der Höchstwert 6.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel-Shader](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




