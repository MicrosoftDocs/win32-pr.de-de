---
description: Dieses Ereignis benachrichtigt das Installationsprogramm, ein modales Dialogfeld in ein anderes Dialogfeld zu überwechseln. Das Installationsprogramm entfernt das aktuelle Dialogfeld und erstellt das neue Dialogfeld mit dem im Argument angegebenen Namen.
ms.assetid: bd1aa465-55a0-4983-8c71-7e7075ee9dfb
title: NewDialog ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aed643272bf5cb329e04dc73426d5448ad71cca781bd129992e29f03b02b9dd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519720"
---
# <a name="newdialog-controlevent"></a>NewDialog ControlEvent

Dieses Ereignis benachrichtigt das Installationsprogramm, ein modales Dialogfeld in ein anderes Dialogfeld zu überwechseln. Das Installationsprogramm entfernt das aktuelle Dialogfeld und erstellt das neue Dialogfeld mit dem im Argument angegebenen Namen.

Dieses Ereignis kann von einem [PushButton-Steuerelement oder einem](pushbutton-control.md) [SelectionTree-Steuerelement veröffentlicht werden.](selectiontree-control.md) Dieses Ereignis sollte in der [ControlEvent-Tabelle verfasst werden.](controlevent-table.md)

Für dieses ControlEvent muss die Benutzeroberfläche auf der vollständigen [*Benutzeroberflächenebene ausgeführt*](f-gly.md) werden. Dieses Ereignis funktioniert nicht mit einer reduzierten [*Benutzeroberfläche oder*](r-gly.md) einer [*einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Levels](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

Dieses ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Eine Zeichenfolge, die den Namen des neuen Dialogfelds angibt.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Dieses ControlEvent führt keine Aktion auf Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Ein [PushButton-Steuerelement](pushbutton-control.md) in einem modalen Dialogfeld ist an dieses Ereignis in der [ControlEvent-Tabelle](controlevent-table.md) gebunden, um einen Übergang zum nächsten oder vorherigen Dialogfeld derselben Assistentensequenz zu signalisieren.

 

 



