---
description: Dieses Ereignis benachrichtigt den Installer, dass ein modales Dialogfeld in ein anderes Dialogfeld übergeht. Das Installationsprogramm entfernt das vorhandene Dialogfeld und erstellt das neue Dialogfeld mit dem Namen, der im-Argument angegeben ist.
ms.assetid: bd1aa465-55a0-4983-8c71-7e7075ee9dfb
title: Newdialog-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 439c459bc5bfe061cc7f888d9c0a3374afa9098b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130673"
---
# <a name="newdialog-controlevent"></a>Newdialog-ControlEvent

Dieses Ereignis benachrichtigt den Installer, dass ein modales Dialogfeld in ein anderes Dialogfeld übergeht. Das Installationsprogramm entfernt das vorhandene Dialogfeld und erstellt das neue Dialogfeld mit dem Namen, der im-Argument angegeben ist.

Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden. Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Eine Zeichenfolge, die den Namen des neuen Dialog Felds ist.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Diese ControlEvent führt keine Aktion für Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem modalen Dialogfeld ist an dieses Ereignis in der Tabelle [ControlEvent](controlevent-table.md) gebunden, um einen Übergang zum nächsten oder vorherigen Dialogfeld der gleichen Assistenten Sequenz zu signalisieren.

 

 



