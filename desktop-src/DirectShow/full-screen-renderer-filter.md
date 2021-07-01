---
description: Vollbild-Rendererfilter
ms.assetid: 59332096-bdfe-4208-b99a-1f434652f287
title: Vollbild-Rendererfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d331ff6f31d1c985c7e255b23381a289931da60
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120475"
---
# <a name="full-screen-renderer-filter"></a>Vollbild-Rendererfilter

Der Filter Vollbildrenderer ermöglicht das Rendern von Vollbildvideos auf älterer Hardware. Neuere Grafikkarten können das Video so effizient strecken, dass der Vollbildrenderer nicht erforderlich ist. Daher ist die Verwendung dieses Filters jetzt veraltet.

Fügen Sie diesen Filter nicht manuell zum Filterdiagramm hinzu. Wenn eine Anwendung [**IVideoWindow::p ut \_ FullScreenMode**](/windows/desktop/api/Control/nf-control-ivideowindow-put_fullscreenmode)aufruft, wählt der Filter Graph Manager automatisch den entsprechenden Videorenderer für den Vollbildmodus aus. Die Auswahl ist für die Anwendung transparent. Bei aktuellen Grafikkarten ist es unwahrscheinlich, dass der Filter Graph Manager den Vollbildrenderer auswählt.



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IFullScreenVideoEx,**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-ifullscreenvideoex) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) |
| Eingabe-Stecknadelmedientypen                    | MEDIATYPE \_ Video, MEDIASUBTYPE \_ Null                                                                                                                                                                                                               |
| Eingabe-Pin-Schnittstellen                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Medientypen des Ausgabepins                   | Nicht zutreffend                                                                                                                                                                                                                                     |
| Ausgabe-Pin-Schnittstellen                    | Nicht zutreffend                                                                                                                                                                                                                                     |
| Filtern von CLSID                             | CLSID \_ ModexRenderer                                                                                                                                                                                                                               |
| CLSID der Eigenschaftenseite                      | CLSID \_ ModexProperties                                                                                                                                                                                                                             |
| Ausführbare Datei                               | quartz.dll                                                                                                                                                                                                                                         |
| [Verdienst](merit.md)                       | \_UNWAHRSCHEINLICHE WAHRSCHEINLICHKEIT                                                                                                                                                                                                                                    |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Der Vollbildrenderer unterstützt einen statischen Satz von Anzeigemodi. Die Grafikkarte auf dem System des Benutzers unterstützt jedoch möglicherweise nicht jeden Modus. Um zu bestimmen, ob die Karte einen bestimmten Modus unterstützt, rufen Sie die [**IFullScreenVideoEx::IsModeAvailable-Methode**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-ismodeavailable) auf. Sie können einen bestimmten Anzeigemodus auch programmgesteuert deaktivieren, indem Sie [**IFullScreenVideoEx::SetEnabled**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-setenabled)aufrufen. Der Vollbildrenderer unterstützt derzeit die in der folgenden Tabelle gezeigten Anzeigemodi:



| Mode | Breite | Höhe | Bittiefe |
|------|-------|--------|-----------|
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



 

(Alle Modi sind RGB.) Diese Liste kann jedoch geändert werden. Verwenden Sie die [**IFullScreenVideoEx::GetModeInfo-Methode,**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-getmodeinfo) um Informationen zu den Modi abzurufen. Der Vollbildrenderer wählt immer den verfügbaren Modus mit der niedrigsten Auflösung aus, der durch eine Eigenschaft namens *Clipfaktor* eingeschränkt wird. Dadurch wird bestimmt, wie viel Video der Vollbildrenderer ausschneiden darf. Weitere Informationen finden Sie unter [**IFullScreenVideoEx::GetClipFactor**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-getclipfactor).

Wenn die Anwendung den Filtergraphen ausführt oder an hält, wechselt der Vollbildrenderer zum ausgewählten Anzeigemodus. Wenn das Diagramm beendet wird, stellt der Vollbildrenderer den ursprünglichen Anzeigemodus wieder her.

Der Vollbildrenderer kann nur als aktives Vordergrundfenster fungieren. Wenn der Benutzer zu einer anderen Anwendung wechselt, blendet der Vollbildrenderer das Video aus, indem das Videofenster minimiert oder ausgeblendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



