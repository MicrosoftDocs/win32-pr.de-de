---
title: Lesen aus einem Stream
description: Lesen aus einem Stream
ms.assetid: be961f06-cf5f-4093-9b31-7d1d69e62fec
keywords:
- AVISTREAMINFO-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cc7ecd606a33503557e7c7209bff68015756523
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948738"
---
# <a name="reading-from-a-stream"></a>Lesen aus einem Stream

Mithilfe der [**AVISTREAMINFO**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) -Funktion können Sie Informationen zu einem geöffneten Stream abrufen. Diese Funktion füllt die [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) -Struktur mit Informationen wie z. b. dem Datentyp im Datenstrom, der Komprimierungs Methode, die beim Schreiben von Streamdaten verwendet wird, der vorgeschlagenen Puffergröße, der Wiedergabe Rate und einer Textbeschreibung des Streams.

Einige Member der [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) -Struktur sind auch in der [**avifileinfo**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) -Struktur vorhanden. Die Informationen in der **avifileinfo** -Struktur gelten für die gesamte Datei. Die Informationen in der **AVISTREAMINFO** -Struktur sind spezifisch für den Datenstrom, auf den zugegriffen wird, und haben Vorrang vor den Informationen in der **avifileinfo** -Struktur.

Wenn einem Stream zusätzliche Informationen zugeordnet sind, können Sie diese Informationen mithilfe der [**avistreaminfodata**](/windows/desktop/api/Vfw/nf-vfw-avistreamreaddata) -Funktion abrufen. Diese Funktion gibt die Informationen in einem von der Anwendung bereitgestellten Puffer zurück. Ergänzende Datenstrom Informationen können Konfigurationseinstellungen für die Komprimierungs-und dekomprimierungsmethoden enthalten, die in einem Stream verwendet werden. Sie können die erforderliche Puffergröße mit dem [**avistreamdatasize**](/windows/desktop/api/Vfw/nf-vfw-avistreamdatasize) -Makro abrufen.

Sie können Formatierungsinformationen zu einem Stream abrufen, indem Sie die [**avistreamread Format**](/windows/desktop/api/Vfw/nf-vfw-avistreamreadformat) -Funktion verwenden. Diese Funktion gibt eine Datenstrom spezifische Struktur in einem von der Anwendung bereitgestellten Puffer zurück. Bei einem Videostream enthält der Puffer Formatierungsinformationen in einer [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur. Bei einem Audiostream enthält der Puffer Formatierungsinformationen in einer [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) -oder [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) -Struktur. Bei anderen Streamtypen gibt der streamhandler Informationen für den Datenstrom zurück. Sie können die erforderliche Puffergröße mithilfe von **avistreamread Format** ermitteln und eine **null** -Puffer Adresse angeben oder das [**avistreamformatsize**](/windows/desktop/api/Vfw/nf-vfw-avistreamformatsize) -Makro verwenden.

Sie können den Multimedia-Inhalt in einem Stream mithilfe der [**avistreamread**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) -Funktion abrufen. Diese Funktion kopiert Rohdaten aus dem Stream in einen von der Anwendung bereitgestellten Puffer. Bei Videostreams ruft diese Funktion die bitzugeordneten Bilder ab, die den Frame Inhalt bilden. Für Audiostreams ruft diese Funktion Waveform-Audio-Beispiele ab, aus denen der Sound Inhalt besteht. Sie können die erforderliche Puffergröße mithilfe von **avistreamread** ermitteln und eine **null** -Puffer Adresse angeben oder das [**avistreamsamplesize**](/windows/desktop/api/Vfw/nf-vfw-avistreamsamplesize) -Makro verwenden.

Einige AVI-Datenstrom Handler verursachen Verzögerungen im Zusammenhang mit der Initialisierung oder Koordination von Software und Hardware. Sie können diese Handler informieren, dass Sie das Datenstreaming mithilfe der [**avistreambeginstreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreambeginstreaming) -Funktion vorbereiten. Diese Funktion ermöglicht es dem streamhandler, die benötigten Ressourcen zuzuordnen und zu initialisieren. Wenn Sie diese Handler beim Beenden des Streamings informieren möchten, verwenden Sie die [**avistreamendstreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreamendstreaming) -Funktion. Diese Funktion ermöglicht dem streamhandler das Aufheben der Zuordnung der Ressourcen, die ihm für **avistreambeginstreaming** zugeordnet wurden.

Die [**avistreamread**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) -Funktion stellt keine Debug-Dienste bereit. Weitere Informationen zum Komprimieren und Dekomprimieren von Audiodatenströmen finden Sie unter [Audiokomprimierungs-Manager](audio-compression-manager.md). Weitere Informationen zum Komprimieren und Dekomprimieren von Videostreams finden Sie unter [Video Compression Manager](video-compression-manager.md). Informationen zur Komprimierung und Dekomprimierung einzelner Frames in einem Videostream finden Sie unter [Arbeiten mit komprimierten Videodaten in einem Stream](working-with-compressed-video-data-in-a-stream.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Streamoperationen](stream-operations.md)
</dt> </dl>

 

 