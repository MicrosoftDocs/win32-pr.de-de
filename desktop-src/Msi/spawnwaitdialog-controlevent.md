---
description: Das handlevent spawnwaitdialog löst das von der Argument-Spalte der ControlEvent-Tabelle angegebene Dialogfeld aus, wenn der Ausdruck in der Spalte Bedingung als false ausgewertet wird.
ms.assetid: 38a5d896-2c11-4ce9-b829-104a882723b6
title: Spawnwaitdialog ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20059c936a8534d00799c93dfbe3408a19c6dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959034"
---
# <a name="spawnwaitdialog-controlevent"></a>Spawnwaitdialog ControlEvent

Das handlevent spawnwaitdialog löst das von der Argument-Spalte der [ControlEvent-Tabelle](controlevent-table.md)angegebene Dialogfeld aus, wenn der Ausdruck in der Spalte Bedingung als false ausgewertet wird. Das Dialogfeld bleibt so lange aktiv, bis der bedingte Ausdruck false bleibt, und wird entfernt, sobald die Bedingung "true" ergibt.

Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden. Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Ein Dialogfeld in der [Dialogfeld Tabelle](dialog-table.md).

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Das handlevent spawnwaitdialog kann verwendet werden, um auf alle Hintergrundaufgaben zu warten, deren Abschluss mit einem bedingten Ausdruck wie dem Zustand einer Eigenschaft getestet werden kann. Ein Beispiel für die Verwendung des handlevent spawnwaitdialog finden Sie im Abschnitt [Erstellen einer bedingten "Bitte warten..." ](authoring-a-conditional-please-wait-------message-box.md)Meldungs Feld.

 

 



