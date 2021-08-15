---
title: Lesen aus einem Stream
description: Lesen aus einem Stream
ms.assetid: be961f06-cf5f-4093-9b31-7d1d69e62fec
keywords:
- AVIStreamInfo-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c56e1bd34fb9b0555c4eb0ed86944be3b7603645865144ac053604cd515cb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371650"
---
# <a name="reading-from-a-stream"></a>Lesen aus einem Stream

Sie können Informationen zu einem geöffneten Stream mithilfe der [**FUNKTION AVIStreamInfo**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) abrufen. Diese Funktion füllt die [**AVISTREAMINFO-Struktur**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) mit Informationen wie dem Typ der Daten im Stream, der beim Schreiben von Streamdaten verwendeten Komprimierungsmethode, der vorgeschlagenen Puffergröße, der Wiedergaberate und einer Textbeschreibung des Streams auf.

Einige Member der [**AVISTREAMINFO-Struktur**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) sind auch in der [**AVIFILEINFO-Struktur**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) vorhanden. Die Informationen in der **AVIFILEINFO-Struktur** gelten für die gesamte Datei. Die Informationen in der **AVISTREAMINFO-Struktur** sind spezifisch für den Datenstrom, auf den zugegriffen wird, und haben Vorrang vor den Informationen in der **AVIFILEINFO-Struktur.**

Wenn einem Stream ergänzende Informationen zugeordnet sind, können Sie diese Informationen mithilfe der [**AVIStreamReadData-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avistreamreaddata) abrufen. Diese Funktion gibt die Informationen in einem von der Anwendung bereitgestellten Puffer zurück. Ergänzende Streaminformationen können Konfigurationseinstellungen für die Komprimierungs- und Dekomprimierungsmethoden enthalten, die für einen Stream verwendet werden. Sie können die erforderliche Puffergröße mithilfe des [**MAKROS AVIStreamDataSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamdatasize) abrufen.

Sie können Formatierungsinformationen zu einem Stream mithilfe der [**FUNKTION AVIStreamReadFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamreadformat) abrufen. Diese Funktion gibt eine streamspezifische Struktur in einem von der Anwendung bereitgestellten Puffer zurück. Bei einem Videostream enthält der Puffer Formatierungsinformationen in einer [**BITMAPINFO-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) Bei einem Audiostream enthält der Puffer Formatierungsinformationen in einer [**WAVEFORMATEX-**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) oder [**PCMWAVEFORMAT-Struktur.**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) Bei anderen Streamtypen gibt der Streamhandler spezifische Informationen für den Stream zurück. Sie können die erforderliche Puffergröße ermitteln, indem Sie **AVIStreamReadFormat** verwenden und eine **NULL-Pufferadresse** angeben oder das MAKRO [**AVIStreamFormatSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamformatsize) verwenden.

Sie können den Multimediainhalt in einem Stream mithilfe der [**AVIStreamRead-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) abrufen. Diese Funktion kopiert Rohdaten aus dem Stream in einen von der Anwendung bereitgestellten Puffer. Bei Videostreams ruft diese Funktion die Bitmapbilder ab, aus denen sich der Frameinhalt zusammenbildet. Für Audiostreams ruft diese Funktion Waveform-Audiobeispiele ab, aus denen der Soundinhalt zusammengeformt wird. Sie können die erforderliche Puffergröße ermitteln, indem Sie **AVIStreamRead** verwenden und eine **NULL-Pufferadresse** angeben oder das MAKRO [**AVIStreamSampleSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamsamplesize) verwenden.

Einige AVI-Streamhandler führen zu Verzögerungen im Zusammenhang mit der Initialisierung oder Koordination von Software und Hardware. Sie können diese Handler über die [**AVIStreamBeginStreaming-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avistreambeginstreaming) informieren, um sich auf das Datenstreaming vorzubereiten. Mit dieser Funktion kann der Streamhandler die benötigten Ressourcen zuordnen und initialisieren. Um diese Handler zu informieren, wenn das Streaming beendet wurde, verwenden Sie [**die FUNKTION AVIStreamEndStreaming.**](/windows/desktop/api/Vfw/nf-vfw-avistreamendstreaming) Diese Funktion ermöglicht es dem Streamhandler, die Zugeordneten Ressourcen für **AVIStreamBeginStreaming zu entfernen.**

Die [**AVIStreamRead-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) stellt keine Dekomprimierungsdienste zur Verfügung. Informationen zum Komprimieren und Dekomprimieren von Audiostreams finden Sie unter [Audio Compression Manager](audio-compression-manager.md). Informationen zum Komprimieren und Dekomprimieren von Videostreams finden Sie unter [Video Compression Manager](video-compression-manager.md). Informationen zum Komprimieren und Dekomprimieren einzelner Frames in einem Videostream finden Sie unter Arbeiten mit komprimierten [Videodaten in einem Stream.](working-with-compressed-video-data-in-a-stream.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Streamoperationen](stream-operations.md)
</dt> </dl>

 

 