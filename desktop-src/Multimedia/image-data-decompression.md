---
title: Image-Data-Komprimierung
description: Image-Data-Komprimierung
ms.assetid: 4bff02be-dac8-41f4-a3af-2da6a2693ffe
keywords:
- Videokomprimierungs-Manager (VCM), Abbild-Daten-Komprimierung
- VCM (Videokomprimierungs-Manager), Abbild-Datenkomprimierung
- Icdecompressex-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25614f157436056f7f24c340f6cc6f4dbc62d9ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314870"
---
# <a name="image-data-decompression"></a>Image-Data-Komprimierung

Die Anwendung verwendet eine Reihe von [**icdecompressex**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) -Funktionen, um den Dekompressor zu steuern. Mithilfe der-Funktionen können Sie die folgenden Aufgaben ausführen:

-   Wählen Sie einen Debug aus.
-   Bereiten Sie den-Debug vor.
-   Entkomprimieren Sie die Daten.
-   Beenden Sie die Komprimierung.

Die Anwendung verarbeitet die Dekomprimierung ähnlich wie die Komprimierung, mit der Ausnahme, dass das Eingabeformat ein komprimiertes Format und das Ausgabeformat ein anzeigbares Format ist. Das Eingabeformat für die Dekomprimierung wird normalerweise aus dem Datenstrom Header abgerufen. Nachdem Sie das Eingabeformat festgelegt haben, kann Ihre Anwendung die [**iclocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) -Funktion oder die [**icopen**](/windows/desktop/api/Vfw/nf-vfw-icopen) -Funktion verwenden, um einen Dekompressor zu finden, der Sie verarbeiten kann.

Die [**icdecompressex**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) -Funktionen und-Makros sind eine supermenge der [**icdecompress**](/windows/desktop/api/Vfw/nf-vfw-icdecompress) -Funktionsgruppe und stellen weitere Funktionen bereit. Die Funktionalität von **icdecompressex**, [**icdecompressexbegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin), [**icdecompressexend**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend)und [**icdecompressexquery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) ersetzt die Funktionen " **icdecompress**", " [**icdecompressbegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin)", " [**icdecompressend**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend)" und " [**icdecompressquery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) ". Verwenden Sie die **icdecompressex** -Funktionen und-Makros anstelle der **icdecompress** -Entsprechungen.

## <a name="decompressor-and-decompression-format-selection"></a>Dekompressor-und dekomprimierungsformatauswahl

Wenn Sie Daten dekomprimieren möchten und die Anwendung ein bestimmtes Ausgabeformat erfordert, können Sie die [**icdecompressexquery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) -Funktion verwenden, um den Dekompressor abzufragen und zu ermitteln, ob die Eingabe-und Ausgabeformate unterstützt werden.

Wenn das Ausgabeformat in der Anwendung nicht wichtig ist, müssen Sie nur einen Dekompressor finden, der das Eingabeformat verarbeiten kann. Um zu ermitteln, ob ein Dekompressor das Eingabeformat verarbeiten kann, verwenden Sie [**icdecompressexquery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) , und geben Sie für den *lpbidst* -Parameter **null** an. Die Anwendung kann die erforderliche Puffergröße für die Daten bestimmen, die das Dekomprimierungs Format angeben, indem die [**ICM \_ Decompress \_ get- \_ Format**](icm-decompress-get-format.md) Meldung gesendet wird (oder das [**icdecompressgetformatsize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) -Makro verwendet wird). Sie können auch **ICM \_ Decompress \_ get \_ Format** (oder das Makro [**icdecompressgetformat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) ) senden, um die Format Daten abzurufen. Der Dekompressor gibt das vorgeschlagene Format in einer [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur zurück. Dieses Format speichert in der Regel die meisten Informationen während der Dekomprimierung. Die Anwendung muss sicherstellen, dass der Dekompressor erfolgreich zurückkehrt, bevor die Informationen dekomprimiert werden.

Da Ihre Anwendung den erforderlichen Speicher für die Dekomprimierung zuordnet, muss Sie den maximalen Arbeitsspeicher bestimmen, den der Dekompressor für das Ausgabeformat benötigen kann. Die **ICM \_ Decompress \_ get- \_ Format** Meldung Ruft die Anzahl der Bytes ab, die vom Dekompressor für das Standard Format verwendet werden.

Wenn Ihre Anwendung ein eigenes Format mithilfe von [**icdecompressexquery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)definiert, muss Sie auch eine Palette für die Bitmap erhalten. **Icabcompressexquery** stellt keine palettendefinitionen bereit. (Bei den meisten Anwendungen werden Standardformate verwendet, und es muss keine Palette abgerufen werden.) Die Anwendung kann die Palette durch Senden der [**ICM \_ Decompress \_ get- \_ palettennachricht**](icm-decompress-get-palette.md) abrufen (oder verwenden Sie das [**icdecompressgetpalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) -Makro).

## <a name="decompressor-initialization"></a>Initialisierung von "Debug"

Nachdem die Anwendung einen Dekompressor ausgewählt hat, der die benötigten Eingabe-und Ausgabeformate verarbeiten kann, können Sie den Dekompressor mithilfe der [**icdecompressexbegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin) -Funktion initialisieren. Diese Funktion erfordert das Dekompressor-Handle und die Eingabe-und Ausgabeformate.

## <a name="data-decompression"></a>Datenkomprimierung

Sie können die [**icdebug**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) -Funktion verwenden, um einen Frame zu komprimieren. Die Anwendung muss diese Funktion wiederholt verwenden, bis alle Frames in einer Sequenz dekomprimiert werden.

Wenn Ihr Videostream während der Wiedergabe anderen Komponenten (z. b. Audiodaten) hinterherhinkt, kann die Anwendung das **icdecompress- \_ hurryup** -Flag angeben, um die Dekomprimierung zu beschleunigen. Zu diesem Zweck extrahiert ein Dekompressor möglicherweise nur die Informationen, die er benötigt, um den nächsten Frame zu dekomprimieren und den aktuellen Frame nicht vollständig zu dekomprimieren. Daher sollte Ihre Anwendung nicht versuchen, die entkomprimierten Daten zu zeichnen, wenn dieses Flag verwendet wird.

Nachdem die Anwendung die Daten dekomprimiert hat, kann Sie die [**ICM \_ decompressex- \_ Endnachricht**](icm-decompressex-end.md) senden (oder das Makro [**icdecompressexend**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) verwenden), um den Dekompressor zu benachrichtigen, dass der Vorgang abgeschlossen wurde. Wenn Sie die initikomprimierung nach der Verwendung dieser Funktion neu starten möchten, muss die Anwendung den Debug mithilfe von [**icdebug**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)erneut initialisieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VCM-Dienste](vcm-services.md)
</dt> </dl>

 

 