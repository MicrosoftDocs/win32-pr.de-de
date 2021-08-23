---
description: Verfügbarmachen von Erfassungs- und Komprimierungsformaten
ms.assetid: f7466cfe-b13e-4ee9-82f9-0528ed97bf99
title: Verfügbarmachen von Erfassungs- und Komprimierungsformaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80821ade82b894a7c3e2752528ffdd72bc2223a4616b629f7e2b236461b31e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685740"
---
# <a name="exposing-capture-and-compression-formats"></a>Verfügbarmachen von Erfassungs- und Komprimierungsformaten

In diesem Artikel wird beschrieben, wie Erfassungs- und Komprimierungsformate mithilfe der [**IAMStreamConfig::GetStreamCaps-Methode**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) zurückgegeben werden. Diese Methode kann mehr Informationen zu akzeptierten Medientypen erhalten als die herkömmliche Methode zum Aufzählen der Medientypen eines Pins, sodass sie in der Regel stattdessen verwendet werden sollte. **GetStreamCaps** kann Informationen zu den Für Audio- oder Videodaten zulässigen Formaten zurückgeben. Darüber hinaus enthält dieser Artikel Beispielcode, der veranschaulicht, wie der Eingabepin eines Transformationsfilters erneut verbunden wird, um sicherzustellen, dass Ihr Filter eine bestimmte Ausgabe erzeugen kann.

Die **GetStreamCaps-Methode** gibt ein Array von Paaren von Medientyp- und Funktionenstrukturen zurück. Der Medientyp ist eine [**AM \_ MEDIA \_ TYPE-Struktur,**](/windows/win32/api/strmif/ns-strmif-am_media_type) und die Funktionen werden entweder durch eine AUDIO STREAM [**\_ \_ CONFIG \_ CAPS-Struktur**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) oder eine [**VIDEO STREAM \_ \_ CONFIG \_ CAPS-Struktur**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) dargestellt. Der erste Abschnitt dieses Artikels enthält ein Videobeispiel und der zweite ein Audiobeispiel.

Dieser Artikel enthält folgende Themen:

-   [Videofunktionen](video-capabilities.md)
-   [Audiofunktionen](audio-capabilities.md)
-   [Erneutes Verbinden ihrer Eingabe, um bestimmte Ausgabetypen sicherzustellen](reconnecting-your-input-to-ensure-specific-output-types.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



