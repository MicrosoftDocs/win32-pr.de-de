---
title: Konstantes ganzzahliges Register (HLSL vs-Referenz)
description: Konstante ganzzahlige Register werden nur von Loop-vs und rep-vs verwendet.
ms.assetid: da9916d4-655b-4c98-99a4-1abfa66459b5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4cf2612eccb891ce0cffd04955e4997173e84007
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976776"
---
# <a name="constant-integer-register-hlsl-vs-reference"></a>Konstantes ganzzahliges Register (HLSL vs-Referenz)

Konstante ganzzahlige Register werden nur von [Loop-vs](loop---vs.md) und [Rep-vs](rep---vs.md)verwendet.

Sie können mithilfe von " [defi-vs](defi---vs.md) " oder " [**setvertexshaderconstanti**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)" festgelegt werden.

Bei Verwendung als Argument für die [Loop-vs-](loop---vs.md) Anweisung:

-   . x ist die Iterations Anzahl. ([Rep-vs](rep---vs.md) verwendet nur diese Komponente).
-   . y ist der Anfangswert des Schleifen Zählers.
-   . z ist der Inkrement-Schritt für den Schleifen Zählers.

Das Verhalten der shaderkonstanten wurde zwischen Direct3D 8 und Direct3D 9 geändert.

-   Bei Direct3D 9 weisen Konstanten, die mit defx festgelegt sind, dem Shader-konstantenbereich Werte zu. Die Lebensdauer einer mit defx deklarierten Konstante ist nur auf die Ausführung dieses Shaders beschränkt. Umgekehrt werden Konstanten, die mithilfe der APIs setxxxshaderconstantx festgelegt wurden, Konstanten im globalen Raum initialisieren. Konstanten im globalen Raum werden erst in den lokalen Bereich (sichtbar für den Shader) kopiert, bis setxxxshaderconstants aufgerufen wird.
-   Bei Direct3D 8 weisen Konstanten, die mit defx oder den APIs festgelegt sind, dem Shader-konstantenbereich Werte zu. Jedes Mal, wenn der Shader ausgeführt wird, werden die Konstanten vom aktuellen Shader verwendet, unabhängig von dem Verfahren, mit dem Sie festgelegt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Register](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 