---
description: VBI Surface Allocator
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: VBI Surface Allocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5849b23b8f21a7b49e477060386628ba4c19b2e5
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909008"
---
# <a name="vbi-surface-allocator"></a>VBI Surface Allocator

Der VBI Surface Allocator steuert die Zuordnung von VBI-Puffern in analogen Fernsehgraphen mit Hardwarevideoporterfassungsszenarien. Bei Geräten wie dem Bt829-Decoder kann der Framepuffer mehrere VBI-Erfassungspuffer enthalten, auf die über einen proprietären hardwarebasierten Mechanismus zugegriffen wird, der allgemein als Videoport bezeichnet wird. Der VBI Surface Allocator-Filter verbindet downstream vom Erfassungsfilter und verfügt über keinen Ausgabepin. Der Filter arbeitet eng mit dem [Overlay-Mixer](overlay-mixer-filter.md) (über DirectDraw) zusammen, um koordinierte Vorgänge am Hardwarevideoport durchzuführen, wobei der gleiche eingeschränkte SVGA-Framepufferspeicher genutzt wird.



| Bezeichnung | Wert |
|------------------------------------------|-------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| Eingabe-Stecknadelmedientypen                    | MEDIATYPE \_ Video, MEDIASUBTYPE \_ VPVBI                                               |
| Eingabe-Pin-Schnittstellen                     | [**IKsPropertySet**](ikspropertyset.md)                                            |
| Medientypen des Ausgabepins                   | MEDIATYPE \_ NULL, MEDIASUBTYPE \_ NULL. (Nichts ist jemals mit dem Ausgabepin verbunden.) |
| Ausgabe-Pin-Schnittstellen                    | Nicht zutreffend                                                                     |
| Filtern von CLSID                             | CLSID \_ VBISurfaces                                                                  |
| CLSID der Eigenschaftenseite                      | Keine Eigenschaftenseite.                                                                   |
| Ausführbare Datei                               | vbisurf.ax                                                                          |
| [Verdienst](merit.md)                       | MERIT \_ NORMAL                                                                       |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



