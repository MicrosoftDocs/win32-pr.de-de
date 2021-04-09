---
description: AVI-Kompressor-Filter
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: AVI-Kompressor-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3ef342d1ea740503d9fc1e9e9b898aadc3801
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103859967"
---
# <a name="avi-compressor-filter"></a>AVI-Kompressor-Filter

Der AVI-Kompressor-Filter ermöglicht die Verknüpfung von Video Komprimierungs-Manager-Codecs (VCM) mit einem Filter Diagramm. Jeder Codec wird als separate Instanz des Filters angezeigt. Dieser Filter kann nicht direkt mit cokreatanstance erstellt werden. Stattdessen müssen Sie den Enumerator für Systemgeräte verwenden. Weitere Informationen finden Sie unter [using the System Device Enumerator](using-the-system-device-enumerator.md).

Die Eingabe-PIN des Filters stellt eine Verbindung mit Filtern her, die unkomprimierte Videodaten ausgeben, z. b. Video Erfassungs Filter oder den [avi-Splitter Filter](avi-splitter-filter.md) Die Ausgabepin des Filters stellt in der Regel eine Verbindung mit einem MUX-Filter her, z. b. dem [AVI MUX](avi-mux-filter.md)

Wenn der Codec ein Dialogfeld oder ein Dialogfeld für eine VFW-Konfiguration im alten Stil unterstützt, kann eine Anwendung Sie mithilfe der [**iamvfwcompressdialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) -Schnittstelle anzeigen.

> [!Note]  
> MPEG-Kompressoren werden nie als VCM-Codecs implementiert, sondern nur als Native DirectShow-Filter.

 



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Iamvfwcompressdialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages                                                                                                             |
| Eingabe-PIN-Medientypen                    | MediaType- \_ Video, mediasubtype \_ null                                                                                                                                                                                                               |
| PIN-Eingabeschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Ausgabe-PIN-Medientypen                   | MediaType- \_ Video, mediasubtype \_ null                                                                                                                                                                                                               |
| PIN-Schnittstellen                    | [**Iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID Filtern                             | Nicht verfügbar                                                                                                                                                                                                                                     |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite.                                                                                                                                                                                                                                  |
| Ausführbare Datei                               | qcap.dll                                                                                                                                                                                                                                           |
| [Verdienst](merit.md)                       | das Verdienst wird \_ \_ nicht \_ verwendet.                                                                                                                                                                                                                                |
| [Filter Kategorie](filter-categories.md) | CLSID \_ videocompressorcategory                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



