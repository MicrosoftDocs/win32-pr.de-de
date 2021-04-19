---
description: Filter für Vollbild-Renderer
ms.assetid: 59332096-bdfe-4208-b99a-1f434652f287
title: Filter für Vollbild-Renderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d580442887896f271b0f5b7fea5f7a33553f53f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346385"
---
# <a name="full-screen-renderer-filter"></a>Filter für Vollbild-Renderer

Der Vollbild-Renderer-Filter bietet Vollbild-Video Rendering auf älterer Hardware. Neuere Grafikkarten können das Video so effizient gestalten, dass der Vollbild-Renderer nicht erforderlich ist. Daher ist die Verwendung dieses Filters nun veraltet.

Fügen Sie diesen Filter nicht manuell zum Filter Diagramm hinzu. Wenn eine Anwendung [**IVideoWindow::p UT \_ Fullscreenmode**](/windows/desktop/api/Control/nf-control-ivideowindow-put_fullscreenmode)aufruft, wählt der Filter Graph-Manager automatisch den entsprechenden Videorenderer für den Vollbildmodus aus. Die Auswahl ist für die Anwendung transparent. Bei aktuellen Grafikkarten ist es unwahrscheinlich, dass der Filter Graph-Manager den vollbildrenderer auswählt.



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ifullscreenvideoex**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-ifullscreenvideoex), [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**iqualprop**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) |
| Eingabe-PIN-Medientypen                    | MediaType- \_ Video, mediasubtype \_ null                                                                                                                                                                                                               |
| PIN-Eingabeschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Ausgabe-PIN-Medientypen                   | Nicht verfügbar                                                                                                                                                                                                                                     |
| PIN-Schnittstellen                    | Nicht verfügbar                                                                                                                                                                                                                                     |
| CLSID Filtern                             | CLSID- \_ modexrenderer                                                                                                                                                                                                                               |
| CLSID der Eigenschaften Seite                      | CLSID- \_ modexproperties                                                                                                                                                                                                                             |
| Ausführbare Datei                               | quartz.dll                                                                                                                                                                                                                                         |
| [Verdienst](merit.md)                       | nicht \_ wahrscheinlich                                                                                                                                                                                                                                    |
| [Filter Kategorie](filter-categories.md) | CLSID \_ legacyamfiltercategory                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Der Vollbild-Renderer unterstützt einen statischen Satz von Anzeigemodi. Die Grafikkarte im System des Benutzers unterstützt jedoch möglicherweise nicht jeden Modus. Um zu ermitteln, ob die Karte einen bestimmten Modus unterstützt, müssen Sie die [**ifullscreenvideoex:: ismodeavailable**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-ismodeavailable) -Methode aufrufen. Sie können einen bestimmten Anzeigemodus auch Programm gesteuert deaktivieren, indem Sie [**ifullscreenvideoex:: abtenabled**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-setenabled)aufrufen. Der Vollbild-Renderer unterstützt derzeit die Anzeigemodi in der folgenden Tabelle:



|      |       |        |           |
|------|-------|--------|-----------|
| Mode | Breite | Höhe | Bittiefe |
| 0    | 320   | 200    | 16        |
| 1    | 320   | 200    | 8         |
| 2    | 320   | 240    | 16        |
| 3    | 320   | 240    | 8         |
| 4    | 640   | 400    | 16        |
| 5    | 640   | 400    | 8         |
| 6    | 640   | 480    | 16        |
| 7    | 640   | 480    | 8         |
| 8    | 800   | 600    | 16        |
| 9    | 800   | 600    | 8         |
| 10   | 1024  | 768    | 16        |
| 11   | 1024  | 768    | 8         |
| 12   | 1152  | 864    | 16        |
| 13   | 1152  | 864    | 8         |
| 14   | 1280  | 1024   | 16        |
| 15   | 1280  | 1024   | 8         |



 

(Alle Modi sind RGB.) Diese Liste kann jedoch geändert werden. Verwenden Sie die [**ifullscreenvideoex:: getmodeinfo**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-getmodeinfo) -Methode, um Informationen zu den Modi zu erhalten. Der Vollbild-Renderer wählt immer den Modus mit der niedrigsten Auflösung aus, der durch eine Eigenschaft namens " *Clip Faktor*" begrenzt ist, die bestimmt, wie viel des Videos der Vollbild-Renderer Ausschneiden darf. Weitere Informationen finden Sie unter [**ifullscreenvideoex:: getclipfactor**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-getclipfactor).

Wenn die Anwendung das Filter Diagramm ausführt oder anhält, schaltet der vollbildrenderer in den ausgewählten Anzeigemodus um. Wenn das Diagramm angehalten wird, stellt der vollbildrenderer den ursprünglichen Anzeigemodus wieder her.

Der vollbildrenderer kann nur als aktives Vordergrund Fenster fungieren. Wenn der Benutzer zu einer anderen Anwendung wechselt, verbirgt der Vollbild-Renderer das Video durch minimieren oder Ausblenden des Videofensters.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



