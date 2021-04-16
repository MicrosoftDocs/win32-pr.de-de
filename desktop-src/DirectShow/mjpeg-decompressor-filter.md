---
description: MJPEG-Debug-Filter
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: MJPEG-Debug-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebe8f5f19cb94d75c1ce01cd94dc723100560de
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522456"
---
# <a name="mjpeg-decompressor-filter"></a>MJPEG-Debug-Filter

Dieser Filter decodiert einen Videostream von Motion JPEG in unkomprimiertes Video. Einige digitale Videokameras entwickeln einen Videodaten Strom in Motion JPEG.



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Eingabe-PIN-Medientypen                    | MediaType- \_ Video, mediasubtype \_ mjpg                                                                                                               |
| PIN-Eingabeschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Ausgabe-PIN-Medientypen                   | MediaType- \_ Video, mediasubtype \_ null                                                                                                               |
| PIN-Schnittstellen                    | [**Imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID Filtern                             | CLSID- \_ mjpgdec                                                                                                                                    |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite                                                                                                                                   |
| Ausführbare Datei                               | quartz.dll                                                                                                                                         |
| [Verdienst](merit.md)                       | Verdienst \_ Normal                                                                                                                                      |
| [Filter Kategorie](filter-categories.md) | CLSID \_ legacyamfiltercategory                                                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Dieser Filter ist kompatibel mit dem Motion JPEG-Video, das den FourCC-Code "mjpg" verwendet. Andere Varianten von Motion JPEG können nicht decodiert werden. Hierzu müssen Sie einen Drittanbieter-Decoder-Filter verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



