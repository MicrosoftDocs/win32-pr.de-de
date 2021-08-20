---
title: Konfigurieren von Audio Streams
description: Konfigurieren von Audio Streams
ms.assetid: 6ddd9bc1-3fde-4098-afce-fdda461ced62
keywords:
- Streams,Konfigurieren von Audiostreams
- Codecs,Konfigurieren von Audiostreams
- Audiostreams,Konfigurieren
- Codecs, Formate
- streams,IWMCodecInfo-Schnittstelle
- IWMCodecInfo, Audiostreams
- Streams, A/V-Synchronisierung
- Audiostreams, A/V-Synchronisierung
- A/V-Synchronisierung
- Streams,Synchronisieren von A/V
- Audiostreams, Synchronisieren von A/V
- Streams, Audioformate mit geringer Verzögerung
- Audiostreams, Audioformate mit geringer Verzögerung
- Codecs, Audioformate mit geringer Verzögerung
- Streams, variable Bitrate (VBR)
- Audiostreams, variable Bitrate (VBR)
- Codecs, variable Bitrate (VBR)
- Variable Bitrate (VBR),Konfigurieren
- VBR (variable Bitrate),Konfigurieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e28c32e9d0e237e72f693bded74c7620d33845261a6137afdf58b04f35f441f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548030"
---
# <a name="configuring-audio-streams"></a>Konfigurieren von Audio Streams

Audiostreams sind im Allgemeinen am einfachsten zu konfigurieren. Abrufen einer Streamkonfiguration vom Codec mithilfe der Methoden von [**IWMCodecInfo,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo) wie unter [Abrufen von Streamkonfigurationsinformationen aus Codecs](getting-stream-configuration-information-from-codecs.md)beschrieben. In den meisten Fällen sollten Sie die Einstellungen der abgerufenen Einstellungen nicht ändern.

Das Codecformat, das Sie aus den aufgeführten Formaten auswählen, hängt von der beabsichtigten Verwendung der ASF-Dateien ab, die mit dem Profil erstellt wurden. Die von [**IWMCodecInfo2::GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc) abgerufene Codecformatbeschreibung fasst die Merkmale des Formats zusammen. Wenn Ihre Anwendung nicht die Beschreibungen anzeigt, die zwischen ihnen ausgewählt werden sollen, können Sie **QueryInterface** für die [**IWMStreamConfig-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) des Codecformats aufrufen, um die [**IWMMediaProps-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) abzurufen. Anschließend können Sie die [**WM \_ MEDIA \_ TYPE-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) abrufen, indem Sie [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)aufrufen. Indem Sie die **WM \_ MEDIA \_ TYPE-Struktur** und die [**WAVEFORMATEX-Struktur**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) untersuchen, auf die sie verweist, können Sie die Einstellungen des Codecformats bestimmen und sie mit Ihren Anforderungen vergleichen.

## <a name="getting-audio-formats-for-av-synchronization"></a>Abrufen von Audioformaten für die A/V-Synchronisierung

Der Windows Medienaudiocodec und Windows Medienaudio-Professional-Codec unterstützen formate sowohl für Audiodateien als auch für Audio-/Videodateien. Die reinen Audioformate sind für Dateien optimiert, die nur Audiodaten enthalten, während die Audio-/Videoformate für Audiodaten optimiert sind, die sich in einer Datei mit einem Videostream befinden. Beim Aufzählen von Codecformaten für diese Codecs folgen die Audio-/Videoformate nach den reinen Audioformaten. Die Audio-/Videoformatbeschreibungen enthalten alle die Zeichenfolge "(A/V)". Sie können die Für die Audio-/Videosynchronisierung konzipierten Formate programmgesteuert identifizieren, indem Sie die Anzahl der Pakete pro Sekunde überprüfen. Formate für die Synchronisierung haben 5 oder mehr Pakete pro Sekunde, wenn die Bitrate größer oder gleich 32.000 Bits pro Sekunde ist. Formate mit Bitraten unter 32.000 Bits pro Sekunde können mit synchronisierten Videos verwendet werden, wenn sie 3 oder mehr Pakete pro Sekunde verwenden. Das Codebeispiel im Thema [To Find Audio Formats (So suchen Sie Audioformate)](to-find-audio-formats.md) enthält den Code, der für diese Überprüfung erforderlich ist:


```C++
if((pWave->nAvgBytesPerSec / pWave->nBlockAlign) >= 
       ((pWave->nAvgBytesPerSec >= 4000) ? 5.0 : 3.0))
{
    // Set this stream configuration as the new best match.
}
```



## <a name="getting-low-delay-audio-formats"></a>Abrufen von Low-Delay Audioformaten

Der Windows Media 9.1-Codec und der Windows Media Audio 9.1 Professional-Codec unterstützen beide Formate mit geringer Verzögerung. Diese Formate verfügen über ein kleineres Pufferfenster als andere Audioformate. Audio mit geringer Verzögerung soll die Leistung in Szenarien verbessern, in denen Dateien oder Streams häufig gewechselt werden. Beispielsweise eine Anwendung, die eine Reihe von Musiktiteln für das Streaming auf der Benutzeroberfläche auflistet und benutzern das willkürliche Wechseln zwischen ihnen ermöglicht.

Formate mit geringer Verzögerung sind nur im CBR-Modus (Ein- oder Zwei-Durchlauf) verfügbar. Die Formatbeschreibungen mit geringer Verzögerung enthalten alle die Zeichenfolge "Low Delay". Sie können die Formate programmgesteuert identifizieren, indem Sie den Bitratenwert des Formats überprüfen. Den Formaten mit niedriger Verzögerung werden Bitraten zugewiesen, die 1 Kilobit kleiner als die Bitraten des entsprechenden normalen Formats sind. Beispielsweise unterstützt der Windows Media Audio 9.1-Codec ein CBR-Einzeldurchlaufformat mit einer Bitrate von 192 KBit/s. Das entsprechende Format mit niedriger Verzögerung weist eine Bitrate von 191 KBit/s auf. Mit Ausnahme des mono-Formats mit 5 KBit/s, das vom Windows Media Audio 9.1-Codec unterstützt wird, sind die Formate mit geringer Verzögerung die einzigen Formate, die einen ungeraden Bitratenwert aufweisen.

## <a name="configuring-variable-bit-rate-audio"></a>Konfigurieren von Audiodaten mit variabler Bitrate

Wenn Sie ein FORMAT mit variabler Bitrate (VBR) für einen der Windows Medienaudiocodecs benötigen, können Sie es abrufen, indem Sie die Enumerationseinstellungen in der [**IWMCodecInfo3::SetCodecEnumerationSetting-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) festlegen. Legen Sie g \_ wszVBREnabled auf True und g \_ wszNumPasses für qualitätsbasierte VBR auf 1 oder für VBR mit zwei Durchläufen (eingeschränkt oder uneingeschränkt) auf 2 fest. Wenn Sie eingeschränkte VBR mit zwei Durchläufen verwenden, müssen Sie die maximale Bitrate und das Pufferfenster für den Stream manuell mithilfe der Methoden von [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) festlegen, wie unter [Konfigurieren von VBR Streams](configuring-vbr-streams.md)beschrieben.

In qualitätsbasierten VBR-Profilen enthält der **nAvgBytesPerSec-Member** der **WAVEFORMATEX-Struktur** die Qualitätsstufe (1 bis 100) im Low-Order-Byte, und die drei bytes hoher Ordnung werden auf 0x7fffff festgelegt. Versuchen Sie nicht, die Qualitätseinstellung durch manuelles Ändern dieses Werts zu ändern. Sie müssen das Format verwenden, da es aus dem Codec abgerufen wird. Um einen anderen Qualitätswert zu verwenden, müssen Sie Formate aufzählen, bis Sie eines finden, das Ihren Anforderungen entspricht. Außerdem wird **nAvgBytesPerSec** nicht in der ASF-Datei beibehalten. Wenn Sie die **WAVEFORMATEX-Struktur** für eine Datei abrufen, die mit dem Readerobjekt geöffnet wurde, enthält **nAvgBytesPerSec** einen ungefähren Wert, der die durchschnittliche Anzahl von Bytes pro Sekunde darstellt.

> [!Note]  
> Beim Konfigurieren von Audiostreams sollten Sie nie über einen Wert für das Audiopufferfenster verfügen, der größer als der Wert für Videostreams in der Datei ist. Normalerweise ist dies kein Problem, da die Werte des Audiopufferfensters zwischen 1,5 und 3 Sekunden und die Videowerte zwischen 3 und 5 Sekunden liegen sollten. Wenn ein Audiopufferfenster größer als ein Videopufferfenster ist, wird die Datei mit den Streams etwas außerhalb der Synchronisierung wiedergegeben.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Configuration Common to All Streams**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Konfigurieren von Streams**](configuring-streams.md)
</dt> <dt>

[**So suchen Sie Audioformate**](to-find-audio-formats.md)
</dt> </dl>

 

 