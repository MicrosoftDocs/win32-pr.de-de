---
description: DVD-Filter Graph Konfiguration
ms.assetid: 0c68c456-2240-4090-b45c-bd098cfea645
title: DVD-Filter Graph Konfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ece69f77ac4a4e6674bbcd12404a10b7f765a514e18cb31963d2ed7f981799e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653086"
---
# <a name="dvd-filter-graph-configuration"></a>DVD-Filter Graph Konfiguration

In diesem Abschnitt werden die verschiedenen Filterdiagrammkonfigurationen für die DVD-Wiedergabe in DirectShow beschrieben. Diese Diagramme werden hauptsächlich als Referenz bereitgestellt. Der DVD-Navigator erstellt das Diagramm, sodass es im Allgemeinen nicht erforderlich ist, die Details der Konfiguration des Graphen zu verstehen. Weitere Informationen finden Sie unter [Building the DVD Filter Graph](building-the-dvd-filter-graph.md).

Die folgende Abbildung zeigt ein DVD-Filterdiagramm mit einem Softwaredecoder.

![DVD-Filterdiagramm für Windows XP](images/dvd-graph-xp.png)

Wenn ein Hardwaredecoder vorhanden ist, wird er in der Regel über einen Videoport direkt mit der Grafikkarte verbunden. Dadurch können die decodierten Videobits direkt an den Framepuffer auf der Grafikkarte gesendet werden, ohne an den Hostspeicher zu übergeben. Um diese direkte Verbindung in früheren Versionen von Windows zu verwalten, unterstützt DirectShow DirectDraw Video Port Extensions (VPE) über eine Schnittstelle auf dem [Overlay-Mixer Filter](overlay-mixer-filter.md).

> [!Note]  
> Das Overlay-Mixer ist jetzt veraltet.

 

In Windows XP und höher kann ein Hardwaredecoder eine Verbindung mit dem [Videoport-Manager-Filter](video-port-manager.md) herstellen.

![DVD-Diagramm für Windows XP mit einem Hardwaredecoder](images/dvd-hwgraph-xp.png)

In all diesen Diagrammen ist der DVD-Navigator der Quellfilter. Er führt mehrere Aufgaben aus:

-   Liest die Navigations- und Videodaten vom Datenträger.
-   Demultiplexiert die Video-, Audio- und Unterbilddaten in separate Streams.
-   Die Datenströme werden zur weiteren Verarbeitung und zum letztlichen Rendering in das Diagramm gestreamt.
-   Informiert Ihre Anwendung über DVD-bezogene Ereignisse.

Im Audiostream verbindet sich der DVD-Navigator nachgeschaltet mit einem Audiodecoder, der eine Verbindung mit dem [DirectSound-Rendererfilter](directsound-renderer-filter.md)herstellt, dem Standardaudiorenderer. In den Video- und Unterbildstreams sind die Downstreamfilter der Videodecoder eines Drittanbieters und der VideoMischungsrenderer (oder [der Overlay Mixer](overlay-mixer-filter.md)und der [Videorenderer](video-renderer-filter.md) in downlevel-Anwendungen). Wenn Ihre Anwendung Zeilen 21-Daten mit Untertiteln verarbeitet, müssen Sie dem Diagramm den Filter DirectShow Line 21 Decoder 2 hinzufügen. Dies umfasst einen einzelnen Methodenaufruf. Der Filter wird automatisch verbunden.

Ihre Anwendung kommuniziert mit dem DVD-Navigator und steuert ihn über die benutzerdefinierten Schnittstellen, die der DVD-Navigator verfügbar macht: [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)– die "set"-Methoden – und [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)– die "get"-Methoden. Sie muss auch mit dem Filterdiagramm-Manager (über [**IMediaControl)**](/windows/desktop/api/Control/nn-control-imediacontrol)kommunizieren, um das Diagramm zu beenden, zu starten und andernfalls zu steuern. Möglicherweise müssen Sie auch andere einzelne Filter steuern, z. B. den Overlay Mixer filter for switching between windowed and full-screen display ." (Überlagerungsfilter zum Wechseln zwischen Fenstern und Vollbildanzeige). Weitere Informationen finden Sie unter [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2). Die genaue Konfiguration des Diagramms hängt davon ab, welche Art von MPEG-2-Decoder Sie installiert haben, ob Sie Daten mit Untertiteln in Zeile 21 und andere Faktoren verarbeiten müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



