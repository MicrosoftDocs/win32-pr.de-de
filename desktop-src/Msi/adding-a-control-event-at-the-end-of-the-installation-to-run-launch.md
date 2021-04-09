---
description: Das Installationsprogramm führt die Installations-Assistenten Sequenz des Beispiels nur dann aus, wenn die vollständige Benutzeroberflächen Ebene zum Installieren der Anwendung verwendet wird.
ms.assetid: 323d62ae-333b-49fd-96a1-55b228c8ab2c
title: Hinzufügen eines Steuerungs Ereignisses am Ende der Installation zum Ausführen des Starts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545901c4cfd0936f63078d5ad56586022fb4ec4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959549"
---
# <a name="adding-a-control-event-at-the-end-of-the-installation-to-run-launch"></a>Hinzufügen eines Steuerungs Ereignisses am Ende der Installation zum Ausführen des Starts

Das Installationsprogramm führt die Installations-Assistenten Sequenz des Beispiels nur dann aus, wenn die [*vollständige Benutzer*](f-gly.md) Oberflächenebene zum Installieren der Anwendung verwendet wird. Das letzte Dialogfeld der Beispiel dialogsequenz ist ein [Exit-Dialog](exit-dialog.md) Feld mit dem Namen Exitdialog. Wenn ein Benutzer mit der Schaltfläche OK in Exitdialog interagiert, wird zuerst ein [EndDialog-ControlEvent](enddialog-controlevent.md) veröffentlicht, das die Steuerung an den Installer zurückgibt. Das-Steuerelement veröffentlicht dann einen [doaction-ControlEvent](doaction-controlevent.md) , der die benutzerdefinierte Aktion "Launch" ausführt. Jedes Steuerelement Ereignis erfordert einen Datensatz in der [ControlEvent-Tabelle](controlevent-table.md). Weitere Informationen finden Sie unter [ControlEvent Overview](controlevent-overview.md).

[ControlEvent-Tabelle](controlevent-table.md)



| Dialog     | Steuerelement\_ | Ereignis     | Argument | Bedingung                     | Sortieren |
|------------|-----------|-----------|----------|-------------------------------|----------|
| Exitdialog | OK        | EndDialog | Rückgabewert   | 1                             | 1        |
| Exitdialog | OK        | DoAction  | Starten   | Nicht installiert und $Tutorial = 3 | 2        |



 

Die Bedingung im doaction-Steuerelement stellt sicher, dass die benutzerdefinierte Aktion nur während der ersten Installation der Anwendung ausgeführt wird und lokal installiert wird. Der Ausdruck $Tutorial = 3 bedeutet, dass der Aktionszustand der tutorialkomponente auf Local festgelegt ist. Siehe [Syntax der Bedingungs Anweisung](conditional-statement-syntax.md).

Dadurch wird das Beispiel abgeschlossen.

 

 



