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
# <a name="complex-scripts"></a><span data-ttu-id="8a2f9-103">Komplexe Skripts</span><span class="sxs-lookup"><span data-stu-id="8a2f9-103">Complex Scripts</span></span>

<span data-ttu-id="8a2f9-104">Obwohl die Funktionen, die in der vorherigen erläutert werden, für viele Sprachen gut funktionieren, sind Sie möglicherweise nicht mit den Anforderungen komplexer Skripts beschäftigt.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-104">While the functions discussed in the preceding work well for many languages, they may not deal with the needs of complex scripts.</span></span> <span data-ttu-id="8a2f9-105">*Komplexe Skripts* sind Sprachen, deren gedruckte Form nicht auf einfache Weise gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-105">*Complex scripts* are languages whose printed form is not rendered in a simple way.</span></span> <span data-ttu-id="8a2f9-106">Ein komplexes Skript kann z. b. ein bidirektionales Rendering, eine kontextabhängige Strukturierung von Symbolen oder das Kombinieren von Zeichen ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-106">For example, a complex script may allow bidirectional rendering, contextual shaping of glyphs, or combining characters.</span></span> <span data-ttu-id="8a2f9-107">Aufgrund dieser speziellen Anforderungen muss das Steuerelement der Textausgabe sehr flexibel sein.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-107">Due to these special requirements, the control of text output must be very flexible.</span></span>

<span data-ttu-id="8a2f9-108">Funktionen, die Text Text [**Text**](/windows/desktop/api/Wingdi/nf-wingdi-textouta), [**exttextout**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), [**tabbedtextout**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext)und [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) anzeigen, wurden erweitert, um komplexe Skripts zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-108">Functions that display text [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta), [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext), and [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) have been extended to support complex scripts.</span></span> <span data-ttu-id="8a2f9-109">Im Allgemeinen ist diese Unterstützung für die Anwendung transparent.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-109">In general, this support is transparent to the application.</span></span> <span data-ttu-id="8a2f9-110">Allerdings sollten Anwendungen Zeichen in einem Puffer speichern und jeweils eine ganze Textzeile anzeigen, sodass die komplexen Skript Strukturierungs Module Kontext zum ordnungsgemäßen anordnen und Generieren von Symbolen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-110">However, applications should save characters in a buffer and display a whole line of text at one time, so that the complex script shaping modules can use context to reorder and generate glyphs correctly.</span></span> <span data-ttu-id="8a2f9-111">Da die Breite eines Symbols je nach Kontext variieren kann, sollten Anwendungen [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) verwenden, um die Zeilenlänge anstelle der zwischengespeicherten Zeichenbreite zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-111">In addition, because the width of a glyph can vary by context, applications should use [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) to determine line length rather than using cached character widths.</span></span>

<span data-ttu-id="8a2f9-112">Außerdem sollten komplexe Skript fähige Anwendungen in Erwägung gezogen werden, die Lesefolge von rechts nach links und die richtige Ausrichtung Ihrer Anwendungen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-112">In addition, complex script-aware applications should consider adding support for right-to-left reading order and right alignment to their applications.</span></span> <span data-ttu-id="8a2f9-113">Sie können die Lesereihenfolge oder die Ausrichtung zwischen Links und rechts mit folgendem Code umschalten:</span><span class="sxs-lookup"><span data-stu-id="8a2f9-113">You can toggle the reading order or alignment between left and right with the following code:</span></span>


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



<span data-ttu-id="8a2f9-114">Um beide Attribute gleichzeitig zu aktivieren, führen Sie die folgende Anweisung aus, und nennen Sie dann [**setTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) und [**exttextout**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), wie zuvor gezeigt:</span><span class="sxs-lookup"><span data-stu-id="8a2f9-114">To toggle both attributes at once, execute the following statement and then call [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) and [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), as shown previously:</span></span>


```C++
lAlign = TA_RIGHT^TA_RTLREADING;  //pre-inline !
```



<span data-ttu-id="8a2f9-115">Sie können auch komplexe Skripts mit unischreiber verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-115">You can also process complex scripts with Uniscribe.</span></span> <span data-ttu-id="8a2f9-116">Unischreiber ist eine Reihe von Funktionen, die ein feines Maß an Kontrolle für komplexe Skripts ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="8a2f9-116">Uniscribe is a set of functions that allow a fine degree of control for complex scripts.</span></span> <span data-ttu-id="8a2f9-117">Weitere Informationen finden Sie unter [unischreiber](../intl/uniscribe.md) und [verarbeiten komplexer Skripts](../intl/processing-complex-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="8a2f9-117">For more information, see [Uniscribe](../intl/uniscribe.md) and [Processing Complex Scripts](../intl/processing-complex-scripts.md).</span></span>

 

 
