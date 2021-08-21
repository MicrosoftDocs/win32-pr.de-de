---
description: AVI-Filter
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: AVI-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa074f5ad4a72fe1e1a32f45baa4888a526b1a0532a562c2fadb7753ea71e0aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159272"
---
# <a name="avi-compressor-filter"></a>AVI-Filter

Mit dem FILTER AVI-Filter können Codecs des Videokomprimierungs-Managers (Video Compression Manager, VCM) einem Filterdiagramm beitreten. Jeder Codec wird als separate Instanz des Filters angezeigt. Sie können diesen Filter nicht direkt mit CoCreateInstance erstellen. Stattdessen müssen Sie den Systemgeräte-Enumerator verwenden. Weitere Informationen finden Sie unter [Verwenden des Systemgeräte-Enumerators](using-the-system-device-enumerator.md).

Der Eingabepin des Filters stellt eine Verbindung mit Filtern her, die nicht komprimierte Videodaten ausgeben, z. B. Videoaufnahmefilter oder [den AVI-Splitterfilter.](avi-splitter-filter.md) Der Ausgabepin des Filters stellt in der Regel eine Verbindung mit einem MUX-Filter her, z. B. mit dem [AVI Mux-Filter.](avi-mux-filter.md)

Wenn der Codec ein VFW-Konfigurationsdialogfeld im alten Stil oder das Dialogfeld About unterstützt, kann eine Anwendung es über die [**IAMVfwCompressDialogs-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) anzeigen.

> [!Note]  
> MPEG-Komprimierungsfilter werden nie als VCM-Codecs implementiert, sondern nur als native DirectShow-Filter.

 



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages                                                                                                             |
| Eingabepinmedientypen                    | MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                               |
| Eingabe-Pin-Schnittstellen                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Medientypen des Ausgabepins                   | MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                               |
| Ausgabe-Pin-Schnittstellen                    | [**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMVideoCompression,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtern von CLSID                             | Nicht zutreffend                                                                                                                                                                                                                                     |
| CLSID der Eigenschaftenseite                      | Keine Eigenschaftenseite.                                                                                                                                                                                                                                  |
| Ausführbare Datei                               | qcap.dll                                                                                                                                                                                                                                           |
| [Verdienst](merit.md)                       | NOT USE (NICHT \_ \_ \_ VERWENDEN)                                                                                                                                                                                                                                |
| [Filterkategorie](filter-categories.md) | CLSID \_ VideoCompressorCategory                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



