---
description: Mit diesem Ereignis wird das Installationsprogramm benachrichtigt, dass überprüft werden muss, ob der ausgewählte Pfad beschreibbar ist. Wenn der Pfad nicht geschrieben werden kann, blockiert das Ereignis weitere ControlEvents, die dem Steuerelement zugeordnet sind.
ms.assetid: 4672e2e4-a789-4050-81b9-92ec491745ac
title: Checkexistingtargetpath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1117de57c5474d196da1f40da6fda3cce60b8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347120"
---
# <a name="checkexistingtargetpath-controlevent"></a>Checkexistingtargetpath ControlEvent

Mit diesem Ereignis wird das Installationsprogramm benachrichtigt, dass überprüft werden muss, ob der ausgewählte Pfad beschreibbar ist. Wenn der Pfad nicht geschrieben werden kann, blockiert das Ereignis weitere ControlEvents, die dem Steuerelement zugeordnet sind.

Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden. Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Der Name der Eigenschaft, die den Pfad enthält. Wenn die Eigenschaft deretendiert ist, wird der Eigenschaftsname in eckige Klammern eingeschlossen.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Diese ControlEvent führt keine Aktion für Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem Dialogfeld zum Durchsuchen ist an dieses Ereignis in der Tabelle [ControlEvent](controlevent-table.md) gebunden, um den ausgewählten Pfad vor der Rückgabe zum Auswahl Dialogfeld zu überprüfen.

 

 



