---
title: Informationen über Diskontinuität
description: Informationen über Diskontinuität
ms.assetid: 29210758-a1e6-47f2-9428-38f79623fbca
keywords:
- Windows Media Player-Plug-ins, audiodsp
- Plug-ins, audiodsp
- Plug-Ins für die digitale Signalverarbeitung, Audiodiskontinuität
- DSP-Plug-ins, Audiodiskontinuität
- audiodsp-Plug-ins, Diskontinuität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0448220d4616122b3c99670357bbbd78de11c392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388025"
---
# <a name="about-discontinuity"></a>Informationen über Diskontinuität

Zu jedem Zeitpunkt kann Windows Media Player eine Unterbrechung im Eingabestream durch Aufrufen der **imediaobject::D iscontinuity** -Methode signalisieren. Dies tritt regelmäßig am Anfang und am Ende eines Streams und vor jedem Suchvorgang auf, oder wenn Streaming-Inhalte aus irgendeinem Grund unterbrochen werden. Das Beispiel-DSP-Plug-in, das vom Assistenten für Windows-Media Player-Plug-ins generiert wird, muss aus folgenden Gründen nicht mit Diskontinuitäten behandelt werden:

-   PCM-Beispiele sind atomarisch, d. h., Sie können ohne Rücksicht auf die anderen Beispiele im Stream verarbeitet werden. Einige Videoformate enthalten Daten, die von Keyframes und komprimierten Beispielen abhängen.
-   Der Beispielcode wird so geschrieben, dass der Client immer gezwungen wird, die gesamte Ausgabe zu verarbeiten, bevor das Plug-in mehr Eingaben akzeptiert.

Die Standard Implementierung von **imediaobject::D iscontinuity** gibt einfach S \_ OK zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren eines audiodsp-Plug-ins**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




