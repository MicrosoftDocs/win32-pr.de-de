---
description: Direktes Hosting eines DMO
ms.assetid: 10fb99cf-78d9-4519-9aec-23b0daeca9e2
title: Direktes Hosting eines DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3c933cf4eb946abb9ffefd5186159595480887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747657"
---
# <a name="directly-hosting-a-dmo"></a>Direktes Hosting eines DMO

In diesem Abschnitt wird beschrieben, wie eine Anwendung als direkter Client eines DMO fungieren kann. Die Anwendung übermittelt Eingaben an den DMO, der DMO erstellt eine Ausgabe, und die Anwendung verwendet die Ausgabe zum Rendern, zur weiteren Verarbeitung usw. Die Anwendung ist für Probleme verantwortlich, wie z. b. Speicher Belegung, Zeitplanung und Synchronisierung und Threading. Diese Anforderungen hängen von der Art der Anwendung ab.

Die Informationen in diesem Abschnitt gelten auch, wenn Sie eine Komponente schreiben, die als Schicht zwischen einer Anwendung und einem DMO fungiert (z. b. ein ActiveX-Steuerelement, das ein DMO hostet). Außerdem sollten Sie diesen Abschnitt lesen, wenn Sie ein DMO schreiben, da darin die Funktionen beschrieben werden, die von Ihrem DMO implementiert werden müssen.

Dieser Abschnitt enthält die folgenden Themen:

-   [Festlegen von Medientypen in einem DMO](setting-media-types-on-a-dmo.md)
-   [Verarbeiten von Daten in einem DMO](processing-data-in-a-dmo.md)
-   [Direkte Verarbeitung](in-place-processing.md)
-   [Optionale Streams](optional-streams.md)
-   [Implementieren von imediabuffer](implementing-imediabuffer.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von dmos](using-dmos.md)
</dt> </dl>

 

 



