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
# <a name="adding-palette-message-handlers"></a>Hinzufügen von palettenmeldungs Handlern

Das folgende Beispiel veranschaulicht einfache Nachrichten Handler für die Nachrichten " [**WM \_ palettechanged**](/windows/desktop/gdi/wm-palettechanged) " und " [**WM \_ querynewpalette**](/windows/desktop/gdi/wm-querynewpalette) ". Im Beispiel wird die " [**drawdibrealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) "-Funktion verwendet, um die **WM- \_ querynewpalette** -Nachricht zu verarbeiten.

Die Anwendung sollte auf die [**WM- \_ Abfrage "querynewpalette**](/windows/desktop/gdi/wm-querynewpalette) " reagieren, indem Sie das Zielfenster ungültig machen, damit die [**drawdibdraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) -Funktion ein Bild neu zeichnet. Sie sollten auf die Meldung " [**WM \_ palettechanged**](/windows/desktop/gdi/wm-palettechanged) " reagieren, indem Sie die [**drawdibrealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) -Funktion verwenden, um die Palette zu erkennen.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von drawdib](using-drawdib.md)
</dt> </dl>

 

 