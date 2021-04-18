---
title: Verwenden von unkomprimierten Audiodaten und Videostreams
description: Verwenden von unkomprimierten Audiodaten und Videostreams
ms.assetid: 1a8fe604-bd99-4ba1-878f-8e1fd89483b3
keywords:
- Streams, Konfigurieren von nicht komprimierten Audiodatenströmen
- Codecs, Konfigurieren von nicht komprimierten Audiodaten und Videostreams
- Videostreams, nicht komprimiert
- Audiostreams, nicht komprimiert
- nicht komprimierte Audiodaten und Videostreams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00d81bd0a9f8c53751e404a0cfb0e55d57d4242
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106338440"
---
# <a name="using-uncompressed-audio-and-video-streams"></a>Verwenden von unkomprimierten Audiodaten und Videostreams

In den meisten Fällen sind bei nicht komprimierten Medien sehr hohe Speicher-und Übermittlungs Anforderungen zu erfüllen. für einige lokale Wiedergabe Szenarios ist die Qualitätsstufe jedoch wichtig genug, um die Verwendung der Komprimierung zu gewährleisten.

Die Einstellungen für einen unkomprimierten Mediendaten Strom sollten die Einstellungen der Quell Medien widerspiegeln. Wenn Sie einen unkomprimierten Stream konfigurieren, müssen Sie die Bitrate der Medien berechnen und den Stream entsprechend festlegen, indem Sie [**iwmstreamconfig:: setbitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate)aufrufen. Da nicht komprimierte Streams für das Streaming nicht nutzbar sind, sollten Sie das Puffer Fenster für nicht komprimierte Mediendaten Ströme immer auf NULL festlegen, indem Sie [**iwmstreamconfig:: setbufferwindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow)aufrufen.

Die folgenden Pixel Formate werden für unkomprimierte Videostreams unterstützt:

-   Wmmediasubtype \_ RGB555
-   Wmmediasubtype \_ RGB24
-   Wmmediasubtype \_ RGB32
-   Wmmediasubtype \_ I420
-   wmmediasubtype \_ IYUV
-   Wmmediasubtype \_ YV12
-   Wmmediasubtype \_ im YUY2
-   wmmediasubtype \_ UYVY
-   wmmediasubtype \_ yvyu

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Konfiguration für alle Streams**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Konfigurieren von Audiodatenströmen**](configuring-audio-streams.md)
</dt> <dt>

[**Konfigurieren von Streams**](configuring-streams.md)
</dt> <dt>

[**Konfigurieren von Videostreams**](configuring-video-streams.md)
</dt> </dl>

 

 




