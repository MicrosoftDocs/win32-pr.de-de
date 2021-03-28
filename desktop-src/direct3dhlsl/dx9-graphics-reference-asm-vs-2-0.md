---
title: vs_2_0
description: Ein programmierbarer Vertex-Shader besteht aus einer Reihe von Anweisungen, die für Scheitelpunkt Daten verwendet werden. Registriert Übertragungsdaten in und aus dem Alu. Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce4e986e610ff95716cd6899d6167e4f69efe042
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976145"
---
# <a name="vs_2_0"></a>vs \_ 2 \_ 0

Ein programmierbarer Vertex-Shader besteht aus einer Reihe von Anweisungen, die für Scheitelpunkt Daten verwendet werden. Registriert Übertragungsdaten in und aus dem Alu. Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.

-   [Anweisungen: vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) enthält eine Liste der verfügbaren Anweisungen.
-   [Register-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) listet die verschiedenen Register Typen auf, die von Vertex-Shader-Alu verwendet werden.
-   [Vertex-Shader-registermodifiziererer](dx9-graphics-reference-asm-vs-registers-modifiers.md) werden verwendet, um die Funktionsweise einer Anweisung zu ändern.
-   [Vertex-Shader-Quell Registrierungs Modifizierers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) ändern die Quell Registrierungsdaten, bevor die Anweisung ausgeführt wird.
-   Das [Quellen Register "Schwenken](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) " bietet zusätzliche Kontrolle darüber, welche Register Komponenten gelesen, kopiert oder geschrieben werden.
-   Die [Ziel Register Maskierung](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) bestimmt, welche Komponenten des Ziel Registers geschrieben werden.

## <a name="instruction-count"></a>Anweisungs Anzahl

Jeder Vertex-Shader kann bis zu 256 Anweisungen enthalten. Die Anzahl der auszuwerenden Anweisungen kann aufgrund der Unterstützung für Schleifen/Rep erheblich höher sein und wird von D3DCAPS9 begrenzt. Maxvshaderinstructionsexecuted, mindestens 0xFFFF.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




