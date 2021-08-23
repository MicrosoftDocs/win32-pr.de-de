---
description: Damit Anwendungen die Ausgabe im Arbeitsspeicher platzieren können, anstatt sie an ein tatsächliches Gerät zu senden, verwenden Sie einen speziellen Gerätekontext für Bitmapvorgänge, die als Speichergerätekontext bezeichnet werden.
ms.assetid: 0a682dc4-31a4-43c8-b0b1-ab01986b1dac
title: Speichergerätekontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63469823e38eb98da5d43ede006e6b1e64af874d300127db6cd4cc7743672d29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118760058"
---
# <a name="memory-device-contexts"></a>Speichergerätekontexte

Damit Anwendungen die Ausgabe im Arbeitsspeicher platzieren können, anstatt sie an ein tatsächliches Gerät zu senden, verwenden Sie einen speziellen Gerätekontext für Bitmapvorgänge, die als Speichergerätekontext *bezeichnet werden.* Ein Speicherdomänencontroller ermöglicht es dem System, einen Teil des Arbeitsspeichers als virtuelles Gerät zu behandeln. Es handelt sich um ein Array von Bits im Arbeitsspeicher, die eine Anwendung vorübergehend verwenden kann, um die Farbdaten für Bitmaps zu speichern, die auf einer normalen Zeichenoberfläche erstellt wurden. Da die Bitmap mit dem Gerät kompatibel ist, wird ein Speicherdomänencontroller manchmal auch als *kompatibler Gerätekontext bezeichnet.*

Der Arbeitsspeicher-DC speichert Bitmapbilder für ein bestimmtes Gerät. Eine Anwendung kann einen Speicherdomänencontroller erstellen, indem sie die [**CreateCompatibleDC-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc) aufruft.

Die ursprüngliche Bitmap in einem Speicherdomänencontroller ist einfach ein Platzhalter. Die Abmessungen sind ein Pixel nach einem Pixel. Bevor eine Anwendung mit dem Zeichnen beginnen kann, muss sie eine Bitmap mit der entsprechenden Breite und Höhe im DC auswählen, indem die [**SelectObject-Funktion aufruft.**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) Um eine Bitmap der entsprechenden Dimensionen zu erstellen, verwenden Sie die [**Funktion CreateBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)oder [**CreateCompatibleBitmap.**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) Nachdem die Bitmap im Arbeitsspeicher-DC ausgewählt wurde, ersetzt das System das Ein-Bit-Array durch ein Array, das groß genug ist, um Farbinformationen für das angegebene Pixelrechteck zu speichern.

Wenn eine Anwendung das von [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc) zurückgegebene Handle an eine der Zeichnungsfunktionen übergibt, wird die angeforderte Ausgabe nicht auf der Zeichenoberfläche eines Geräts angezeigt. Stattdessen speichert das System die Farbinformationen für die resultierende Linie, Kurve, Text oder Region im Array von Bits. Die Anwendung kann das im Arbeitsspeicher gespeicherte Bild wieder auf eine Zeichenoberfläche kopieren, indem sie die [**BitBlt-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) aufruft und den Speicher-DC als Quellgerätekontext und einen Fenster- oder Bildschirm-DC als Zielgerätekontext identifiziert.

Beim Anzeigen eines DIB oder einer DDB, die aus einem DIB auf einem Palettengerät erstellt wurde, können Sie die Geschwindigkeit, mit der das Bild gezeichnet wird, verbessern, indem Sie die logische Palette so anordnen, dass sie dem Layout der Systempalette passt. Rufen Sie hierzu [**GetDeviceCaps mit**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) dem NUMRESERVED-Wert auf, um die Anzahl der reservierten Farben im System zu erhalten. Rufen Sie dann [**GetSystemPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteentries) auf, und füllen Sie die ersten und letzten NUMRESERVED/2-Einträge der logischen Palette mit den entsprechenden Systemfarben aus. Wenn NUMRESERVED beispielsweise 20 ist, füllen Sie die ersten und letzten 10 Einträge der logischen Palette mit den Systemfarben aus. Füllen Sie dann die verbleibenden 256 NUMRESERVED-Farben der logischen Palette (in unserem Beispiel die verbleibenden 236 Farben) mit Farben aus dem DIB aus, und legen Sie das PC NOCOLLAPSE-Flag für jede dieser Farben \_ fest.

Weitere Informationen zu Farben und Paletten finden Sie unter [Farben](colors.md). Weitere Informationen zu Bitmaps und Bitmapvorgängen finden Sie unter [Bitmaps](bitmaps.md).

 

 



