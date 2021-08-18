---
description: Das Installationsprogramm verwendet dieses Ereignis, um den Namen der aktuellen Aktion zu veröffentlichen. Der Name kann in einem Dialogfeld von einem Textsteuerelement angezeigt werden, das dieses ControlEvent abonniert. Dieses Ereignis sollte in der EventMapping-Tabelle erstellt werden.
ms.assetid: 2b4928fe-2d5c-46c1-8a31-cbebbc78d304
title: ActionText ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a216cb30dbcaa0be9972f12f7a83c8e45e5bb5686d93ce210bf96087aa3c4552
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927380"
---
# <a name="actiontext-controlevent"></a>ActionText ControlEvent

Das Installationsprogramm verwendet dieses Ereignis, um den Namen der aktuellen Aktion zu veröffentlichen. Der Name kann in einem Dialogfeld von einem [Textsteuerelement](text-control.md) angezeigt werden, das dieses ControlEvent abonniert. Dieses Ereignis sollte in der [EventMapping-Tabelle](eventmapping-table.md)erstellt werden.

Dieses ControlEvent kann von einer Benutzeroberfläche verarbeitet werden, die auf der [*grundlegenden Benutzeroberfläche,*](b-gly.md)der [*reduzierten Benutzeroberfläche*](r-gly.md)oder [*auf der vollständigen Benutzeroberflächenebene*](f-gly.md) ausgeführt wird. Informationen zu Benutzeroberflächenebenen finden Sie unter [Benutzeroberfläche Ebenen.](user-interface-levels.md)

## <a name="published-by"></a>Veröffentlicht von

Dieses ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Dieses ControlEvent verwendet kein Argument.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Die Abonnenten werden angezeigt, wenn neue Statusdaten vom Installationsprogramm eintreffen.

## <a name="typical-use"></a>Typische Verwendung

Ein [Textsteuerelement](text-control.md) in einem moduslosen Dialogfeld abonniert dieses Ereignis über die [EventMapping-Tabelle](eventmapping-table.md). Das [Textsteuerelementattribut](text-control-attribute.md) sollte im Feld Attribute dieser Tabelle aufgeführt werden, um den Namen der aktuellen Aktion zu erhalten.

 

 



