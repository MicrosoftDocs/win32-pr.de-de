---
description: Das Installationsprogramm verwendet das timeremainor-Ereignis, um die ungefähre verbleibende Zeit (in Sekunden) für die aktuelle Fortschritts Sequenz zu veröffentlichen.
ms.assetid: ec5fc2b3-13a9-4681-89f0-fd39bab1de5f
title: Timeremainung ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8978dfb7ed3be855921ad66af8554ea50972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050432"
---
# <a name="timeremaining-controlevent"></a>Timeremainung ControlEvent

Das Installationsprogramm verwendet das timeremainor-Ereignis, um die ungefähre verbleibende Zeit (in Sekunden) für die aktuelle Fortschritts Sequenz zu veröffentlichen. Die verbleibende Zeit kann in einem Dialogfeld durch ein [Text Steuer](text-control.md) Element angezeigt werden, das diese ControlEvent abonniert. Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.

Diese ControlEvent kann von einer Benutzeroberfläche verarbeitet werden, die auf der [*grundlegenden*](b-gly.md)Benutzeroberfläche, der [*reduzierten*](r-gly.md)Benutzeroberfläche oder der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Weitere Informationen zu UI-Ebenen finden Sie unter [Benutzeroberflächen](user-interface-levels.md)Ebenen.

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Keine.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [Text Steuer](text-control.md) Element in einem nicht modalem Dialogfeld abonniert dieses Ereignis über die [EventMapping-Tabelle](eventmapping-table.md) und verwendet das [timeremainung-Attribut](timeremaining-control-attribute.md) , um die verbleibende Zeit anzuzeigen.

Das gleiche Text Steuerelement, das das timeremainingcontrolevent abonniert, kann auch den [scriptinprogress ControlEvent](scriptinprogress-controlevent.md)abonnieren. In diesem Fall wird die vorläufige scriptinprogress-Meldungs Zeichenfolge durch die Zeichenfolge "verbleibende Zeit: XX Minuten" ersetzt.

 

 



