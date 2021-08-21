---
title: Hinzufügen von Palettenmeldungshandlern
description: Hinzufügen von Palettenmeldungshandlern
ms.assetid: bfd77f42-6a9d-4195-b1a0-1688e44358e3
keywords:
- DrawDib, Paletten
- DrawDibRealize-Funktion
- DrawDibDraw-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b17512025cadf0e457b596a3bfc07399db4eb9185195f4c836ee154d5ff64a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808630"
---
# <a name="adding-palette-message-handlers"></a>Hinzufügen von Palettenmeldungshandlern

Das folgende Beispiel veranschaulicht einfache Meldungshandler für die [**WM \_ PALETTECHANGED-**](/windows/desktop/gdi/wm-palettechanged) und [**WM \_ QUERYNEWPALETTE-Meldungen.**](/windows/desktop/gdi/wm-querynewpalette) Im Beispiel wird die [**DrawDibRealize-Funktion**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) verwendet, um die **WM \_ QUERYNEWPALETTE-Nachricht zu** verarbeiten.

Ihre Anwendung sollte auf die [**WM \_ QUERYNEWPALETTE-Nachricht**](/windows/desktop/gdi/wm-querynewpalette) reagieren, indem sie das Zielfenster für ungültig erklärt, damit die [**DrawDibDraw-Funktion**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) ein Bild neu zeichnen kann. Sie sollten auf die [**WM \_ PALETTECHANGED-Nachricht**](/windows/desktop/gdi/wm-palettechanged) antworten, indem Sie die [**DrawDibRealize-Funktion**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) verwenden, um die Palette zu realisieren.


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

[Verwenden von DrawDib](using-drawdib.md)
</dt> </dl>

 

 