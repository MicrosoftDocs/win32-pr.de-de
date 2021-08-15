---
description: MJPEG-Dekomprimierungsfilter
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: MJPEG-Dekomprimierungsfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f0587abe77d1f76df043a37bc8e54db91d65d81e00b0a2677268b6d61bc782
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684940"
---
# <a name="mjpeg-decompressor-filter"></a>MJPEG-Dekomprimierungsfilter

Dieser Filter decodiert einen Videostream von motion JPEG in unkomprimiertes Video. Einige digitale Videokameras erzeugen einen JPEG-Videostream mit Bewegung.



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Eingabepin-Medientypen                    | \_MEDIATYPE-Video, MEDIASUBTYPE \_ MJPG                                                                                                               |
| Eingabepinschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Ausgabepin-Medientypen                   | MEDIATYPE \_ VIDEO, MEDIASUBTYPE \_ NULL                                                                                                               |
| Ausgabe-PIN-Schnittstellen                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtern der CLSID                             | CLSID \_ MjpegDec                                                                                                                                    |
| Eigenschaftenseite CLSID                      | Keine Eigenschaftenseite                                                                                                                                   |
| Ausführbare Datei                               | quartz.dll                                                                                                                                         |
| [Verdienst](merit.md)                       | MERIT \_ NORMAL                                                                                                                                      |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Hinweise

Dieser Filter ist mit MOTION JPEG-Videos kompatibel, die den FOURCC-Code "MJPG" verwenden. Andere Jpeg-Bewegungsvarianten können nicht decodiert werden. Für diese müssen Sie einen Decoderfilter eines Drittanbieters verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



