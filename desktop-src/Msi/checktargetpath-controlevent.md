---
description: Dieses Ereignis benachrichtigt das Installationsprogramm, dass es überprüfen muss, ob der ausgewählte Pfad gültig ist. Wenn der Pfad ungültig ist, blockiert dieses Ereignis weitere ControlEvents, die dem Steuerelement zugeordnet sind.
ms.assetid: b7c1de6e-5738-4ecb-a033-9379d79dddb9
title: Checktargetpath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49301dbe1fcc6becc1bc757a0fe487061e1dcdbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349163"
---
# <a name="checktargetpath-controlevent"></a>Checktargetpath ControlEvent

Dieses Ereignis benachrichtigt das Installationsprogramm, dass es überprüfen muss, ob der ausgewählte Pfad gültig ist. Wenn der Pfad ungültig ist, blockiert dieses Ereignis weitere ControlEvents, die dem Steuerelement zugeordnet sind.

Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden. Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Der Name der Eigenschaft, die den Pfad enthält. Wenn die Eigenschaft deretendiert ist, wird der Eigenschaftsname in eckige Klammern eingeschlossen.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Diese ControlEvent führt keine Aktion für Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem Dialogfeld zum Durchsuchen ist an dieses Ereignis in der Tabelle [ControlEvent](controlevent-table.md) gebunden, um den ausgewählten Pfad vor der Rückgabe zum Dialogfeld Auswahl zu überprüfen.

 

 



