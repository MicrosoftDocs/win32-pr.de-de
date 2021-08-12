---
description: Erstellen des DVD-Filterfilters Graph
ms.assetid: 1d2f8284-2deb-4207-b067-24a54d6b286c
title: Erstellen des DVD-Filterfilters Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 049c8bc52fd382be863cdf5a0e6b124534e0b9280d28536abc58a6f4e64e81e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662646"
---
# <a name="building-the-dvd-filter-graph"></a>Erstellen des DVD-Filterfilters Graph

Wie bei jeder DirectShow-Anwendung beginnt eine DVD-Wiedergabeanwendung mit dem Erstellen eines Filterdiagramms. DirectShow bietet die folgenden Komponenten für die DVD-Wiedergabe:

-   [DVD Graph Builder](dvd-graph-builder.md). Ein Hilfsobjekt, das das Filterdiagramm erstellt. Es macht die [**IDvdGraphBuilder-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) verfügbar.
-   [DVD Navigator-Filter.](dvd-navigator-filter.md) Ein DirectShow-Filter, der dvd-Wiedergabe, -Navigation und andere Befehle verarbeitet.

Die DVD-Wiedergabe erfordert auch einen MPEG-2-Decoder. MPEG-2-Decoder für Hardware und Software sind von Drittanbietern verfügbar. Erstellen Sie zunächst eine Instanz des DVD-Graph Builder-Objekts.


```C++
IDvdGraphBuilder *pBuild = NULL;
hr = CoCreateInstance(CLSID_DvdGraphBuilder, NULL, 
    CLSCTX_INPROC_SERVER, IID_IDvdGraphBuilder, (void **)&pBuild);
```



An diesem Punkt können Sie den Videorenderer auswählen und konfigurieren, bevor Sie den Rest des Diagramms erstellen. Dieser optionale Schritt wird im nächsten Abschnitt ausführlicher beschrieben. Wenn Sie diesen Schritt weglassen, wählt der DVD Graph Generator einen Standardrenderer aus. Erstellen Sie als Nächstes das Diagramm, indem Sie die [**IDvdGraphBuilder::RenderDvdVideoVolume-Methode**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume) aufrufen.


```C++
AM_DVD_RENDERSTATUS buildStatus;
hr = pBuild->RenderDvdVideoVolume(L"Z:\\video_ts", 0, &buildStatus);
```



Der erste Parameter ist der Name eines Verzeichnisses, das die DVD-Dateien enthält. Auf einem DVD-Datenträger befinden sich diese Dateien in einem Verzeichnis mit dem Namen VIDEO \_ TS. Wenn der erste Parameter **NULL ist,** verwendet der DVD Graph Builder das erste Laufwerk, das ein DVD-Volume enthält.

Der zweite Parameter enthält verschiedene optionale Flags für die Auswahl des Decodertyps (Hardware oder Software) und anderer Optionen.

Der dritte Parameter ist eine [**AM \_ DVD \_ RENDERSTATUS-Struktur,**](/windows/win32/api/strmif/ns-strmif-am_dvd_renderstatus) die Statusinformationen empfängt. Wenn die [**RenderDvdVideoVolume-Methode**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume) S FALSE zurückgibt, bedeutet dies, dass der Aufruf teilweise erfolgreich war (oder teilweise fehlgeschlagen ist, wenn Sie ein \_ Pessimist sind). Beispielsweise kann die -Methode den Unterbilddatenstrom nicht rendern, obwohl die anderen Streams erfolgreich gerendert wurden. Wenn die **RenderDvdVideoVolume-Methode** einen Fehlercode oder den Wert S FALSE zurückgibt, können Sie die \_ AM DVD **\_ \_ RENDERSTATUS-Struktur** auf Details zum Fehler untersuchen.

Rufen Sie als Nächstes einen Zeiger auf den Filter Graph Manager ab, indem Sie [**IDvdGraphBuilder::GetFiltergraph aufrufen.**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getfiltergraph) Diese Methode gibt einen Zeiger auf die [**IGraphBuilder Graph-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) des Filter-Managers zurück.


```C++
IGraphBuilder *pGraph = NULL;
hr =  pBuild->GetFiltergraph(&m_pGraph);
```



Verwenden Sie [**die IDvdGraphBuilder::GetDvdInterface-Methode,**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) um DVD-bezogene Schnittstellen abzurufen, einschließlich der folgenden:

-   [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2). Steuert die Wiedergabe und DVD-Befehle
-   [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2). Gibt Informationen zum aktuellen Status des DVD-Navigators zurück.
-   [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder). Steuert die Anzeige von Untertiteln. Die Anzeige von Untertiteln ist standardmäßig aktiviert. Rufen Sie zum Deaktivieren [**IAMLine21Decoder::SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) mit dem AM \_ L21 \_ CCSTATE \_ Off-Flag auf.
-   [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio). Steuert das Audiovolumen und das Gleichgewicht.

Der folgende Code gibt beispielsweise die [**IDvdControl2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) zurück.


```C++
IDvdControl2 *pDvdControl = NULL;
hr = pBuild->GetDvdInterface(IID_IDvdControl2, (void**)&pDvdControl);
```



Die empfohlene Methode zum Erstellen des DVD-Wiedergabefilterdiagramms besteht im automatischen Erstellen einer [DVD Graph Builder-Objekts.](dvd-graph-builder.md) Dieser Ansatz wird unten und in der DVD-Beispielanwendung demonstriert. Wenn Sie Ihr DVD-Filterdiagramm manuell erstellen müssen, können Sie dazu die grundlegenden Regeln für die Graph-Erstellung befolgen, die an anderer Stelle in der DirectShow-Dokumentation erläutert werden. Im Allgemeinen sollten Sie einzelne Filter, die von der DVD Graph Builder erstellt wurden, nicht manuell hinzufügen, entfernen, verbinden oder trennen, da dies den Bereinigungscode verwirren kann.

Konfigurieren des Videorenderers

DirectShow bietet mehrere Videorendererfilter. Bevor Sie das Diagramm erstellen, können Sie den von Ihnen bevorzugten Videorenderer wählen. Wählen Sie den Renderer aus, indem Sie [**IDvdGraphBuilder::GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) aufrufen und eine schnittstelle anfordern, die für diesen Renderer spezifisch ist:

-   Overlay Mixer Filter: [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo).
-   Video Mixing Renderer 7 (VMR-7): [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig).
-   Video Mixing Renderer 9 (VMR-9): [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9).
-   Enhanced Video Renderer (EVR): [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig).

Wenn Sie eine dieser Schnittstellen vor dem Erstellen des Filterdiagramms anfordern, erstellt der DVD-Graph Builder den entsprechenden Videorenderer. Später, wenn Sie das Diagramm erstellen, versucht der DVD Graph Builder, diesen Renderer zu verwenden. Wenn das Diagramm jedoch nicht mit dem von Ihnen ausgewählten Renderer erstellen kann, kann es zu einem anderen Renderer wechseln. Beispielsweise ist Ihr MPEG-2-Decoder möglicherweise nicht mit dem VMR-Filter kompatibel. In diesem Fall würde die DVD Graph Builder standardmäßig auf overlay Mixer.

Diese Schnittstellen bieten Ihnen auch die Möglichkeit, den Renderer zu konfigurieren, bevor er mit dem Decoder verbunden wird. Beispielsweise können Sie festlegen, dass der VMR den fensterlosen Modus anstelle des Standardfenstermodus verwendet. Weitere Informationen zu Videorenderern finden Sie im Thema [About Video Rendering in DirectShow](about-video-rendering-in-directshow.md).

Auf Windows XP und höher verwendet der DVD Graph Builder immer den [Video Mixing Renderer 7](video-mixing-renderer-filter-7.md) (VMR-7), es sei denn:

-   Der Aufrufer fragt Schnittstellen ab, die nur die Overlay-Mixer gefunden [haben,](overlay-mixer-filter.md)z. B. [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2). Dadurch wird der DVD-Graph Builder darauf hindeutet, dass die Anwendung die Overlay-Mixer und nicht die VMR verwenden möchte. Windows Media Player verfügt auch über eine Dialogfeldoption, um die Verwendung des Overlay-Mixer.
-   Der installierte Decoder ist nicht VMR-kompatibel. Während der Graph-Entwicklung wird die neue [**IAMDecoderCaps-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps) verwendet, um die VMR-Unterstützung des Decoders zu überprüfen. Wenn dies nicht vorhanden ist, verwendet der DVD-Graph Builder das Overlay-Mixer.
-   Bei Verwendung eines Hardwaredecoders kann der Decoder keine Verbindung mit dem [Videoport-Manager](video-port-manager.md) (VPM) herstellen. Wenn ein Hardwaredecoder den VPM nicht verwenden kann, kann er den VMR nicht verwenden. Daher versucht der DVD Graph Builder, mithilfe des Overlay-Mixer.
-   Es ist bekannt, dass die Anzeigekarte nicht über unzureichende Ressourcen und/oder Funktionen verfügt, um die VMR zu unterstützen, aber sie wird im Treiber nicht ordnungsgemäß angezeigt. (Einige bekannte Fälle werden speziell vom DVD-Graph Builder ausgeschlossen.)
-   Die Verbindung zwischen dem Decoder und der VMR schlägt aus irgendeinem Grund fehl, in der Regel aufgrund eines Mangels an VRAM, um die erforderlichen Oberflächen zu erstellen. In diesen Fällen schaltet der DVD Graph Builder die VMR-Verwendung ab und versucht, die Overlay-Mixer zu verwenden, um ein Diagramm zu erstellen.

Fenstermodus

Im Fenstermodus (Overlay Mixer oder VMR) erstellt der Renderer ein eigenes Videofenster. Um dieses Fenster als untergeordnetes Fenster des Anwendungsfensters zu erstellen, rufen Sie [**IVideoWindow::p ut \_ Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) mit einem Handle für die Anwendung auf. Rufen Sie [**außerdem IVideoWindow::p ut \_ WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) auf, um die Formate WS CHILD und \_ WS CLIPSIBLINGS im Videofenster des Renderers \_ zu festlegen. Um Mausmeldungen aus dem Videofenster des Renderers zu erhalten, rufen Sie [**IVideoWindow::p ut \_ MessageDrain**](/windows/desktop/api/Control/nf-control-ivideowindow-put_messagedrain) mit einem Handle für das Anwendungsfenster auf. Diese Methode richtet einen "Nachrichtenentleerung" ein. Das Videofenster weitert alle empfangenen Mausnachrichten an das Fenster zum Leeren der Nachricht.


```C++
pVideoWindow->put_Owner((OAHWND)hwnd);
pVideoWindow->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
pVideoWindow->put_MessageDrain((OAHWND)hwnd) ;
```



Der Nachrichtenabfluss macht die Auswahl von DVD-Menüschaltflächen etwas kompliziert. Wenn das Videofenster nicht den gesamten Clientbereich der Anwendung ausfüllt, werden einige Mausereignisse außerhalb des Videofensters angezeigt. Wenn Sie innerhalb des  Videofensters ein Mausereignis erhalten, sollten Sie es für die Navigation im DVD-Menü verarbeiten. Mausereignisse *außerhalb des* Videofensters sollten nicht verarbeitet werden. Beim Nachrichtenentleerung gibt es keine Möglichkeit, zwischen den beiden zu unterscheiden. Darüber hinaus sind die Koordinaten für Mausereignisse aus dem Videofenster relativ zum Clientbereich des Videofensters. Mausereignisse außerhalb des Videofensters sind jedoch relativ zum Clientbereich der Anwendung.

Fensterloser Modus

Im fensterlosen Modus werden die Probleme mit Mausnachrichten vollständig vermieden. Sie benötigen keinen Nachrichtenentleerung, da die VMR (oder EVR) kein eigenes Fenster im fensterlosen Modus erstellt. Stattdessen wird es direkt in Ihr Anwendungsfenster gelost. Wenn das Zielrechteck kleiner als der Anwendungsclientbereich ist, berücksichtigt der DVD-Navigator dies bei der Berechnung der DVD-Schaltflächenpositionen. Wenn Sie also eine Mausnachricht erhalten, können Sie die Koordinaten direkt an den DVD-Navigator übergeben, wie im Abschnitt Menünavigation beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 
