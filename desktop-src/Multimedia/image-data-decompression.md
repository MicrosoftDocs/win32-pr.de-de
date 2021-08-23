---
title: Image-Data Dekomprimierung
description: Image-Data Dekomprimierung
ms.assetid: 4bff02be-dac8-41f4-a3af-2da6a2693ffe
keywords:
- Videokomprimierungs-Manager (VCM), Bild-Daten-Dekomprimierung
- VCM (Videokomprimierungs-Manager), Bild-Daten-Dekomprimierung
- ICDecompressEx-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5006a019fd3fcf24a08f620186af8eb09d9516e103722395ed96722b48696cb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495600"
---
# <a name="image-data-decompression"></a>Image-Data Dekomprimierung

Ihre Anwendung verwendet eine Reihe von [**ICDecompressEx-Funktionen,**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) um den Dekomprimator zu steuern. Die Funktionen können Ihnen helfen, die folgenden Aufgaben auszuführen:

-   Wählen Sie einen Dekomprimator aus.
-   Bereiten Sie den Dekomprimator vor.
-   Dekomprimieren Sie die Daten.
-   Beenden Sie die Dekomprimierung.

Ihre Anwendung behandelt die Dekomprimierung ähnlich wie die Komprimierung, mit der Ausnahme, dass das Eingabeformat ein komprimiertes Format und das Ausgabeformat ein anzeigebares Format ist. Das Eingabeformat für die Dekomprimierung wird in der Regel aus dem Streamheader ermittelt. Nachdem Sie das Eingabeformat bestimmt haben, kann Ihre Anwendung die [**ICLocate-**](/windows/desktop/api/Vfw/nf-vfw-iclocate) oder [**ICOpen-Funktionen**](/windows/desktop/api/Vfw/nf-vfw-icopen) verwenden, um einen Dekomprimator zu finden, der es verarbeiten kann.

Die [**ICDecompressEx-Funktionen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) und -Makros sind eine Obermenge der [**ICDecompress-Funktionsgruppe**](/windows/desktop/api/Vfw/nf-vfw-icdecompress) und bieten weitere Funktionen. Die Funktionalität von **ICDecompressEx,** [**ICDecompressExBegin,**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin) [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend)und [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) ersetzt die Funktionen **ICDecompress**, [**ICDecompressBegin,**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend)und [**ICDecompressQuery.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) Verwenden Sie **die ICDecompressEx-Funktionen** und -Makros statt der **ICDecompress-Entsprechungen.**

## <a name="decompressor-and-decompression-format-selection"></a>Dekomprimierungsformatauswahl und Dekomprimierungsformatauswahl

Wenn Sie Daten dekomprimieren möchten und Ihre Anwendung ein bestimmtes Ausgabeformat erfordert, können Sie mithilfe der [**ICDecompressExQuery-Funktion**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) den Dekomprimator abfragen, um zu ermitteln, ob er die Eingabe- und Ausgabeformate unterstützt.

Wenn das Ausgabeformat in Ihrer Anwendung nicht wichtig ist, müssen Sie nur einen Dekomprimator finden, der das Eingabeformat verarbeiten kann. Um zu bestimmen, ob ein Dekomprimator das Eingabeformat verarbeiten kann, verwenden Sie [**ICDecompressExQuery,**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) und geben Sie **NULL** für den *lpbiDst-Parameter* an. Ihre Anwendung kann die Puffergröße bestimmen, die für die Daten erforderlich ist, die das Dekomprimierungsformat angeben, indem sie die [**ICM \_ DECOMPRESS \_ GET \_ FORMAT-Nachricht**](icm-decompress-get-format.md) sendet (oder das [**ICDecompressGetFormatSize-Makro**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) verwendet). Sie können auch ICM **\_ DECOMPRESS \_ GET \_ FORMAT** (oder das [**Makro ICDecompressGetFormat)**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) senden, um die Formatdaten abzurufen. Der Dekomprimator gibt das vorgeschlagene Format in einer [**BITMAPINFO-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) zurück. Dieses Format behält in der Regel die meisten Informationen während der Dekomprimierung bei. Ihre Anwendung sollte sicherstellen, dass der Dekomprimor erfolgreich zurückgegeben wird, bevor die Informationen dekomprimiert werden.

Da Ihre Anwendung den für die Dekomprimierung erforderlichen Arbeitsspeicher zuordnt, muss sie den maximalen Arbeitsspeicher bestimmen, den der Dekomprimierungsmodul für das Ausgabeformat benötigen kann. Die **ICM \_ DECOMPRESS \_ GET \_ FORMAT-Nachricht** erhält die Anzahl von Bytes, die der Dekomprimator für das Standardformat verwendet.

Wenn Ihre Anwendung mit [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)ein eigenes Format definiert, muss sie auch eine Palette für die Bitmap abrufen. **ICDecompressExQuery** stellt keine Palettendefinitionen zur Verfügung. (Die meisten Anwendungen verwenden Standardformate und müssen keine Palette abrufen.) Ihre Anwendung kann die Palette abrufen, indem sie die ICM [**\_ DECOMPRESS \_ GET \_ PALETTE-Nachricht**](icm-decompress-get-palette.md) sendet (oder das [**MAKRO ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) verwendet).

## <a name="decompressor-initialization"></a>Dekomprimierungsinalisierung

Nachdem Ihre Anwendung einen Dekomprimierer ausgewählt hat, der die benötigten Eingabe- und Ausgabeformate verarbeiten kann, können Sie den Dekomprimierer mithilfe der [**ICDecompressExBegin-Funktion**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin) initialisieren. Diese Funktion erfordert das Dekomprimierungshand handle sowie die Eingabe- und Ausgabeformate.

## <a name="data-decompression"></a>Datendekomprimierung

Sie können die [**ICDecompressEx-Funktion verwenden,**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) um einen Frame zu dekomprimieren. Ihre Anwendung muss diese Funktion wiederholt verwenden, bis alle Frames in einer Sequenz dekomprimiert werden.

Wenn Ihr Videodatenstrom während der Wiedergabe hinter anderen Komponenten (z. B. Audio) zurückbängt, kann Ihre Anwendung das **ICDECOMPRESS-FLAGRYUP \_** angeben, um die Dekomprimierung zu beschleunigen. Zu diesem Grund extrahiert ein Dekomprimator möglicherweise nur die Informationen, die er zum Dekomprimieren des nächsten Frames benötigt, und dekomprimiert den aktuellen Frame nicht vollständig. Daher sollte Ihre Anwendung nicht versuchen, die dekomprimierten Daten zu zeichnen, wenn sie dieses Flag verwendet.

Nachdem Ihre Anwendung die Daten dekomprimiert hat, kann sie die [**ICM \_ DECOMPRESSEX \_ END-Nachricht**](icm-decompressex-end.md) senden (oder das [**ICDecompressExEnd-Makro**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) verwenden), um den Dekomprimator zu benachrichtigen, dass er abgeschlossen ist. Wenn Sie die Dekomprimierung nach der Verwendung dieser Funktion neu starten möchten, muss Ihre Anwendung den Dekomprimator mithilfe von [**ICDecompressExBegin erneut initialisieren.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[VCM-Dienste](vcm-services.md)
</dt> </dl>

 

 