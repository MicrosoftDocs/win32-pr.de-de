---
title: Arbeiten mit Streamingressourcen
description: Arbeiten mit Streamingressourcen
ms.assetid: 0258ad24-f1b9-4cb3-921c-068072fd2dbb
keywords:
- Windows Media Player-Plug-ins, Echo Sample Streaming Resources
- Plug-ins, Echo Sample Streaming-Ressourcen
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample Streaming-Ressourcen
- DSP-Plug-ins, Echo Sample Streaming-Ressourcen
- Echo DSP-Plug-in-Beispiel, Streamingressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a1df8cc221f3d75c8333b3ffd41a144d28bed7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341478"
---
# <a name="working-with-streaming-resources"></a>Arbeiten mit Streamingressourcen

Das vom Assistenten für den Windows-Media Player-Plug-in generierte Sample audiodsp-Plug-in-Projekt benötigt keine Streamingressourcen, die vom Plug-in zugeordnet werden. Das Echo-Beispiel erfordert jedoch einen separaten Puffer zum Speichern der Audiodaten für einen bestimmten Zeitraum, um den Verzögerungseffekt zu erzeugen. Der Puffer wird mit zwei Methoden verwaltet: **imediaobject:: depaseestreamingresources**, wodurch der Puffer erstellt wird, und **imediaobject:: freestreamingresources**, der den Puffer freigibt. Die **imediaobject** -Methoden werden in Echo. cpp implementiert.

In den folgenden Abschnitten finden Sie weitere Informationen zur Verwaltung der Puffer:

-   [Variablen zum Verwalten des Verzögerungs Puffers](variables-to-manage-the-delay-buffer.md)
-   [Implementieren von imediaobject:: Zuweisung](implementing-imediaobject--allocatestreamingresources.md)
-   [Implementieren von imediaobject:: freestreamingresources](implementing-imediaobject--freestreamingresources.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Das Echo-Beispiel**](the-echo-sample.md)
</dt> </dl>

 

 




