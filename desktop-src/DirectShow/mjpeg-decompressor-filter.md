---
description: MJPEG-Dekomprimierungsfilter
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: MJPEG-Dekomprimierungsfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23a3e3c09d218a83f5243bf6702d3b5fc3ae1c16
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910018"
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
| [Verdienst](merit.md)                       | NORMALER WERT \_                                                                                                                                      |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Dieser Filter ist mit jpeg-Bewegungsvideos kompatibel, die den FOURCC-Code "MJPG" verwenden. Andere Arten von Motion JPEG können nicht decodiert werden. Für diese müssen Sie einen Drittanbieter-Decoderfilter verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



