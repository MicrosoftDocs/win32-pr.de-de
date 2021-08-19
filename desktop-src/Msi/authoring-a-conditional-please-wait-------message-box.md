---
description: Im folgenden Beispiel wird veranschaulicht, wie sie ein bedingtes Meldungsfeld erstellen, das angezeigt wird und den Benutzer warnt, dass eine Hintergrundaufgabe immer noch ausgeführt wird, wenn der Benutzer ein angezeigtes Steuerelement vorzeitig aktiviert.
ms.assetid: 4a99a96b-50c2-42eb-82ad-acdfa186a71f
title: Erstellen eines "Please Wait . . ." Meldungsfeld
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f7abc26254b9656ca3d522fa7458ded30fbf09cc20a39a9f960e7509bee8a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086360"
---
# <a name="authoring-a-conditional-please-wait-message-box"></a>Erstellen eines bedingten "Please Wait..." Meldungsfeld

Im folgenden Beispiel wird veranschaulicht, wie sie ein bedingtes Meldungsfeld erstellen, das angezeigt wird und den Benutzer warnt, dass eine Hintergrundaufgabe immer noch ausgeführt wird, wenn der Benutzer ein angezeigtes Steuerelement vorzeitig aktiviert.

Das Beispiel veranschaulicht auch, wie [das SpawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md) im Allgemeinen verwendet werden kann, um ein Steuerelement zu schützen, das eine Aktion auslöst, die vom Abschluss einer Hintergrundaufgabe abhängig ist.

In diesem Beispiel [](selection-dialog.md) wird dem Benutzer während des Installationsvorgangs ein  Auswahldialogfeld mit drei Schaltflächen-Steuerelementen mit der Bezeichnung Jetzt **installieren,** Weiter und Datenträgerkosten angezeigt.  Beim Anzeigen dieses Dialogfelds führt das Installationsprogramm jedoch auch im Hintergrund eine Aufgabe mit Kosten für Speicherplatz aus. Der Autor möchte diese Schaltflächen vor der Aktivierung schützen und möchte, dass ein Meldungsfeld "Bitte warten" angezeigt wird, wenn der Benutzer auf eine der Schaltflächen klickt, bevor die Kostenerstellung abgeschlossen ist. Der Autor möchte außerdem, dass dieses Meldungsfeld die **Schaltfläche** Abbrechen enthält und nicht mehr angezeigt wird, sobald die Hintergrundaufgabe abgeschlossen ist.

**So zeigen Sie ein Dialogfeld an, in dem der Benutzer aufgefordert wird, zu warten, bis die Kosten für den Hintergrunddatenträger abgeschlossen sind**

1.  Verwenden Sie die Erstellungsfunktionen des Installationsprogramms, um der Dialogtabelle ein neues modales Dialogfeld namens **WaitForCosting** [hinzuzufügen.](dialog-table.md) Das Dialogfeld sollte eine Textzeichenfolge mit dem Hinweis "Please wait while disk space costing is completed" (Bitte warten Sie, bis die Speicherplatzkosten abgeschlossen sind) angezeigt werden.
2.  Fügen Sie diesem Dialogfeld ein einzelnes Schaltflächen-Steuerelement mit der Bezeichnung Abbrechen hinzu, indem Sie es in der [Control-Tabelle erstellen.](control-table.md)
3.  Verknüpfen Sie **die Schaltfläche Abbrechen** mit einem ControlEvent, das das **Dialogfeld WaitForCosting** schließt, indem Sie ein [EndDialog ControlEvent](enddialog-controlevent.md) in der [ControlEvent-Tabelle erstellen.](controlevent-table.md) Legen Sie das Argument des EndDialog Control-Ereignisses auf Exit fest.
4.  Verknüpfen Sie [ein SpawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md) mit den vorhandenen Steuerelementen **Install Now**( Jetzt installieren), **Next**(Weiter) und **Disk Cost** (Datenträgerkosten), die im Dialogfeld Auswahl [angezeigt](selection-dialog.md) werden. Legen Sie das Argument dieses ControlEvent in der ControlEvent-Tabelle auf das **Dialogfeld WaitForCosting** fest, und legen Sie den Ausdruck in der Spalte Bedingung der Tabelle auf [**CostingComplete**](costingcomplete.md) =1 fest.

 

 



