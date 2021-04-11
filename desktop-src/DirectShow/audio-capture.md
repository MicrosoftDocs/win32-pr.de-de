---
description: Audioerfassung
ms.assetid: 2b7fbdcb-7b59-407e-8e82-e66bd5606507
title: Audioerfassung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e91c9063d96a5e56d078651c338b0ffd80f5aa79
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104342018"
---
# <a name="audio-capture"></a>Audioerfassung

Eine Anwendung kann mithilfe von DirectShow Audiodaten von Mikrofonen, Band Playern und anderen Geräten über die Eingaben auf der Soundkarte erfassen. Zu den typischen Szenarien gehören:

-   Aufzeichnen von VoiceOver-Erzählungen zum späteren DUBBING über einen Videostream.
-   Die typinstallation von Inhalt von Legacy-Inhalt in das digitale Format.
-   Erfassen von Stimme oder Musik für die Übertragung über ein Netzwerk.

Endbenutzer haben mehrere Optionen zum Erfassen von Audio von der Soundkarte auf der Festplatte. Bei den meisten Karten werden Anwendungen zum Mischen und Aufzeichnen von Audioeingaben bereitgestellt. Windows bietet Sound Recorder, eine einfache hilfsprogrammanwendung für die Aufzeichnung von einem Mikrofon. Der Windows Media Encoder kann als [DirectX-Medienobjekt](directx-media-objects.md) (DMO) in eine DirectShow-Anwendung integriert werden. In diesem Abschnitt wird beschrieben, wie Sie die audioerfassungs Funktionalität in Ihre eigene Anwendung mithilfe von DirectShow integrieren.

Dieser Abschnitt enthält die folgenden Themen:

-   [Informationen zum audioerfassungs Filter](about-the-audio-capture-filter.md)
-   [Auswählen eines Erfassungs Geräts](selecting-a-capture-device.md)
-   [Erstellen eines audioerfassungs Diagramms](creating-an-audio-capture-graph.md)
-   [Erstellen eines audioerfassungs Diagramms mit Vorschau](creating-an-audio-capture-graph-with-preview.md)
-   [Festlegen von Eigenschaften für die Audioerfassung](setting-audio-capture-properties.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DirectShow](using-directshow.md)
</dt> </dl>

 

 



