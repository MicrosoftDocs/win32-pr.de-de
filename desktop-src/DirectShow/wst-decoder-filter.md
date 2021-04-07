---
description: WST-Decoderfilter
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: WST-Decoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f2d20873ff9a5e7c009c4a84f7a23c273d6590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863383"
---
# <a name="wst-decoder-filter"></a>WST-Decoderfilter

Diese Komponente wurde aus Windows Vista und höheren Betriebssystemen entfernt. Es ist für die Verwendung in den Betriebssystemen Windows XP und Windows Server 2003 verfügbar.

> [!Note]  
> Ab Windows Vista bietet DirectShow keinen Filter zum Decodieren von "World Standard Teletext (WST)".

 

Der WST-Decoder ist ein kernelmodusfilter, der decodierte World Standard-Teletextdaten aus dem [WST-Codec](wst-codec-filter.md) akzeptiert und die Bitmaps mit den von Microsoft bereitgestellten Schriftarten an Pin 2 auf dem [Overlay-Mixer](overlay-mixer-filter.md) übergibt. Zurzeit werden nur westeuropäische Sprachen unterstützt. Zurzeit werden keine Unicode-Schriftarten bereitgestellt.

Dieser Filter kann durch Aufrufen von [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)mithilfe der Ausgabe-PIN des WST-Codecs automatisch dem Diagramm hinzugefügt werden.



|                                          |                                                               |
|------------------------------------------|---------------------------------------------------------------|
| Filter Schnittstellen                        | ISpecifyPropertyPages, [ **iamwstdecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder) |
| Eingabe-PIN-Medientypen                    | MediaType \_ VBI, mediasubtype \_ Teletext                        |
| PIN-Eingabeschnittstellen                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| Ausgabe-PIN-Medientypen                   | MediaType- \_ Video                                              |
| PIN-Schnittstellen                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| CLSID Filtern                             | CLSID- \_ wstdecoder                                             |
| CLSID der Eigenschaften Seite                      | CLSID \_ wstdecoderpropertypage                                 |
| Ausführbare Datei                               | Wstdecod.DLL                                                  |
| [Verdienst](merit.md)                       | Verdienst \_ Normal                                                 |
| [Filter Kategorie](filter-categories.md) | CLSID \_ legacyamfiltercategory                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Anzeigen von World Standard-Teletext](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



