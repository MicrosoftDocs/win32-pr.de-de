---
description: In diesem Tutorial erfahren Sie, wie Sie Mediendateien mithilfe des Mediensitzungsobjekts wiedergeben.
ms.assetid: cdd67082-8153-4f48-abc5-278be82ae082
title: Wiedergeben von Mediendateien mit Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ba44212227be87e78d29c60a76bc3acdc2b1483b1029c62dd288bb7434b2a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878859"
---
# <a name="how-to-play-media-files-with-media-foundation"></a>Wiedergeben von Mediendateien mit Media Foundation

In diesem Tutorial erfahren Sie, wie Sie Mediendateien mithilfe des [Mediensitzungsobjekts](media-session.md) wiedergeben.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie dieses Thema lesen, sollten Sie mit den folgenden Media Foundation Konzepten vertraut sein:

-   [Mediensitzung](media-session.md)
-   [Quelllöser](source-resolver.md)
-   [Topologien](topologies.md)
-   [Medienereignisgeneratoren](media-event-generators.md)
-   [Präsentationsdeskriptoren](presentation-descriptors.md)

> [!Note]  
> In diesem Thema wird nicht beschrieben, wie Dateien wiedergegeben werden, die durch drm (Digital Rights Management) geschützt sind. Informationen zu DRM in Microsoft Media Foundation finden Sie unter [Wiedergeben geschützter Mediendateien.](how-to-play-protected-media-files.md)

 

## <a name="overview"></a>Übersicht

Die folgenden Objekte werden verwendet, um eine Mediendatei mit der Mediensitzung wiederzuspielen:

-   Eine *Medienquelle* ist ein Objekt, das eine Mediendatei oder eine andere Quelle von Mediendaten analysiert. Die Medienquelle erstellt *Streamobjekte* für jeden Audio- oder Videostream in der Datei. *Decoder* konvertieren codierte Mediendaten in unkomprimierte Video- und Audiodaten.
-   Der *Quelllöser* erstellt eine Medienquelle aus einer URL.
-   Der [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) rendert Videos auf dem Bildschirm.
-   Der [StreamingAudiorenderer](streaming-audio-renderer.md) (SAR) rendert Audiodaten an einen Lautsprecher oder ein anderes Audioausgabegerät.
-   Eine *Topologie* definiert den Datenfluss von der Medienquelle zu EVR und SAR.
-   Die *Mediensitzung* steuert den Datenfluss und sendet Statusereignisse an die Anwendung. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![Diagramm, das die Wiedergabe mithilfe der Mediensitzung zeigt](images/session-playback.gif)

Im Folgenden werden die Schritte beschrieben, die zum Wiedergeben einer Mediendatei mithilfe der Mediensitzung erforderlich sind:

1.  Rufen Sie die [**MFStartup-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) auf, um die Media Foundation Plattform zu initialisieren.
2.  Rufen Sie [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) auf, um eine neue Instanz der Mediensitzung zu erstellen.
3.  Verwenden Sie den Quell resolver, um eine Medienquelle zu erstellen. Weitere Informationen finden Sie unter [Verwenden des Quelllösers.](using-the-source-resolver.md)
4.  Erstellen Sie eine Topologie, die die Medienquelle mit evr und SAR verbindet. In diesem Schritt erstellt  die Anwendung eine Teiltopologie, die die Decoder nicht enthält. Weitere Informationen finden Sie unter [Erstellen von Wiedergabetopologien.](creating-playback-topologies.md)
5.  Rufen Sie [**DIE DATEI ÜBERMEDIASESSION::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) auf, um die Topologie in der Mediensitzung festzulegen.
6.  Verwenden Sie die [**SCHNITTSTELLE VONMEDIAEVENTGENERATOR,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) um Ereignisse aus der Mediensitzung abzurufen.
7.  Rufen Sie [**DEN AUFRUF VONMEDIASESSION::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) auf, um die Wiedergabe zu starten. Nachdem die Wiedergabe gestartet wurde, können Sie sie anhalten, indem Sie [**DEN AUFRUF VONMEDIASESSION::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)ausführen, oder sie beenden, indem Sie [**DEN AUFRUF VONMEDIASESSION::Stop ausführen.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)
8.  Wenn die Anwendung beendet wird, geben Sie Ressourcen frei:

    1.  Rufen Sie [**ÜBERMEDIASESSION::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) auf, um die Mediensitzung zu schließen. Diese Methode ist asynchron. Nach Abschluss des Vorgangs sendet die Mediensitzung ein [MESessionClosed-Ereignis.](mesessionclosed.md) Anschließend ist es sicher, die verbleibenden Schritte auszuführen.
    2.  Rufen Sie [**ÜBERMEDIASOURCE::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) auf, um die Medienquelle herunterzufahren.
    3.  Rufen Sie [**DIE SPERREMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) auf, um die Mediensitzung herunterzufahren.
    4.  Rufen Sie [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) auf, um die Media Foundation Plattform herunterzufahren.

In den folgenden Abschnitten wird ein vollständiges Codebeispiel gezeigt:

-   [Schritt 1: Deklarieren der CPlayer-Klasse](step-1--declare-the-cplayer-class.md)
-   [Schritt 2: Erstellen des CPlayer-Objekts](step-2--create-the-cplayer-object.md)
-   [Schritt 3: Öffnen einer Mediendatei](step-3--open-a-media-file.md)
-   [Schritt 4: Erstellen der Mediensitzung](step-4--create-the-media-session.md)
-   [Schritt 5: Behandeln von Mediensitzungsereignissen](step-5--handle-media-session-events.md)
-   [Schritt 6: Steuern der Wiedergabe](step-6--control-playback.md)
-   [Schritt 7: Herunterfahren der Mediensitzung](step-7--shut-down-the-media-session.md)
-   [Beispiel für die Mediensitzungswiedergabe](media-session-playback-example.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mediensitzung](media-session.md)
</dt> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> </dl>

 

 



