---
description: Konfiguration des DVD-Filter Diagramms
ms.assetid: 0c68c456-2240-4090-b45c-bd098cfea645
title: Konfiguration des DVD-Filter Diagramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec7bb8757e5246fc01309fbef55e654436560b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522403"
---
# <a name="dvd-filter-graph-configuration"></a>Konfiguration des DVD-Filter Diagramms

In diesem Abschnitt werden die verschiedenen Filter Diagramm Konfigurationen für die DVD-Wiedergabe in DirectShow beschrieben. Diese Diagramme werden hauptsächlich zur Referenz bereitgestellt. Der DVD-Navigator erstellt das Diagramm. im Allgemeinen ist es nicht notwendig, die Details der Konfiguration des Diagramms zu verstehen. Weitere Informationen finden Sie unter [Building the DVD Filter Graph](building-the-dvd-filter-graph.md).

Die folgende Abbildung zeigt ein DVD-Filter Diagramm mit einem Software Decoder.

![DVD-Filter Diagramm für Windows XP](images/dvd-graph-xp.png)

Wenn ein Hardware Decoder vorhanden ist, wird er normalerweise direkt mit der Grafikkarte von einem Videoport verbunden. Dadurch können die decodierten Video Bits direkt an den Frame Puffer auf der Grafikkarte gesendet werden, ohne in den Host Speicher zu übergeben. Um diese direkte Verbindung unter früheren Versionen von Windows zu verwalten, unterstützt DirectShow DirectDraw Video Port Extensions (VPE) über eine Schnittstelle auf dem [Überlagerungs-Mischungs Filter](overlay-mixer-filter.md).

> [!Note]  
> Der Überlagerungs-Mixer ist nun veraltet.

 

In Windows XP und höher kann ein Hardware Decoder eine Verbindung mit dem [Video Port-Manager](video-port-manager.md) -Filter herstellen.

![DVD-Diagramm für Windows XP mit einem Hardware Decoder](images/dvd-hwgraph-xp.png)

In allen diesen Diagrammen ist der DVD-Navigator der Quell Filter. Er führt mehrere Aufgaben aus:

-   Liest die Navigations-und Videodaten von der Festplatte.
-   Demultiplexe der Video-, Audio-und Teil Bilddaten in separate Streams.
-   Pumpt die Streams zur weiteren Verarbeitung und zum endgültigen Rendering in das Diagramm.
-   Informiert ihre Anwendung über DVD-bezogene Ereignisse.

Im Audiostream stellt der DVD-Navigator eine Downstream-Verbindung mit einem Audiodecoder her, der eine Verbindung mit dem [DirectSound-rendererfilter](directsound-renderer-filter.md)herstellt, dem Standardaudiorenderer. In den Video-und subbildstreams sind die downstreamfilter der Video Decoder von Drittanbietern und der Video Mischungs-Renderer (oder der [Überlagerungs-Mixer](overlay-mixer-filter.md)und der [Videorenderer](video-renderer-filter.md) bei Anwendungen mit kompatible). Wenn die Anwendung die von Closed unterteilten Daten in Zeile 21 behandelt, müssen Sie den Filter DirectShow Line 21 Decoder 2 dem Diagramm hinzufügen. Dies umfasst einen einzelnen Methoden aufzurufen. der Filter wird automatisch verbunden.

Ihre Anwendung kommuniziert mit und steuert den DVD-Navigator über die benutzerdefinierten Schnittstellen, die der DVD-Navigator verfügbar macht: [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)– die "Set"-Methoden – und [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)– die "Get"-Methoden. Außerdem muss Sie mit dem Filter Graph-Manager (über [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) kommunizieren, um das Diagramm zu starten, zu starten und anderweitig zu steuern. Möglicherweise müssen Sie auch andere einzelne Filter steuern, z. b. den Überlagerungs Filter Filter zum Wechseln zwischen Fenster-und voll Bild Anzeige. Weitere Informationen finden Sie unter [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2). Die genaue Konfiguration des Diagramms variiert abhängig davon, welche Art von MPEG-2-Decoder Sie installiert haben, ob Sie die von Closed beschrifteten Zeilen 21 und anderen Faktoren verarbeiten müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



