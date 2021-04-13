---
description: Im folgenden Beispiel wird veranschaulicht, wie ein bedingtes Meldungs Feld erstellt wird, das angezeigt wird, und der Benutzer wird gewarnt, dass eine Hintergrundaufgabe noch ausgeführt wird, wenn der Benutzer ein angezeigtes Steuerelement vorzeitig aktiviert
ms.assetid: 4a99a96b-50c2-42eb-82ad-acdfa186a71f
title: Erstellen eines "Bitte warten. . ." Meldungs Feld
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c5f0cb1e4f1a0224c3b71d42d6fc63c1940483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528865"
---
# <a name="authoring-a-conditional-please-wait-message-box"></a>Erstellen einer bedingten "Bitte warten..." Meldungs Feld

Im folgenden Beispiel wird veranschaulicht, wie ein bedingtes Meldungs Feld erstellt wird, das angezeigt wird, und der Benutzer wird gewarnt, dass eine Hintergrundaufgabe noch ausgeführt wird, wenn der Benutzer ein angezeigtes Steuerelement vorzeitig aktiviert

Das Beispiel veranschaulicht auch, wie das [handlevent spawnwaitdialog](spawnwaitdialog-controlevent.md) verwendet werden kann, um ein Steuerelement zu schützen, das eine Aktion auslöst, die vom Abschluss einer Hintergrundaufgabe abhängig ist.

In diesem Beispiel wird dem Benutzer während der Installation ein [Auswahl Dialogfeld](selection-dialog.md) mit drei Push-Schaltflächen-Steuerelementen mit der Bezeichnung **jetzt installieren**, **weiter** und Datenträger **Kosten** angezeigt. Beim Anzeigen dieses Dialog Felds führt das Installationsprogramm jedoch auch einen Task für den Speicherplatz Kosten im Hintergrund aus. Der Autor möchte diese Schaltflächen vor der Aktivierung schützen und möchte, dass das Meldungs Feld "Bitte warten" angezeigt wird, wenn der Benutzer auf eine der Schaltflächen klickt, bevor die Kosten abgeschlossen sind. Der Autor möchte auch, dass dieses Meldungs Feld eine Schaltfläche **Abbrechen** enthält und nach Abschluss der Hintergrundaufgabe verschwindet.

**So zeigen Sie ein Dialogfeld an, das den Benutzer auffordert, zu warten, bis die Kosten für die Datenträger**

1.  Verwenden Sie die Erstellungs Funktionen des Installers, um ein neues modales Dialogfeld mit dem Namen **waitforkostenin** der [Dialogfeld Tabelle](dialog-table.md)hinzuzufügen. Im Dialogfeld sollte eine Text Zeichenfolge angezeigt werden, die besagt, dass der Speicherplatz auf dem Datenträger abgeschlossen ist.
2.  Fügen Sie diesem Dialogfeld mit der Bezeichnung **Abbrechen** ein einzelnes Push-Schaltflächen-Steuerelement hinzu, indem Sie es in der [Steuerelement Tabelle](control-table.md)erstellen.
3.  Verknüpfen Sie die Schaltfläche **Abbrechen (Abbrechen** ) mit einem ControlEvent, der das Dialogfeld **waitforkostenschließt** , indem Sie einen [EndDialog-ControlEvent](enddialog-controlevent.md) in der [ControlEvent-Tabelle](controlevent-table.md)erstellen. Legen Sie das-Argument des EndDialog-Steuerelement Ereignisses auf Exit fest.
4.  Verknüpfen Sie ein [spawnwaitdialog ControlEvent](spawnwaitdialog-controlevent.md) mit den vorhandenen Schaltflächen " **jetzt installieren**", " **weiter**" und "Datenträger **Kosten** ", die im Dialog Feld " [Auswahl](selection-dialog.md) " angezeigt werden. Legen Sie das Argument dieses ControlEvent in der Tabelle ControlEvent auf das Dialogfeld **waitforkostenfest** , und legen Sie den Ausdruck in der Spalte Bedingung der Tabelle auf " [**costingcomplete**](costingcomplete.md) = 1" fest.

 

 



