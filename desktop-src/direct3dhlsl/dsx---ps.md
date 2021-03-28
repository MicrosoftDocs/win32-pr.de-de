---
title: DSX-PS
description: Berechnen Sie die Änderungs Rate in der x-Richtung des Renderziels.
ms.assetid: 3358ddca-97a3-421d-8e5d-6b425903e683
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 701dbe0125d10850760e6a1f08a2f84a50c55fe2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103948327"
---
# <a name="dsx---ps"></a>DSX-PS

Berechnen Sie die Änderungs Rate in der x-Richtung des Renderziels.

## <a name="syntax"></a>Syntax



| DSX DST, src |
|--------------|



 

Hierbei gilt:

-   DST ist ein Ziel Register.
-   src ist ein Eingabe Quellen Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| DSX                   |      |      |      |      |      | x    | x     | x    | x     |



 

Die vom Quell Register berechnete Änderungs Rate ist ein Näherungswert für den Inhalt des gleichen Registers in angrenzenden Pixeln, auf denen der Pixelshader in einem Sperr Schritt mit dem aktuellen Pixel ausgeführt wird.

Die Anweisungen DSX und [DSY](dsy---ps.md) berechnen das Ergebnis, indem Sie sich den aktuellen Inhalt des Quell Registers (pro Komponente) für die verschiedenen Pixel im lokalen Bereich ansehen, der im Sperr Schritt ausgeführt wird. Die exakte Formel für die Berechnung des Farbverlaufs variiert abhängig von der Hardware, sollte jedoch mit der Art und Weise konsistent sein, wie die Hardware die gleichen Vorgänge im Rahmen der Detail Berechnung durchführt, um die Textur Stichproben zu verarbeiten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[texldd-PS](texldd---ps.md)
</dt> </dl>

 

 




