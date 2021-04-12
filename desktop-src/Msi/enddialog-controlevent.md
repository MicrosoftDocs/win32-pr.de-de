---
description: Dieses Ereignis benachrichtigt das Installationsprogramm, ein modales Dialogfeld zu entfernen. In jedem Fall entfernt das Installationsprogramm das vorhandene Dialogfeld.
ms.assetid: 74a28696-6387-4d62-8955-4708ba5872bb
title: EndDialog-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08449bffe29093e32066e92e1b8fc739efa02d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216374"
---
# <a name="enddialog-controlevent"></a>EndDialog-ControlEvent

Dieses Ereignis benachrichtigt das Installationsprogramm, ein modales Dialogfeld zu entfernen. In jedem Fall entfernt das Installationsprogramm das vorhandene Dialogfeld.

Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden. Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

In der folgenden Tabelle wird die Aktion des-Ereignisses aufgelistet, das sich aus verschiedenen in der [ControlEvent-Tabelle](controlevent-table.md)eingegebenen Argumenten ergibt.



| Argument | Aktion durch das Installationsprogramm                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beenden     | Die Assistenten Sequenz ist geschlossen, und das Steuerelement wird mit dem Userexit-Wert an das Installationsprogramm zurückgegeben. Dieses Argument kann nicht in einem Dialogfeld verwendet werden, das einem anderen Dialogfeld untergeordnet ist. |
| Erneut versuchen    | Die Assistenten Sequenz ist geschlossen, und das Steuerelement wird mit dem Suspend-Wert an das Installationsprogramm zurückgegeben. Dieses Argument kann nicht in einem Dialogfeld verwendet werden, das einem anderen Dialogfeld untergeordnet ist.  |
| Ignorieren   | Die Assistenten Sequenz ist geschlossen, und das Steuerelement wird mit dem fertigen Wert an das Installationsprogramm zurückgegeben. Dieses Argument kann nicht in einem Dialogfeld verwendet werden, das einem anderen Dialogfeld untergeordnet ist. |
| Rückgabewert   | Das Steuerelement wird an das übergeordnete Element des aktuellen Dialog Felds zurückgegeben, oder, wenn kein übergeordnetes Element vorhanden ist, wird das Steuerelement mit dem Wert Erfolg an das Installationsprogramm zurückgegeben                                 |



 

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

In regulären Dialogfeldern kann die Argument-Spalte der [ControlEvent-Tabelle](controlevent-table.md) "Return", "Exit", "Retry" oder "Ignore" lauten.

Im Dialogfeld Fehler kann die Argument-Spalte der [ControlEvent-Tabelle](controlevent-table.md) "errorok", "errorcancel", "errorabort", "errorretry", "errorignore", "erroryes" oder "errorno" lauten.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem modalen Dialogfeld ist an dieses Ereignis in der Tabelle [ControlEvent](controlevent-table.md) gebunden, um ein Dialogfeld zu schließen.

 

 



