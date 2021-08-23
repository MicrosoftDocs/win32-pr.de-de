---
description: Dieses Ereignis benachrichtigt das Installationsprogramm, dass es überprüfen muss, ob der ausgewählte Pfad gültig ist. Wenn der Pfad ungültig ist, blockiert dieses Ereignis weitere ControlEvents, die dem Steuerelement zugeordnet sind.
ms.assetid: b7c1de6e-5738-4ecb-a033-9379d79dddb9
title: CheckTargetPath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d8ae179a3d6e0debba4cecfd620bc0cebf99361875517d944886b82ff4d55f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066060"
---
# <a name="checktargetpath-controlevent"></a>CheckTargetPath ControlEvent

Dieses Ereignis benachrichtigt das Installationsprogramm, dass es überprüfen muss, ob der ausgewählte Pfad gültig ist. Wenn der Pfad ungültig ist, blockiert dieses Ereignis weitere ControlEvents, die dem Steuerelement zugeordnet sind.

Dieses Ereignis kann von einem [PushButton-Steuerelement](pushbutton-control.md)oder einem [SelectionTree-Steuerelement](selectiontree-control.md)veröffentlicht werden. Dieses Ereignis sollte in der [ControlEvent-Tabelle](controlevent-table.md)erstellt werden.

Für dieses ControlEvent muss die Benutzeroberfläche auf [*der vollständigen Benutzeroberflächenebene*](f-gly.md) ausgeführt werden. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzeroberfläche*](r-gly.md) oder [*einer einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Ebenen.](user-interface-levels.md)

## <a name="published-by"></a>Veröffentlicht von

Dieses ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Der Name der Eigenschaft, die den Pfad enthält. Wenn die Eigenschaft indirekt ist, wird der Eigenschaftenname in eckige Klammern eingeschlossen.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Dieses ControlEvent führt keine Aktion auf Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Ein [PushButton-Steuerelement](pushbutton-control.md) in einem Dialogfeld zum Durchsuchen ist an dieses Ereignis in der [ControlEvent-Tabelle](controlevent-table.md) gebunden, um den ausgewählten Pfad vor dem Kehren zum Auswahldialogfeld zu überprüfen.

 

 



