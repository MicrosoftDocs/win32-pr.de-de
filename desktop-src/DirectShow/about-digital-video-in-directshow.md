---
description: Informationen zu digitalen Videos in DirectShow
ms.assetid: 0570bf7c-c38d-4ada-9593-27b9be117893
title: Informationen zu digitalen Videos in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f4ae0253754583bb89132289db87f0aad673d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104568028"
---
# <a name="about-digital-video-in-directshow"></a>Informationen zu digitalen Videos in DirectShow

Digitale Videos (DV) können von einer DV-Kamera aufgezeichnet, in einer Datei auf dem Computer des Benutzers gespeichert oder mithilfe eines Video Tape Recorder (VTR) auf einem Band gespeichert werden. Folglich umfassen die Vorgänge, die eine Anwendung in einem DV-Stream ausführen kann, Folgendes:

-   Erfassen Sie Live Videos von einer DV-Kamera.
-   Übertragen von DV-Daten vom VTR-Band an den Computer.
-   Übertragen von DV-Daten vom Computer an den VTR.
-   Lesen von DV-Daten aus einer Datei.
-   Schreiben von DV-Daten in eine Datei.
-   Die Audiodatei und das Video in einem DV-Stream.

DirectShow stellt die folgenden DV-Filter bereit:

-   [Msdv-Treiber](msdv-driver.md) Der msdv-Treiber steuert ein DV-Gerät (z. b. einen Camcorder). Das Gerät weist möglicherweise eine Kamera-Untereinheit und eine VTR-Untereinheit auf. Msdv steuert beide Subeinheiten. Der msdv-Treiber wird in Anwendungen als DirectShow-Filter angezeigt.
-   [DV-Splitter](dv-splitter-filter.md) Filter. DV-Frames enthalten Audiodateien und Videos im gleichen Frame. Der DV-Splitter Filter extrahiert die Audiodaten und gibt Sie als einen oder zwei Audiostreams aus. Die ursprünglichen Daten werden als separater DV-Videostream ausgegeben.
-   [DV-Video Decoder](dv-video-decoder-filter.md) -Filter. Decodiert DV-Video in unkomprimiertes Video.
-   [DV-Video Encoder](dv-video-encoder-filter.md) -Filter. Codiert unkomprimiertes Video in DV-codiertes Video.
-   [DV-Muxer](dv-muxer-filter.md). Kombiniert einen DV-Videostream mit einem oder zwei Audiostreams, um einen einzelnen verschachtelten DV-Stream zu erstellen.

Der DV-Splitter und der DV-Video Decoder arbeiten zusammen. Der Splitter nimmt den verschachtelten Stream und gibt separate Video-und DV-Videostreams aus. Der Decoder konvertiert das DV-Video in ein unkomprimiertes Video. Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.

![DV-Splitter und DV-Decoder](images/dv-filters1.png)

Der DV-Video Encoder und der DV-Muxer umkehren den Prozess: der Encoder konvertiert unkomprimierte Videos in DV-Video, und das MUX kombiniert Audio-und DV-Videos, um einen einzelnen überlappenden Datenstrom zu erstellen, wie im folgenden Diagramm dargestellt.

![DV-Encoder und DV-Muxer](images/dv-filters2.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



