---
title: Integerregister für Konstante (HLSL-PS-Referenz)
description: Konstanten ganzzahlige Register werden nur von der -Schleife verwendet – ps und rep – ps.
ms.assetid: 85720ec0-b6aa-4a24-910c-3ad0468300dc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce2d9ba19f97439da098563639bc8940cdae2f202a6f24cdd1940e25cfc14e9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489381"
---
# <a name="constant-integer-register-hlsl-ps-reference"></a>Integerregister für Konstante (HLSL-PS-Referenz)

Ganzzahlige Konstantenregister werden nur von [der -Schleife](loop---ps.md) verwendet : ps und [rep - ps](rep---ps.md).

Sie können [mithilfe](defi---ps.md) von defi - ps oder [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)festgelegt werden.

Bei Verwendung als Argument für die [-Schleife – ps-Anweisung:](loop---ps.md)

-   .x ist die Iterationsanzahl. ([rep – ps](rep---ps.md) verwendet nur diese Komponente).
-   .y ist der Anfangswert für den Schleifenzähler.
-   .z ist der Schritt inkrementieren für den Schleifenzähler.



| Pixelshaderversionen     | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| Constant Integer Register |      |      |      |      |      |       | x    | x    | x     |



 

Das Verhalten von Shaderkonstanten hat sich zwischen Direct3D 8 und Direct3D 9 geändert.

-   Für Direct3D 9 weisen konstanten Konstanten, die mit defx festgelegt sind, Werte dem Konstantenbereich des Shaders zu. Die Lebensdauer einer Konstanten, die mit defx deklariert wurde, ist auf die Ausführung dieses Shaders beschränkt. Umgekehrt initialisieren Konstanten, die mithilfe der APIs SetXXXShaderConstantX festgelegt werden, Konstanten im globalen Raum. Konstanten im globalen Raum werden erst in den lokalen Bereich kopiert (für den Shader sichtbar), wenn SetxxxShaderConstants aufgerufen wird.
-   Für Direct3D 8 weisen konstanten Konstanten, die mit defx oder den APIs festgelegt wurden, dem Konstantenbereich des Shaders Werte zu. Jedes Mal, wenn der Shader ausgeführt wird, werden die Konstanten vom aktuellen Shader verwendet, unabhängig von der Technik, mit der sie festgelegt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 