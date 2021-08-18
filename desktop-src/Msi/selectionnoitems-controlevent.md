---
description: Das SelectionTree-Steuerelement verwendet das SelectionNoItems-Ereignis, um veralteten Elementbeschreibungstext zu löschen oder Schaltflächen zu deaktivieren, die unbrauchbar geworden sind. Dieses Ereignis sollte in der EventMapping-Tabelle erstellt werden.
ms.assetid: a79abd77-a6e5-4a1f-8a63-51644151404a
title: SelectionNoItems ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17220849c6bf50a28a0a0596bcd347e2f0a4c5af77cb53c9d9fa0041ced59abe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040460"
---
# <a name="selectionnoitems-controlevent"></a>SelectionNoItems ControlEvent

Das [SelectionTree-Steuerelement](selectiontree-control.md) verwendet das SelectionNoItems-Ereignis, um veralteten Elementbeschreibungstext zu löschen oder Schaltflächen zu deaktivieren, die unbrauchbar geworden sind. Dieses Ereignis sollte in der [EventMapping-Tabelle](eventmapping-table.md)erstellt werden.

Für dieses ControlEvent muss die Benutzeroberfläche auf [*der vollständigen Benutzeroberflächenebene*](f-gly.md) ausgeführt werden. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzeroberfläche*](r-gly.md) oder [*einer einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Ebenen.](user-interface-levels.md)

Dieses Ereignis kann sich nur auf Steuerelemente auswirken, die sich im selben Dialogfeld wie das SelectionTree-Steuerelement befinden.

## <a name="published-by"></a>Veröffentlicht von

[SelectionTree-Steuerelement,](selectiontree-control.md) wenn die Auswahl keine Knoten aufweist.

## <a name="argument"></a>Argument

Keine.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Löscht veralteten Elementbeschreibungstext oder deaktiviert veraltete Schaltflächen.

## <a name="typical-use"></a>Typische Verwendung

Kann verwendet werden, um die Schaltflächen Weiter, Zurücksetzen und Datenträgercost im [Auswahldialogfeld](selection-dialog.md) zu deaktivieren, wenn eine Auswahl über keine Knoten verfügt und diese Schaltflächen unbrauchbar werden.

 

 



