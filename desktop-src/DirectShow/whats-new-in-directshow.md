---
description: Neues in DirectShow
ms.assetid: 675a34d4-7a33-4125-86af-cd4ed73ad430
title: Neues in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74747349848a7b370cd4766113085c84d0c7a1d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354011"
---
# <a name="whats-new-in-directshow"></a>Neues in DirectShow

## <a name="whats-new-for-directshow-in-windows-7"></a>Neues in DirectShow in Windows 7

Neue Schnittstellen:

-   [**Iamasynkreadertimestampscaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling)
-   [**Iamplugincontrol**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol)

Neue oder aktualisierte Filter:

-   [**Microsoft MPEG-1/DD/AAC-Audiodecoder**](microsoft-mpeg-1-dd-audio-decoder.md)
-   [**Microsoft MPEG-2-Video Decoder**](microsoft-mpeg-2-video-decoder.md)

Die "Intelligent Connect"-Algorithmen wurden so geändert, dass bevorzugte und blockierte Filter unterstützt werden. Weitere Informationen finden Sie unter [Intelligent Connect](intelligent-connect.md).

DVD-Wiedergabe: neue Optionen für die [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) -Methode.

## <a name="whats-new-for-directshow-in-windows-vista"></a>Neues in DirectShow in Windows Vista

-   DirectShow ist nun Teil der Windows SDK. Die DirectShow-Header,-Bibliotheken,-Beispiele und-Tools sind nicht mehr im DirectX SDK enthalten.
-   Die DirectX-Video Beschleunigung (DXVA) 2,0 enthält viele Erweiterungen von DXVA 1,0.

    -   Die Hardware Video Pipeline wurde deutlich verbessert.
    -   Komponenten wie Decoder können direkt auf DXVA 2,0 zugreifen, ohne über den Videorenderer zu kommunizieren.
    -   Mit dem Direct3D-Device Manager können Komponenten dasselbe Direct3D-Gerät gemeinsam verwenden.

    Weitere Informationen zu DXVA 2,0 finden Sie in der Dokumentation zu [DirectX Video Acceleration 2,0](../medfound/directx-video-acceleration-2-0.md) , die Teil der [Microsoft Media Foundation](../medfound/microsoft-media-foundation-sdk.md) Dokumentation ist.

-   Der [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) ist ein leistungsfähiger neuer Videorenderer, der das gleiche Plug-in-Modell wie die Media Foundation Version des EVR gemeinsam nutzt. Weitere Informationen zum EVR finden Sie in der [Microsoft Media Foundation](../medfound/microsoft-media-foundation-sdk.md) -Dokumentation.
-   Unterstützung für die Windows Vista-Anzeigetreiber Modell-Erfassung (WDDM). Diese Funktion ermöglicht es filtern, Grafikkarten mit integrierter Video Erfassung in vollem Umfang zu nutzen, um unnötige Kopien zwischen Videospeicher und System Arbeitsspeicher zu verringern. Weitere Informationen finden Sie unter [using WDDM Capture in DirectShow](using-wddm-capture-in-directshow.md).
-   Der MPEG-1 Layer II-Audiodecoder verwendet jetzt Gleit Komma Arithmetik, um die Decodierung der Qualität zu verbessern.
-   Erweiterungen der DVD-Wiedergabe. Einzelheiten finden Sie unter [Verbesserungen der DVD-Wiedergabe in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).
    -   Bessere Unterstützung bei der Unterstützung von Trick Modi: reibungslose Übergänge zwischen Raten Übergänge zwischen Vorwärts-und umgekehrter Wiedergabe; Unterstützung für die Audiowiedergabe während der schnellen und umgekehrten Umkehrung.
    -   Erweitertes Zwischenspeichern. Anwendungen können festlegen, wie viele Daten der DVD-Navigator vorab liest. Durch das Festlegen eines größeren Caches kann die Akku Lebensdauer verlängert und die automatische Wiedergabe aktiviert werden (nachdem das Laufwerk heruntergefahren wurde). Weitere Informationen finden Sie unter [**\_ \_ Flag**](/windows/win32/api/strmif/ne-strmif-dvd_option_flag)für die DVD-Option.
-   Audioendpunktgeräte: Anwendungen können den [DirectSound-rendererfilter](directsound-renderer-filter.md) einem bestimmten audioendpunktgerät zuordnen. Anwendungen können die API für Multimedia-Geräte (mmdevice) verwenden, um das Endpunktgerät aufzulisten und auszuwählen. Weitere Informationen finden Sie in der Dokumentation zur kernton-API in der Windows SDK.
-   Die folgenden Filter wurden aus Windows Vista entfernt:
    -   [Bbbbfilter](/previous-versions/windows/desktop/mstv/bda-ip-sink-filter)
    -   [Filter für den BDA-Debug-Filter](/previous-versions/windows/desktop/mstv/bda-slip-deframer-filter)
    -   [CC-Decoderfilter](cc-decoder-filter.md)
    -   [Nabts/FEC-VBI-Codec-Filter](/previous-versions/windows/desktop/mstv/nabts-fec-vbi-codec-filter)
    -   [Qt-Debug-Filter](qt-decompressor-filter.md)
    -   [QuickTime Movie Parser-Filter](quicktime-movie-parser-filter.md)
    -   [WST-Codec-Filter](wst-codec-filter.md)
    -   [WST-Decoderfilter](wst-decoder-filter.md)
-   Der Proxy-/Stubcode für viele der DirectShow-Schnittstellen wurde von quartz.dll in proppage.dll verschoben. Dieser Code wurde aus quartz.dll entfernt, da er nicht für die Verwendung durch Anwendungen vorgesehen war. Dies ist jedoch für das Debuggen nützlich, da es einer Testanwendung ermöglicht, eine Remote Verbindung mit einem DirectShow-Filter Diagramm in einem anderen Prozess herzustellen. Um dieses Feature in Windows Vista verwenden zu können, müssen Sie zuerst proppage.dll registrieren. Diese dll ist im Verzeichnis Windows SDK Tools verfügbar. (Weitere Informationen finden Sie unter [Laden eines Diagramms aus einem externen Prozess](loading-a-graph-from-an-external-process.md).)

 

 
