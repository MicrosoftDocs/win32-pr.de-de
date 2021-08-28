---
description: Farbraumkonverterfilter
ms.assetid: a6765184-43ce-47b8-9eb1-e15af7e11c93
title: Farbraumkonverterfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cadc3f980116f6745d578a06220639b181fe13
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477366"
---
# <a name="color-space-converter-filter"></a>Farbraumkonverterfilter

Dieser Transformationsfilter konvertiert von einem RGB-Farbtyp in einen anderen RGB-Typ, z. B. zwischen 24-Bit- und 8-Bit-RGB-Farbe. Da diese Art der Konvertierung in der Regel effizienter innerhalb eines Videodekomprimierers verarbeitet wird, wird der Farbraumkonverter hauptsächlich verwendet, wenn die Streamquelle aus unkomprimierten RGB-Frames besteht.




| | | Filterschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter-| |</strong></a> Eingabepin-Medientypen | MEDIATYPE_Video, FORMAT_VideoInfo.<br /> Die folgenden Untertypen sind gültig:<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul> | | Eingabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl | |</strong></a> Ausgabepin-Medientypen | MEDIATYPE_Video, FORMAT_VideoInfo.<br /> Die folgenden Untertypen sind gültig:<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul> | | Ausgabepinschnittstellen | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl | |</strong></a> Filtern von CLSID-| CLSID_Colour | | CLSID-Eigenschaftsseite | Keine Eigenschaftenseite. | | Ausführbare | quartz.dll | | <a href="merit.md">Leistungs-|</a> MERIT_UNLIKELY | | <a href="filter-categories.md">Filterkategorie-|</a> CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




