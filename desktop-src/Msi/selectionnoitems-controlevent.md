---
description: Das SelectionTree-Steuerelement verwendet das selectionnoitems-Ereignis, um veralteten Element Beschreibungstext zu löschen oder um Schaltflächen zu deaktivieren, die unbrauchbar werden. Dieses Ereignis sollte in der Tabelle EventMapping erstellt werden.
ms.assetid: a79abd77-a6e5-4a1f-8a63-51644151404a
title: Selectionnoitems ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544dfcaad3d22b63d71703ea95d1aa4f09a1efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363005"
---
# <a name="selectionnoitems-controlevent"></a>Selectionnoitems ControlEvent

Das [SelectionTree-Steuer](selectiontree-control.md) Element verwendet das selectionnoitems-Ereignis, um veralteten Element Beschreibungstext zu löschen oder um Schaltflächen zu deaktivieren, die unbrauchbar werden. Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

Dieses Ereignis kann sich nur auf Steuerelemente auswirken, die sich im gleichen Dialogfeld wie das SelectionTree-Steuerelement befinden.

## <a name="published-by"></a>Veröffentlicht von

[SelectionTree-Steuer](selectiontree-control.md) Element, wenn die Auswahl keine Knoten aufweist.

## <a name="argument"></a>Argument

Keine.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Löscht veraltete Element Beschreibungstext oder deaktiviert veraltete Schaltflächen.

## <a name="typical-use"></a>Typische Verwendung

Kann verwendet werden, um die Schaltflächen "Next", "Reset" und "diskcost" im [Auswahl Dialogfeld](selection-dialog.md) zu deaktivieren, wenn eine Auswahl keine Knoten aufweist und diese Schaltflächen unbrauchbar werden

 

 



