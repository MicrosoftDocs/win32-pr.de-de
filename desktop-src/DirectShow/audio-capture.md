---
description: Audioaufnahme
ms.assetid: 2b7fbdcb-7b59-407e-8e82-e66bd5606507
title: Audioaufnahme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f76924e170c29e4488e2b7bd31bddbe8702ebe78d9ed146471bdfa21598d12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108710"
---
# <a name="audio-capture"></a>Audioaufnahme

Eine Anwendung kann DirectShow verwenden, um Audiodaten von Mikrofonen, Bandplayern und anderen Geräten über die Eingaben auf der Soundkarte zu erfassen. Zu den typischen Szenarien gehören:

-   Aufzeichnen einer Sprachausgabe zur späteren Färbung über einen Videostream.
-   Konvertieren von analogen Legacyaudioinhalten in ein digitales Format.
-   Erfassen von Stimme oder Musik für die Übertragung über ein Netzwerk.

Endbenutzer haben mehrere Optionen zum Erfassen von Audiodaten von der Soundkarte auf der Festplatte. Die meisten Karten bieten Anwendungen zum Mischen und Aufzeichnen aus ihren Audioeingaben. Windows bietet Sound Recorder, eine einfache Hilfsprogrammanwendung für die Aufzeichnung über ein Mikrofon. Der Windows Media Encoder kann in eine DirectShow-Anwendung als [DirectX](directx-media-objects.md) Media Object (DMO) integriert werden. In diesem Abschnitt wird beschrieben, wie Sie die Audioerfassungsfunktionen mit DirectShow in Ihre eigene Anwendung integrieren.

Dieser Abschnitt enthält die folgenden Themen:

-   [Informationen zum Audioaufnahmefilter](about-the-audio-capture-filter.md)
-   [Auswählen eines Erfassungsgeräts](selecting-a-capture-device.md)
-   [Erstellen eines Audioaufnahme-Graph](creating-an-audio-capture-graph.md)
-   [Erstellen eines Audio capture-Graph mit Vorschauversion](creating-an-audio-capture-graph-with-preview.md)
-   [Festlegen von Audioaufnahmeeigenschaften](setting-audio-capture-properties.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DirectShow](using-directshow.md)
</dt> </dl>

 

 



