---
description: AVI-160-Filter
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: AVI-160-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212ab58eb3800e0ad5531ebc5c50d3b054e7866c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909468"
---
# <a name="avi-compressor-filter"></a>AVI-160-Filter

Mit dem FILTER AVI-Filter können Codecs des Videokomprimierungs-Managers (Video Compression Manager, VCM) einem Filterdiagramm beitreten. Jeder Codec wird als separate Instanz des Filters angezeigt. Sie können diesen Filter nicht direkt mit CoCreateInstance erstellen. Stattdessen müssen Sie den Systemgeräte-Enumerator verwenden. Weitere Informationen finden Sie unter [Verwenden des Systemgeräte-Enumerators](using-the-system-device-enumerator.md).

Der Eingabepin des Filters stellt eine Verbindung mit Filtern her, die nicht komprimierte Videodaten ausgeben, z. B. Videoaufnahmefilter oder [den AVI-Splitterfilter.](avi-splitter-filter.md) Der Ausgabepin des Filters stellt in der Regel eine Verbindung mit einem MUX-Filter her, z. B. mit dem [AVI Mux-Filter.](avi-mux-filter.md)

Wenn der Codec ein VFW-Konfigurationsdialogfeld im alten Stil oder das Dialogfeld About unterstützt, kann eine Anwendung es über die [**IAMVfwCompressDialogs-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) anzeigen.

> [!Note]  
> MPEG-Komprimierungsfilter werden nie als VCM-Codecs implementiert, sondern nur als native DirectShow-Filter.

 



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages                                                                                                             |
| Eingabe-Stecknadelmedientypen                    | MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                               |
| Eingabe-Pin-Schnittstellen                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Medientypen des Ausgabepins                   | MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                               |
| Ausgabe-PIN-Schnittstellen                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtern der CLSID                             | Nicht zutreffend                                                                                                                                                                                                                                     |
| Eigenschaftenseite CLSID                      | Keine Eigenschaftenseite.                                                                                                                                                                                                                                  |
| Ausführbare Datei                               | qcap.dll                                                                                                                                                                                                                                           |
| [Verdienst](merit.md)                       | NICHT \_ \_ VERWENDEN \_                                                                                                                                                                                                                                |
| [Filterkategorie](filter-categories.md) | CLSID \_ VideoCompressorCategory                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



