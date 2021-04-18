---
title: Konfigurieren von Audiodatenströmen
description: Konfigurieren von Audiodatenströmen
ms.assetid: 6ddd9bc1-3fde-4098-afce-fdda461ced62
keywords:
- Streams, Konfigurieren von Audiodatenströmen
- Codecs, Konfigurieren von Audiodatenströmen
- Audiodatenströme, konfigurieren
- Codecs, Formate
- Streams, iwmcodecinfo-Schnittstelle
- Iwmcodecinfo, Audiodatenströme
- Streams, A/V-Synchronisierung
- Audiodatenströme, A/V-Synchronisierung
- A/V-Synchronisierung
- Streams, synchronisieren A/V
- Audiodatenströme, Synchronisieren von A/V
- Streams, Audioformate mit niedriger Verzögerung
- Audiostreams, Audioformate mit geringer Verzögerung
- Codecs, Audioformate mit niedriger Verzögerung
- Streams, Variable Bitrate (VBR)
- Audiodatenströme, Variable Bitrate (VBR)
- Codecs, Variable Bitrate (VBR)
- variablenbitrate (VBR), konfigurieren
- VBR (Variable Bitrate), konfigurieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad3931ec41e73c125417d39cdd177dc16056e9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337861"
---
# <a name="configuring-audio-streams"></a>Konfigurieren von Audiodatenströmen

Audiodatenströme sind in der Regel die einfachste zu konfigurieren. Sie erhalten eine streamkonfiguration aus dem Codec mithilfe der Methoden von [**iwmcodecinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo) , wie unter [Get Stream Configuration Information from Codecs](getting-stream-configuration-information-from-codecs.md)beschrieben. In den meisten Fällen sollten Sie die Einstellungen nicht von den abgerufenen Einstellungen ändern.

Das von Ihnen gewählte Codec-Format hängt von der vorgesehenen Verwendung der mit dem Profil erstellten ASF-Dateien ab. Die von [**IWMCodecInfo2:: getcodecformatdesc abgerufene**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc) Codec-Formatbeschreibung fasst die Merkmale des Formats zusammen. Wenn in der Anwendung nicht die Beschreibungen angezeigt werden, die Sie auswählen können, können Sie **QueryInterface** für die [**iwmstreamconfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) -Schnittstelle des Codec-Formats aufrufen, um die [**iwmmediarequigenschnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) abzurufen. Anschließend können Sie die [**\_ \_ Typ**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) -Struktur des WM-Mediums abrufen, indem Sie [**iwmmedia-Eigenschaften:: getmediatype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)aufrufen. Durch Untersuchen der **WM- \_ \_ Medientyp** Struktur und der [**WaveFormatEx**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) -Struktur, auf die Sie verweist, können Sie die Einstellungen des Codec-Formats ermitteln und Sie mit Ihren Anforderungen vergleichen.

## <a name="getting-audio-formats-for-av-synchronization"></a>Erhalten von Audioformaten für eine/V-Synchronisierung

Sowohl der Windows Media Audio Codec als auch Windows Media Audio Professional-Codec unterstützen Formate für reine Audiodateien und Audiodateien und Videodateien. Die reinen Audioformate sind für Dateien optimiert, die nur Audiodaten enthalten, während die Audio-/Videoformate für Audiodaten optimiert sind, die sich in einer Datei mit einem Videostream befinden. Beim Auflisten von Codec-Formaten für diese Codecs werden die Audioformate und Videoformate nach den reinen Audioformaten angezeigt. Die Audio-/videoformatbeschreibungen enthalten die Zeichenfolge "(A/V)". Sie können die für die Audio-/Videosynchronisierung entwickelten Formate Programm gesteuert ermitteln, indem Sie die Anzahl der Pakete pro Sekunde überprüfen. Die Formate für die Synchronisierung haben mindestens 5 Pakete pro Sekunde, wenn die Bitrate größer oder gleich 32.000 Bits pro Sekunde ist. Formate mit Bitraten, die kleiner als 32.000 Bits pro Sekunde sind, können mit synchronisiertem Video verwendet werden, wenn Sie drei oder mehr Pakete pro Sekunde verwenden. Das Codebeispiel im Thema [für die Suche nach Audioformaten](to-find-audio-formats.md) enthält den Code, der für diese Überprüfung erforderlich ist:


```C++
if((pWave->nAvgBytesPerSec / pWave->nBlockAlign) >= 
       ((pWave->nAvgBytesPerSec >= 4000) ? 5.0 : 3.0))
{
    // Set this stream configuration as the new best match.
}
```



## <a name="getting-low-delay-audio-formats"></a>Erhalten von Low-Delay Audioformaten

Der Windows Media 9,1-Codec und der Windows Media Audio 9,1 Professional-Codec unterstützen beide Low-Delay-Formate. Diese Formate verfügen über ein kleineres Puffer Fenster als andere Audioformate. Die Audiogeschwindigkeit ist darauf ausgerichtet, die Leistung in Szenarien zu verbessern, in denen Dateien oder Streams häufig gewechselt werden. beispielsweise eine Anwendung, die eine Reihe von Titeln für das Streaming in der Benutzeroberfläche auflistet und es den Benutzern ermöglicht, zwischen Ihnen willkürlich zu wechseln.

Low-Delay-Formate sind nur im CBR-Modus (ein-oder zwei-Durchlauf) verfügbar. Die Beschreibungen mit dem Low-Delay-Format enthalten die Zeichenfolge "Low Delay". Sie können die Formate Programm gesteuert ermitteln, indem Sie den Bitraten Wert des Formats überprüfen. Den niedrig verzögerten Formaten werden Bitraten zugewiesen, die 1 Kilobit niedriger sind als die Bitraten des entsprechenden normalen Formats. Der Windows Media Audio 9,1-Codec unterstützt z. b. ein Single-Pass-CBR-Format mit einer Bitrate von 192 Kbit/s. Das entsprechende Low-Delay-Format hat eine Bitrate von 191 Kbit/s. Außerdem sind mit Ausnahme des 5-kbit/s-Mono-Formats, das vom Windows Media Audio 9,1-Codec unterstützt wird, die Low-Delay-Formate die einzigen Formate, die einen ungeraden Bitrate-Wert aufweisen.

## <a name="configuring-variable-bit-rate-audio"></a>Konfigurieren der Variablen Bitrate Audiodaten

Wenn Sie ein VBR-Format (Variable Bitrate) für eines der Windows Media-Audiocodecs benötigen, können Sie es durch Festlegen der [**enumerationseinstellungen in der IWMCodecInfo3:: setcodecenumerationsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) -Methode erhalten. Legen \_ Sie g wszvbrenabled auf true fest, und legen \_ Sie für Qualitäts basiertes VBR den Wert 1 und für die 2-Pass-VBR (eingeschränkt oder uneingeschränkt) den Wert 1 fest. Wenn Sie einen eingeschränkten zweistufigen VBR verwenden, müssen Sie die maximale Bitrate und das Puffer Fenster für den Stream manuell mithilfe der Methoden von [**iwmpropertyvault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) festlegen, wie unter [Konfigurieren von VBR-Streams](configuring-vbr-streams.md)beschrieben.

In Qualitäts basierten VBR-Profilen enthält das **navgbytespersec** -Element der **WaveFormatEx** -Struktur die Qualitätsstufe (1 bis 100) im nieder wertigen Byte, und die drei höherwertigen Bytes werden auf 0x7fffff festgelegt. Versuchen Sie nicht, die Qualitätseinstellung zu ändern, indem Sie diesen Wert manuell ändern. Sie müssen das Format verwenden, das vom Codec abgerufen wird. Wenn Sie einen anderen Qualitäts Wert verwenden möchten, müssen Sie die Formate auflisten, bis Sie eine gefunden haben, die Ihren Anforderungen entspricht. Außerdem wird **navgbytespersec** in der ASF-Datei nicht beibehalten. Wenn Sie die **WaveFormatEx** -Struktur für eine Datei abrufen, die mit dem Reader-Objekt geöffnet wurde, enthält **navgbytespersec** einen ungefähren Wert, der die durchschnittliche Anzahl von Bytes pro Sekunde darstellt.

> [!Note]  
> Beim Konfigurieren von Audiodatenströmen sollten Sie nie über einen Wert für das audiopufferfenster verfügen, der größer ist als der Wert für alle Videostreams in der Datei. Normalerweise ist dies kein Problem, da die Werte des audiopufferfensters zwischen 1,5 und 3 Sekunden liegen sollten und die Video Werte zwischen 3 und 5 Sekunden liegen sollten. Wenn ein audiopufferfenster größer als ein Video Puffer Fenster ist, wird die Datei mit den Datenströmen aus der Synchronisierung leicht wiedergegeben.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Konfiguration für alle Streams**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Konfigurieren von Streams**](configuring-streams.md)
</dt> <dt>

[**So suchen Sie Audioformate**](to-find-audio-formats.md)
</dt> </dl>

 

 