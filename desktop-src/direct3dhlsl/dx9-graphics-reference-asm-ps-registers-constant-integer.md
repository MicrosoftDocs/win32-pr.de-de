---
title: Konstantes ganzzahliges Register (HLSL PS-Referenz)
description: Konstante ganzzahlige Register werden nur von Loop-PS und rep-PS verwendet.
ms.assetid: 85720ec0-b6aa-4a24-910c-3ad0468300dc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b03a27a95f84ae30a70147caaf5662e1949cf18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976753"
---
# <a name="constant-integer-register-hlsl-ps-reference"></a>Konstantes ganzzahliges Register (HLSL PS-Referenz)

Konstante ganzzahlige Register werden nur von [Loop-PS](loop---ps.md) und [Rep-PS](rep---ps.md)verwendet.

Sie können mithilfe von " [defi-PS](defi---ps.md) " oder " [**setpixelshaderconstanti**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)" festgelegt werden.

Bei Verwendung als Argument für die [Loop-PS-](loop---ps.md) Anweisung:

-   . x ist die Iterations Anzahl. ([Rep-PS](rep---ps.md) verwendet nur diese Komponente).
-   . y ist der Anfangswert des Schleifen Zählers.
-   . z ist der Inkrement-Schritt für den Schleifen Zählers.



| Pixel-Shader-Versionen     | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| Konstanter ganzzahliges Register |      |      |      |      |      |       | x    | x    | x     |



 

Das Verhalten der shaderkonstanten wurde zwischen Direct3D 8 und Direct3D 9 geändert.

-   Bei Direct3D 9 weisen Konstanten, die mit defx festgelegt sind, dem Shader-konstantenbereich Werte zu. Die Lebensdauer einer mit defx deklarierten Konstante ist nur auf die Ausführung dieses Shaders beschränkt. Umgekehrt werden Konstanten, die mithilfe der APIs setxxxshaderconstantx festgelegt wurden, Konstanten im globalen Raum initialisieren. Konstanten im globalen Raum werden erst in den lokalen Bereich (sichtbar für den Shader) kopiert, bis setxxxshaderconstants aufgerufen wird.
-   Bei Direct3D 8 weisen Konstanten, die mit defx oder den APIs festgelegt sind, dem Shader-konstantenbereich Werte zu. Jedes Mal, wenn der Shader ausgeführt wird, werden die Konstanten vom aktuellen Shader verwendet, unabhängig von dem Verfahren, mit dem Sie festgelegt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 