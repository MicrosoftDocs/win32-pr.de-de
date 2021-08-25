---
title: Paletten
description: Paletten
ms.assetid: ee048f9a-3036-40dc-a6d7-f612b9ef767c
keywords:
- DrawDib, Paletten
- DrawDibRealize-Funktion
- DrawDibDraw-Funktion
- DrawDibSetPalette-Funktion
- DrawDibGetPalette-Funktion
- DrawDibChangePalette-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db474a9e983c442f21fd479342ac8b0786719f36f1494e307154c6cc0a0bd50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893020"
---
# <a name="palettes"></a>Paletten

Die DrawDib-Funktionen erfordern, dass eine Anwendung auf zwei palettenorientierte Nachrichten reagiert: [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) und [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged). Wenn Ihre Anwendung nicht palettenbewusst ist, müssen Sie für jede dieser Meldungen einen Handler hinzufügen. Weitere Informationen zum Verarbeiten der **WM \_ QUERYNEWPALETTE-** und **WM \_ PALETTECHANGED-Meldungen** finden Sie unter [Adding Palette Message Handlers](adding-palette-message-handlers.md).

Sie können die aktuelle DrawDib-Palette für den DC mithilfe der [**DrawDibRealize-Funktion**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) realisieren. Sie sollten die Palette als Reaktion auf die [**WM \_ QUERYNEWPALETTE-**](/windows/desktop/gdi/wm-querynewpalette) oder [**WM \_ PALETTECHANGED-Meldung**](/windows/desktop/gdi/wm-palettechanged) oder bei der Vorbereitung der Anzeige einer Bildsequenz mithilfe der [**DrawDibDraw-Funktion**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) realisieren.

Sie können ein Bild zeichnen, das einer anderen Palette zugeordnet ist, indem Sie die [**DrawDibSetPalette-Funktion**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) verwenden. Diese Funktion zwingt den DrawDib-DC, die angegebene Palette zu verwenden, was sich auf die Bildqualität auswirken kann. Beispielsweise könnte eine Anwendung, die palettenbewusst ist, eine Palette realisiert haben und verhindern müssen, dass DrawDib seine eigene Palette realisiert. Die Anwendung kann **DrawDibSetPalette** verwenden, um DrawDib über die zu verwendende Palette zu benachrichtigen.

Sie können ein Handle der aktuellen Vordergrundpalette abrufen, indem Sie die [**DrawDibGetPalette-Funktion**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetpalette) verwenden. Wenn Ihre Anwendung die aktuelle Vordergrundpalette verwendet, wird die Palette nicht exklusiv verwendet, und eine andere Anwendung kann das Palettenhand handle ungültig machen. Ihre Anwendung sollte die Palette nicht frei geben, wenn Sie sie nicht mehr verwenden. Durch das Freihanden der Palette kann das Palettenhand handle für eine andere Anwendung ungültig werden.

Sie können DrawDib vorbereiten, um neue Farbwerte für seine Palette zu erhalten, indem Sie die [**DrawDibChangePalette-Funktion**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette) verwenden. Im Code nach **DrawDibChangePalette** weisen Sie neue Werte für die Farbtabelle der Palette zu. Wenn das **DDF \_ ANIMATE-Flag** nicht im DrawDib-DC festgelegt ist, wenn Sie **DrawDibChangePalette** aufrufen, können Sie die Palettenänderungen mit [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) vornehmen, um die Palette zu realisieren. Sie können dann [**DrawDibDraw verwenden,**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) um das Bild neu zu zeichnen. Wenn das **DDF \_ ANIMATE-Flag** im DrawDib-DC festgelegt ist, können Sie die Palette und die Farben der angezeigten Bitmap mit **DrawDibDraw** oder **DrawDibRealize animieren.** Sie können das **\_ DDF-Flag ANIMATE** mithilfe der [**Funktionen DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) und [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) aktualisieren.

> [!Note]  
> Wenn Sie die DrawDib-Palette frei geben, während sie von einem DC ausgewählt wird, kann ein GDI-Fehler (Graphics Device Interface) entstehen, wenn der DC die Palette verwendet. Stattdessen sollte Ihre Anwendung [**DrawDibSetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) verwenden, um den DrawDib-DC so zu ändern, dass die Standardpalette oder eine andere Palette verwendet wird.

 

Mit [**den Funktionen DrawDibEnd,**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose)und [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) kann die DrawDib-Palette frei werden. Diese Funktionen sollten jedoch nur verwendet werden, wenn die Palette nicht vom DC ausgewählt wurde. Die DrawDibDraw-Funktion kann die Palette auch dann frei geben, wenn sie den gleichen DrawDib-DC verwendet, aber verschiedene Zeichnungsparameter (*lpbi*, *dxDst,* *dyDst,* *dxSrc* oder *dySrc*) oder ein anderes Format angibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern von Bildern](image-rendering.md)
</dt> </dl>

 

 