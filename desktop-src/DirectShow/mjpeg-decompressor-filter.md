---
description: MJPEG-Dekomprimiererfilter
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: MJPEG-Dekomprimiererfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f0587abe77d1f76df043a37bc8e54db91d65d81e00b0a2677268b6d61bc782
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684940"
---
# <a name="mjpeg-decompressor-filter"></a>MJPEG-Dekomprimiererfilter

Dieser Filter decodiert einen Videostream von Motion JPEG in unkomprimiertes Video. Einige digitale Videokameras erzeugen einen JPEG-Videostream für Bewegung.



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Eingabepinmedientypen                    | MEDIATYPE \_ Video, MEDIASUBTYPE \_ MJPG                                                                                                               |
| Eingabe-Pin-Schnittstellen                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Medientypen des Ausgabepins                   | MEDIATYPE \_ VIDEO, MEDIASUBTYPE \_ NULL                                                                                                               |
| Ausgabe-Pin-Schnittstellen                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtern von CLSID                             | CLSID \_ MjpegDec                                                                                                                                    |
| CLSID der Eigenschaftenseite                      | Keine Eigenschaftenseite                                                                                                                                   |
| Ausführbare Datei                               | quartz.dll                                                                                                                                         |
| [Verdienst](merit.md)                       | NORMALER WERT \_                                                                                                                                      |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Hinweise

Dieser Filter ist mit jpeg-Bewegungsvideos kompatibel, die den FOURCC-Code "MJPG" verwenden. Andere Arten von Motion JPEG können nicht decodiert werden. Für diese müssen Sie einen Drittanbieter-Decoderfilter verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



