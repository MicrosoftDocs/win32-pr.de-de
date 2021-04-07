---
description: Verfügbar machen von Erfassung und Komprimierungs Formaten
ms.assetid: f7466cfe-b13e-4ee9-82f9-0528ed97bf99
title: Verfügbar machen von Erfassung und Komprimierungs Formaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02051d9e68b3ad919b96dca53b674305787b3186
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747640"
---
# <a name="exposing-capture-and-compression-formats"></a>Verfügbar machen von Erfassung und Komprimierungs Formaten

In diesem Artikel wird beschrieben, wie Sie Erfassungs-und Komprimierungs Formate mit der [**iamstreamconfig:: getstreamcaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) -Methode zurückgeben. Diese Methode kann mehr Informationen über akzeptierte Medientypen als die herkömmliche Methode zum Auflisten der Medientypen einer PIN erhalten. Daher sollte Sie normalerweise stattdessen verwendet werden. **Getstreamcaps** kann Informationen zu den Arten von Formaten zurückgeben, die für Audiodaten oder Videos zulässig sind. Darüber hinaus enthält dieser Artikel einen Beispielcode, der veranschaulicht, wie die Eingabe-PIN eines Transformations Filters erneut verbunden wird, um sicherzustellen, dass Ihr Filter eine bestimmte Ausgabe erzeugt.

Die **getstreamcaps** -Methode gibt ein Array von Paaren von Medientyp-und Funktionsstrukturen zurück. Beim Medientyp handelt es sich um eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, und die Funktionen werden entweder durch eine [**\_ audiodatenstream- \_ Konfigurations \_**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) Ober Struktur oder eine [**\_ Textstream- \_ config \_**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) -Struktur dargestellt. Der erste Abschnitt dieses Artikels enthält ein Video Beispiel, und das zweite Beispiel zeigt ein Audiobeispiel.

Dieser Artikel enthält folgende Themen:

-   [Video Funktionen](video-capabilities.md)
-   [Audiofunktionen](audio-capabilities.md)
-   [Erneutes Verbinden Ihrer Eingabe, um bestimmte Ausgabetypen sicherzustellen](reconnecting-your-input-to-ensure-specific-output-types.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



