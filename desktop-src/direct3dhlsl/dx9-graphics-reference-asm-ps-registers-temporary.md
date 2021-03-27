---
title: Temporäres Register (HLSL PS-Referenz)
description: Temporäre Register der Pixel-Shader-Eingabe werden verwendet, um Zwischenergebnisse zu speichern.
ms.assetid: e61daaa1-0a9b-4b1c-b91c-56573be59ed9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7aebee99a693ac629d9cc8a372fba7589a9e29ef
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "103857831"
---
# <a name="temporary-register-hlsl-ps-reference"></a>Temporäres Register (HLSL PS-Referenz)

Temporäre Register der Pixel-Shader-Eingabe werden verwendet, um Zwischenergebnisse zu speichern.

Syntax


```
no declaration is required
```





| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Temporäres Register    |      |      |      |      | x    | x     | x    | x    | x     |



 

-   Es gibt 12 Pixel-Shader-temporäre Register: R0 bis R11.
-   Diese Register werden zum Speichern von Zwischenergebnissen während Berechnungen verwendet.
-   Wenn für ein temporäres Register Komponenten verwendet werden, die nicht im vorherigen Code definiert sind, tritt bei der shadervalidierung ein Fehler auf.
-   Dabei handelt es sich um mindestens eine Gleit Komma Genauigkeit.
-   In einer einzelnen Anweisung können maximal drei verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




