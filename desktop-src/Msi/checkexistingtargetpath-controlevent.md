---
description: Dieses Ereignis benachrichtigt das Installationsprogramm, dass es überprüfen muss, ob der ausgewählte Pfad schreibbar ist. Wenn der Pfad nicht geschrieben werden kann, blockiert das Ereignis weitere ControlEvents, die dem Steuerelement zugeordnet sind.
ms.assetid: 4672e2e4-a789-4050-81b9-92ec491745ac
title: CheckExistingTargetPath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d523d04eba4ede88ca1382c17c5d40d48dadadbc9520d766b5cfca2b26b77fb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520190"
---
# <a name="checkexistingtargetpath-controlevent"></a>CheckExistingTargetPath ControlEvent

Dieses Ereignis benachrichtigt das Installationsprogramm, dass es überprüfen muss, ob der ausgewählte Pfad schreibbar ist. Wenn der Pfad nicht geschrieben werden kann, blockiert das Ereignis weitere ControlEvents, die dem Steuerelement zugeordnet sind.

Dieses Ereignis kann von einem [PushButton-Steuerelement](pushbutton-control.md)oder einem [SelectionTree-Steuerelement](selectiontree-control.md)veröffentlicht werden. Dieses Ereignis sollte in der [ControlEvent-Tabelle](controlevent-table.md)erstellt werden.

Für dieses ControlEvent muss die Benutzeroberfläche auf [*der vollständigen Benutzeroberflächenebene*](f-gly.md) ausgeführt werden. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzeroberfläche*](r-gly.md) oder [*einer einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Ebenen.](user-interface-levels.md)

## <a name="published-by"></a>Veröffentlicht von

Dieses ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Der Name der Eigenschaft, die den Pfad enthält. Wenn die Eigenschaft indirekt ist, wird der Eigenschaftenname in eckige Klammern eingeschlossen.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Dieses ControlEvent führt keine Aktion auf Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Ein [PushButton-Steuerelement](pushbutton-control.md) in einem Dialogfeld zum Durchsuchen ist an dieses Ereignis in der [ControlEvent-Tabelle](controlevent-table.md) gebunden, um den ausgewählten Pfad zu überprüfen, bevor zum Auswahldialogfeld zurückzukehren.

 

 



