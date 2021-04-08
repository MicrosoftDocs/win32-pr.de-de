---
description: VBI-Oberflächen Zuweisung
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: VBI-Oberflächen Zuweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4edd698ed37c7b180bee27d0a99e95096080d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757675"
---
# <a name="vbi-surface-allocator"></a>VBI-Oberflächen Zuweisung

Der VBI Surface Allocator steuert die Zuordnung von VBI-Puffern in analogen Fernseh Diagrammen mit hardwareporterfassungs-Szenarios. Bei Geräten wie dem Bt829-Decoder kann der Frame Puffer mehrere VBI-Aufzeichnungs Puffer enthalten, auf die über einen proprietären hardwarebasierten Mechanismus zugegriffen wird, der generisch als Videoport bekannt ist. Der VBI-Oberflächen Zuordnungsfilter stellt eine Downstreamverbindung mit dem Erfassungs Filter her und hat keine Ausgabe-PIN Der Filter arbeitet eng mit dem [Überlagerungs-Mixer](overlay-mixer-filter.md) (über DirectDraw) zusammen, um koordinierte Vorgänge auf dem Hardwareport durchzuführen, wobei der gleiche beschränkte SVGA-Frame Puffer Arbeitsspeicher verwendet wird.



|                                          |                                                                                     |
|------------------------------------------|-------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| Eingabe-PIN-Medientypen                    | MediaType- \_ Video, mediasubtype \_ vpvbi                                               |
| PIN-Eingabeschnittstellen                     | [**"Ikspropertyset"**](ikspropertyset.md)                                            |
| Ausgabe-PIN-Medientypen                   | MediaType \_ NULL, mediasubtype \_ NULL. (Nichts ist jemals mit der Ausgabe-PIN verbunden.) |
| PIN-Schnittstellen                    | Nicht zutreffend                                                                     |
| CLSID Filtern                             | CLSID- \_ vbioberflächen                                                                  |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite.                                                                   |
| Ausführbare Datei                               | vbisurf.ax                                                                          |
| [Verdienst](merit.md)                       | Verdienst \_ Normal                                                                       |
| [Filter Kategorie](filter-categories.md) | CLSID \_ legacyamfiltercategory                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



