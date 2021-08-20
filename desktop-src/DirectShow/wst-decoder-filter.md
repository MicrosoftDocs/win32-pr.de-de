---
description: WST-Decoderfilter
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: WST-Decoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d61da0540c683e8c4646074715b0518717b4e1958beea5b8ca2ae41fb4629790
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290770"
---
# <a name="wst-decoder-filter"></a>WST-Decoderfilter

Diese Komponente wurde aus den Betriebssystemen Windows Vista und höher entfernt. Es ist für die Verwendung in den Betriebssystemen Windows XP und Windows Server 2003 verfügbar.

> [!Note]  
> Ab Windows Vista stellt DirectShow keinen Filter zum Decodieren von World Standard Teletext (WST) zur Verfügung.

 

Der WST-Decoder ist ein Kernelmodusfilter, der decodierte World Standard Teletext-Daten aus dem [WST-Codec](wst-codec-filter.md) akzeptiert und die Bitmaps mithilfe der von Microsoft bereitgestellten Schriftarten an Pin 2 auf dem [Overlay](overlay-mixer-filter.md) Mixer übermittelt. Derzeit werden nur weste europäische Sprachen unterstützt. Derzeit werden keine Unicode-Schriftarten bereitgestellt.

Dieser Filter kann dem Diagramm automatisch hinzugefügt werden, indem [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)mithilfe des Ausgabepins des WST-Codecs aufruft.



| Bezeichnung | Wert |
|------------------------------------------|---------------------------------------------------------------|
| Filterschnittstellen                        | ISpecifyPropertyPages, [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder) |
| Eingabepin-Medientypen                    | MEDIATYPE \_ VBI, MEDIASUBTYPE \_ TELETEXT                        |
| Eingabepinschnittstellen                     | [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| Ausgabepin-Medientypen                   | \_MEDIATYPE-Video                                              |
| Ausgabe-PIN-Schnittstellen                    | [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| Filtern der CLSID                             | CLSID \_ WSTDecoder                                             |
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

 

 



