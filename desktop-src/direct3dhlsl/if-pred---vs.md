---
title: Wenn pred-vs
description: Start von, wenn pred-vs... Else-vs... der "eindif-vs"-Block mit der Bedingung, die vom Inhalt des Prädikats registriert wird.
ms.assetid: 03f60ca3-cda0-4653-8582-74d1a75e0aee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a1a36bb0c6c68f5132757719bbc7e37fbc71501
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313637"
---
# <a name="if-pred---vs"></a>Wenn pred-vs

Start von, wenn pred-vs... [else-vs](else---vs.md)... der " [eindif-vs"-](endif---vs.md) Block mit der Bedingung, die vom Inhalt des Prädikats registriert wird.

## <a name="syntax"></a>Syntax



| Wenn \[ ! \] pred. replialisieswizzle |
|-------------------------------|



 

Hierbei gilt:

-   \[!\] ein optionaler not-Modifizierer. Dadurch wird der Wert im Prädikat Register geändert.
-   pred ist das Prädikat Register, p0. Siehe [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   repliereswizzle ist eine einzelne Komponente, die in alle vier Komponenten kopiert (oder repliziert) wird (swizzled). Gültige Komponenten sind: x, y, z, w oder r, g, b, a.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| Wenn pred                |      |      | x    | x     | x    | x     |



 

Diese Anweisung wird verwendet, um einen Codeblock auf Grundlage eines Kanals des Prädikats zu überspringen. Jeder, wenn der \_ pred-Block mit einer Else-oder endif-Anweisung enden muss.

Es gelten folgende Beschränkungen:

, wenn \_ pred-Blöcke eingefügt werden können. Dadurch wird die gesamte dynamische Schachtelungs Tiefe zusammen mit [if \_ Comp](if-comp---vs.md) -Blöcken gezählt.

Ein if \_ -pred-Block kann einen Schleifen Block nicht durchlaufen, er muss sich entweder vollständig darin befinden oder umschließen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




