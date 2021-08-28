---
description: Farbraumkonverterfilter
ms.assetid: a6765184-43ce-47b8-9eb1-e15af7e11c93
title: Farbraumkonverterfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c0a519772a6d38971654cb92a895fcd95f5ecc8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987063"
---
# <a name="color-space-converter-filter"></a>Farbraumkonverterfilter

Dieser Transformationsfilter konvertiert von einem RGB-Farbtyp in einen anderen RGB-Typ, z. B. zwischen 24-Bit- und 8-Bit-RGB-Farbe. Da diese Art der Konvertierung in der Regel effizienter innerhalb eines Videodekomprimierers verarbeitet wird, wird der Farbraumkonverter hauptsächlich verwendet, wenn die Streamquelle aus unkomprimierten RGB-Frames besteht.




| Bezeichnung | Wert |
|--------|-------|
| Filterschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | 
| Eingabepin-Medientypen | MEDIATYPE_Video, FORMAT_VideoInfo.<br /> Die folgenden Untertypen sind gültig:<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul> | 
| Eingabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Ausgabepin-Medientypen | MEDIATYPE_Video, FORMAT_VideoInfo.<br /> Die folgenden Untertypen sind gültig:<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul> | 
| Ausgabe-PIN-Schnittstellen | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Filtern der CLSID | CLSID_Colour | 
| Eigenschaftenseite CLSID | Keine Eigenschaftenseite. | 
| Ausführbare Datei | quartz.dll | 
| <a href="merit.md">Verdienst</a> | MERIT_UNLIKELY | 
| <a href="filter-categories.md">Filterkategorie</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




