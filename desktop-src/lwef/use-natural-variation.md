---
title: Natürliche Variation verwenden
description: Natürliche Variation verwenden
ms.assetid: 5d5750e4-cf30-43dc-9419-7e6bbdb9aa5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fd2d35afeb168dc8839ba259f0079434b487c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100642"
---
# <a name="use-natural-variation"></a>Natürliche Variation verwenden

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Obwohl die Konsistenz der Darstellung in der herkömmlichen Schnittstelle Ihrer Anwendung, wie z. b. Menüs und Dialogfeldern, die Schnittstelle besser vorhersagbar macht, verändern Sie die Animation und die gesprochene Ausgabe in der Schnittstelle des Zeichens. Eine angemessene Variation der Zeichen Antworten bietet eine natürlichere Oberfläche. Wenn ein Zeichen den Benutzer immer genau auf die gleiche Weise adressiert, Wenn Sie z. b. immer die gleichen Wörter sagen, ist es wahrscheinlich, dass der Benutzer das Zeichen langweilig, uneigennützig oder sogar ungrob betrachtet. Die menschliche Kommunikation umfasst selten eine genaue Wiederholung. Auch wenn etwas in ähnlicher Situation wiederholt wird, können wir den Wortlaut, Gesten oder Gesichtsausdruck ändern.

Mit dem Microsoft-Agent können Sie in einer Variation für ein Zeichen erstellen. Wenn Sie die Animationen eines Zeichens definieren, können Sie die Verzweigungs Wahrscheinlichkeiten in jedem Animations Frame verwenden, um eine Animation zu ändern, wenn Sie wiedergegeben wird. Sie können jedem Zustand auch mehrere Animationen zuweisen. Der Microsoft-Agent wählt nach dem Zufallsprinzip eine der zugewiesenen Animationen aus. Bei der Sprachausgabe können Sie auch vertikale Balken Zeichen in den Ausgabetext einschließen, damit der gesprochene Text automatisch variiert. Der Microsoft-Agent wählt z. b. nach dem Zufallsprinzip eine der folgenden Anweisungen aus, wenn dieser Text als Teil der [**Sprech**](speak-method.md) Methode verarbeitet wird:

"Ich kann dies sagen. \| Das kann ich sagen. \| Ich kann etwas anderes sagen. "

 

 




