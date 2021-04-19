---
description: Dieser Artikel enthält Anleitungen zum Erstellen von Histogrammen beim Decodieren von Videos mit Direct3D 11-oder 12-Video-APIs.
ms.assetid: ''
title: Direct3D-Video-Decodieren von Histogrammen
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 6e25abd39ba95b669c2d76ced5f825ea80c4e3c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342789"
---
# <a name="direct3d-video-decode-histograms"></a>Direct3D-Video-Decodieren von Histogrammen

Dieser Artikel enthält Anleitungen zum Erstellen von Histogrammen beim Decodieren von Videos mit Direct3D 11-oder 12-Video-APIs.

## <a name="checking-the-video-device-for-histogram-capabilities"></a>Überprüfen des Videogeräts auf histogrammfunktionen

Bevor Sie versuchen, Histogramme zu generieren, müssen Sie überprüfen, ob das aktuelle Videogerät das Feature zum Decodieren von Video decodieren unterstützt.

### <a name="direct3d-12"></a>Direct3D 12

Wenden Sie sich an [ID3D12VideoDevice:: checkfeaturesupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) , um die Support Details für Direct3D 12-Video Decodierungs Vorgänge zu überprüfen. Übergeben Sie den **D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM** Wert aus der [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) -Enumeration, um anzugeben, dass Sie Unterstützung für Histogramme zum Decodieren von Videos anfordern.

### <a name="direct3d-11"></a>Direct3D 11

Wenden Sie [ID3D11VideoDevice2:: checkfeaturesupport](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videodevice2-checkfeaturesupport) an, und übergeben Sie den **D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM** Wert des [D3D11_FEATURE_VIDEO](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_feature_video) , um zu ermitteln, ob Histogramme für das aktuelle Gerät unterstützt werden.

## <a name="enabling-histogram-during-decode"></a>Aktivieren von Histogramm während der Decodierung

Die Sammlung der Histogrammdaten wird vom Aufrufer aktiviert, der die Puffer bereitstellt, in denen die Histogrammdaten gespeichert werden.  Ein NULL-histogrammausgabepuffer für eine bestimmte Komponente gibt an, dass die histogrammauflistung deaktiviert ist.

### <a name="direct3d-12"></a>Direct3D 12

Um Ausgabepuffer zum Empfangen von Histogrammdaten mithilfe von Direct3D 12 bereitzustellen, sollten Sie die decodierbefehlsliste mithilfe der [ID3D12VideoDecodeCommandList1::D ecodeframe1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1) -Methode erstellen. Diese Methode nimmt eine [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1) Struktur als Argument an. **D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1** verfügt über ein Feld vom Typ [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram), mit dem Sie ein [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) angeben können, in das Histogrammdaten ausgegeben werden.

### <a name="direct3d-11"></a>Direct3D 11

Die [ID3D11VideoContext3](/windows/win32/api/d3d11_4/nn-d3d11_4-id3d11videocontext3) -Schnittstelle stellt die [DecoderBeginFrame1](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videocontext3-decoderbeginframe1) -Methode bereit, mit der Sie eine oder mehrere [ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) -Schnittstellen bereitstellen können, in die die Histogrammdaten ausgegeben werden. Der [D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_video_decoder_histogram_component) , um die Komponenten anzugeben, für die Histogrammdaten generiert werden sollen.


## <a name="buffer-format"></a>Puffer Format

Die Decodierung der histogrammausgabe wird als ganzzahliger Leistungs-Counter pro Komponente in einen Puffer geschrieben.  Das Puffer Format ist ein 32-Bit-Wert pro bin.  Ein Gerät verwendet möglicherweise eine ganzzahlige Bittiefe, die kleiner als 32 Bits ist, aber 16, 24 oder 32 Bits betragen muss.  Wenn dies der Fall ist, wird der Leistungswert in den unteren Bits gespeichert, und die oberen nicht verwendeten Bits sind 0 (null).  Wenn die Anzahl für einen "bin" den maximalen Wert überschreitet, legt das Gerät stattdessen den maximalen Wert fest. Von den Geräten wird die Anzahl der unterstützten Behälter gemeldet, bei der es sich um einen Wert von 2 handeln muss.  Die Mindestanzahl von Containern, die für Geräte erforderlich sind, die dieses Feature unterstützen, ist 64. 

Sie müssen einen Puffer mit einem abgeglichen 256-Byte-Offset und einer Größe angeben, die die unterstützte Anzahl von Containern multipliziert mit der bin-Größe (4 Bytes) für jede angeforderte Komponente ist.  Die bin-Platzierung wird durch Folgendes bestimmt:

`binIndex = floor(value / [max value of channel + 1] * (countBins))`


Wenn ein Format die nützlichen Bits einer Komponente als kleiner als die Anzahl der Speicher Bits definiert (z. b. P010 verwendet die ersten 10 Bits von 16 Bits des Komponenten Speichers), werden nur die nützlichen Bits berücksichtigt (P010 wird als 10-Bit-Wert behandelt). 

Das Videogerät meldet, welche Komponenten unterstützt werden.  Wenn der Aufrufer kein Histogramm für eine bestimmte Komponente wünschen, geben Sie nullptr an.  Wenn der Treiber ein Histogramm für eine bestimmte Komponente nicht unterstützt, muss der histogrammpuffer der Komponente "nullptr" lauten.

Wenn mehrere Komponenten unterstützt werden, kann die Anwendung jede beliebige Kombination von Komponenten pro Frame-Decodierung anfordern.  Wenn die Hardware z. b. die Unterstützung für y-, U-und v-Komponenten meldet, kann die Anwendung das Y-Histogramm nur für Frame 1, das U-Histogramm nur für Frame 2 und das V-Histogramm nur für Frame 3 anfordern.  Sie können auch eine beliebige Kombination von zwei Komponenten oder alle drei Komponenten anfordern.

Anwendungen stellen für jede angeforderte Komponente einen separaten Offset-und Puffer Zeiger bzw.-handle bereit.  Dieser Zeiger weist möglicherweise auf dieselbe Ressource wie eine andere Komponente oder eine separate Ressource hin.  Der Offset ermöglicht das Platzieren mehrerer Komponenten im gleichen Puffer, aber der vom Offset und der histogrammgröße angegebene Ausgabebereich darf sich nicht überlappen.  Das Histogramm kann auch in denselben Puffer wie andere nicht zusammenhängende Inhalte geschrieben werden, z. b. bei der Verwendung in einer Ressourcen-unter Zuordnungs Strategie.


Die D3D-Laufzeit überprüft, ob Aufrufer nur das Histogramm für unterstützte Komponenten aktivieren, ob der Puffer Offset ausgerichtet ist, und dass die Puffergröße für die gemeldete Anzahl von Containern ausreichend ist.


## <a name="protected-content"></a>Geschützter Inhalt

Die histogrammpuffer benötigen denselben Oberflächenschutz wie die decodierausgabeoberfläche. Wenn die Decodierung der Ausgabe Oberfläche keine geschützte Ressource ist, darf der histogrammpuffer keine geschützte Ressource sein. Wenn die Decodierung der Ausgabe Oberfläche eine geschützte Ressource ist, muss es sich bei dem Histogramm um eine geschützte Ressource handeln.








## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>
[Direct3D 12-Video-APIs](direct3d-12-video-apis.md) 
 [Media Foundation-Programmier Handbuch](media-foundation-programming-guide.md)
</dt> </dl>

 

 




