---
description: Videorenderer-Filter
ms.assetid: 7719ed9d-e3b9-4c84-b587-4e120b5cabf8
title: Videorenderer-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c71e72375a43a57ce94b38d01f48abba9309e603
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215000"
---
# <a name="video-renderer-filter"></a>Videorenderer-Filter

Der Videorendererfilter ist ein robuster Video-Renderer, der für alle Zwecke Zweck basiert.

> [!Note]  
> Unter Windows XP und höher ist der Standardvideorenderer der [Video Mischungs-Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7). VMR-7 und der Videorenderer haben beide den anzeigen Amen "Videorenderer". Auf früheren Plattformen ist der Videorenderer der Standard-Renderer. Weitere Informationen finden Sie [unter Auswählen des richtigen Renderers](choosing-the-right-renderer.md).

 

Der Videorenderer verwendet DirectDraw-und Overlay-Oberflächen, wenn diese von der Grafikkarte unterstützt werden. Der Filter Graph-Manager macht die [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstelle verfügbar, mit der Anwendungen Eigenschaften für den Videorenderer festlegen und abrufen können. Mit neueren Grafikkarten unterstützt der Videorenderer das voll Bild Rendering. Andernfalls wechselt der Filter Graph-Manager automatisch zum Vollbild- [Renderer](full-screen-renderer-filter.md) -Filter für den Vollbildmodus. Weitere Informationen finden Sie unter [**IVideoWindow::p UT \_ Fullscreenmode**](/windows/desktop/api/Control/nf-control-ivideowindow-put_fullscreenmode) .

-   \[! Wichtig\]  
    > Normalerweise verarbeitet das Videofenster dieses Filters Nachrichten auf einem Arbeits Thread, der vom Filter Graph-Manager erstellt wurde. Wenn eine Anwendung den Filter mithilfe von **cokreateingestance** direkt erstellt, verarbeitet das Videofenster Nachrichten im Anwendungs Thread. In diesem Fall muss der Anwendungs Thread eine Meldungs Schleife aufweisen, um Nachrichten an das Videofenster zu senden. Außerdem darf der Thread erst beendet werden, wenn der endgültige **releaseaufruf** an den Videorenderer erfolgt, der beim Herunterfahren des Filter-Graph-Managers auftritt. Andernfalls könnte die Anwendung einen Deadlock verursachen.

     



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo), [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2), [**idirectdrawvideo**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo), [**ikspropertyset**](ikspropertyset.md), [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**iqualprop**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop), [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) |
| Eingabe-PIN-Medientypen                    | Nicht komprimierte Videoformate.                                                                                                                                                                                                                                                                                                                                                                              |
| PIN-Eingabeschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**ipinconnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                                                                                           |
| Ausgabe-PIN-Medientypen                   | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                          |
| PIN-Schnittstellen                    | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                          |
| CLSID Filtern                             | CLSID- \_ Videorenderer                                                                                                                                                                                                                                                                                                                                                                                     |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite.                                                                                                                                                                                                                                                                                                                                                                                        |
| Ausführbare Datei                               | quartz.dll                                                                                                                                                                                                                                                                                                                                                                                               |
| [Verdienst](merit.md)                       | Windows XP und höher: Höchstwert **\_ unwahrscheinlich**                                                                                                                                                                                                                                                                                                                                                                |
| [Filter Kategorie](filter-categories.md) | **CLSID \_ legacyamfiltercategory**                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Bemerkungen

In der Debugversion von Quartz.dll \_ zeigt der Videorenderer die Zeitstempel jedes Frames im Videofenster an, wenn die Debug-Ebene für die Protokoll Ablauf Verfolgung auf 5 oder höher festgelegt ist. Diese Zahlen werden nicht in der Verkaufsversion der dll angezeigt. Weitere Informationen finden Sie unter [Debug Output Functions](debug-output-functions.md).

Die folgenden Hinweise sind für Filter Entwickler gedacht:

Der Videorenderer akzeptiert YUV-Formate, wenn die Video Grafikkarte YUV-über Lagerungs Oberflächen unterstützt. Beim ersten Herstellen einer Verbindung mit dem upstreamfilter benötigt der Videorenderer jedoch ein RGB-Format, das mit der Farbtiefe der aktuellen Monitoreinstellungen übereinstimmt. Wenn die aktuelle Anzeige Einstellung beispielsweise 24-Bit-Farbe hat, muss der upstreamfilter in der Lage sein, 24-Bit-RGB-Videos bereitzustellen. Wenn das Filter Diagramm in einen runingstatus wechselt, aushandt der Videorenderer eine dynamische Formatänderung in den entsprechenden YUV-Farbraum.

Durch Herstellen einer Verbindung mit einem RGB-Typ stellt der Videorenderer sicher, dass GDI für den Fall verwendet werden kann, dass DirectDraw nicht verfügbar ist. Es wechselt zu GDI, wenn eine andere Anwendung den Videospeicher verwendet, wenn das Video Rechteck zwei Monitore in einem Multimonitor-System überschreitet oder wenn das Video Rechteck vollständig von einem anderen Fenster verdeckt wird.

> [!Note]  
> Der Video Mischungs-Renderer führt diese Art von dynamischer Formatänderung nicht aus und erfordert keinen RGB-Medientyp, da er für das Rendering niemals GDI verwendet.

 

Um eine Formatänderung auszuhandeln, ruft der Videorenderer [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) mit dem neuen Medientyp auf. Wenn der upstreamfilter S \_ OK zurückgibt, fügt der Videorenderer die neuen Medien an das nächste Beispiel an. Der upstreamfilter sollte in jedem Beispiel [**imediasample:: getmediatype**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) aufrufen. Wenn **getmediatype** einen nicht-**null** -Wert zurückgibt, gibt es eine Formatänderung an, und der upstreamfilter sollte Antworten, indem Ausgabetypen gewechselt werden. (Wechseln Sie in der **queryaccept** -Methode nicht in die Typen.) Der upstreamfilter sollte mindestens die großen RGB-Typen akzeptieren und idealerweise die allgemeinen YUV-Typen unterstützen. Beim Streaming kann der Videorenderer beliebig oft zwischen YUV-und RGB-Typen hin-und herwechseln. Der Videorenderer akzeptiert keine dynamischen Formatierungs Änderungen, die vom upstreamfilter initiiert werden.

Wenn der Videorenderer eine DirectDraw-Overlay-Oberfläche zeichnet, ordnet er einen einzelnen Puffer für seine Eingabe-PIN zu. Wenn der upstreamfilter versucht, eine Verbindung mithilfe mehrerer Puffer zu erzwingen, kann der Videorenderer die Überlagerungs Oberfläche nicht verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



