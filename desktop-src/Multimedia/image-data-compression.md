---
title: Image-Data-Komprimierung
description: Image-Data-Komprimierung
ms.assetid: 689cf403-cbb5-4ccb-a05b-0caa617430ed
keywords:
- Videokomprimierungs-Manager (VCM), Bild-Daten-Komprimierung
- VCM (Videokomprimierungs-Manager), Bild-Daten-Komprimierung
- ICCompress-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf638467e3685b24a65cd47492faed6660e77e5c49864a339a3874eb81e9b5af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038680"
---
# <a name="image-data-compression"></a>Image-Data-Komprimierung

Ihre Anwendung kann eine Reihe von [**ICCompress-Funktionen**](/windows/desktop/api/Vfw/nf-vfw-iccompress) und -Makros verwenden, um Daten zu komprimieren. Die Funktionen und Makros können Ihnen helfen, die folgenden Aufgaben auszuführen:

-   Bestimmen Sie das Komprimierungsformat, das für ein angegebenes Eingabeformat verwendet werden soll.
-   Bereiten Sie die Vorbereitung vor.
-   Komprimieren Sie die Daten.
-   Beenden sie die Komprimierung.

Ihre Anwendung kann die Kontrolle über den Komprimierungsprozess mithilfe der [**ICCompress-Funktionen**](/windows/desktop/api/Vfw/nf-vfw-iccompress) und -Makros erhöhen. Diese Gruppe von Funktionen und Makros verarbeitet einzelne Frames und nicht die Sequenz als Ganzes. Beispielsweise kann Ihre Anwendung die Frames identifizieren, die als Keyframes komprimiert werden, indem sie die **ICCompress-Funktion** verwendet.

Ein Primierer empfängt Daten in einem Format, komprimiert die Daten und gibt eine komprimierte Version der Daten in einem angegebenen Format zurück. Das typische Eingabeformat gibt DIBs mithilfe der [**BITMAPINFO-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) an. Das typische Ausgabeformat gibt komprimierte DIBs an, die auch die **BITMAPINFO-Struktur** verwenden.

> [!Note]  
> Vermeiden Sie es, eine AVI-Datei mehr als einmal zu komprimieren, um die Bild- und Audiobeeinträchtigung während der Wiedergabe zu minimieren. Kombinieren Sie unkomprimierte Videoteile in Ihrem Bearbeitungssystem, und komprimieren Sie dann das endgültige Produkt.

 

## <a name="compressor-and-compression-format-selection"></a>Auswahl des Formats "Komprimieren" und "Komprimierung"

Wenn Sie Daten komprimieren möchten und Ihre Anwendung ein bestimmtes Ausgabeformat erfordert, senden Sie die [**ICM \_ COMPRESS \_ QUERY-Nachricht**](icm-compress-query.md) (oder verwenden Sie das [**ICCompressQuery-Makro),**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) um die Zeichenfolge zu abfragen, um zu ermitteln, ob sie die Eingabe- und Ausgabeformate unterstützt.

Wenn das Ausgabeformat für Ihre Anwendung nicht wichtig ist, müssen Sie nur eine Maske finden, die das Eingabeformat verarbeiten kann. Um zu bestimmen, ob ein Zierer das Eingabeformat verarbeiten kann, können Sie ICM **\_ COMPRESS \_ QUERY** senden und **NULL** für den *lParam-Parameter* angeben. Diese Meldung gibt das Ausgabeformat nicht an Ihre Anwendung zurück. Ihre Anwendung kann die Puffergröße bestimmen, die für die Daten erforderlich ist, die das Komprimierungsformat angeben, indem sie die ICM [**\_ COMPRESS GET \_ \_ FORMAT-Nachricht**](icm-compress-get-format.md) sendet (oder das [**MAKRO ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) verwendet). Sie können die Formatdaten auch abrufen, indem Sie ICM \_ COMPRESS \_ GET FORMAT \_ (oder das [**ICCompressGetFormat-Makro)**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) senden.

Wenn Sie den größten Puffer ermitteln möchten, der für die Komprimierung erforderlich sein könnte, senden Sie die ICM [**\_ COMPRESS GET \_ \_ SIZE-Nachricht**](icm-compress-get-size.md) (oder verwenden Sie das [**ICCompressGetSize-Makro).**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) Sie können die Anzahl der von der [**ICSendMessage-Funktion zurückgegebenen**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) Bytes verwenden, um einen Puffer für nachfolgende Bildkomprimierungen zu reservieren.

## <a name="compressor-initialization"></a>Initialisierung von 1000000

Nachdem Ihre Anwendung einen Ierer ausgewählt hat, der die benötigten Eingabe- und Ausgabeformate verarbeiten kann, können Sie die Maske mithilfe der [**ICM \_ COMPRESS \_ BEGIN-Nachricht**](icm-compress-begin.md) initialisieren (oder das [**ICCompressBegin-Makro**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) verwenden). Diese Nachricht erfordert das Hand handle und die Eingabe- und Ausgabeformate.

## <a name="data-compression"></a>Datenkomprimierung

Sie können die [**ICCompress-Funktion verwenden,**](/windows/desktop/api/Vfw/nf-vfw-iccompress) um einen Frame zu komprimieren. Ihre Anwendung muss diese Funktion wiederholt verwenden, bis alle Frames in einer Sequenz komprimiert sind. Ihre Anwendung muss außerdem die Anzahl der mit ICCompress komprimierten **Frames nachverfolgen und erhöhen.** Die -Komprimierung verwendet diesen Wert, um zu überprüfen, ob Frames während der schnellen temporalen Komprimierung nicht in der Reihenfolge gesendet werden (speicherung der Unterschiede zwischen aufeinander folgenden Frames). Wenn Ihre Anwendung einen Frame erneut verwendet, sollte sie die gleiche Framenummer wie beim ersten Komprimieren des Frames verwenden. Wenn Ihre Anwendung ein Bild mit einem Stillrahmen komprimiert, kann sie eine Framenummer von 0 (null) angeben.

Ihre Anwendung kann das **ICCOMPRESS \_ KEYFRAME-Flag** verwenden, um den Frame durch [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) zu einem Keyframe zu komprimieren.

Wenn VCM die Steuerung an Ihre Anwendung zurückgibt, nachdem ein Frame komprimiert wurde, speichert VCM die komprimierten Daten in den Strukturen, auf die die *Parameter lpbiOutput* und *lpData* verweisen. Wenn Ihre Anwendung die komprimierten Daten verschieben muss, kann sie ihre Größe im *element biSizeImage* der [**BITMAPINFO-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) finden, die in *lpbiOutput angegeben ist.*

> [!Note]  
> Ihre Anwendung muss die Strukturen und Puffer zuordnen, in denen die unkomprimierten und komprimierten Daten gespeichert sind. Wenn die -Komprimierung die temporale Komprimierung unterstützt, muss Ihre Anwendung auch eine Struktur und einen Puffer zuordnen, um das Format und die Daten für den vorherigen Informationsrahmen zu speichern.

 

## <a name="ending-compression"></a>Beenden der Komprimierung

Nachdem Ihre Anwendung die Daten komprimiert hat, kann sie das [**ICCompressEnd-Makro**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) verwenden, um den Benachrichtigungs-, dass sie abgeschlossen ist. Wenn Sie die Komprimierung nach der Verwendung dieser Funktion neu starten möchten, muss Ihre Anwendung die Komprimierung erneut initialisieren, indem sie die ICM [**\_ COMPRESS \_ BEGIN-Nachricht**](icm-compress-begin.md) sendet (oder das [**ICCompressBegin-Makro**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) verwendet).

 

 