---
title: Verwenden von Rechtecke (Windows Media Player SDK)
description: Verwenden von Rechtecke
ms.assetid: b3fc16b4-dc93-43c0-a97d-5234e36437c8
keywords:
- Visualisierungen, Rechtecke
- benutzerdefinierte Visualisierungen, Rechtecke
- Visualisierungen, Rendering-Funktion
- benutzerdefinierte Visualisierungen, Rendering-Funktion
- Rendering-Funktion, Rechtecke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b48f16888d8e71c052d216a838683f2b7127e75
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106338705"
---
# <a name="using-rectangles-windows-media-player-sdk"></a>Verwenden von Rechtecke (Windows Media Player SDK)

Rechtecke werden verwendet, um rechteckige Bereiche in Microsoft Windows anzugeben. Sie können in Ihrem Fenster viele Rechtecke erstellen, aber Windows Media Player die Werte eines Rechtecks über die [iwmpeffects:: Rendering](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) -Funktion bereitstellt. Wenn das Plug-in mithilfe eines Fensters gerendert wird, ist das Rechteck der Client Bereich des Fensters. Dies wird als PRC-Rechteck bezeichnet und definiert das Rechteck, mit dem die Visualisierung in Windows Media Player angezeigt wird. Verwenden Sie dies häufig, um sicherzustellen, dass Sie nicht über die Blöcke der von Windows Media Player bereitgestellten Rechteck hinaus zeichnen.

Ein Rechteck hat vier Werte, die es definieren. Sie sind Links, oben, rechts und unten. Die obere linke Ecke des Rechtecks wird von Links und oben definiert, und die untere rechte Ecke des Rechtecks wird von unten und rechts definiert.

Verwenden Sie den folgenden Code, um die Blöcke des Zeichnungs Rechtecks zu erhalten. Dies ist erforderlich, da der Benutzer die Größe des Fensters ändern kann, und Sie möchten sicher sein, dass Sie immer in einem Bereich zeichnen, den der Benutzer sehen kann.


```C++
int leftside = prc->left;
int rightside = prc->right;
int topside = prc->top;
int bottomside = prc->bottom;

```



Wenn Sie z. b. von links nach rechts am oberen Rand des Fensters zeichnen möchten, verwenden Sie Code wie den folgenden:


```C++
::MoveToEx( hdc, prc->left, prc->top, NULL );  
::LineTo(hdc, prc->right, prc->top);

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von Rendering**](implementing-render.md)
</dt> </dl>

 

 




