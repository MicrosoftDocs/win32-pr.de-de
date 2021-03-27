---
title: ps_2_0
description: Ein programmierbarer Pixelshader besteht aus einer Reihe von Anweisungen, die auf Pixeldaten angewendet werden. Registriert Übertragungsdaten in und aus dem Alu. Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98b0f252d87a1f7e08c3531415d7ebcb93d4f6f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104975905"
---
# <a name="ps_2_0"></a>PS \_ 2 \_ 0

Ein programmierbarer Pixelshader besteht aus einer Reihe von Anweisungen, die auf Pixeldaten angewendet werden. Registriert Übertragungsdaten in und aus dem Alu. Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.

-   [die \_ Anweisungen für PS 2 \_ 0](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) enthalten eine Liste der verfügbaren Anweisungen.
-   [PS \_ 2 \_ 0-Register](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) listet die verschiedenen Register Typen auf, die von Vertex-Shader Alu verwendet werden.
-   [Modifiziererer](dx9-graphics-reference-asm-ps-registers-modifiers.md) Wird verwendet, um die Funktionsweise einer Anweisung zu ändern.
-   Die [Ziel Register-Schreib Maske](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) bestimmt, welche Komponenten des Ziel Registers geschrieben werden.
-   [Pixel-Shader-Quell Registrierungs Modifizierern](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) ändern die Quell Registrierungsdaten, bevor die Anweisung ausgeführt wird.
-   Das [Quellen Register "Schwenken](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) " bietet zusätzliche Kontrolle darüber, welche Register Komponenten gelesen, kopiert oder geschrieben werden.

## <a name="instruction-count"></a>Anweisungs Anzahl

Shader haben Beschränkungen für die maximale Anweisungs Anzahl. Anweisungs Slots gesamt: 96 (64 Arithmetik und 32 Textur).

## <a name="sampler-count"></a>Sampleranzahl

Die Anzahl der verfügbaren Textur-Samplern ist 16.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel-Shader](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




