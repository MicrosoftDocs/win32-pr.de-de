---
title: Hinzufügen von palettenmeldungs Handlern
description: Hinzufügen von palettenmeldungs Handlern
ms.assetid: bfd77f42-6a9d-4195-b1a0-1688e44358e3
keywords:
- Drawdib, Paletten
- Drawdibrealize-Funktion
- Drawdibdraw-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 679990dce5977430eb2a46fc3cd06622246d357f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390279"
---
# <a name="adding-palette-message-handlers"></a><span data-ttu-id="78cb1-106">Hinzufügen von palettenmeldungs Handlern</span><span class="sxs-lookup"><span data-stu-id="78cb1-106">Adding Palette Message Handlers</span></span>

<span data-ttu-id="78cb1-107">Das folgende Beispiel veranschaulicht einfache Nachrichten Handler für die Nachrichten " [**WM \_ palettechanged**](/windows/desktop/gdi/wm-palettechanged) " und " [**WM \_ querynewpalette**](/windows/desktop/gdi/wm-querynewpalette) ".</span><span class="sxs-lookup"><span data-stu-id="78cb1-107">The following example illustrates simple message handlers for the [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) messages.</span></span> <span data-ttu-id="78cb1-108">Im Beispiel wird die " [**drawdibrealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) "-Funktion verwendet, um die **WM- \_ querynewpalette** -Nachricht zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="78cb1-108">The example uses the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) function to process the **WM\_QUERYNEWPALETTE** message.</span></span>

<span data-ttu-id="78cb1-109">Die Anwendung sollte auf die [**WM- \_ Abfrage "querynewpalette**](/windows/desktop/gdi/wm-querynewpalette) " reagieren, indem Sie das Zielfenster ungültig machen, damit die [**drawdibdraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) -Funktion ein Bild neu zeichnet.</span><span class="sxs-lookup"><span data-stu-id="78cb1-109">Your application should respond to the [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) message by invalidating the destination window to let the [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) function redraw an image.</span></span> <span data-ttu-id="78cb1-110">Sie sollten auf die Meldung " [**WM \_ palettechanged**](/windows/desktop/gdi/wm-palettechanged) " reagieren, indem Sie die [**drawdibrealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) -Funktion verwenden, um die Palette zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="78cb1-110">You should respond to the [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) message by using the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) function to realize the palette.</span></span>


```C++
case WM_PALETTECHANGED: 
    if ((HWND)wParam == hwnd) 
        break; 
case WM_QUERYNEWPALETTE: 
    hdc = GetDC(hwnd); 
    f = DrawDibRealize(hdd, hdc, FALSE) > 0; 
    ReleaseDC(hwnd, hdc); 
    if (f) 
        InvalidateRect(hwnd, NULL, TRUE); 
    break; 

```



## <a name="related-topics"></a><span data-ttu-id="78cb1-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="78cb1-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78cb1-112">Verwenden von drawdib</span><span class="sxs-lookup"><span data-stu-id="78cb1-112">Using DrawDib</span></span>](using-drawdib.md)
</dt> </dl>

 

 