---
description: Dateicodierungs- und Decodierungsschnittstellen
ms.assetid: 5456392d-2557-43b6-93b7-b2ebde218d12
title: Dateicodierungs- und Decodierungsschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6654497b0d2407666b286fb74f06a91e66834cfb963b62b7e22eb5755fa30b0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639660"
---
# <a name="file-encoding-and-decoding-interfaces"></a>Dateicodierungs- und Decodierungsschnittstellen

Diese Schnittstellen unterstützen die Dateicodierung und -decodierung.



| Schnittstelle                                                    | BESCHREIBUNG                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)                   | Rufen Sie Metadaten aus einem Stream ab, z. B. den Autor und titel.                                              |
| [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)                   | Bestimmen Sie den Status eines Dateiöffnungsvorgang.                                                             |
| [**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse)                                 | Fragen Sie die Analysezeit für die aktuelle Position in einem MPEG-Stream ab, und legen Sie sie fest.                                     |
| [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)                   | Steuern Sie, welche logischen Streams abgespielt werden, und rufen Sie Informationen darüber ab.                               |
| [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)       | Anzeigen von Dialogfeldern, die von VFW-Codecs bereitgestellt werden.                                                                 |
| [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)           | Legen Sie Parameter für die Videokomprimierung fest.                                                                            |
| [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)                 | Steuern Sie, wie [der WM ASF Writer-Filter](wm-asf-writer-filter.md) ASF-Dateien (Advanced Systems Format) schreibt. |
| [**IConfigAviMux**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)                       | Steuern Sie, wie [der AVI Mux-Filter](avi-mux-filter.md) AVI-Dateien schreibt.                                       |
| [**IConfigInterleaving**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)           | Konfigurieren Sie die Überlappung, wenn der AVI Mux-Filter AVI-Dateien schreibt.                                             |
| [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc)                                     | Legen Sie die Codierungsauflösung für den [DV Video Encoder-Filter](dv-video-encoder-filter.md) fest.                   |
| [**IDVSplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                           | Herabstufen der Bildfrequenz für einen Digitalen Videostream (DV)                                                      |
| [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec)                                 | Legen Sie die Decodierungsauflösung für den [DV-Videodecoderfilter](dv-video-decoder-filter.md) fest.                   |
| [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag) | Legen Sie INFO- und DISP-Block in AVI-Streams fest, und rufen Sie sie ab.                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schnittstellen](interfaces.md)
</dt> </dl>

 

 



