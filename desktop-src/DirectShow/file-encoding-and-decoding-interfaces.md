---
description: Datei Codierung und Decodierungs Schnittstellen
ms.assetid: 5456392d-2557-43b6-93b7-b2ebde218d12
title: Datei Codierung und Decodierungs Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73de2304f2b473a634127755ca900b99592ed63
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125594"
---
# <a name="file-encoding-and-decoding-interfaces"></a>Datei Codierung und Decodierungs Schnittstellen

Diese Schnittstellen unterstützen Datei Codierung und Decodierung.



| Schnittstelle                                                    | BESCHREIBUNG                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Iammediacontent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)                   | Abrufen von Metadaten aus einem Stream, z. b. Autor und Titel.                                              |
| [**Iamopenprogress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)                   | Legen Sie den Fortschritt eines Datei Öffnungs Vorgangs fest.                                                             |
| [**Iamanalysieren**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse)                                 | Fragen Sie die Analysezeit für die aktuelle Position in einem MPEG-Stream ab, und legen Sie Sie fest.                                     |
| [**Iamstreamselect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)                   | Steuern Sie, welche logischen Streams abgespielt werden, und rufen Sie Informationen zu diesen Datenströmen ab.                               |
| [**Iamvfwcompressdialogfelder**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)       | Dialogfelder anzeigen, die von VFW-Codecs bereitgestellt werden.                                                                 |
| [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)           | Legen Sie Video Komprimierungs Parameter fest.                                                                            |
| [**Iconfigasfwriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)                 | Steuern der Art und Weise, wie der [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter Dateien des erweiterten Systems formatiert |
| [**Iconfigavimux**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)                       | Steuern Sie, wie der [AVI MUX](avi-mux-filter.md) -Filter AVI-Dateien schreibt.                                       |
| [**Iconfiginterleaving**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)           | Konfigurieren Sie die über Lapp Zeit, wenn der AVI MUX-Filter AVI-Dateien schreibt.                                             |
| [**Idvenc**](/windows/desktop/api/Strmif/nn-strmif-idvenc)                                     | Legen Sie die Codierungs Auflösung für den [DV-Video Encoder](dv-video-encoder-filter.md) -Filter fest.                   |
| [**Idvsplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                           | Herabstufen der Framerate für einen Datenstrom im digitalen Video (DV)                                                      |
| [**Iipdvdec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec)                                 | Legen Sie die Decodierungs Auflösung für den [DV-Video Decoder](dv-video-decoder-filter.md) Filter fest.                   |
| [**Ipersistmediapropertybag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag) | Festlegen und Abrufen von Informations-und DISP-Blöcken in AVI-Streams.                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schnittstellen](interfaces.md)
</dt> </dl>

 

 



