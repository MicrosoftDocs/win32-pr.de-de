---
description: Dieser Artikel enthält Anleitungen zum Generieren von Histogrammen beim Decodieren von Videos mithilfe von Direct3D 11- oder 12-Video-APIs.
ms.assetid: ''
title: Direct3D-Videodecodierungshistogramme
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 94371fd68c981a98c4ba629822f928e148c230565b5103dfaa2350543bbe9a57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061630"
---
# <a name="direct3d-video-decode-histograms"></a>Direct3D-Videodecodierungshistogramme

Dieser Artikel enthält Anleitungen zum Generieren von Histogrammen beim Decodieren von Videos mithilfe von Direct3D 11- oder 12-Video-APIs.

## <a name="checking-the-video-device-for-histogram-capabilities"></a>Überprüfen des Videogeräts auf Histogrammfunktionen

Bevor Sie versuchen, Histogramme zu erstellen, müssen Sie überprüfen, ob das aktuelle Videogerät die Videodecodierungshistogrammfunktion unterstützt.

### <a name="direct3d-12"></a>Direct3D 12

Rufen [Sie ID3D12VideoDevice::CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) auf, um die Supportdetails für Direct3D 12-Videodecodierungsvorgänge zu überprüfen. Übergeben Sie **D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM** wert der [](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) D3D12_FEATURE_VIDEO -Enumeration, um anzugeben, dass Sie Unterstützung für Videodecodierungshistogramme anfordern.

### <a name="direct3d-11"></a>Direct3D 11

Rufen [Sie ID3D11VideoDevice2::CheckFeatureSupport](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videodevice2-checkfeaturesupport) auf, und übergeben Sie den **D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM-Wert** der [D3D11_FEATURE_VIDEO,](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_feature_video) um zu bestimmen, ob Histogramme für das aktuelle Gerät unterstützt werden.

## <a name="enabling-histogram-during-decode"></a>Aktivieren des Histogramms während der Decodierung

Die Sammlung von Histogrammdaten wird vom Aufrufer aktiviert, der die Puffer an stellt, in denen die Histogrammdaten gespeichert werden.  Ein NULL-Histogramm-Ausgabepuffer für eine bestimmte Komponente gibt an, dass die Histogrammsammlung deaktiviert ist.

### <a name="direct3d-12"></a>Direct3D 12

Um Ausgabepuffer zum Empfangen von Histogrammdaten mit Direct3D 12 bereitstellen zu können, sollten Sie ihre Decodierungsbefehlsliste mithilfe der [ID3D12VideoDecodeCommandList1::D ecodeFrame1-Methode](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1) erstellen. Diese Methode verwendet eine [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1-Struktur](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1) als Argument. **D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1** verfügt über ein Feld vom Typ [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram), mit dem Sie eine [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) angeben können, in die Histogrammdaten ausgegeben werden.

### <a name="direct3d-11"></a>Direct3D 11

Die [ID3D11VideoContext3-Schnittstelle](/windows/win32/api/d3d11_4/nn-d3d11_4-id3d11videocontext3) stellt die [DecoderBeginFrame1-Methode](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videocontext3-decoderbeginframe1) bereit, mit der Sie eine oder mehrere [ID3D11Buffer-Schnittstellen](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) bereitstellen können, in die die Histogrammdaten ausgegeben werden. Die [D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT,](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_video_decoder_histogram_component) um die Komponenten anzugeben, für die Histogrammdaten generiert werden sollen.


## <a name="buffer-format"></a>Pufferformat

Die Ausgabe des Decodierungshistogramms wird als ganzzahliger Indikator pro Komponente in einen Puffer geschrieben.  Das Pufferformat ist ein 32-Bit-Wert pro Bin.  Ein Gerät kann eine ganzzahlige Indikatorbittiefe verwenden, die kleiner als 32 Bits ist, aber 16, 24 oder 32 Bits sein muss.  Wenn dies der Wert ist, wird der Indikatorwert in den unteren Bits gespeichert, und die oberen nicht verwendeten Bits sind 0 (null).  Wenn die Anzahl für eine Behälter den maximalen Wert überschreiten würde, legt das Gerät stattdessen den maximalen Wert fest. Geräte melden die Anzahl der unterstützten Behälter. Dies muss ein Wert von 2 sein.  Für Geräte, die dieses Feature unterstützen, sind mindestens 64 Geräte erforderlich. 

Sie müssen einen Puffer mit einem 256-Byte-ausgerichteten Offset und einer Größe zur Verfügung stellen, die der unterstützten Anzahl von Behältern multipliziert mit der Bin-Größe (4 Byte) für jede angeforderte Komponente entspricht.  Die Bin-Platzierung wird durch:

`binIndex = floor(value / [max value of channel + 1] * (countBins))`


Wenn ein Format die nützlichen Bits einer Komponente als kleiner als die Anzahl der Speicherbits definiert (p010 verwendet z. B. die ersten 10 Bits von 16 Bits des Komponentenspeichers), werden nur die nützlichen Bits berücksichtigt (P010 wird als 10-Bit-Wert behandelt). 

Das Videogerät meldet, welche Komponenten unterstützt werden.  Wenn der Aufrufer kein Histogramm für eine bestimmte Komponente möchte, gibt er nullptr an.  Wenn der Treiber kein Histogramm für eine bestimmte Komponente unterstützt, muss der Histogrammpuffer dieser Komponente NULLptr sein.

Wenn mehrere Komponenten unterstützt werden, kann die Anwendung eine beliebige Kombination von Komponenten pro Framedecodierung anfordern.  Wenn die Hardware beispielsweise Unterstützung für Y-, U- und V-Komponenten meldet, kann die Anwendung das Y-Histogramm nur für Frame 1, das U-Histogramm nur für Frame 2 und das V-Histogramm nur für Frame 3 anfordern.  Sie können auch eine beliebige Kombination aus zwei oder allen drei Komponenten anfordern.

Anwendungen stellen für jede angeforderte Komponente einen separaten Offset- und Pufferzeiger/-handle zur Verfügung.  Dieser Zeiger kann auf dieselbe Ressource wie eine andere Komponente oder eine separate Ressource zeigen.  Der Offset ermöglicht das Platzieren mehrerer Komponenten in demselben Puffer, aber der durch den Offset und die Histogrammgröße angegebene Ausgabebereich darf keine andere Histogrammkomponentenausgabe überlappen.  Das Histogramm kann auch in den gleichen Puffer geschrieben werden wie andere nicht verknüpfte Inhalte, z. B. bei Verwendung in einer Strategie für die Ressourcenunterzuordnung.


Die D3D-Laufzeit überprüft, ob Aufrufer das Histogramm nur für unterstützte Komponenten aktivieren, ob der Pufferoffset ausgerichtet ist und dass diese Puffergröße für die gemeldete Anzahl von Behältern ausreicht.


## <a name="protected-content"></a>Geschützter Inhalt

Die Histogrammpuffer müssen denselben Oberflächenschutz wie die Decodierungsausgabeoberfläche haben. Wenn die Decodierungsausgabeoberfläche keine geschützte Ressource ist, darf der Histogrammpuffer keine geschützte Ressource sein. Wenn die Decodierungsausgabeoberfläche eine geschützte Ressource ist, muss das Histogramm eine geschützte Ressource sein.








## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>
[Direct3D 12-Video-APIs](direct3d-12-video-apis.md) 
 [Media Foundation-Programmierhandbuch](media-foundation-programming-guide.md)
</dt> </dl>

 

 




