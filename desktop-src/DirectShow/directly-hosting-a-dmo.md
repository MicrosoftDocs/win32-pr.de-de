---
description: Direktes Hosten eines DMO
ms.assetid: 10fb99cf-78d9-4519-9aec-23b0daeca9e2
title: Direktes Hosten eines DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f421ed470ae1d39c04054e1cb4ec6252652ed2083ea336a58525f60a6e525b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982990"
---
# <a name="directly-hosting-a-dmo"></a>Direktes Hosten eines DMO

In diesem Abschnitt wird beschrieben, wie eine Anwendung als direkter Client eines DMO fungieren kann. Die Anwendung übermittelt Eingaben an die DMO, die DMO erstellt die Ausgabe, und die Anwendung verwendet die Ausgabe für rendering, further processing oder andere Zwecke. Die Anwendung ist für Probleme wie Speicherbelegung, Zeitsteuerung und Synchronisierung sowie Threading verantwortlich. Diese Anforderungen hängen von der Art der Anwendung ab.

Die Informationen in diesem Abschnitt gelten auch, wenn Sie eine Komponente schreiben, die als Ebene zwischen einer Anwendung und einer DMO fungiert (z. B. ein ActiveX Control, das eine DMO hostet). Darüber hinaus sollten Sie diesen Abschnitt lesen, wenn Sie eine DMO schreiben, da darin die Funktionalität beschrieben wird, die ihr DMO implementieren muss.

Dieser Abschnitt enthält die folgenden Themen:

-   [Festlegen von Medientypen auf einem DMO](setting-media-types-on-a-dmo.md)
-   [Verarbeiten von Daten in einem DMO](processing-data-in-a-dmo.md)
-   [In-Place Processing](in-place-processing.md)
-   [Optionale Streams](optional-streams.md)
-   [Implementieren von IMediaBuffer](implementing-imediabuffer.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DMOs](using-dmos.md)
</dt> </dl>

 

 



