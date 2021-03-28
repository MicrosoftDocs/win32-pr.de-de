---
title: DSY-PS
description: Berechnen Sie die Änderungs Rate in der y-Richtung des Renderziels.
ms.assetid: b35862d7-fc43-4cf8-bfe3-3eccbda2a133
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5f595d836ed8eb8525175ddb81e743cb7a04811
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389514"
---
# <a name="dsy---ps"></a>DSY-PS

Berechnen Sie die Änderungs Rate in der y-Richtung des Renderziels.

## <a name="syntax"></a>Syntax



| DSY DST, src |
|--------------|



 

Hierbei gilt:

-   DST ist ein Ziel Register.
-   src ist ein Eingabe Quellen Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| DSY                   |      |      |      |      |      | x    | x     | x    | x     |



 

Die vom Quell Register berechnete Änderungs Rate ist ein Näherungswert für den Inhalt des gleichen Registers in angrenzenden Pixeln, auf denen der Pixelshader in einem Sperr Schritt mit dem aktuellen Pixel ausgeführt wird.

Die Anweisungen [DSX](dsx---ps.md) und DSY berechnen das Ergebnis, indem Sie sich den aktuellen Inhalt des Quell Registers (pro Komponente) für die verschiedenen Pixel im lokalen Bereich ansehen, der im Sperr Schritt ausgeführt wird. Die exakte Formel für die Berechnung des Farbverlaufs variiert abhängig von der Hardware, sollte jedoch mit der Art und Weise konsistent sein, wie die Hardware die gleichen Vorgänge im Rahmen der Detail Berechnung durchführt, um die Textur Stichproben zu verarbeiten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[texldd-PS](texldd---ps.md)
</dt> </dl>

 

 




