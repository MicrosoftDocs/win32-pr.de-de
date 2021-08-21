---
description: Die Erstellung der Sequenztabellen ist ein wesentlicher Bestandteil der Entwicklung eines Installationspakets, da diese Tabellen die Ausführungsreihenfolge für die Standardaktionen angeben, die den Installationsvorgang steuern und die Dialogfelder der Benutzeroberfläche anzeigen.
ms.assetid: db9a9cae-2a66-4e0d-a981-8de66d7c2a13
title: Verwenden einer Sequenztabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16adf47a554bf70298b0efc893847f84eafd6e97313b09ba9ea3182398cdd97d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809010"
---
# <a name="using-a-sequence-table"></a>Verwenden einer Sequenztabelle

Die Erstellung der Sequenztabellen ist ein wesentlicher Bestandteil der Entwicklung eines Installationspakets, da diese Tabellen die Ausführungsreihenfolge für die [Standardaktionen](standard-actions.md) angeben, die den Installationsvorgang steuern und die Dialogfelder der Benutzeroberfläche anzeigen.

Es gibt drei Installationsmodi und zwei Arten von Sequenztabellen für jeden Modus.

Die drei separaten Installationsmodi, die derzeit vom Installationsprogramm unterstützt werden, sind:

-   Einfache Installation
-   Administratorinstallation
-   Ankündigungsinstallation

Die Sequenztabellen verfügen jeweils über drei Felder: Aktion, Bedingung und Sequenz. Das Feld Aktion benennt entweder eine standard- oder benutzerdefinierte Aktion oder ein benutzerdefiniertes Dialogfeld oder eine Vom Installationsprogramm ausgeführte Sequenz. Mit dem Feld Bedingung kann der Autor einen logischen Ausdruck angeben, der steuert, ob eine Aktion oder ein benutzerdefiniertes Dialogfeld ausgeführt oder angezeigt wird. Wenn das Feld Bedingung leer ist oder einen Ausdruck enthält, der zu True ausgewertet wird, wird die Aktion oder das Dialogfeld ausgeführt oder angezeigt. Die Aktion oder das Dialogfeld wird übersprungen, wenn der Ausdruck als False ausgewertet wird. Das Feld Sequenz gibt die Ausführungsreihenfolge der einzelnen Aktionen oder benutzerdefinierten Dialogfelder in der Tabelle an.

Jeder dieser Installationsmodi verarbeitet die Benutzeroberflächensequenztabellen und die Ausführungssequenztabellen. Die Sequenztabellen der Benutzeroberfläche werden nur verarbeitet, wenn das Installationsprogramm mit der Anzeigeebene der Benutzeroberfläche initialisiert wurde, die auf Reduziert oder Vollständig festgelegt ist. Weitere Informationen zu Anzeigeebenen der Benutzeroberfläche finden Sie in der [**MsiSetInternalUI-Referenz.**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

Die Sequenztabellen der Benutzeroberfläche enthalten in der Regel Standardaktionen im Zusammenhang mit dem Sammeln von Systeminformationen, die dem Benutzer über die Benutzeroberfläche angezeigt werden. Die Benutzeroberfläche wird angezeigt, indem die Fremdschlüssel in den Namen der Dialogfelder in der [Dialogtabelle](dialog-table.md) im Feld Aktion der Sequenztabelle der Benutzeroberfläche aufgezeichnet werden. Der Benutzer hat dann die Möglichkeit, die Systeminformationen zu ändern oder zu akzeptieren und mit der Installation zu beginnen. Dies geschieht, wenn die Ausführungssequenztabelle verarbeitet wird.

Während einer einfachen Installation wird die Aktion [INSTALL](install-action.md) der obersten Ebene ausgeführt, die wiederum die [Tabelle InstallUISequence](installuisequence-table.md) und die [Tabelle InstallExecuteSequence](installexecutesequence-table.md)verarbeitet.

Eine Administratorinstallation wird in der Regel von einem Netzwerkadministrator initiiert, um Anwendungen für einzelne Benutzer und Benutzergruppen zuzuweisen und zu installieren. Während dieser Art der Installation wird [die](admin-action.md) Admin-Aktion der obersten Ebene ausgeführt, die die [AdminUISequence-Tabelle](adminuisequence-table.md) und die [AdminExecuteSequence-Tabelle](adminexecutesequence-table.md)verarbeitet.

Um eine Anwendung oder ein Feature [anzukündigen,](advertisement.md) muss das Installationsprogramm mit der [AKTION "ADVERTISE"](advertise-action.md) initiiert werden. Während dieser Art der Installation wird die [Tabelle AdvtExecuteSequence](advtexecutesequence-table.md) verarbeitet.

Beim Erstellen einer Sequenztabelle empfiehlt es sich, die Sequenznummer für Standardaktionen aus den vorgeschlagenen Sequenzen in den folgenden Themen zu verwenden. Verwenden Sie für Standardaktionen ohne Standardposition in der Sequenztabelle wie [ForceReboot](forcereboot-action.md), [ValidateProductID](validateproductid-action.md)und [InstallExecute](installexecute-action.md)eine Sequenznummer, die ein Vielfaches von zehn ist, um die Aktion als Standardaktion zu identifizieren. Verwenden Sie für benutzerdefinierte Aktionen eine Sequenznummer, die kein Vielfaches von zehn ist, um sie von Standardaktionen in der Sequenztabelle zu unterscheiden.

Empfohlene Aktionssequenzen für jede Sequenztabelle finden Sie in den folgenden Themen:

-   [Empfohlene InstallationUISequence](suggested-installuisequence.md)
-   [Empfohlene InstallationExecuteSequence](suggested-installexecutesequence.md)
-   [Empfohlene AdminUISequence](suggested-adminuisequence.md)
-   [Vorgeschlagene AdminExecuteSequence](suggested-adminexecutesequence.md)
-   [Vorgeschlagene AdvtUISequence](suggested-advtuisequence.md)
-   [Vorgeschlagene AdvtExecuteSequence](suggested-advtexecutesequence.md)

Eine ausführliche Beschreibung der Sequenztabellen und der Ausführung von Standardaktionen finden Sie im detaillierten Beispiel der [Sequenztabelle.](sequence-table-detailed-example.md)

**Windows Installer 3.0 und höher: **

Ab Windows Installer 3.0 kann ein Patchpaket die [Tabelle MsiPatchSequence](msipatchsequence-table.md)enthalten. Diese Tabelle enthält alle Informationen, die das Installationsprogramm benötigt, um die Reihenfolge der Anwendung eines kleinen Updatepatches relativ zu allen anderen Patches zu bestimmen. Weitere Informationen finden Sie unter [Patchen und Upgrades.](patching-and-upgrades.md)

> [!Note]
>
> [Mergemodule](merge-modules.md) können [Mergemodul-Datenbanktabellen](merge-module-database-tables.md) enthalten, die die Aktionssequenztabellen der Zieldatei .msi ändern. Das Zusammenführen des Moduls zu einer Datenbank kann die Informationen in der Sequenztabelle ändern, fügt diese Tabellen jedoch nicht der .msi-Datei hinzu. Weitere Informationen finden Sie unter [Erstellen von Mergemodulsequenztabellen.](authoring-merge-module-sequence-tables.md)

 

 

 



