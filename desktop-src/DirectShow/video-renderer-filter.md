---
description: Videorendererfilter
ms.assetid: 7719ed9d-e3b9-4c84-b587-4e120b5cabf8
title: Videorendererfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca3becb4fbdbb52a9968481aade07d14d963828
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908418"
---
# <a name="video-renderer-filter"></a>Videorendererfilter

Der Videorenderer-Filter ist ein robuster, allzweckbasierter Videorenderer.

> [!Note]  
> Unter Windows XP und höher ist der Standardvideorenderer der [Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7). DIE VMR-7 und der Videorenderer haben jeweils den Anzeigenamen "Videorenderer". Auf früheren Plattformen ist der Videorenderer der Standardrenderer. Weitere Informationen finden Sie unter [Auswählen des richtigen Renderers.](choosing-the-right-renderer.md)

 

Der Videorenderer verwendet DirectDraw und Überlagerungsoberflächen, wenn diese von der Grafikkarte unterstützt werden. Der Filtergraph-Manager macht die [**IVideoWindow-Schnittstelle**](/windows/desktop/api/Control/nn-control-ivideowindow) verfügbar, mit der Anwendungen Eigenschaften für den Videorenderer festlegen und abrufen können. Bei neueren Grafikkarten unterstützt der Videorenderer das Vollbildrendering. Andernfalls wechselt der Filter Graph-Manager automatisch zum [Vollbild-Rendererfilter](full-screen-renderer-filter.md) für den Vollbildmodus. Weitere Informationen finden Sie unter [**IVideoWindow::p ut \_ FullScreenMode.**](/windows/desktop/api/Control/nf-control-ivideowindow-put_fullscreenmode)

-   \[! Wichtig\]  
    > Normalerweise verarbeitet das Videofenster dieses Filters Nachrichten in einem Arbeitsthread, der vom Filtergraph-Manager erstellt wurde. Howerver: Wenn eine Anwendung den Filter direkt mit **CoCreateInstance** erstellt, verarbeitet das Videofenster Nachrichten im Anwendungsthread. In diesem Fall muss der Anwendungsthread über eine Nachrichtenschleife verfügen, um Nachrichten an das Videofenster zu senden. Außerdem darf der Thread erst nach dem letzten **Releaseaufruf** des Videorenderers beendet werden, der auftritt, wenn der Filtergraph-Manager heruntergefahren wird. Andernfalls kann die Anwendung zu einem Deadlock führen.

     



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo), [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2), [**IDirectDrawVideo**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo), [**IKsPropertySet**](ikspropertyset.md), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop), [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) |
| Eingabepin-Medientypen                    | Unkomprimierte Videoformate.                                                                                                                                                                                                                                                                                                                                                                              |
| Eingabepinschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                                                                                           |
| Ausgabepin-Medientypen                   | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                          |
| Ausgabe-PIN-Schnittstellen                    | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                          |
| Filtern der CLSID                             | CLSID \_ VideoRenderer                                                                                                                                                                                                                                                                                                                                                                                     |
| Eigenschaftenseite CLSID                      | Keine Eigenschaftenseite.                                                                                                                                                                                                                                                                                                                                                                                        |
| Ausführbare Datei                               | quartz.dll                                                                                                                                                                                                                                                                                                                                                                                               |
| [Verdienst](merit.md)                       | Windows XP und höher: **UNWAHRSCHEINLICHER \_ UNWAHRSCHEINLICHER**                                                                                                                                                                                                                                                                                                                                                                |
| [Filterkategorie](filter-categories.md) | **CLSID \_ LegacyAmFilterCategory**                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Bemerkungen

Wenn in der Debugversion von Quartz.dll die LOG TRACE-Debugebene auf 5 oder höher festgelegt ist, zeigt der Videorenderer die Zeitstempel der einzelnen Frames im \_ Videofenster an. Diese Zahlen werden in der Verkaufsversion der DLL nicht angezeigt. Weitere Informationen finden Sie unter [Debugausgabefunktionen](debug-output-functions.md).

Die folgenden Hinweise sind für Filterentwickler vorgesehen:

Der Videorenderer akzeptiert YUV-Formate, wenn die Grafikkarte YUV-Überlagerungsoberflächen unterstützt. Beim ersten Herstellen einer Verbindung mit dem Upstreamfilter benötigt der Videorenderer jedoch ein RGB-Format, das der Farbtiefe der aktuellen Monitoreinstellungen entspricht. Wenn die aktuelle Anzeigeeinstellung beispielsweise eine 24-Bit-Farbe hat, muss der Upstreamfilter 24-Bit-RGB-Video bereitstellen können. Wenn das Filterdiagramm in den Ausführungszustand wechselt, handelt der Videorenderer eine dynamische Formatänderung in den entsprechenden YUV-Farbraum aus.

Durch herstellen einer Verbindung mit einem RGB-Typ stellt der Videorenderer sicher, dass er GDI verwenden kann, falls DirectDraw nicht verfügbar ist. Sie wechselt zu GDI, wenn eine andere Anwendung den Videospeicher verwendet, wenn das Videorechteck zwei Monitore auf einem System mit mehreren Monitoren umgeht oder wenn das Videorechteck vollständig durch ein anderes Fenster verdeckt wird.

> [!Note]  
> Der Video Mixing Renderer führt diese Art dynamischer Formatänderungen nicht durch und erfordert keinen RGB-Medientyp, da er GDI nie für das Rendering verwendet.

 

Um eine Formatänderung auszuhandeln, ruft der Videorenderer [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) mit dem neuen Medientyp auf. Wenn der Upstreamfilter S \_ OK zurückgibt, fügt der Videorenderer die neuen Medien an das nächste Beispiel an. Der Upstreamfilter sollte [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) für jedes Beispiel aufrufen. Wenn **GetMediaType** einen Wert ungleich **NULL** zurückgibt, weist dies auf eine Formatänderung hin, und der Upstreamfilter sollte reagieren, indem er die Ausgabetypen wechselt. (Wechseln Sie in der **QueryAccept-Methode** nicht zwischen Typen.) Der Upstreamfilter sollte mindestens die wichtigsten RGB-Typen akzeptieren und im Idealfall die allgemeinen YUV-Typen unterstützen. Während des Streamings kann der Videorenderer beliebig oft zwischen YUV- und RGB-Typen hin und her wechseln. Der Videorenderer akzeptiert keine vom Upstreamfilter initiierten dynamischen Formatänderungen.

Wenn der Videorenderer auf eine DirectDraw-Überlagerungsoberfläche zeichnet, ordnet er einen einzelnen Puffer für seinen Eingabepin zu. Wenn der Upstreamfilter versucht, eine Verbindung mit mehreren Puffern zu erzwingen, kann der Videorenderer die Überlagerungsoberfläche nicht verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



