---
title: Verwenden von unkomprimierten Audio- und Videodateien Streams
description: Verwenden von unkomprimierten Audio- und Videodateien Streams
ms.assetid: 1a8fe604-bd99-4ba1-878f-8e1fd89483b3
keywords:
- Streams,Konfigurieren von unkomprimierten Audio- und Videostreams
- Codecs,Konfigurieren von unkomprimierten Audio- und Videostreams
- Videostreams,unkomprimiert
- Audiostreams,unkomprimiert
- Unkomprimierte Audio- und Videostreams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f71809686413b386508da59879c81ea7b2d68204b6c210503aa80fa0dd37c4d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117844903"
---
# <a name="using-uncompressed-audio-and-video-streams"></a>Verwenden von unkomprimierten Audio- und Videodateien Streams

In den meisten Fällen gelten für unkomprimierte Medien sehr große Speicher- und Übermittlungsanforderungen, aber für einige lokale Wiedergabeszenarien ist die Qualitätsstufe wichtig genug, um die Verwendung der Komprimierung zu rechtfertigen.

Die Einstellungen für einen nicht komprimierten Medienstream sollten die Einstellungen des Quellmediums widerspiegeln. Beim Konfigurieren eines unkomprimierten Streams müssen Sie die Bitrate des Mediums berechnen und den Stream entsprechend festlegen, indem Sie [**IWMStreamConfig::SetBitrate aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) Da nicht komprimierte Streams für das Streaming nicht praktikabel sind, sollten Sie das Pufferfenster für nicht komprimierte Medienstreams immer auf null festlegen, indem Sie [**IWMStreamConfig::SetBufferWindow aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow)

Die folgenden Pixelformate werden für nicht komprimierte Videostreams unterstützt:

-   WMMEDIASUBTYPE \_ RGB555
-   WMMEDIASUBTYPE \_ RGB24
-   WMMEDIASUBTYPE \_ RGB32
-   WMMEDIASUBTYPE \_ I420
-   WMMEDIASUBTYPE \_ IYUV
-   WMMEDIASUBTYPE \_ YV12
-   WMMEDIASUBTYPE \_ YUY2
-   WMMEDIASUBTYPE \_ UYMEDIA
-   WMMEDIASUBTYPE \_ YVMEDIA

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Configuration Common to All Streams**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Konfigurieren von Audiodaten Streams**](configuring-audio-streams.md)
</dt> <dt>

[**Konfigurieren Streams**](configuring-streams.md)
</dt> <dt>

[**Konfigurieren von Streams**](configuring-video-streams.md)
</dt> </dl>

 

 




