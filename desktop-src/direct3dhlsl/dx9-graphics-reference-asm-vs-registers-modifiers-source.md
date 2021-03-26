---
title: Vertex-Shader-Quell Registrierungs Modifiers
description: Quellmodifiziererer können angewendet werden, um die aus einem Quell Register gelesenen Daten zu ändern, bevor die Daten von der Anweisung verwendet werden.
ms.assetid: 516ff7ca-0071-44ac-a246-612a9faa7e7b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c663741da50620e03cfde9f13d67a0c0063453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388519"
---
# <a name="vertex-shader-source-register-modifiers"></a>Vertex-Shader-Quell Registrierungs Modifiers

Quellmodifiziererer können angewendet werden, um die aus einem Quell Register gelesenen Daten zu ändern, bevor die Daten von der Anweisung verwendet werden.

## <a name="negate"></a>Negate

Negieren Sie den Inhalt des Quell Registers.



| Komponentenmodifizierer | BESCHREIBUNG     |
|--------------------|-----------------|
| \- r               | Quell Negation |



 

Der Negation-Modifizierer kann nicht für das zweite Quell Register dieser Anweisungen verwendet werden: [m3x2-vs](m3x2---vs.md), [M3x3-vs](m3x3---vs.md), [M3x4-vs](m3x4---vs.md), [m4x3-vs](m4x3---vs.md), [M4x4-vs](m4x4---vs.md).



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| \-                     | x    | x    | x    | x     | x    | x     |



 

## <a name="absolute-value"></a>Absoluter Wert

Nehmen Sie den absoluten Wert des Register.



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| abs                    |      |      |      |       | x    | x     |



 

Wenn ein Shader der Version 3 aus mindestens einem konstanten float-Register (c \# ) liest, muss einer der folgenden Werte zutreffen.

-   Alle Konstanten Gleit Komma Register müssen den ABS-Modifizierer verwenden.
-   Keines der Konstanten Gleit Komma Register kann den ABS-Modifizierer verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-registermodifiziererer](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




