---
description: Das Installationsprogramm verwendet das TimeRemaining-Ereignis, um die ungefähre verbleibende Zeit (in Sekunden) für die aktuelle Statussequenz zu veröffentlichen.
ms.assetid: ec5fc2b3-13a9-4681-89f0-fd39bab1de5f
title: TimeRemaining ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fa29184c489e3d3a0b0f71d0dcd01297aa5359b25b3c463d3ccd3def6991257
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810710"
---
# <a name="timeremaining-controlevent"></a>TimeRemaining ControlEvent

Das Installationsprogramm verwendet das TimeRemaining-Ereignis, um die ungefähre verbleibende Zeit (in Sekunden) für die aktuelle Statussequenz zu veröffentlichen. Die verbleibende Zeit kann in einem Dialogfeld von einem [Textsteuerelement](text-control.md) angezeigt werden, das dieses ControlEvent abonniert. Dieses Ereignis sollte in der [EventMapping-Tabelle](eventmapping-table.md)erstellt werden.

Dieses ControlEvent kann von einer Benutzeroberfläche verarbeitet werden, die auf der [*grundlegenden Benutzeroberfläche,*](b-gly.md)der [*reduzierten Benutzeroberfläche*](r-gly.md)oder [*auf der vollständigen Benutzeroberflächenebene*](f-gly.md) ausgeführt wird. Informationen zu Benutzeroberflächenebenen finden Sie unter [Benutzeroberfläche Ebenen.](user-interface-levels.md)

## <a name="published-by"></a>Veröffentlicht von

Dieses ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Keine.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [Textsteuerelement](text-control.md) in einem moduslosen Dialogfeld abonniert dieses Ereignis über die [EventMapping-Tabelle](eventmapping-table.md) und verwendet das [TimeRemaining-Attribut,](timeremaining-control-attribute.md) um die verbleibende Zeit anzuzeigen.

Das gleiche Textsteuerelement, das das TimeRemaining ControlEvent abonniert, kann auch [scriptInProgress ControlEvent](scriptinprogress-controlevent.md)abonnieren. In diesem Fall wird sie als vorläufige ScriptInProgress-Meldungszeichenfolge durch die Zeichenfolge "Verbleibende Zeit: xx Minuten" ersetzt.

 

 



