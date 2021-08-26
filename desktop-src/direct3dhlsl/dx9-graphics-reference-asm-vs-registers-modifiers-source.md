---
title: Vertex-Shader-Quellregistermodifizierer
description: Quellmodifizierer können angewendet werden, um die aus einem Quellregister gelesenen Daten zu ändern, bevor die Daten von der Anweisung verwendet werden.
ms.assetid: 516ff7ca-0071-44ac-a246-612a9faa7e7b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3f50942d32691d9dc76aa30ddcef36df390fccfe058c31af3527c0eafe0d7df0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067980"
---
# <a name="vertex-shader-source-register-modifiers"></a>Vertex-Shader-Quellregistermodifizierer

Quellmodifizierer können angewendet werden, um die aus einem Quellregister gelesenen Daten zu ändern, bevor die Daten von der Anweisung verwendet werden.

## <a name="negate"></a>Negate

Negieren Sie den Inhalt des Quellregisters.



| Komponentenmodifizierer | BESCHREIBUNG     |
|--------------------|-----------------|
| \- R               | Quell negation |



 

Der Negationmodifizierer kann nicht im zweiten Quellregister dieser Anweisungen verwendet werden: [m3x2 – vs](m3x2---vs.md), [m3x3 – vs](m3x3---vs.md), [m3x4 – vs](m3x4---vs.md), [m4x3 – vs](m4x3---vs.md), [m4x4 – vs](m4x4---vs.md).



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| \-                     | x    | x    | x    | x     | x    | x     |



 

## <a name="absolute-value"></a>Absoluter Wert

Nehmen Sie den absoluten Wert des Registers.



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| abs                    |      |      |      |       | x    | x     |



 

Wenn ein Shader der Version 3 aus einem oder mehreren konstanten float-Registern (c) liest, \# muss eines der folgenden Punkte zutreffen.

-   Alle konstanten Gleitkommaregister müssen den Abs-Modifizierer verwenden.
-   Keiner der konstanten Gleitkommaregister kann den Abs-Modifizierer verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Registermodifizierer](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




