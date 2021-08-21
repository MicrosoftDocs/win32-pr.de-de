---
description: MJPEG-Filter "Filter für Filter"
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: MJPEG-Filter "Filter für Filter"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7891a85aa32b0ec7572a8c3be08f216c75f8655a7782261a675521aa952bf40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791390"
---
# <a name="mjpeg-compressor-filter"></a>MJPEG-Filter "Filter für Filter"

Dieser Filter komprimiert einen unkomprimierten Videostream unter Verwendung der JPEG-Bewegungskomprimierung.



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**                                                                                                                                                                                             |
| Eingabepin-Medientypen                    | MEDIATYPE \_ VIDEO, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                               |
| Eingabepinschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Ausgabepin-Medientypen                   | \_MEDIATYPE-Video, MEDIASUBTYPE \_ MJPG                                                                                                                                                                                                               |
| Ausgabe-PIN-Schnittstellen                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtern der CLSID                             | CLSID \_ MJPGEnc                                                                                                                                                                                                                                     |
| Eigenschaftenseite CLSID                      | Keine Eigenschaftenseite                                                                                                                                                                                                                                   |
| Ausführbare Datei                               | quartz.dll                                                                                                                                                                                                                                         |
| [Verdienst](merit.md)                       | NICHT \_ \_ VERWENDEN \_                                                                                                                                                                                                                                |
| [Filterkategorie](filter-categories.md) | CLSID \_ VideoCompressorCategory                                                                                                                                                                                                                     |



 

## <a name="remarks"></a>Hinweise

Dieser Filter codiert mithilfe des Medienuntertyps MEDIASUBTYPE MJPG, der dem \_ FOURCC-Code "MJPG" entspricht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



