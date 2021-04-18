---
description: In diesem Tutorial wird gezeigt, wie Mediendateien mithilfe des Medien Sitzungs Objekts wiedergegeben werden.
ms.assetid: cdd67082-8153-4f48-abc5-278be82ae082
title: Wiedergeben von Mediendateien mit Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163dba2f9f67139ce7477470889e13a54e2c8b5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104558835"
---
# <a name="how-to-play-media-files-with-media-foundation"></a>Wiedergeben von Mediendateien mit Media Foundation

In diesem Tutorial wird gezeigt, wie Mediendateien mithilfe des [Medien Sitzungs](media-session.md) Objekts wiedergegeben werden.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie dieses Thema lesen, sollten Sie sich mit den folgenden Media Foundation Konzepten vertraut machen:

-   [Medien Sitzung](media-session.md)
-   [Quellresolver](source-resolver.md)
-   [Topologien](topologies.md)
-   [Medienereignis Generatoren](media-event-generators.md)
-   [Präsentations Deskriptoren](presentation-descriptors.md)

> [!Note]  
> In diesem Thema wird nicht beschrieben, wie Dateien wiedergegeben werden, die durch Digital Rights Management (DRM) geschützt sind. Weitere Informationen zu DRM in Microsoft Media Foundation finden Sie unter Wiedergeben [geschützter Mediendateien](how-to-play-protected-media-files.md).

 

## <a name="overview"></a>Übersicht

Die folgenden Objekte werden verwendet, um eine Mediendatei mit der Medien Sitzung wiederzugeben:

-   Eine *Medienquelle* ist ein Objekt, das eine Mediendatei oder eine andere Quelle von Mediendaten analysiert. Die Medienquelle erstellt *Streamobjekte* für jeden Audiostream oder Videostream in der Datei. *Decoders* konvertieren codierte Mediendaten in unkomprimierte Videos und Audiodaten.
-   Der *Quell Löser* erstellt eine Medienquelle aus einer URL.
-   Der [Erweiterte Videorenderer](enhanced-video-renderer.md) (EVR) rendert Videos auf dem Bildschirm.
-   Der [streamingaudiorenderer](streaming-audio-renderer.md) (SAR) rendert Audiodaten auf einem Redner oder einem anderen Audioausgabegerät.
-   Eine *Topologie* definiert den Datenfluss von der Medienquelle zum EVR und SAR.
-   Die *Medien Sitzung* steuert den Datenfluss und sendet Statusereignisse an die Anwendung. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![Darstellung der Wiedergabe mithilfe der Medien Sitzung](images/session-playback.gif)

Im folgenden finden Sie eine allgemeine Übersicht über die Schritte, die zum Wiedergeben einer Mediendatei mithilfe der Medien Sitzung erforderlich sind:

1.  Ruft die [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) -Funktion auf, um die Media Foundation Plattform zu initialisieren.
2.  Rufen Sie [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) auf, um eine neue Instanz der Medien Sitzung zu erstellen.
3.  Verwenden Sie den quellresolver, um eine Medienquelle zu erstellen. Weitere Informationen finden Sie unter [using the Source Resolver](using-the-source-resolver.md).
4.  Erstellen Sie eine Topologie, die die Medienquelle mit dem EVR und SAR verbindet. In diesem Schritt erstellt die Anwendung eine *partielle* Topologie, in der die Decoders nicht enthalten sind. Weitere Informationen finden Sie unter [Erstellen von Wiedergabe Topologien](creating-playback-topologies.md).
5.  Wenden Sie [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) an, um die Topologie für die Medien Sitzung festzulegen.
6.  Verwenden Sie die [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle, um Ereignisse aus der Medien Sitzung zu erhalten.
7.  [**Imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) wird aufgerufen, um die Wiedergabe zu starten. Nachdem die Wiedergabe gestartet wurde, können Sie Sie anhalten, indem Sie [**imfmediasession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)aufrufen, oder Sie durch Aufrufen von [**imfmediasession:: stoppen**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)anhalten.
8.  Wenn die Anwendung beendet wird, geben Sie Ressourcen frei:

    1.  [**Imfmediasession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) wird aufgerufen, um die Medien Sitzung zu schließen. Diese Methode ist asynchron. Wenn der Vorgang abgeschlossen ist, sendet die Medien Sitzung ein [mesessionclosed](mesessionclosed.md) -Ereignis. Anschließend ist es sicher, die verbleibenden Schritte auszuführen.
    2.  Wenden Sie [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) an, um die Medienquelle zu schließen.
    3.  Wenden Sie [**imfmediasession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) an, um die Medien Sitzung zu beenden.
    4.  Zum Herunterfahren der Media Foundation Plattform wird [**mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) aufgerufen.

In den folgenden Abschnitten wird ein umfassendes Codebeispiel gezeigt:

-   [Schritt 1: Deklarieren der cplayer-Klasse](step-1--declare-the-cplayer-class.md)
-   [Schritt 2: Erstellen des cplayer-Objekts](step-2--create-the-cplayer-object.md)
-   [Schritt 3: Öffnen einer Mediendatei](step-3--open-a-media-file.md)
-   [Schritt 4: Erstellen der Medien Sitzung](step-4--create-the-media-session.md)
-   [Schritt 5: Behandeln von Medien Sitzungs Ereignissen](step-5--handle-media-session-events.md)
-   [Schritt 6: Wiedergabe von Steuerelementen](step-6--control-playback.md)
-   [Schritt 7: Herunterfahren der Medien Sitzung](step-7--shut-down-the-media-session.md)
-   [Beispiel für Medien Sitzungs Wiedergabe](media-session-playback-example.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Sitzung](media-session.md)
</dt> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> </dl>

 

 



