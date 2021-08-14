---
description: Dieses Ereignis benachrichtigt das Installationsprogramm, ein modales Dialogfeld zu entfernen. In allen Fällen entfernt das Installationsprogramm das aktuelle Dialogfeld.
ms.assetid: 74a28696-6387-4d62-8955-4708ba5872bb
title: EndDialog ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f6e61ab12f072e31d6e4efc5f3d2b27ef8629c933baad65fb101b1078ca1f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378252"
---
# <a name="enddialog-controlevent"></a>EndDialog ControlEvent

Dieses Ereignis benachrichtigt das Installationsprogramm, ein modales Dialogfeld zu entfernen. In allen Fällen entfernt das Installationsprogramm das aktuelle Dialogfeld.

Dieses Ereignis kann von einem [PushButton-Steuerelement](pushbutton-control.md)oder einem [SelectionTree-Steuerelement veröffentlicht werden.](selectiontree-control.md) Dieses Ereignis sollte in der [ControlEvent-Tabelle verfasst werden.](controlevent-table.md)

Für dieses ControlEvent muss die Benutzeroberfläche auf der vollständigen [*Benutzeroberflächenebene ausgeführt*](f-gly.md) werden. Dieses Ereignis funktioniert nicht mit einer reduzierten [*Benutzeroberfläche oder*](r-gly.md) einer [*einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Levels](user-interface-levels.md).

In der folgenden Tabelle ist die Aktion des Ereignisses aufgeführt, das sich aus verschiedenen Argumenten ergibt, die in die [ControlEvent-Tabelle eingegeben wurden.](controlevent-table.md)



| Argument | Aktion durch das Installationsprogramm                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beenden     | Die Assistentensequenz wird geschlossen, und das Steuerelement kehrt mit dem Wert UserExit zum Installationsprogramm zurück. Dieses Argument kann nicht in einem Dialogfeld verwendet werden, das ein untergeordnetes Dialogfeld eines anderen Dialogfelds ist. |
| Erneut versuchen    | Die Assistentensequenz wird geschlossen, und das Steuerelement kehrt mit dem Suspend-Wert zum Installationsprogramm zurück. Dieses Argument kann nicht in einem Dialogfeld verwendet werden, das ein untergeordnetes Dialogfeld eines anderen Dialogfelds ist.  |
| Ignorieren   | Die Assistentensequenz wird geschlossen, und das Steuerelement kehrt mit dem Wert Finished zum Installationsprogramm zurück. Dieses Argument kann nicht in einem Dialogfeld verwendet werden, das ein untergeordnetes Dialogfeld eines anderen Dialogfelds ist. |
| Rückgabewert   | Das Steuerelement kehrt zum übergeordneten Element des aktuellen Dialogfelds zurück, oder wenn kein übergeordnetes Element vorhanden ist, kehrt das Steuerelement mit dem Wert Success zum Installationsprogramm zurück.                                 |



 

## <a name="published-by"></a>Veröffentlicht von

Dieses ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

In regulären Dialogfeldern kann die Argument -Spalte der [ControlEvent-Tabelle](controlevent-table.md) "Return", "Exit", "Retry" oder "Ignore" sein.

In Fehlerdialogfeldern kann die Argument -Spalte der [ControlEvent-Tabelle](controlevent-table.md) "ErrorOk", "ErrorCancel", "ErrorAbort", "ErrorRetry", "ErrorIgnore", "ErrorYes" oder "ErrorNo" sein.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [PushButton-Steuerelement](pushbutton-control.md) in einem modalen Dialogfeld ist an dieses Ereignis in der [ControlEvent-Tabelle](controlevent-table.md) gebunden, um ein Dialogfeld zu schließen.

 

 



