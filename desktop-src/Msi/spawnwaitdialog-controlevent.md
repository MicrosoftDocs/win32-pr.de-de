---
description: SpawnWaitDialog ControlEvent löst das dialogfeld aus, das von der Argument -Spalte der ControlEvent-Tabelle angegeben wird, wenn der Ausdruck in der Spalte Bedingung als FALSE ausgewertet wird.
ms.assetid: 38a5d896-2c11-4ce9-b829-104a882723b6
title: SpawnWaitDialog ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffeddfcb46f67d292de81a5a8195ba17c2a63b305be229ae96b2133448d41f00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628010"
---
# <a name="spawnwaitdialog-controlevent"></a>SpawnWaitDialog ControlEvent

Das SpawnWaitDialog ControlEvent löst das dialogfeld aus, das von der Argument -Spalte der [ControlEvent-Tabelle](controlevent-table.md)angegeben wird, wenn der Ausdruck in der Spalte Bedingung als FALSE ausgewertet wird. Das Dialogfeld bleibt so lange verfügbar, wie der bedingte Ausdruck FALSE bleibt, und wird entfernt, sobald die Bedingung TRUE auswertet.

Dieses Ereignis kann von einem [PushButton-Steuerelement oder einem](pushbutton-control.md) [SelectionTree-Steuerelement veröffentlicht werden.](selectiontree-control.md) Dieses Ereignis sollte in der [ControlEvent-Tabelle verfasst werden.](controlevent-table.md)

Für dieses ControlEvent muss die Benutzeroberfläche auf der vollständigen [*Benutzeroberflächenebene ausgeführt*](f-gly.md) werden. Dieses Ereignis funktioniert nicht mit einer reduzierten [*Benutzeroberfläche oder*](r-gly.md) einer [*einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Levels](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

Dieses ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Ein Dialogfeld in der [Tabelle Dialog.](dialog-table.md)

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Das SpawnWaitDialog ControlEvent kann verwendet werden, um auf jede Hintergrundaufgabe zu warten, deren Abschluss mithilfe eines bedingten Ausdrucks, z. B. des Zustands einer Eigenschaft, getestet werden kann. Ein Beispiel für die Verwendung von SpawnWaitDialog ControlEvent finden Sie im Abschnitt Erstellen eines bedingten ["Please wait . . ". Meldungsfeld](authoring-a-conditional-please-wait-------message-box.md).

 

 



