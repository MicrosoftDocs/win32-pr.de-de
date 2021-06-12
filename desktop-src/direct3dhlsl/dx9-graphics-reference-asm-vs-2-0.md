---
title: vs_2_0
description: Erfahren Sie vs_2_0, einem programmierbaren Vertex-Shader, der aus einer Reihe von Anweisungen besteht, die mit Scheitelpunktdaten arbeiten.
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fe951d62b869a303a0c07839b46840dc8f9fda00
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010853"
---
# <a name="vs_2_0"></a>vs \_ 2 \_ 0

Ein programmierbarer Vertex-Shader besteht aus einer Reihe von Anweisungen, die mit Scheitelpunktdaten arbeiten. Registriert Übertragungsdaten in und aus der ALU. Zusätzliche Steuerung kann angewendet werden, um die Anweisung, die Ergebnisse oder die ausgeschriebenen Daten zu ändern.

-   [Anweisungen im Vergleich \_ zu \_ 2 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) enthält eine Liste der verfügbaren Anweisungen.
-   [Register : Im Vergleich \_ zu 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) werden die verschiedenen Typen von Registern aufgeführt, die vom Vertex-Shader ALU verwendet werden.
-   [Vertex-Shader-Registermodifizierer](dx9-graphics-reference-asm-vs-registers-modifiers.md) werden verwendet, um die Art und Weise zu ändern, wie eine Anweisung funktioniert.
-   [Vertex-Shader-Quellregistermodifizierer](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) ändern die Quellregisterdaten, bevor die Anweisung ausgeführt wird.
-   [Source Register Swizzling bietet](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) zusätzliche Kontrolle darüber, welche Registerkomponenten gelesen, kopiert oder geschrieben werden.
-   [Zielregistermaskierung](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) bestimmt, welche Komponenten des Zielregisters geschrieben werden.

## <a name="instruction-count"></a>Anweisungsanzahl

Für jeden Vertex-Shader können bis zu 256 Anweisungen gespeichert sein. Die Anzahl der ausgeführten Anweisungen kann viel höher sein (aufgrund der Unterstützung von Schleifen/Wiederholungen) und ist durch D3DCAPS9 begrenzt. MaxVShaderInstructionsExecuted, die mindestens 0xFFFF.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




