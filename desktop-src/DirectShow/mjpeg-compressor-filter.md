---
description: MJPEG-Daemon-Filter
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: MJPEG-Daemon-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a20c559bb889750959a4868fa08c03b3eb12dfb5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346200"
---
# <a name="mjpeg-compressor-filter"></a>MJPEG-Daemon-Filter

Dieser Filter komprimiert einen nicht komprimierten Videostream mithilfe der Motion JPEG-Komprimierung.



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**                                                                                                                                                                                             |
| Eingabe-PIN-Medientypen                    | MediaType- \_ Video, mediasubtype \_ null                                                                                                                                                                                                               |
| PIN-Eingabeschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Ausgabe-PIN-Medientypen                   | MediaType- \_ Video, mediasubtype \_ mjpg                                                                                                                                                                                                               |
| PIN-Schnittstellen                    | [**Iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID Filtern                             | CLSID- \_ mjpgenc                                                                                                                                                                                                                                     |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite                                                                                                                                                                                                                                   |
| Ausführbare Datei                               | quartz.dll                                                                                                                                                                                                                                         |
| [Verdienst](merit.md)                       | das Verdienst wird \_ \_ nicht \_ verwendet.                                                                                                                                                                                                                                |
| [Filter Kategorie](filter-categories.md) | CLSID \_ videocompressorcategory                                                                                                                                                                                                                     |



 

## <a name="remarks"></a>Bemerkungen

Dieser Filter codiert mithilfe des Medien Untertyps mediasubtype \_ mjpg, der dem FourCC-Code ' mjpg ' entspricht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



