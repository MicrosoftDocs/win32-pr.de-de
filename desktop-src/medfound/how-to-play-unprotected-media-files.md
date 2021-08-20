---
description: In diesem Tutorial wird gezeigt, wie Mediendateien mithilfe des Media Session-Objekts wieder verwendet werden.
ms.assetid: cdd67082-8153-4f48-abc5-278be82ae082
title: Wiederspielen von Mediendateien mit Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ba44212227be87e78d29c60a76bc3acdc2b1483b1029c62dd288bb7434b2a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878859"
---
# <a name="how-to-play-media-files-with-media-foundation"></a>Wiederspielen von Mediendateien mit Media Foundation

In diesem Tutorial wird gezeigt, wie Mediendateien mithilfe des [Media Session-Objekts wieder verwendet](media-session.md) werden.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie dieses Thema lesen, sollten Sie mit den folgenden Konzepten Media Foundation vertraut sein:

-   [Mediensitzung](media-session.md)
-   [Quellre resolver](source-resolver.md)
-   [Topologien](topologies.md)
-   [Medienereignis-Generatoren](media-event-generators.md)
-   [Präsentationsdeskriptoren](presentation-descriptors.md)

> [!Note]  
> In diesem Thema wird nicht beschrieben, wie Dateien wiedergespielt werden, die durch Digital Rights Management (DRM) geschützt sind. Informationen zu DRM in Microsoft Media Foundation finden Sie unter [How to Play Protected Media Files](how-to-play-protected-media-files.md).

 

## <a name="overview"></a>Übersicht

Die folgenden Objekte werden verwendet, um eine Mediendatei mit der Mediensitzung wieder zu spielen:

-   Eine *Medienquelle* ist ein Objekt, das eine Mediendatei oder eine andere Quelle von Mediendaten analysiert. Die Medienquelle erstellt *Streamobjekte* für jeden Audio- oder Videostream in der Datei. *Decoder konvertieren* codierte Mediendaten in unkomprimiertes Video und Audio.
-   Der *Quellre resolver* erstellt eine Medienquelle aus einer URL.
-   Der [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) rendert Video auf dem Bildschirm.
-   Der [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR) rendert Audio auf einem Lautsprecher oder einem anderen Audioausgabegerät.
-   Eine *Topologie definiert* den Datenfluss von der Medienquelle zur EVR und SAR.
-   Die *Mediensitzung* steuert den Datenfluss und sendet Statusereignisse an die Anwendung. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![Diagramm, das die Wiedergabe mithilfe der Mediensitzung zeigt](images/session-playback.gif)

Im Folgenden finden Sie eine allgemeine Übersicht über die Schritte, die zum Wiederspielen einer Mediendatei mithilfe der Mediensitzung erforderlich sind:

1.  Rufen Sie die [**MFStartup-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) auf, um die Media Foundation zu initialisieren.
2.  Rufen [**Sie MFCreateMediaSession auf,**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) um eine neue Instanz der Mediensitzung zu erstellen.
3.  Verwenden Sie den Quellre konfliktlöser, um eine Medienquelle zu erstellen. Weitere Informationen finden Sie unter [Verwenden des Quellre resolvers](using-the-source-resolver.md).
4.  Erstellen Sie eine Topologie, die die Medienquelle mit evr und SAR verbindet. In diesem Schritt erstellt die Anwendung eine *Teiltopologie,* die die Decoder nicht enthält. Weitere Informationen finden Sie unter [Erstellen von Wiedergabetopologien.](creating-playback-topologies.md)
5.  Rufen [**Sie ZUM FESTLEGEN DERMEDIASESSION::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) auf, um die Topologie für die Mediensitzung festzugeben.
6.  Verwenden Sie [**die BENUTZEROBERFLÄCHEMEDIAEventGenerator,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) um Ereignisse aus der Mediensitzung zu erhalten.
7.  Rufen [**Sie ZUM STARTEN DERMEDIASESSION::Start auf,**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) um die Wiedergabe zu starten. Nachdem die Wiedergabe gestartet wurde, können Sie sie anhalten, indem Sie [**DURCH AUFRUFEN VON 10000255 :P 5555111115511111113333333331111111333333333333111111117111111177711111222**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) [](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)
8.  Wenn die Anwendung beendet wird, geben Sie Ressourcen frei:

    1.  Rufen [**Sie ZUM SCHLIEßEN DIEMEDIASESSION::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) auf, um die Mediensitzung zu schließen. Diese Methode ist asynchron. Nach Abschluss sendet die Mediensitzung ein [MESessionClosed-Ereignis.](mesessionclosed.md) Anschließend ist es sicher, die verbleibenden Schritte durchzuführen.
    2.  Rufen [**Sie DIE MEDIENQUELLE::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) auf, um die Medienquelle herunter zu fahren.
    3.  Rufen [**Sie ZUM HERUNTERFAHREN DER**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) MEDIENSITZUNG AUF.
    4.  Rufen [**Sie MFShutdown auf,**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) um die Media Foundation herunterfahren.

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

 

 



