---
description: Das Installationsprogramm führt die Sequenz des Installations-Assistenten des Beispiels nur aus, wenn die vollständige Benutzeroberflächenebene zum Installieren der Anwendung verwendet wird.
ms.assetid: 323d62ae-333b-49fd-96a1-55b228c8ab2c
title: Hinzufügen eines Steuerelementereignisses am Ende der Installation zum Ausführen des Starts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0cf2a32a30187ea263bd2e3530e6eaae7d236e111826cbcab2461746d9c8e48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078220"
---
# <a name="adding-a-control-event-at-the-end-of-the-installation-to-run-launch"></a>Hinzufügen eines Steuerelementereignisses am Ende der Installation zum Ausführen des Starts

Das Installationsprogramm führt die Sequenz des Installations-Assistenten des Beispiels nur aus, wenn die [*vollständige Benutzeroberflächenebene*](f-gly.md) zum Installieren der Anwendung verwendet wird. Das letzte Dialogfeld der Beispieldialogsequenz ist ein [ExitDialog](exit-dialog.md) mit dem Namen ExitDialog. Wenn ein Benutzer mit der Schaltfläche OK in ExitDialog interagiert, wird zuerst ein [EndDialog ControlEvent](enddialog-controlevent.md) veröffentlicht, das das Steuerelement an das Installationsprogramm zurückgibt. Das Steuerelement veröffentlicht dann ein [DoAction ControlEvent,](doaction-controlevent.md) das die benutzerdefinierte Aktion Starten ausführt. Jedes Steuerelementereignis erfordert einen Datensatz in der [ControlEvent-Tabelle](controlevent-table.md). Weitere Informationen finden Sie [unter Übersicht über ControlEvent.](controlevent-overview.md)

[ControlEvent-Tabelle](controlevent-table.md)



| Dialog     | Steuerelement\_ | Ereignis     | Argument | Bedingung                     | Sortieren |
|------------|-----------|-----------|----------|-------------------------------|----------|
| ExitDialog | OK        | EndDialog | Rückgabewert   | 1                             | 1        |
| ExitDialog | OK        | DoAction  | Starten   | NICHT installiert UND $Tutorial=3 | 2        |



 

Die Bedingung im DoAction-Steuerelement stellt sicher, dass die benutzerdefinierte Aktion nur während der ersten Installation der Anwendung ausgeführt wird und lokal installiert wird. Der Ausdruck $Tutorial=3 bedeutet, dass der Aktionsstatus der Tutorialkomponente auf local festgelegt ist. Weitere Informationen finden Sie unter [Syntax der bedingten Anweisung.](conditional-statement-syntax.md)

Damit wird das Beispiel abgeschlossen.

 

 



