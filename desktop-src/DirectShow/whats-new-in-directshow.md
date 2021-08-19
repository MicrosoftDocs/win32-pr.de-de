---
description: Neuerungen in DirectShow
ms.assetid: 675a34d4-7a33-4125-86af-cd4ed73ad430
title: Neuerungen in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd05d11931d7c23a078643724b99dfed84b65e3a7db3e4ed60df9cd2a3273f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071884"
---
# <a name="whats-new-in-directshow"></a>Neuerungen in DirectShow

## <a name="whats-new-for-directshow-in-windows-7"></a>Neuerungen bei DirectShow in Windows 7

Neue Schnittstellen:

-   [**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling)
-   [**IAMPluginControl**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol)

Neue oder aktualisierte Filter:

-   [**Microsoft MPEG-1/DD/AAC-Audiodecoder**](microsoft-mpeg-1-dd-audio-decoder.md)
-   [**Microsoft MPEG-2-Videodecoder**](microsoft-mpeg-2-video-decoder.md)

Die Intelligent Connect-Algorithmen wurden geändert, um bevorzugte und blockierte Filter zu unterstützen. Weitere Informationen finden Sie unter [Intelligent Verbinden](intelligent-connect.md).

DVD-Wiedergabe: Neue Optionen für die [**IDvdControl2::SetOption-Methode.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption)

## <a name="whats-new-for-directshow-in-windows-vista"></a>Neuerungen bei DirectShow in Windows Vista

-   DirectShow ist jetzt Teil des Windows SDK. Die DirectShow-Header, -Bibliotheken, -Beispiele und -Tools sind nicht mehr im DirectX SDK enthalten.
-   DirectX Video Acceleration (DXVA) 2.0 enthält viele Verbesserungen von DXVA 1.0.

    -   Die Hardwarevideopipeline wurde erheblich verbessert.
    -   Komponenten wie Decoder können direkt auf DXVA 2.0 zugreifen, ohne über den Videorenderer zu kommunizieren.
    -   Mit dem Direct3D-Geräte-Manager können Komponenten dasselbe Direct3D-Gerät gemeinsam nutzen.

    Weitere Informationen zu DXVA 2.0 finden Sie in der [DirectX Video Acceleration 2.0-Dokumentation,](../medfound/directx-video-acceleration-2-0.md) die Teil der [Microsoft Media Foundation-Dokumentation](../medfound/microsoft-media-foundation-sdk.md) ist.

-   Der [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) ist ein leistungsstarker neuer Videorenderer, der das gleiche Plug-In-Modell wie die Media Foundation Version von EVR nutzt. Weitere Informationen zur EVR finden [](../medfound/microsoft-media-foundation-sdk.md) Sie in der Microsoft Media Foundation-Dokumentation.
-   Unterstützung für Windows Vista Display Driver Model (WDDM)-Erfassung. Mit diesem Feature können Filter die Vorteile von Grafikkarten mit integrierter Videoaufnahme voll ausschöpfen, um unnötige Kopien zwischen Videospeicher und Systemspeicher zu reduzieren. Weitere Informationen finden Sie unter [Verwenden von WDDM Capture in DirectShow.](using-wddm-capture-in-directshow.md)
-   Der MPEG-1 Layer II-Audiodecoder verwendet jetzt Gleitkommaarithmetik, um die Decodierungsqualität zu verbessern.
-   Verbesserungen bei der DVD-Wiedergabe. Weitere Informationen finden Sie unter [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).
    -   Bessere Unterstützung für den Trickmodus: Reibungslose Übergänge zwischen Raten; Übergänge zwischen vorwärts- und umgekehrter Wiedergabe; Unterstützung für die Audiowiedergabe während der schnellen Vorwärts- und Umgekehrt-Wiedergabe.
    -   Erweitertes Zwischenspeichern. Anwendungen können festlegen, wie viele Daten der DVD-Navigator im Voraus liest. Das Festlegen eines größeren Caches kann die Akkulaufzeit verlängern und die unbeaufsichtigten Wiedergabe ermöglichen (nach dem Herunterfahren des Laufwerks). Weitere Informationen finden Sie unter [**DVD \_ OPTION \_ FLAG**](/windows/win32/api/strmif/ne-strmif-dvd_option_flag).
-   Audioendpunktgeräte: Anwendungen können den [DirectSound-Rendererfilter](directsound-renderer-filter.md) einem bestimmten Audioendpunktgerät zuordnen. Anwendungen können die MMDevice-API (Multimedia Device) verwenden, um das Endpunktgerät aufzuzählen und auszuwählen. Weitere Informationen finden Sie in der Core Audio API-Dokumentation im Windows SDK.
-   Die folgenden Filter wurden aus Windows Vista entfernt:
    -   [BDA-IP-Senkenfilter](/previous-versions/windows/desktop/mstv/bda-ip-sink-filter)
    -   [BDA SLIP-Deframerfilter](/previous-versions/windows/desktop/mstv/bda-slip-deframer-filter)
    -   [CC-Decoderfilter](cc-decoder-filter.md)
    -   [CODTS/FEC-VBI-Codecfilter](/previous-versions/windows/desktop/mstv/nabts-fec-vbi-codec-filter)
    -   [QT-Dekomprimiererfilter](qt-decompressor-filter.md)
    -   [QuickTime Movie Parser-Filter](quicktime-movie-parser-filter.md)
    -   [WST-Codecfilter](wst-codec-filter.md)
    -   [WST-Decoderfilter](wst-decoder-filter.md)
-   Der Proxy-/Stubcode für viele directShow-Schnittstellen wurde von quartz.dll in proppage.dll verschoben. Dieser Code wurde aus quartz.dll entfernt, da er nicht für die Verwendung durch Anwendungen vorgesehen war. Sie ist jedoch nützlich für das Debuggen, da sie es einer Testanwendung ermöglicht, eine Remoteverbindung mit einem DirectShow-Filterdiagramm in einem anderen Prozess herzustellen. Um dieses Feature in Windows Vista verwenden zu können, müssen Sie zuerst proppage.dll registrieren. Diese DLL ist im Verzeichnis Windows SDK-Tools verfügbar. (Weitere Informationen finden Sie unter [Laden eines Graph aus einem externen Prozess.)](loading-a-graph-from-an-external-process.md)

 

 
