---
description: Entwickeln des DVD-Filter Diagramms
ms.assetid: 1d2f8284-2deb-4207-b067-24a54d6b286c
title: Entwickeln des DVD-Filter Diagramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96d15c7d84ec138771e1f5da8be4270faae049cc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125312"
---
# <a name="building-the-dvd-filter-graph"></a>Entwickeln des DVD-Filter Diagramms

Wie bei jeder DirectShow-Anwendung beginnt eine DVD-Wiedergabe Anwendung mit dem Aufbau eines Filter Diagramms. DirectShow stellt die folgenden Komponenten für die DVD-Wiedergabe bereit:

-   [DVD-Diagramm](dvd-graph-builder.md)-Generator. Ein Hilfsobjekt, das das Filter Diagramm erstellt. Sie macht die [**idvdgraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) -Schnittstelle verfügbar.
-   Filter für den [DVD-Navigator](dvd-navigator-filter.md) . Ein DirectShow-Filter, der die DVD-Wiedergabe, Navigation und andere Befehle behandelt.

Die DVD-Wiedergabe erfordert auch einen MPEG-2-Decoder. Die Hardware-und Software-Decoder von MPEG-2 sind von Drittanbietern verfügbar. Erstellen Sie zunächst eine Instanz des DVD Graph Builder-Objekts.


```C++
IDvdGraphBuilder *pBuild = NULL;
hr = CoCreateInstance(CLSID_DvdGraphBuilder, NULL, 
    CLSCTX_INPROC_SERVER, IID_IDvdGraphBuilder, (void **)&pBuild);
```



An diesem Punkt können Sie den Videorenderer auswählen und konfigurieren, bevor Sie den Rest des Diagramms erstellen. Dieser Schritt, der optional ist, wird im nächsten Abschnitt ausführlicher beschrieben. Wenn Sie diesen Schritt weglassen, wählt der DVD Graph-Generator einen Standardrenderer aus. Erstellen Sie als nächstes das Diagramm, indem Sie die [**idvdgraphbuilder:: renderdvdvideovolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume) -Methode aufrufen.


```C++
AM_DVD_RENDERSTATUS buildStatus;
hr = pBuild->RenderDvdVideoVolume(L"Z:\\video_ts", 0, &buildStatus);
```



Der erste Parameter ist der Name eines Verzeichnisses, das die DVD-Dateien enthält. Auf einem DVD-CD befinden sich diese Dateien in einem Verzeichnis mit dem Namen "Video \_ TS". Wenn der erste Parameter **null** ist, verwendet der DVD Graph-Generator das erste Laufwerk, das ein DVD-Volume enthält.

Der zweite Parameter enthält verschiedene optionale Flags zum Auswählen des Typs von Decoder (Hardware oder Software) und anderen Optionen.

Der dritte Parameter ist eine [**am- \_ DVD- \_ Renderstatus**](/windows/win32/api/strmif/ns-strmif-am_dvd_renderstatus) -Struktur, die Statusinformationen empfängt. Wenn die [**renderdvdvideovolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume) -Methode den Wert "false" zurückgibt \_ , bedeutet dies, dass der-Befehl teilweise erfolgreich war (oder teilweise fehlgeschlagen ist, wenn Sie ein pessimistisch sind). Beispielsweise kann die-Methode den subbildstream nicht rendern, auch wenn die anderen Streams erfolgreich gerendert wurden. Wenn die **renderdvdvideovolume** -Methode einen Fehlercode oder den Wert S \_ false zurückgibt, können Sie die **am-DVD- \_ \_ Renderstatus** -Struktur auf Details zum Fehler überprüfen.

Rufen Sie als nächstes einen Zeiger auf den Filter Graph-Manager ab, indem Sie [**idvdgraphbuilder:: getfiltergraph**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getfiltergraph)aufrufen. Diese Methode gibt einen Zeiger auf die [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Schnittstelle des Filter Graph-Managers zurück.


```C++
IGraphBuilder *pGraph = NULL;
hr =  pBuild->GetFiltergraph(&m_pGraph);
```



Verwenden Sie die [**idvdgraphbuilder:: getdvdinterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) -Methode, um DVD-bezogene Schnittstellen abzurufen, einschließlich der folgenden:

-   [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2). Steuert Wiedergabe-und DVD-Befehle
-   [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2). Gibt Informationen zum aktuellen Zustand des DVD-Navigators zurück.
-   [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder). Steuert die Anzeige von Closed Caption. Die Anzeige von Closed Caption ist standardmäßig aktiviert. Um dies zu deaktivieren, müssen Sie [**IAMLine21Decoder:: SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) mit dem Flag "am \_ L21 \_ ccstate Off" aufrufen \_ .
-   [**Ibasicaudio.**](/windows/desktop/api/Control/nn-control-ibasicaudio) Steuert die audiomenge und den Saldo.

Der folgende Code gibt z. b. die [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) -Schnittstelle zurück.


```C++
IDvdControl2 *pDvdControl = NULL;
hr = pBuild->GetDvdInterface(IID_IDvdControl2, (void**)&pDvdControl);
```



Die empfohlene Vorgehensweise zum Erstellen des DVD-Wiedergabe Filter Diagramms besteht darin, dass ein [DVD Graph](dvd-graph-builder.md) -Generator-Objekt dies automatisch durchführen kann. Diese Vorgehensweise wird im folgenden und in der DVD-Beispielanwendung veranschaulicht. Wenn Sie das DVD-Filter Diagramm manuell erstellen müssen, können Sie dies tun, indem Sie die grundlegenden Regeln der Graph-Erstellung befolgen, die an anderer Stelle in der DirectShow-Dokumentation erörtert werden. Im Allgemeinen sollten Sie im Diagramm, das vom DVD Graph-Generator erstellt wurde, keine einzelnen Filter manuell hinzufügen, entfernen, verbinden oder trennen, da dadurch der Bereinigungs Code verwechselt werden kann.

Konfigurieren des Videorenderers

DirectShow stellt mehrere Videorendererfilter bereit. Vor dem Erstellen des Diagramms können Sie auswählen, welchen Videorenderer Sie bevorzugen. Wählen Sie den Renderer aus, indem Sie [**idvdgraphbuilder:: getdvdinterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) aufrufen und eine Schnittstelle anfordern, die für diesen Renderer spezifisch ist:

-   Filter für Überlagerungs-Mixer: [**iddrawexclmodevideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo).
-   Video Mischungs-Renderer 7 (VMR-7): [**ivmrfilterconfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig).
-   Video Mischungs-Renderer 9 (VMR-9): [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9).
-   Erweiterter Videorenderer (EVR): [**ievrfilterconfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig).

Wenn Sie eine dieser Schnittstellen vor dem Erstellen des Filter Diagramms anfordern, erstellt der DVD Graph-Generator den entsprechenden Videorenderer. Wenn Sie später das Diagramm erstellen, versucht der DVD Graph-Generator, diesen Renderer zu verwenden. Wenn das Diagramm jedoch nicht mit dem ausgewählten Renderer erstellt werden kann, wechselt es möglicherweise zu einem anderen Renderer. Beispielsweise ist der MPEG-2-Decoder möglicherweise nicht mit dem VMR-Filter kompatibel. in diesem Fall würde der DVD-Diagramm-Generator standardmäßig den Überlagerungs-Mixer enthalten.

Diese Schnittstellen haben außerdem die Möglichkeit, den Renderer zu konfigurieren, bevor er mit dem Decoder verbunden ist. Beispielsweise können Sie VMR so festlegen, dass der fensterlose Modus anstelle des Standardfenster Modus verwendet wird. Weitere Informationen zu videorendererfehlern finden Sie im Thema zum Rendern [von Videos in DirectShow](about-video-rendering-in-directshow.md).

Unter Windows XP und höher verwendet der DVD Graph-Generator immer den [Video Mischungs-Renderer 7](video-mixing-renderer-filter-7.md) (VMR-7), es sei denn,

-   Die Aufrufer-Abfrageschnittstellen haben nur den [Überlagerungs-Mixer](overlay-mixer-filter.md)wie [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2)gefunden. Dies sendet einen Hinweis an den DVD-Diagramm-Generator, dass die Anwendung den Overlay-Mixer und nicht den VMR verwenden möchte. Windows Media Player verfügt auch über eine Dialogfeld Option, um die Verwendung des Überlagerungs Mischers zu erzwingen.
-   Der installierte Decoder ist nicht VMR-kompatibel. Während der Diagramm Bildung wird die neue [**iamdecodercaps**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps) -Schnittstelle verwendet, um die VMR-Unterstützung des Decoders zu überprüfen. Wenn dies nicht der Fall ist, verwendet der DVD Graph-Generator den Overlay-Mixer.
-   Bei Verwendung eines Hardware-Decoders kann der Decoder keine Verbindung mit dem [Videoport-Manager](video-port-manager.md) (VPM) herstellen. Wenn ein Hardware Decoder das VPM nicht verwenden kann, kann der VMR nicht verwendet werden. daher versucht der DVD Graph-Generator, mit dem Überlagerungs Mixer ein Diagramm zu erstellen.
-   Die Anzeigekarte hat bekanntermaßen nicht genügend Ressourcen und/oder Funktionen zur Unterstützung der VMR, aber dies wird im Treiber nicht korrekt gemeldet. (Einige bekannte Fälle werden explizit vom DVD Graph-Generator ausgeschlossen.)
-   Die Verbindung zwischen dem Decoder und VMR schlägt aus irgendeinem Grund fehl, normalerweise aufgrund eines fehlenden VRAM, um die erforderlichen Oberflächen zu erstellen. In diesen Fällen schaltet der DVD Graph-Generator die Verwendung von VMR ein und versucht, den Overlay-Mixer zu verwenden, um ein Diagramm zu erstellen.

Fenstermodus

Im Fenstermodus (Overlay-Mixer oder VMR) erstellt der Renderer ein eigenes Videofenster. Um dieses Fenster zu einem untergeordneten Element des Anwendungsfensters zu machen, nennen Sie [**IVideoWindow::p UT- \_ Besitzer**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) mit einem Handle für die Anwendung. Nennen Sie auch " [**IVideoWindow::p UT \_ WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) ", um die Stile "WS \_ Child" und "WS \_ clipneben" im Videofenster des Renderers festzulegen. Um Maus Meldungen aus dem Videofenster des Renderers abzurufen, nennen Sie [**IVideoWindow::p UT \_ messagedrain**](/windows/desktop/api/Control/nf-control-ivideowindow-put_messagedrain) mit einem Handle für das Anwendungsfenster. Diese Methode richtet eine "Nachrichten Ableitung" ein – im Videofenster werden alle empfangenen Maus Meldungen an das Fenster für die Nachrichten Ableitung weitergeleitet.


```C++
pVideoWindow->put_Owner((OAHWND)hwnd);
pVideoWindow->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
pVideoWindow->put_MessageDrain((OAHWND)hwnd) ;
```



Der Nachrichten Ausgleich macht das Auswählen von DVD-Menü Schaltflächen etwas kompliziert. Wenn im Videofenster der gesamte Client Bereich der Anwendung nicht ausgefüllt wird, fallen einige Mausereignisse außerhalb des Videofensters. Wenn Sie ein Maus Ereignis *innerhalb* des Videofensters erhalten, sollten Sie es für die DVD-Menü Navigation verarbeiten. Mausereignisse von *außerhalb* des Videofensters sollten nicht verarbeitet werden. Bei der Nachrichten Ableitung gibt es keine Möglichkeit, zwischen beiden zu unterscheiden. Außerdem sind die Koordinaten für Mausereignisse aus dem Videofenster relativ zum Client Bereich des Videofensters. Mausereignisse von außerhalb des Videofensters sind jedoch relativ zum Client Bereich der Anwendung.

Fensterloser Modus

Im fensterlosen Modus werden die Probleme mit Maus Meldungen vermieden. Sie benötigen keine Nachrichten Ableitung, da VMR (oder EVR) kein eigenes Fenster im fensterlosen Modus erstellt. Stattdessen wird Sie direkt in das Anwendungsfenster gezeichnet. Wenn das Ziel Rechteck kleiner als der Anwendungs Client Bereich ist, berücksichtigt der DVD-Navigator dies beim Berechnen der DVD-Schaltflächen Positionen. Wenn Sie also eine Maus Meldung erhalten, können Sie die Koordinaten direkt an den DVD-Navigator übergeben, wie im Abschnitt Menü Navigation beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 
