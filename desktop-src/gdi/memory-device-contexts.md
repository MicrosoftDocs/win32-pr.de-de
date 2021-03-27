---
description: Um es Anwendungen zu ermöglichen, die Ausgabe im Arbeitsspeicher zu platzieren, anstatt Sie an ein tatsächliches Gerät zu senden, verwenden Sie einen speziellen Gerätekontext für bitmapvorgänge, die als Speichergeräte Kontext bezeichnet werden.
ms.assetid: 0a682dc4-31a4-43c8-b0b1-ab01986b1dac
title: Arbeitsspeicher-Geräte Kontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095de04fdf965a87011895015ad7ea6c9782e286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754384"
---
# <a name="memory-device-contexts"></a>Arbeitsspeicher-Geräte Kontexte

Um es Anwendungen zu ermöglichen, die Ausgabe im Arbeitsspeicher zu platzieren, anstatt Sie an ein tatsächliches Gerät zu senden, verwenden Sie einen speziellen Gerätekontext für bitmapvorgänge, die als *Speichergeräte Kontext* bezeichnet werden. Ein Speicher-DC ermöglicht dem System, einen Teil des Arbeitsspeichers als virtuelles Gerät zu behandeln. Es handelt sich um ein Array von Bits im Arbeitsspeicher, das eine Anwendung vorübergehend zum Speichern der Farbdaten für Bitmaps verwenden kann, die auf einer normalen Zeichen Oberfläche erstellt werden. Da die Bitmap mit dem Gerät kompatibel ist, wird auch ein Speicher-DC auch als *kompatibler Gerätekontext* bezeichnet.

Der Speicher-DC speichert Bitmapbilder für ein bestimmtes Gerät. Eine Anwendung kann einen Speicher-DC erstellen, indem Sie die [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc) -Funktion aufrufen.

Die ursprüngliche Bitmap in einem Speicher-DC ist einfach ein Platzhalter. Die Abmessungen sind ein Pixel um ein Pixel. Bevor eine Anwendung mit dem Zeichnen beginnen kann, muss Sie durch Aufrufen der [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) -Funktion eine Bitmap mit der entsprechenden Breite und Höhe in den DC auswählen. Verwenden Sie zum Erstellen einer Bitmap mit den entsprechenden Dimensionen die Funktion " [**kreatebitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap)", " [**kreatebitmapindirekte**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)" oder " [**kreatecompatiblebitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) ". Nachdem die Bitmap im Speicher-DC ausgewählt wurde, ersetzt das System das Einzelbit-Array durch ein Array, das groß genug ist, um Farbinformationen für das angegebene Rechteck von Pixeln zu speichern.

Wenn eine Anwendung das von " [**kreatecompatibledc**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc) " zurückgegebene Handle an eine der Zeichnungsfunktionen übergibt, wird die angeforderte Ausgabe nicht auf der Zeichnungs Oberfläche des Geräts angezeigt. Stattdessen speichert das System die Farbinformationen für die resultierende Linie, Kurve, den Text oder den Bereich im Array von Bits. Die Anwendung kann das im Arbeitsspeicher gespeicherte Image zurück auf eine Zeichen Oberfläche kopieren, indem Sie die [**BitBLT**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) -Funktion aufrufen und den Speicher-DC als Quell Gerätekontext und ein Fenster oder einen Bildschirm-DC als Zielgeräte Kontext identifiziert.

Beim Anzeigen eines DIB oder einer DDB, die von einem DIB auf einem palettengerät erstellt wurde, können Sie die Geschwindigkeit, mit der das Bild gezeichnet wird, verbessern, indem Sie die logische Palette so anordnen, dass Sie dem Layout der Systempalette entspricht. Um dies zu erreichen, müssen Sie [**gettovicecaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) mit dem numreserved-Wert aufrufen, um die Anzahl der reservierten Farben im System abzurufen. Anschließend wird [**getsystempaletteentries**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteentries) aufgerufen und der erste und letzte numreserved/2-Einträge der logischen Palette mit den entsprechenden Systemfarben ausgefüllt. Wenn numreserved z. b. 20 ist, werden die ersten und letzten 10 Einträge der logischen Palette mit den Systemfarben ausgefüllt. Füllen Sie dann die restlichen 256-numreserved-Farben der logischen Palette (in unserem Beispiel die verbleibenden 236-Farben) mit den Farben aus dem DIB aus, und legen Sie das PC- \_ nocollapse-Flag für jede dieser Farben fest.

Weitere Informationen zu Farben und Paletten finden Sie unter [Farben](colors.md). Weitere Informationen zu Bitmaps und Bitmap-Vorgängen finden Sie unter [Bitmaps](bitmaps.md).

 

 



