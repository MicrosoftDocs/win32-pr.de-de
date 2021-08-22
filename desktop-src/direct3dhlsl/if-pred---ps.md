---
title: if pred - ps
description: Start eines if bool - ps... else - ps... endif – ps-Block mit der Bedingung, die aus dem Inhalt des Prädikatregisters übernommen wird.
ms.assetid: 7b43bf71-a2e9-468f-805f-620de065db08
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1a9e1c531e5dc6cd76bdd220a94730f2fb7b859eb99d9bba217a008fb02b4c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511916"
---
# <a name="if-pred---ps"></a>if pred - ps

Start eines if [bool - ps](if-bool---ps.md)... [else - ps](else---ps.md)... [endif – ps-Block](endif---ps.md) mit der Bedingung, die aus dem Inhalt des Prädikatregisters übernommen wird.

## <a name="syntax"></a>Syntax



| wenn \[ ! \] pred.replicateSwizzle |
|-------------------------------|



 

Hierbei gilt:

-   \[!\] ist ein optionaler NOT-Modifizierer. Dadurch wird der Wert im Prädikatregister verändert.
-   pred ist das [Prädikatregister.](dx9-graphics-reference-asm-ps-registers-predicate.md)
-   replicateSwizzle ist eine einzelne Komponente, die in alle vier Komponenten kopiert (oder repliziert) wird (swizzled). Gültige Komponenten sind: \[ x, y, z, w \] oder \[ r, g, b, a \] .

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| if \_ pred              |      |      |      |      |      | x    | x     | x    | x     |



 

Diese Anweisung wird verwendet, um einen Codeblock basierend auf einem Kanal des Prädikatregisters zu überspringen. Jeder if \_ pred-Block muss mit einer [else-Anweisung enden: ps](else---ps.md) oder [endif - ps.](endif---ps.md)

Es gelten folgende Beschränkungen:

, \_ wenn vordefinierte Blöcke geschachtelt werden können. Dies zählt zur gesamten dynamischen Schachtelungstiefe zusammen mit [if \_ comp-Blöcken.](if-comp---ps.md)

Ein , wenn ein pred-Block einen Schleifenblock nicht umschließen kann. Er sollte sich entweder vollständig darin oder \_ umschließen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




