---
description: Informationen zu digitalen Videos in DirectShow
ms.assetid: 0570bf7c-c38d-4ada-9593-27b9be117893
title: Informationen zu digitalen Videos in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061927618c1cb3340e0771376a7a1e232e078e043a554829f99580262ea29c58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664812"
---
# <a name="about-digital-video-in-directshow"></a>Informationen zu digitalen Videos in DirectShow

Digitales Video (DV) kann von einer DV-Kamera erfasst, in einer Datei auf dem Computer des Benutzers gespeichert oder mithilfe eines Videobandrecorders (VTR) auf Band gespeichert werden. Daher umfassen die Vorgänge, die eine Anwendung für einen DV-Datenstrom ausführen kann, Folgendes:

-   Erfassen Sie Livevideos von einer DV-Kamera.
-   Übertragen Sie DV-Daten vom VTR-Band an den Computer.
-   Übertragen Sie DV-Daten vom Computer an den VTR.
-   Liest DV-Daten aus einer Datei.
-   Schreiben sie DV-Daten in eine Datei.
-   Rendern Der Audio- und Videodatenstrom wird in einem DV-Stream gerendert.

DirectShow bietet die folgenden DV-Filter:

-   [MSDV-Treiber](msdv-driver.md). Der MSDV-Treiber steuert ein DV-Gerät, z. B. ein Messgerät. Das Gerät kann eine Kamerauntereinheit und eine VTR-Untereinheit haben. MSDV steuert beide Untereinheiten. Der MSDV-Treiber wird Anwendungen als DirectShow-Filter angezeigt.
-   [DV-Splitterfilter.](dv-splitter-filter.md) DV-Frames enthalten Audio- und Videodaten im gleichen Frame. Der DV-Splitterfilter extrahiert die Audiodaten und gibt sie als ein oder zwei Audiostreams aus. Die ursprünglichen Daten werden als separater DV-Videostream ausgegeben.
-   [DV-Videodecoder-Filter.](dv-video-decoder-filter.md) Decodiert DV-Video in unkomprimiertes Video.
-   [DV Video Encoder-Filter.](dv-video-encoder-filter.md) Codiert unkomprimierte Videos in DV-codierte Videos.
-   [DV Muxer](dv-muxer-filter.md). Kombiniert einen DV-Videostream mit einem oder zwei Audiostreams, um einen einzelnen überlappten DV-Stream zu erstellen.

Der DV-Splitter und der DV-Videodecoder arbeiten zusammen. Der Splitter verwendet den überlappten Stream und gibt separate Audio- und DV-Videostreams aus. Der Decoder konvertiert das DV-Video in unkomprimiertes Video. Die folgende Abbildung veranschaulicht diesen Prozess.

![DV-Splitter und DV-Decoder](images/dv-filters1.png)

Der DV-Videoencoder und der DV Muxer kehren den Prozess um: Der Encoder konvertiert unkomprimierte Videos in DV-Videos, und der Mux kombiniert Audio- und DV-Video, um einen einzelnen überlappten Datenstrom zu erstellen, wie im folgenden Diagramm dargestellt.

![dv encoder und dv muxer](images/dv-filters2.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



