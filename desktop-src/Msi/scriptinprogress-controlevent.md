---
description: Das Installationsprogramm verwendet dieses Ereignis, um eine Informationszeichenfolge anzuzeigen, während das Ausführungsskript der Installation kompiliert wird.
ms.assetid: 088e91e0-734a-4f18-8ceb-cfa4f904f75c
title: ScriptInProgress ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b2e92baf6f1ad3fd4a7ffb714aede88dc90d664564dd5d18f4c97e4d3bdc8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041420"
---
# <a name="scriptinprogress-controlevent"></a>ScriptInProgress ControlEvent

Das Installationsprogramm verwendet dieses Ereignis, um eine Informationszeichenfolge anzuzeigen, während das Ausführungsskript der Installation kompiliert wird. Die Informationszeichenfolge kann in einem Dialogfeld von einem [Textsteuerelement](text-control.md) angezeigt werden, das dieses ControlEvent abonniert. Dieses Ereignis sollte in der [EventMapping-Tabelle](eventmapping-table.md)erstellt werden.

Dieses ControlEvent kann von einer Benutzeroberfläche verarbeitet werden, die auf der [*grundlegenden Benutzeroberfläche,*](b-gly.md)der [*reduzierten Benutzeroberfläche*](r-gly.md)oder [*auf der vollständigen Benutzeroberflächenebene*](f-gly.md) ausgeführt wird. Informationen zu Benutzeroberflächenebenen finden Sie unter [Benutzeroberfläche Ebenen.](user-interface-levels.md)

## <a name="published-by"></a>Veröffentlicht von

Dieses ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Keine.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Ein [Textsteuerelement, das](text-control.md) ScriptInProgress abonniert, zeigt die in [der UIText-Tabelle](uitext-table.md)angegebene Textzeichenfolge an.

## <a name="typical-use"></a>Typische Verwendung

Während das Ausführungsskript kompiliert wird, zeigt das Installationsprogramm eine ProgressBar an, die die verbleibende Zeit vor dem Beginn der Skriptausführung angibt. Der Paketautor kann zu diesem Zeitpunkt eine vorläufige Meldung anzeigen, in der die ProgressBar erläutert wird. Um eine vorläufige Meldung anzuzeigen, schließen Sie ein [Text-Steuerelement](text-control.md) in dasselbe moduslose Dialogfeld ein wie die ProgressBar. Geben Sie an, dass dieses Textsteuerelement das ScriptInProgress ControlEvent über die [EventMapping-Tabelle abonniert.](eventmapping-table.md) Fügen Sie einen Eintrag in die [UIText-Tabelle](uitext-table.md) ein, wobei ScriptInProgress im Feld Schlüssel angegeben ist. Geben Sie die vorläufige Nachricht als Textzeichenfolge im Feld Text der UIText-Tabelle an. Während der Skriptkompilierung zeigt das Installationsprogramm diese Zeichenfolge dann im Textsteuerelement an. Der angezeigte Text verschwindet, sobald die Skriptkompilierung abgeschlossen ist.

Das gleiche Textsteuerelement, das das ScriptInProgress ControlEvent abonniert, kann auch das [TimeRemaining ControlEvent](timeremaining-controlevent.md)abonnieren. In diesem Fall wird der Text der vorläufigen ScriptInProgress-Zeichenfolge durch die Zeichenfolge "Verbleibende Zeit: xx Minuten" ersetzt.

 

 



