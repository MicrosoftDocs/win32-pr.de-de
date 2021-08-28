---
description: Das Installationsprogramm verwendet dieses Ereignis, um Daten für die neueste Aktion zu veröffentlichen. Die Daten können in einem Dialogfeld von einem Textsteuerelement angezeigt werden, das dieses ControlEvent abonniert. Dieses Ereignis sollte in der EventMapping-Tabelle erstellt werden.
ms.assetid: 3c0ab7d0-35f2-4966-8eff-f9f0419d8eed
title: ActionData ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8c280bbd2c0a184ec281e4401037687893942b4c344824b20a59c410b59fce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105480"
---
# <a name="actiondata-controlevent"></a>ActionData ControlEvent

Das Installationsprogramm verwendet dieses Ereignis, um Daten für die neueste Aktion zu veröffentlichen. Die Daten können in einem Dialogfeld von einem [Textsteuerelement](text-control.md) angezeigt werden, das dieses ControlEvent abonniert. Dieses Ereignis sollte in der [EventMapping-Tabelle](eventmapping-table.md)erstellt werden.

Dieses ControlEvent kann von einer Benutzeroberfläche verarbeitet werden, die auf der [*grundlegenden Benutzeroberfläche,*](b-gly.md)der [*reduzierten Benutzeroberfläche*](r-gly.md)oder [*auf der vollständigen Benutzeroberflächenebene*](f-gly.md) ausgeführt wird. Informationen zu Benutzeroberflächenebenen finden Sie unter [Benutzeroberfläche Ebenen.](user-interface-levels.md)

## <a name="published-by"></a>Veröffentlicht von

Dieses ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Dieses ControlEvent verwendet kein Argument.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Die Abonnenten werden ausgeblendet, wenn eine neue Aktion gestartet und angezeigt wird, wenn neue Aktionsdaten vom Installationsprogramm eintreffen.

## <a name="typical-use"></a>Typische Verwendung

Ein [Textsteuerelement](text-control.md) in einem moduslosen Dialogfeld abonniert dieses Ereignis über die [EventMapping-Tabelle](eventmapping-table.md). Das [Textsteuerelementattribut](text-control-attribute.md) wird im Feld Attribute dieser Tabelle aufgeführt, um die aktuellen Aktionsdaten zu empfangen. Wird in der Regel verwendet, um die Namen der Dateien anzuzeigen, die während des Dateikopiervorgang kopiert wurden.

 

 



