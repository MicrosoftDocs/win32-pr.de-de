---
description: MJPEG-Filter
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: MJPEG-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02928df4d09b50c0ac152aed99ed87dc6362fb70
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910008"
---
# <a name="mjpeg-compressor-filter"></a>MJPEG-Filter

Dieser Filter komprimiert einen unkomprimierten Videostream mithilfe der JPEG-Komprimierung für Bewegung.



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**                                                                                                                                                                                             |
| Eingabe-Stecknadelmedientypen                    | MEDIATYPE \_ VIDEO, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                               |
| Eingabe-Pin-Schnittstellen                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Medientypen des Ausgabepins                   | MEDIATYPE \_ Video, MEDIASUBTYPE \_ MJPG                                                                                                                                                                                                               |
| Ausgabe-Pin-Schnittstellen                    | [**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMVideoCompression,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtern von CLSID                             | CLSID \_ MJPGEnc                                                                                                                                                                                                                                     |
| CLSID der Eigenschaftenseite                      | Keine Eigenschaftenseite                                                                                                                                                                                                                                   |
| Ausführbare Datei                               | quartz.dll                                                                                                                                                                                                                                         |
| [Verdienst](merit.md)                       | NICHT \_ \_ VERWENDEN \_                                                                                                                                                                                                                                |
| [Filterkategorie](filter-categories.md) | CLSID \_ VideoCompressorCategory                                                                                                                                                                                                                     |



 

## <a name="remarks"></a>Bemerkungen

Dieser Filter codiert mithilfe des Medienuntertyps MEDIASUBTYPE MJPG, der dem \_ FOURCC-Code "MJPG" entspricht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



