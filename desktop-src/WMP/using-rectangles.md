---
title: Verwenden von Rechtecke (Windows Media Player SDK)
description: Verwenden von Rechtecke
ms.assetid: b3fc16b4-dc93-43c0-a97d-5234e36437c8
keywords:
- Visualisierungen, Rechtecke
- Benutzerdefinierte Visualisierungen, Rechtecke
- Visualisierungen, Renderfunktion
- Benutzerdefinierte Visualisierungen, Renderfunktion
- Renderfunktion, Rechtecke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79dd46928ccf8f8a0a465fa71fbb6b1bc1b4f48cbdb5c37b4b93ffd21c78c6b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117295"
---
# <a name="using-rectangles-windows-media-player-sdk"></a>Verwenden von Rechtecke (Windows Media Player SDK)

Rechtecke werden verwendet, um rechteckige Bereiche in Microsoft Windows anzugeben. Sie können viele Rechtecke in Ihrem Fenster erstellen, aber Windows Media Player stellt die Werte eines Rechtecks über die [IWMPEffects::Render-Funktion](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) zur Verfügung. Wenn das Plug-In mithilfe eines Fensters gerendert wird, ist das Rechteck der Clientbereich des Fensters. Dies wird als prc-Rechteck bezeichnet und definiert das Rechteck, durch das Windows Media Player Ihre Visualisierung anzeigt. Verwenden Sie dies häufig, um sicherzustellen, dass Sie nicht über die Von Windows Media Player bereitgestellten Umfang des Rechtecks hinaus zeichnen.

Ein Rechteck verfügt über vier Werte, die es definieren. Sie sind links, oben, rechts und unten. Die obere, linke Ecke des Rechtecks wird durch links und oben definiert, und die untere rechte Ecke des Rechtecks wird von unten und rechts definiert.

Verwenden Sie den folgenden Code, um die Umfang Ihres Zeichnungsrechtecks abzurufen. Dies ist erforderlich, da der Benutzer die Größe des Fensters ändern kann und Sie sicherstellen möchten, dass Sie immer in einem Bereich zeichnen, der dem Benutzer angezeigt wird.


```C++
int leftside = prc->left;
int rightside = prc->right;
int topside = prc->top;
int bottomside = prc->bottom;

```



Verwenden Sie beispielsweise Code wie den folgenden, um von links nach rechts oben im Fenster zu zeichnen:


```C++
::MoveToEx( hdc, prc->left, prc->top, NULL );  
::LineTo(hdc, prc->right, prc->top);

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von Rendern**](implementing-render.md)
</dt> </dl>

 

 




