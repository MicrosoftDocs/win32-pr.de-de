---
description: Die Erstellung der Sequenz Tabellen ist ein wesentlicher Bestandteil der Entwicklung eines Installer-Pakets, da diese Tabellen die Ausführungsreihenfolge für die Standard Aktionen angeben, die den Installationsvorgang steuern, und die Dialogfelder der Benutzeroberfläche anzeigen.
ms.assetid: db9a9cae-2a66-4e0d-a981-8de66d7c2a13
title: Verwenden einer Sequenz Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0be10082aba05429a63df69444ed28bea350aa5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865472"
---
# <a name="using-a-sequence-table"></a>Verwenden einer Sequenz Tabelle

Die Erstellung der Sequenz Tabellen ist ein wesentlicher Bestandteil der Entwicklung eines Installer-Pakets, da diese Tabellen die Ausführungsreihenfolge für die [Standard Aktionen](standard-actions.md) angeben, die den Installationsvorgang steuern, und die Dialogfelder der Benutzeroberfläche anzeigen.

Es gibt drei Installations Modi und zwei Arten von Sequenz Tabellen für jeden Modus.

Die drei separaten Installations Modi, die derzeit vom Installationsprogramm unterstützt werden, sind:

-   Einfache Installation
-   Administrative Installation
-   Ankündigungs Installation

Die Sequenz Tabellen verfügen jeweils über drei Felder: Aktion, Bedingung und Sequenz. Das Aktionsfeld benennt entweder eine Standard-oder eine benutzerdefinierte Aktion oder ein benutzerdefiniertes Dialogfeld oder eine vom Installationsprogramm ausgeführte Sequenz. Das Feld Bedingung ermöglicht dem Autor, einen logischen Ausdruck anzugeben, der steuert, ob eine Aktion oder ein benutzerdefiniertes Dialogfeld ausgeführt oder angezeigt wird. Wenn das Bedingungs Feld leer ist oder einen Ausdruck enthält, der als true ausgewertet wird, wird die Aktion oder das Dialogfeld ausgeführt oder angezeigt. Die Aktion oder das Dialogfeld wird übersprungen, wenn der Ausdruck zu false ausgewertet wird. Das Feld Sequenz gibt die Ausführungsreihenfolge der einzelnen Aktionen oder benutzerdefinierten Dialogfelder in der Tabelle an.

Jeder dieser Installations Modi verarbeitet die Benutzeroberflächen-Sequenz Tabellen und die Execute Sequence-Tabellen. Die Sequenz Tabellen für die Benutzeroberfläche werden nur verarbeitet, wenn das Installationsprogramm mit der Anzeige Ebene der Benutzeroberfläche auf "reduziert" oder "vollständig" initialisiert wurde. Weitere Informationen zu Anzeige Ebenen der Benutzeroberfläche finden Sie in der [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) -Referenz.

Die Sequenz Tabellen der Benutzeroberfläche enthalten in der Regel Standard Aktionen im Zusammenhang mit der Erfassung von Systeminformationen, die dem Benutzer über die Benutzeroberfläche angezeigt werden. Die Benutzeroberfläche wird angezeigt, indem die Fremdschlüssel in den Namen von Dialogfeldern in der [Dialogfeld Tabelle](dialog-table.md) im Feld Aktion der Sequenz Tabelle der Benutzeroberfläche aufgezeichnet werden. Der Benutzer hat dann die Möglichkeit, die Systeminformationen zu ändern oder zu akzeptieren und die Installation zu starten, die bei der Verarbeitung der Sequenz Tabelle ausgeführt wird.

Bei einer einfachen Installation wird die [install](install-action.md) Top-Level-Aktion ausgeführt, die wiederum die Tabelle [InstallUISequence](installuisequence-table.md) und die [Tabelle InstallExecuteSequence](installexecutesequence-table.md)verarbeitet.

Eine administrative Installation wird normalerweise von einem Netzwerkadministrator initiiert, um Anwendungen für einzelne Benutzer und Benutzergruppen zuzuweisen und zu installieren. Bei dieser Art der Installation wird die auf oberster Ebene ausgeführte [Admin](admin-action.md) -Aktion ausgeführt, die die Tabelle " [AdminUISequence](adminuisequence-table.md) " und die [Tabelle "AdminExecuteSequence](adminexecutesequence-table.md)" verarbeitet.

Zum [ankündigen einer Anwendung](advertisement.md) oder eines Features muss das Installationsprogramm mit [der Aktion ankündigen](advertise-action.md) initiiert werden. Bei dieser Art der Installation wird die [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md) verarbeitet.

Beim Erstellen einer Sequenz Tabelle empfiehlt es sich, die Sequenznummer für Standard Aktionen aus den vorgeschlagenen Sequenzen in den folgenden Themen zu verwenden. Verwenden Sie für Standard Aktionen, die keine Standardposition in der Sequenz Tabelle haben, z. b. [ForceReboot](forcereboot-action.md), [ValidateProductID](validateproductid-action.md)und [InstallExecute](installexecute-action.md), eine Sequenznummer, die ein Vielfaches von zehn ist, um die Aktion als Standardaktion zu identifizieren. Verwenden Sie für benutzerdefinierte Aktionen eine Sequenznummer, bei der es sich nicht um ein Vielfaches von zehn handelt, um Sie von Standard Aktionen in der Sequenz Tabelle zu unterscheiden.

Empfohlene Aktions Sequenzen für jede Sequenz Tabelle finden Sie in den folgenden Themen:

-   [Vorgeschlagene InstallUISequence](suggested-installuisequence.md)
-   [Empfohlene InstallExecuteSequence](suggested-installexecutesequence.md)
-   [Vorgeschlagene AdminUISequence](suggested-adminuisequence.md)
-   [Vorgeschlagene AdminExecuteSequence](suggested-adminexecutesequence.md)
-   [Vorgeschlagene advtuisequence](suggested-advtuisequence.md)
-   [Vorgeschlagene AdvtExecuteSequence](suggested-advtexecutesequence.md)

Eine ausführliche Beschreibung der Sequenz Tabellen und der Ausführung von Standard Aktionen finden Sie im [ausführlichen Beispiel der Sequenz Tabelle](sequence-table-detailed-example.md).

* * Windows Installer 3,0 und höher: * *

Ab Windows Installer 3,0 kann ein Patchpaket die [msipatchsequence-Tabelle](msipatchsequence-table.md)enthalten. Diese Tabelle enthält alle Informationen, die das Installationsprogramm benötigt, um die Reihenfolge der Anwendung eines kleinen Update Patches relativ zu allen anderen Patches zu bestimmen. Weitere Informationen finden Sie unter [Patching und Upgrades](patching-and-upgrades.md).

> [!Note]
>
> [Mergemodule](merge-modules.md) können [Datenbanktabellen des Mergemoduls](merge-module-database-tables.md) enthalten, mit denen die Aktions Sequenz Tabellen der MSI-Ziel Datei geändert werden. Wenn Sie das Modul in eine Datenbank zusammenführen, können Sie die Informationen in der Sequenz Tabelle ändern, aber diese Tabellen nicht der MSI-Datei hinzufügen. Weitere Informationen finden Sie unter [Erstellen von Mergemodul-Sequenz Tabellen](authoring-merge-module-sequence-tables.md).

 

 

 



