---
title: Arbeiten mit Streamingressourcen
description: Arbeiten mit Streamingressourcen
ms.assetid: 0258ad24-f1b9-4cb3-921c-068072fd2dbb
keywords:
- Windows Media Player-Plug-Ins,Echo-Beispielstreamingressourcen
- Plug-Ins, Echo-Beispielstreamingressourcen
- Plug-Ins für die digitale Signalverarbeitung, Echo-Beispielstreamingressourcen
- DSP-Plug-Ins, Echo-Beispielstreamingressourcen
- Echo DSP-Plug-In-Beispiel,Streamingressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 268dc57bfad71f8ee46a3b934e671e478ca6a78a6b05fc30b7123e7b3f7f6ba0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118567169"
---
# <a name="working-with-streaming-resources"></a>Arbeiten mit Streamingressourcen

Für das beispielbasierte DSP-Plug-In-Beispielprojekt, das vom Windows Media Player-Plug-In-Assistenten generiert wird, müssen keine Streamingressourcen vom Plug-In zugeordnet werden. Das Echo-Beispiel erfordert jedoch einen separaten Puffer, um die Audiodaten für einen bestimmten Zeitraum zu halten, um den Verzögerungseffekt zu erzeugen. Der Puffer wird von zwei Methoden verwaltet: **IMediaObject::AllocateStreamingResources**, wodurch der Puffer erstellt wird, und **IMediaObject::FreeStreamingResources**, das den Puffer freigibt. Die **IMediaObject-Methoden** werden in Echo.cpp implementiert.

Die folgenden Abschnitte enthalten weitere Informationen zum Verwalten der Puffer:

-   [Variablen zum Verwalten des Verzögerungspuffers](variables-to-manage-the-delay-buffer.md)
-   [Implementieren von IMediaObject::AllocateStreamingResources](implementing-imediaobject--allocatestreamingresources.md)
-   [Implementieren von IMediaObject::FreeStreamingResources](implementing-imediaobject--freestreamingresources.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Das Echobeispiel**](the-echo-sample.md)
</dt> </dl>

 

 




