---
description: Obwohl die Funktionen, die in der vorherigen erläutert werden, für viele Sprachen gut funktionieren, sind Sie möglicherweise nicht mit den Anforderungen komplexer Skripts beschäftigt.
ms.assetid: a60b50c8-13e8-4c61-989f-187bb67cf929
title: Komplexe Skripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c149aa1d9a6f5caf78fec5227f25aa30146fc273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863683"
---
# <a name="complex-scripts"></a>Komplexe Skripts

Obwohl die Funktionen, die in der vorherigen erläutert werden, für viele Sprachen gut funktionieren, sind Sie möglicherweise nicht mit den Anforderungen komplexer Skripts beschäftigt. *Komplexe Skripts* sind Sprachen, deren gedruckte Form nicht auf einfache Weise gerendert wird. Ein komplexes Skript kann z. b. ein bidirektionales Rendering, eine kontextabhängige Strukturierung von Symbolen oder das Kombinieren von Zeichen ermöglichen. Aufgrund dieser speziellen Anforderungen muss das Steuerelement der Textausgabe sehr flexibel sein.

Funktionen, die Text Text [**Text**](/windows/desktop/api/Wingdi/nf-wingdi-textouta), [**exttextout**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), [**tabbedtextout**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext)und [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) anzeigen, wurden erweitert, um komplexe Skripts zu unterstützen. Im Allgemeinen ist diese Unterstützung für die Anwendung transparent. Allerdings sollten Anwendungen Zeichen in einem Puffer speichern und jeweils eine ganze Textzeile anzeigen, sodass die komplexen Skript Strukturierungs Module Kontext zum ordnungsgemäßen anordnen und Generieren von Symbolen verwenden können. Da die Breite eines Symbols je nach Kontext variieren kann, sollten Anwendungen [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) verwenden, um die Zeilenlänge anstelle der zwischengespeicherten Zeichenbreite zu bestimmen.

Außerdem sollten komplexe Skript fähige Anwendungen in Erwägung gezogen werden, die Lesefolge von rechts nach links und die richtige Ausrichtung Ihrer Anwendungen zu unterstützen. Sie können die Lesereihenfolge oder die Ausrichtung zwischen Links und rechts mit folgendem Code umschalten:


```C++
// Save lAlign (this example uses static variables) 
static LONG lAlign = TA_LEFT;

// When user toggles alignment (assuming TA_CENTER is not supported). 

lAlign = TA_RIGHT;

// When the user toggles reading order. 

lAlign = TA_RTLREADING;

// Before calling ExtTextOut, for example, when processing WM_PAINT  

SetTextAlign (hDc, lAlign);
```



Um beide Attribute gleichzeitig zu aktivieren, führen Sie die folgende Anweisung aus, und nennen Sie dann [**setTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) und [**exttextout**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), wie zuvor gezeigt:


```C++
lAlign = TA_RIGHT^TA_RTLREADING;  //pre-inline !
```



Sie können auch komplexe Skripts mit unischreiber verarbeiten. Unischreiber ist eine Reihe von Funktionen, die ein feines Maß an Kontrolle für komplexe Skripts ermöglichen. Weitere Informationen finden Sie unter [unischreiber](../intl/uniscribe.md) und [verarbeiten komplexer Skripts](../intl/processing-complex-scripts.md).

 

 
