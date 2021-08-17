---
title: if pred – vs
description: Start eines , wenn pred – vs... else – vs... endif – vs block, wobei die Bedingung aus dem Inhalt des Prädikatregisters übernommen wird.
ms.assetid: 03f60ca3-cda0-4653-8582-74d1a75e0aee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad9aba5c9f18b88577a456764a71cc27637d24856cdafa95d811344034d514f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511906"
---
# <a name="if-pred---vs"></a>if pred – vs

Start eines , wenn pred – vs... [else – vs](else---vs.md)... [endif – vs](endif---vs.md) block, wobei die Bedingung aus dem Inhalt des Prädikatregisters übernommen wird.

## <a name="syntax"></a>Syntax



| , wenn \[ ! \] pred.replicateSwizzle |
|-------------------------------|



 

Hierbei gilt:

-   \[!\] ein optionaler NOT-Modifizierer. Dadurch wird der Wert im Prädikatregister geändert.
-   pred ist das Prädikatregister p0. Weitere Informationen finden Sie unter [Prädikatregister.](dx9-graphics-reference-asm-vs-registers-predicate.md)
-   replicateSwizzle ist eine einzelne Komponente, die auf alle vier Komponenten kopiert (oder repliziert) wird (swizzled). Gültige Komponenten sind: x, y, z, w oder r, g, b, a.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| , wenn der Prädiert ist                |      |      | x    | x     | x    | x     |



 

Diese Anweisung wird verwendet, um einen Codeblock basierend auf einem Kanal des Prädikatregisters zu überspringen. Jeder \_ vorangestellte Block muss mit einer else- oder endif-Anweisung enden.

Es gelten folgende Beschränkungen:

, wenn \_ vordefinierte Blöcke geschachtelt werden können. Dies zählt zusammen mit if [comp-Blöcken \_ ](if-comp---vs.md) zur gesamt dynamischen Schachtelungstiefe.

Wenn \_ ein vorangestellter Block einen Schleifenblock nicht umschließen kann, sollte er sich entweder vollständig darin befinden oder ihn umschließen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




