---
title: ps_2_0
description: Erfahren Sie mehr über ps_2_0, einen programmierbaren Pixelshader, der aus einer Reihe von Anweisungen besteht, die mit Pixeldaten arbeiten.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a2433c8490af06d23d8dccef676ec206fdbb88c0
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010983"
---
# <a name="ps_2_0"></a>ps \_ 2 \_ 0

Ein programmierbarer Pixel-Shader besteht aus einer Reihe von Anweisungen, die mit Pixeldaten arbeiten. Registriert Datenübertragungen in und aus der ALU. Es kann ein zusätzliches Steuerelement angewendet werden, um die Anweisung, die Ergebnisse oder die geschriebenen Daten zu ändern.

-   [ps \_ 2 \_ 0 Anweisungen](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) enthält eine Liste der verfügbaren Anweisungen.
-   [ps \_ 2 \_ 0 Register listet](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) die verschiedenen Registertypen auf, die vom Vertex-Shader ALU verwendet werden.
-   [Modifizierer](dx9-graphics-reference-asm-ps-registers-modifiers.md) Werden verwendet, um die Funktionsweise einer Anweisung zu ändern.
-   [Zielregister-Schreibmaske](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) bestimmt, welche Komponenten des Zielregisters geschrieben werden.
-   [Die Quellregistermodifizierer des Pixelshader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) ändern die Quellregisterdaten, bevor die Anweisung ausgeführt wird.
-   [Das Quellenregister swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) bietet zusätzliche Kontrolle darüber, welche Registerkomponenten gelesen, kopiert oder geschrieben werden.

## <a name="instruction-count"></a>Anweisungsanzahl

Shader weisen Einschränkungen für die maximale Anzahl von Anweisungen auf. Anweisungsslots gesamt: 96 (64 arithmetische und 32 Textur).

## <a name="sampler-count"></a>Sampleranzahl

Die Anzahl der verfügbaren Textur-Sampler beträgt 16.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshader](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




