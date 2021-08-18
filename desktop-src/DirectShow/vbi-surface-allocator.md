---
description: VBI Surface Allocator
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: VBI Surface Allocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c586c3ef135722ac259813d918dc4054617b8ae6bfb987083f0a2ceaa986067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071984"
---
# <a name="vbi-surface-allocator"></a>VBI Surface Allocator

Der VBI Surface Allocator steuert die Zuordnung von VBI-Puffern in analogen Fernsehgraphen mit Hardware-Videoporterfassungsszenarien. Bei Geräten wie dem Bt829-Decoder kann der Framepuffer mehrere VBI-Erfassungspuffer enthalten, auf die über einen proprietären hardwarebasierten Mechanismus zugegriffen wird, der allgemein als Videoport bezeichnet wird. Der VBI Surface Allocator-Filter verbindet downstream vom Erfassungsfilter und verfügt über keinen Ausgabepin. Der Filter arbeitet eng mit dem [Overlay-Mixer](overlay-mixer-filter.md) (über DirectDraw) zusammen, um koordinierte Vorgänge am Hardwarevideoport durchzuführen, wobei der gleiche eingeschränkte SVGA-Framepufferspeicher genutzt wird.



| Bezeichnung | Wert |
|------------------------------------------|-------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| Eingabepinmedientypen                    | MEDIATYPE \_ Video, MEDIASUBTYPE \_ VPVBI                                               |
| Eingabe-Pin-Schnittstellen                     | [**IKsPropertySet**](ikspropertyset.md)                                            |
| Medientypen des Ausgabepins                   | MEDIATYPE \_ NULL, MEDIASUBTYPE \_ NULL. (Nichts ist jemals mit dem Ausgabepin verbunden.) |
| Ausgabe-Pin-Schnittstellen                    | Nicht zutreffend                                                                     |
| Filtern von CLSID                             | CLSID \_ VBISurfaces                                                                  |
| CLSID der Eigenschaftenseite                      | Keine Eigenschaftenseite.                                                                   |
| Ausführbare Datei                               | vbisurf.ax                                                                          |
| [Verdienst](merit.md)                       | NORMALER WERT \_                                                                       |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



