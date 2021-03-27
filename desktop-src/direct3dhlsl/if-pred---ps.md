---
title: Wenn pred-PS
description: Start einer if bool-PS... Else-PS... der "eindif-PS"-Block mit der Bedingung, die vom Inhalt des Prädikats registriert wird.
ms.assetid: 7b43bf71-a2e9-468f-805f-620de065db08
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ead7c5936550715d48ee1ef6a3938b6219558823
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719374"
---
# <a name="if-pred---ps"></a>Wenn pred-PS

Start einer [if bool-PS](if-bool---ps.md)... [else-PS](else---ps.md)... der " [eindif-PS"-](endif---ps.md) Block mit der Bedingung, die vom Inhalt des Prädikats registriert wird.

## <a name="syntax"></a>Syntax



| Wenn \[ ! \] pred. replialisieswizzle |
|-------------------------------|



 

Hierbei gilt:

-   \[!\] ist ein optionaler not-Modifizierer. Dadurch wird der Wert im Prädikat Register geändert.
-   pred ist das [Prädikat Register](dx9-graphics-reference-asm-ps-registers-predicate.md).
-   repliereswizzle ist eine einzelne Komponente, die in alle vier Komponenten kopiert (oder repliziert) wird (swizzled). Gültige Komponenten sind: \[ x, y, z, w \] oder \[ r, g, b, a \] .

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Wenn \_ pred              |      |      |      |      |      | x    | x     | x    | x     |



 

Diese Anweisung wird verwendet, um einen Codeblock auf Grundlage eines Kanals des Prädikats zu überspringen. Jeder, wenn der \_ pred-Block mit einer [else-PS](else---ps.md) -oder [EndIf-PS-](endif---ps.md) Anweisung enden muss.

Es gelten folgende Beschränkungen:

, wenn \_ pred-Blöcke eingefügt werden können. Dadurch wird die gesamte dynamische Schachtelungs Tiefe zusammen mit [if \_ Comp](if-comp---ps.md) -Blöcken gezählt.

Ein if \_ -pred-Block kann einen Schleifen Block nicht durchlaufen, er muss sich entweder vollständig darin befinden oder umschließen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




