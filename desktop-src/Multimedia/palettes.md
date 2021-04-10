---
title: Paletten
description: Paletten
ms.assetid: ee048f9a-3036-40dc-a6d7-f612b9ef767c
keywords:
- Drawdib, Paletten
- Drawdibrealize-Funktion
- Drawdibdraw-Funktion
- Drawdibsetpalette-Funktion
- Drawdibgetpalette-Funktion
- Drawdibchangepalette-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5935831d8996c424a386f86082282f9cf7c1c12
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948697"
---
# <a name="palettes"></a>Paletten

Die drawdib-Funktionen erfordern, dass eine Anwendung auf zwei palettenorientierte Nachrichten antwortet: [**WM \_ querynewpalette**](/windows/desktop/gdi/wm-querynewpalette) und [**WM \_ palettechanged**](/windows/desktop/gdi/wm-palettechanged). Wenn Ihre Anwendung nicht palettenabhängig ist, müssen Sie für jede dieser Nachrichten einen Handler hinzufügen. Weitere Informationen zum Verarbeiten der Nachrichten " **WM \_ querynewpalette** " und " **WM \_ palettechanged** " finden Sie unter [Hinzufügen von palettenmeldungs Handlern](adding-palette-message-handlers.md).

Sie können die aktuelle drawdib-Palette mithilfe der [**drawdibrealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) -Funktion auf dem Domänen Controller erkennen. Sie sollten die Palette als Reaktion auf die [**WM- \_ Abfrage "querynewpalette**](/windows/desktop/gdi/wm-querynewpalette) " oder " [**WM \_ palettechanged**](/windows/desktop/gdi/wm-palettechanged) " erkennen oder wenn Sie die Anzeige einer Bildsequenz mithilfe der [**drawdibdraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) -Funktion vorbereiten.

Mithilfe der [**drawdibsetpalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) -Funktion können Sie ein Bild zeichnen, das einer anderen Palette zugeordnet ist. Diese Funktion erzwingt, dass der drawdib-DC die angegebene Palette verwendet, was sich auf die Bildqualität auswirken kann. Beispielsweise könnte eine Anwendung, die palettenfähig ist, eine Palette realisieren und verhindern, dass drawdib eine eigene Palette erkennt. Die Anwendung kann **drawdibsetpalette** verwenden, um drawdib der zu verwendenden Palette zu benachrichtigen.

Sie können ein Handle der aktuellen Vordergrund Palette mithilfe der [**drawdibgetpalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetpalette) -Funktion abrufen. Wenn die Anwendung die aktuelle Vordergrund Palette verwendet, wird die Palette nicht exklusiv verwendet, und eine andere Anwendung kann den Palettenhandle für ungültig erklären. Die Anwendung sollte die Palette nicht freigeben, wenn Sie Sie nicht mehr verwenden. Durch das Freigeben der Palette könnte das Palettenhandle für eine andere Anwendung ungültig werden.

Sie können drawdib vorbereiten, um neue Farbwerte für die Palette mithilfe der [**drawdibchangepalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette) -Funktion zu erhalten. Im Code, der auf **drawdibchangepalette** folgt, weisen Sie neue Werte für die palettenfarbtabelle zu. Wenn das **DDF- \_ animieren** -Flag nicht auf dem drawdib-Domänen Controller festgelegt ist, wenn Sie **drawdibchangepalette** aufzurufen, können Sie die Palettenänderungen mithilfe von [**drawdibrealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) umsetzen, um die Palette zu erkennen. Sie können dann [**drawdibdraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) verwenden, um das Bild neu zu zeichnen. Wenn das **DDF- \_ animieren** -Flag im drawdib-DC festgelegt ist, können Sie die Palette und die Farben der angezeigten Bitmap mithilfe von **drawdibdraw** oder **drawdibrealize** animieren. Sie können das **DDF \_ animieren** -Flag mit den Funktionen [**drawdibend**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) und [**drawdibbegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) aktualisieren.

> [!Note]  
> Wenn Sie die drawdib-Palette freigeben, während Sie von einem DC ausgewählt wird, kann ein GDI-Fehler (Graphics Device Interface) auftreten, wenn der Domänen Controller die Palette verwendet. Stattdessen sollte die Anwendung [**drawdibsetpalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) verwenden, um den drawdib-DC so zu ändern, dass er die Standardpalette oder eine andere Palette verwendet.

 

Die [**drawdibend**](/windows/desktop/api/Vfw/nf-vfw-drawdibend)-, [**drawdibclose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose)-und [**drawdibbegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) -Funktionen können die drawdib-Palette freigeben. Diese Funktionen sollten jedoch nur verwendet werden, wenn die Palette nicht vom Domänen Controller ausgewählt wurde. Die drawdibdraw-Funktion kann die Palette auch freigeben, wenn Sie denselben drawdib-DC verwendet, aber andere Zeichen Parameter (*lpbi*, *dxdst*, *dydst*, *dxsrc* oder *dysrc*) oder ein anderes Format angibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bild Rendering](image-rendering.md)
</dt> </dl>

 

 