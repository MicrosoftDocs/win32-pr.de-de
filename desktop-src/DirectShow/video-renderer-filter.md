---
description: Videorendererfilter
ms.assetid: 7719ed9d-e3b9-4c84-b587-4e120b5cabf8
title: Videorendererfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96df49305b357cf4a889d283c64839c13c38e2b8f89b8d4eda35d06260f18c58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083500"
---
# <a name="video-renderer-filter"></a>Videorendererfilter

Der Videorendererfilter ist ein robuster, allzweckiger Videorenderer.

> [!Note]  
> Unter Windows XP und höher ist der Standardvideorenderer der [VideoMischungsrenderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7). VMR-7 und Videorenderer haben beide den Benutzerfreundlichen Namen "Videorenderer". Auf früheren Plattformen ist der Videorenderer der Standardrenderer. Weitere Informationen [finden Sie unter Auswählen des richtigen Renderers.](choosing-the-right-renderer.md)

 

Der Videorenderer verwendet DirectDraw und Überlagerungsoberflächen, wenn sie von der Grafikkarte unterstützt werden. Der Filter Graph Manager macht die [**IVideoWindow-Schnittstelle**](/windows/desktop/api/Control/nn-control-ivideowindow) verfügbar, mit der Anwendungen Eigenschaften für den Videorenderer festlegen und abrufen können. Mit neueren Grafikkarten unterstützt der Videorenderer das Rendering im Vollbildmodus. Andernfalls wechselt der Graph-Manager automatisch zum [](full-screen-renderer-filter.md) Filter des Vollbildrenderers für den Vollbildmodus. Weitere Informationen finden Sie unter [**IVideoWindow::p ut \_ FullScreenMode.**](/windows/desktop/api/Control/nf-control-ivideowindow-put_fullscreenmode)

-   \[! Wichtig\]  
    > Normalerweise verarbeitet das Videofenster dieses Filters Nachrichten in einem Arbeitsthread, der vom Filter-manager Graph wird. Wenn eine Anwendung den Filter direkt mit **CoCreateInstance** erstellt, verarbeitet das Videofenster Nachrichten im Anwendungsthread. In diesem Fall muss der Anwendungsthread über eine Nachrichtenschleife verfügen, um Nachrichten an das Videofenster zu senden. Außerdem darf der Thread erst nach dem letzten **Releaseaufruf** des Videorenderers beendet werden, der auftritt, wenn der Filter Graph Manager heruntergefahren wird. Andernfalls kann es zu einem Deadlock der Anwendung führen.

     



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
| [Verdienst](merit.md)                       | Windows XP und höher: **UNLIKELY \_ UNLIKELY**                                                                                                                                                                                                                                                                                                                                                                |
| [Filterkategorie](filter-categories.md) | **CLSID \_ LegacyAmFilterCategory**                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Hinweise

Wenn in der Debugversion von Quartz.dll die LOG TRACE-Debugebene auf 5 oder höher festgelegt ist, zeigt der Videorenderer die Zeitstempel der einzelnen Frames im \_ Videofenster an. Diese Zahlen werden in der Verkaufsversion der DLL nicht angezeigt. Weitere Informationen finden Sie unter [Debugausgabefunktionen](debug-output-functions.md).

Die folgenden Hinweise sind für Filterentwickler vorgesehen:

Der Videorenderer akzeptiert YUV-Formate, wenn die Grafikkarte YUV-Überlagerungsoberflächen unterstützt. Bei der ersten Verbindung mit dem Upstreamfilter benötigt der Videorenderer jedoch ein RGB-Format, das der Farbtiefe der aktuellen Monitoreinstellungen entspricht. Wenn die aktuelle Anzeigeeinstellung beispielsweise eine 24-Bit-Farbe hat, muss der Upstreamfilter 24-Bit-RGB-Videos bereitstellen können. Wenn das Filterdiagramm in einen Ausführungszustand wechselt, handelt der Videorenderer eine dynamische Formatänderung in den entsprechenden YUV-Farbraum aus.

Durch das Herstellen einer Verbindung mit einem RGB-Typ stellt der Videorenderer sicher, dass er GDI verwenden kann, falls DirectDraw nicht verfügbar ist. Sie wechselt zu GDI, wenn eine andere Anwendung den Videospeicher verwendet, wenn das Videorechteck zwei Monitore auf einem System mit mehreren Monitoren umgibt oder wenn das Videorechteck von einem anderen Fenster vollständig verdeckt wird.

> [!Note]  
> Der VideoMischungsrenderer führt diese Art von dynamischen Formatänderung nicht durch und erfordert keinen RGB-Medientyp, da er nie GDI für das Rendering verwendet.

 

Um eine Formatänderung auszuhandeln, ruft der Videorenderer [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) mit dem neuen Medientyp auf. Wenn der Upstreamfilter S OK zurückgibt, wird das neue Medium vom \_ Videorenderer an das nächste Beispiel angefügt. Der Upstreamfilter sollte in jedem Beispiel [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) aufrufen. Wenn **GetMediaType einen** Wert zurückgibt, der nicht **NULL** ist, deutet dies auf eine Formatänderung hin, und der Upstreamfilter sollte durch Wechseln der Ausgabetypen reagieren. (Wechseln Sie in der **QueryAccept-Methode nicht zwischen Typen.)** Der Upstreamfilter sollte mindestens die rgb-Haupttypen akzeptieren und idealerweise die allgemeinen YUV-Typen unterstützen. Während des Streamings wechselt der Videorenderer möglicherweise so oft zwischen yuv- und RGB-Typen hin und her. Der Videorenderer akzeptiert keine dynamischen Formatänderungen, die vom Upstreamfilter initiiert werden.

Wenn der Videorenderer auf eine DirectDraw-Überlagerungsoberfläche zeichnet, ordnet er einen einzelnen Puffer für seinen Eingabepin zu. Wenn der Upstreamfilter versucht, eine Verbindung mit mehreren Puffern zu erzwingen, kann der Videorenderer die Überlagerungsoberfläche nicht verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



