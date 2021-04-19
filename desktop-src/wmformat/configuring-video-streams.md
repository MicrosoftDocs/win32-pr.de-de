---
title: Konfigurieren von Videostreams
description: Konfigurieren von Videostreams
ms.assetid: caffdfc1-3c35-4b7b-8643-5a9095cc11f6
keywords:
- Streams, Konfigurieren von Videostreams
- Codecs, Konfigurieren von Videostreams
- Videostreams, konfigurieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d2389026dc1061064c5e687da60c3350ad94a4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106341702"
---
# <a name="configuring-video-streams"></a>Konfigurieren von Videostreams

Videostreams sind in Ihrer Konfiguration flexibler als Audiodatenströme. Dies liegt daran, dass die Eigenschaften der Frames, aus denen sich das Video besteht, von einer Datei zur nächsten variieren können. Wenn Sie das Codec-Format für den Codec abrufen, den Sie verwenden, müssen Sie für videostreamkonfigurationsobjekte die folgenden Werte festlegen.



| Wert                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bitrate                              | Nennen Sie [**iwmstreamconfig:: setbitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) , um auf den gewünschten Wert festzulegen. Der Videocodec versucht, die Medien zu komprimieren, um ihre Spezifikationen zu erfüllen. Wenn Ihre Werte zu niedrig sind, wird das resultierende komprimierte Video stark beeinträchtigt.           |
| Puffer Fenster                         | Nennen Sie [**iwmstreamconfig:: setbufferwindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) , um auf den gewünschten Wert festzulegen. Der Videocodec versucht, die Medien zu komprimieren, um ihre Spezifikationen zu erfüllen. Wenn Ihre Werte zu niedrig sind, wird das resultierende komprimierte Video stark beeinträchtigt. |
| **Wmvideoinfoheader. rcSource**        | Die linke obere Ecke muss auf 0, 0 (null) festgelegt werden. Die untere rechte Ecke muss auf die Frame Dimensionen festgelegt werden. Beispielsweise sind in einem 640 x480-Stream diese Einstellungen 0, 0640480.                                                                                                |
| **Wmvideoinfoheader. rctarget**        | Muss mit **rcSource** verglichen werden.                                                                                                                                                                                                                                                    |
| **Wmvideoinfoheader. dwbitrate**       | Muss mit der für den Stream festgelegten Bitrate identisch sein.                                                                                                                                                                                                                                 |
| **Wmvideoinfoheader. Avgtimeperframe** | Legen Sie auf die ungefähre Zeit pro Frame fest.                                                                                                                                                                                                                                      |
| **BITMAPINFOHEADER. biwidth**          | Legen Sie auf die Breite der gewünschten Frame Größe in Pixel fest.                                                                                                                                                                                                                     |
| **BITMAPINFOHEADER. biheight**         | Legen Sie auf die Höhe der gewünschten Frame Größe in Pixel fest.                                                                                                                                                                                                                    |



 

Video Inhalte werden nur dann ordnungsgemäß abgespielt, wenn Sie in einer Größe codiert sind, die für Breite und Höhe ein Vielfaches von vier ist. Die Ausnahme ist ein nicht komprimiertes [*RGB*](wmformat-glossary.md) -Video, das eine beliebige Größe aufweisen kann. Wenn Sie versuchen, eine Größe festzulegen, die kein Vielfaches von vier ist, wird einer der folgenden Fehler vom Writer zurückgegeben:

-   NS \_ E ( \_ ungültiges \_ Eingabe \_ Format)
-   \_Ungültiges NS E- \_ \_ Ausgabe \_ Format
-   NS \_ E \_ invalidprofile

Wenn Sie die variablenbitrate-Codierung verwenden, müssen Sie möglicherweise weitere Anpassungen vornehmen. Weitere Informationen finden Sie unter [Konfigurieren von VBR-Streams](configuring-vbr-streams.md).

Einige Windows Media Video Codecs unterstützen mehrere Komplexitäts Ebenen. Komplexitäts Ebenen bestimmen die Algorithmen, die der Codec beim Codieren eines Videostreams verwendet. Die Verwendung einer hohen Komplexitäts Stufe erfordert mehr Verarbeitungsleistung für die Codierung und Decodierung.

Jeder Codec, der Komplexitäts Einstellungen unterstützt, macht die folgenden Einstellungen verfügbar, die Sie mit der [**IWMCodecInfo3:: getcodecprop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) -Methode abrufen können.



| Einstellung                 | BESCHREIBUNG                                         |
|-------------------------|-----------------------------------------------------|
| g \_ wszcomplexitymax     | Die vom Codec unterstützte maximale Qualitätsstufe.   |
| g \_ wszcomplexityoffline | Die empfohlene Qualitätsstufe für die Offline Wiedergabe.   |
| g \_ wszcomplexitylive    | Die empfohlene Qualitätsstufe für die Streaming-Wiedergabe. |



 

Um die Komplexität für einen Videostream in einem Profil festzulegen, verwenden Sie die [**iwmpropertyvault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) -Methode mithilfe der Eigenschaft g \_ wszkomplexitäts. Der von Ihnen festgelegte Wert muss kleiner oder gleich der maximalen unterstützten Komplexität für den Codec sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Konfiguration für alle Streams**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Konfigurieren von Streams**](configuring-streams.md)
</dt> <dt>

[**Video Komplexitäts Einstellungen**](video-complexity-settings.md)
</dt> </dl>

 

 




