---
description: WST-Decoderfilter
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: WST-Decoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb6804f82e5d15aa324feb163261544969e3c45
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908478"
---
# <a name="wst-decoder-filter"></a>WST-Decoderfilter

Diese Komponente wurde aus Windows Vista und späteren Betriebssystemen entfernt. Es ist für die Verwendung in den Betriebssystemen Windows XP und Windows Server 2003 verfügbar.

> [!Note]  
> Ab Windows Vista stellt DirectShow keinen Filter zum Decodieren von World Standard Teletext (WST) bereit.

 

Der WST-Decoder ist ein Kernelmodusfilter, der decodierte World Standard Teletext-Daten vom [WST-Codec](wst-codec-filter.md) akzeptiert und die Bitmaps mit von Microsoft bereitgestellten Schriftarten an Pin 2 auf dem [Overlay-Mixer](overlay-mixer-filter.md) übermittelt. Derzeit werden nur westepäische Sprachen unterstützt. Derzeit werden keine Unicode-Schriftarten bereitgestellt.

Dieser Filter kann dem Graphen automatisch hinzugefügt werden, indem [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)mithilfe des Ausgabepins des WST-Codecs aufgerufen wird.



| Bezeichnung | Wert |
|------------------------------------------|---------------------------------------------------------------|
| Filterschnittstellen                        | ISpecifyPropertyPages, [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder) |
| Eingabe-Stecknadelmedientypen                    | MEDIATYPE \_ VBI, MEDIASUBTYPE \_ TELETEXT                        |
| Eingabe-Pin-Schnittstellen                     | [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| Medientypen des Ausgabepins                   | \_MEDIATYPE-Video                                              |
| Ausgabe-Pin-Schnittstellen                    | [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| Filtern von CLSID                             | CLSID \_ WSTDecoder                                             |
| Eigenschaftenseite CLSID                      | CLSID \_ WstDecoderPropertyPage                                 |
| Ausführbare Datei                               | Wstdecod.DLL                                                  |
| [Verdienst](merit.md)                       | MERIT \_ NORMAL                                                 |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Viewing World Standard Teletext](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



