---
title: Konfigurieren von Streams
description: Konfigurieren von Streams
ms.assetid: caffdfc1-3c35-4b7b-8643-5a9095cc11f6
keywords:
- Streams,Konfigurieren von Videostreams
- Codecs,Konfigurieren von Videostreams
- Videostreams,Konfigurieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22bc6e011f32d1ea9a9905c718ad8ff0c13f7d57650a30316ecfec6332978fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809590"
---
# <a name="configuring-video-streams"></a>Konfigurieren von Streams

Videostreams sind in ihrer Konfiguration flexibler als Audiostreams. Dies liegt daran, dass die Eigenschaften der Frames, aus denen das Video besteht, von Datei zu Datei stark variieren können. Wenn Sie das Codecformat für den verwendeten Codec abrufen, müssen Sie die folgenden Werte für Videostream-Konfigurationsobjekte festlegen.



| Wert                                 | Beschreibung                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bitrate                              | Rufen [**Sie IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) auf, um auf den gewünschten Wert zu setzen. Der Videocodec versucht, die Medien zu komprimieren, um Ihre Spezifikationen zu erfüllen. Wenn Ihre Werte zu niedrig sind, wird das resultierende komprimierte Video sehr beeinträchtigt.           |
| Pufferfenster                         | Rufen [**Sie IWMStreamConfig::SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) auf, um auf den gewünschten Wert zu setzen. Der Videocodec versucht, die Medien zu komprimieren, um Ihre Spezifikationen zu erfüllen. Wenn Ihre Werte zu niedrig sind, wird das resultierende komprimierte Video sehr beeinträchtigt. |
| **WMVIDEOINFOHEADER.rcSource**        | Die obere linke Ecke muss auf 0,0 festgelegt werden. Die untere rechte Ecke muss auf die Rahmendimensionen festgelegt werden. In einem 640x480-Stream wären diese Einstellungen beispielsweise 0,0.640.480.                                                                                                |
| **WMVIDEOINFOHEADER.rcTarget**        | Muss mit **rcSource übereinstimmen.**                                                                                                                                                                                                                                                    |
| **WMVIDEOINFOHEADER.dwBitRate**       | Muss mit der für den Stream festgelegten Bitrate übereinstimmen.                                                                                                                                                                                                                                 |
| **WMVIDEOINFOHEADER. AvgTimePerFrame** | Legen Sie auf die ungefähre Zeit pro Frame fest.                                                                                                                                                                                                                                      |
| **BITMAPINFOHEADER.biWidth**          | Legen Sie auf die Breite der gewünschten Framegröße in Pixel fest.                                                                                                                                                                                                                     |
| **BITMAPINFOHEADER.biHeight**         | Legen Sie auf die Höhe der gewünschten Framegröße in Pixel fest.                                                                                                                                                                                                                    |



 

Videoinhalte werden nur dann richtig abspielt, wenn sie in einer Größe codiert sind, die ein Vielfaches von vier für Breite und Höhe ist. Die Ausnahme ist [*rgb*](wmformat-glossary.md) unkomprimiertes Video, das eine beliebige Größe haben kann. Wenn Sie versuchen, eine Größe zu festlegen, die kein Vielfaches von vier ist, wird einer der folgenden Fehler vom Writer zurückgegeben:

-   NS \_ E \_ UNGÜLTIGES \_ \_ EINGABEFORMAT
-   NS \_ E \_ UNGÜLTIGES \_ \_ AUSGABEFORMAT
-   NS \_ E \_ INVALIDPROFILE

Wenn Sie die Codierung mit variabler Bitrate verwenden, müssen Sie möglicherweise weitere Anpassungen vornehmen. Weitere Informationen finden Sie unter [Configuring VBR Streams](configuring-vbr-streams.md).

Einige Windows Media Video-Codecs unterstützen mehrere Komplexitätsstufen. Komplexitätsstufen bestimmen die Algorithmen, die der Codec beim Codieren eines Videostreams verwendet. Die Verwendung einer hohen Komplexitätsebene erfordert mehr Verarbeitungsleistung für die Codierung und Decodierung.

Jeder Codec, der Komplexitätseinstellungen unterstützt, macht die folgenden Einstellungen verfügbar, die Sie mit der [**IWMCodecInfo3::GetCodecProp-Methode abrufen**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) können.



| Einstellung                 | Beschreibung                                         |
|-------------------------|-----------------------------------------------------|
| g \_ wszComplexityMax     | Die maximale Qualitätsstufe, die vom Codec unterstützt wird.   |
| g \_ wszComplexityOffline | Die empfohlene Qualitätsstufe für die Offlinewiedergabe.   |
| g \_ wszComplexityLive    | Die empfohlene Qualitätsstufe für die Streamingwiedergabe. |



 

Verwenden Sie zum Festlegen der Komplexität für einen Videostream in einem Profil die [**IWMPropertyVault::SetProperty-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) mithilfe der Eigenschaft g \_ wszComplexity. Der von Ihnen festgelegte Wert muss kleiner oder gleich der maximal unterstützten Komplexität für den Codec sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Configuration Common to All Streams**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Konfigurieren Streams**](configuring-streams.md)
</dt> <dt>

[**Videokomplexitäts-Einstellungen**](video-complexity-settings.md)
</dt> </dl>

 

 




