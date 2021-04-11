---
description: Benutzerdefinierte Aktionen werden in Sequenz Tabellen auf die gleiche Weise wie Standard Aktionen geplant.
ms.assetid: 1aea75b1-a498-405e-9208-91672455496b
title: Sequenzieren benutzerdefinierter Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7c24fb91247a36880cb808c9b8e10437312cf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218517"
---
# <a name="sequencing-custom-actions"></a>Sequenzieren benutzerdefinierter Aktionen

Benutzerdefinierte Aktionen werden in Sequenz Tabellen auf die gleiche Weise wie Standard Aktionen geplant.

**So planen Sie eine benutzerdefinierte Aktion in einer Sequenz Tabelle**

1.  Geben Sie den Namen der benutzerdefinierten Aktion (bei der es sich um den Primärschlüssel der Tabelle [CustomAction](customaction-table.md)handelt) in die Spalte Aktion der [Sequenz](sequence-table-detailed-example.md) Tabelle ein.
2.  Geben Sie die Sequenz der benutzerdefinierten Aktion in Relation zu den anderen Aktionen in der Tabelle in die Sequence-Spalte der [Sequenz](sequence-table-detailed-example.md) Tabelle ein. Weitere Informationen zu Sequenz Tabellen finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).
3.  Um die Aktion bedingt zu überspringen, geben Sie einen Bedingungs Ausdruck in die Spalte Bedingung der [Sequenz](sequence-table-detailed-example.md) Tabelle ein. Das Installationsprogramm überspringt diese Aktion, wenn der Ausdruck zu false ausgewertet wird.

Wie bei Standard Aktionen werden benutzerdefinierte Aktionen, die in [InstallUISequence](installuisequence-table.md) oder [AdminUISequence](adminuisequence-table.md) geplant sind, nur ausgeführt, wenn die interne Benutzeroberfläche auf die vollständige Ebene festgelegt ist. Die Benutzeroberflächen Ebene wird mithilfe der [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) -Funktion festgelegt.

In den Tabellen [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)oder [AdvtExecuteSequence](advtexecutesequence-table.md) geplante Standard-und benutzerdefinierte Aktionen nehmen keine Systemänderungen vor. Stattdessen fügt das Installationsprogramm Ausführungsdaten Sätze in einem Skript für die nachfolgende Ausführung während des Installations Dienstanbieter ein. Wenn kein Installations Dienst vorhanden ist, werden die in diesen Tabellen geplanten Aktionen im gleichen Kontext wie die UI-Sequenz ausgeführt.

Wenn der Installationsprogramm Server nicht registriert ist, werden die benutzerdefinierten Aktionen auf der Clientseite ausgeführt. Wenn der Server registriert ist und den vollständigen Benutzeroberflächen Modus verwendet, werden die benutzerdefinierten Aktionen auf der Serverseite ausgeführt.

Wenn Sie die vollständige Benutzeroberfläche mit dem Server verwenden, werden die anfänglichen Aktionen vor der [InstallValidate](installvalidate-action.md) -Aktion auf dem Client ausgeführt, um eine vollständige Interaktion zu ermöglichen. Die Ausführung wird dann auf den Server umgestellt, der diese Aktionen wiederholt und die Skript Ausführungs Aktionen ausführt. Danach folgt eine Rückgabe an den Client für die abschließenden Aktionen.

Beachten Sie Folgendes: Wenn ein Produkt durch Festlegen seines Top-Features auf Missing entfernt wird, ist die [**Remove**](remove.md) -Eigenschaft möglicherweise bis nach der [InstallValidate](installvalidate-action.md) -Aktion nicht gleich. Dies bedeutet, dass alle benutzerdefinierten Aktionen, die von Remove = All abhängen, nach der InstallValidate-Aktion sequenziert werden müssen. Eine benutzerdefinierte Aktion kann "entfernen" überprüfen, um zu bestimmen, ob ein Produkt vollständig deinstalliert wurde.

Benutzerdefinierte Aktionen, die auf eine installierte Datei als Quelle verweisen, wie z. b. der benutzerdefinierte Aktionstyp 17 (dll), der benutzerdefinierte Aktionstyp 18 (exe), der benutzerdefinierte Aktionstyp 21 (JScript) und der benutzerdefinierte Aktionstyp 22 (VBScript) müssen die folgenden Sequenz Einschränkungen einhalten.

-   Die benutzerdefinierte Aktion muss nach der Aktion " [costfinalize](costfinalize-action.md) " sequenziert werden, damit der Pfad zu der Datei, auf die verwiesen wird, aufgelöst werden kann.
-   Wenn die Quelldatei nicht bereits auf dem Computer installiert ist, müssen nach den [InstallFiles](installfiles-action.md)verzögerte (in-Script) benutzerdefinierte Aktionen sequenziert werden.
-   Wenn die Quelldatei nicht bereits auf dem Computer installiert ist, müssen nicht verzögerte benutzerdefinierte Aktionen nach der [InstallInitialize](installinitialize-action.md) -Aktion sequenziert werden.

Die folgenden Sequenz Einschränkungen gelten für benutzerdefinierte Aktionen, durch die ein Windows Installer Paket geändert oder aktualisiert wird.

-   Wenn das Paket durch die benutzerdefinierte Aktion geändert wird, z. b. durch das Hinzufügen von Zeilen zu einer Tabelle, muss die Aktion vor der [InstallInitialize](installinitialize-action.md) -Aktion sequenziert werden.
-   Wenn die benutzerdefinierte Aktion Änderungen vornimmt, die sich auf die Kosten auswirken, sollte Sie vor der [costinitialize](costfinalize-action.md) -Aktion sequenziert werden.
-   Wenn die benutzerdefinierte Aktion den Installationsstatus von Features oder Komponenten ändert, muss Sie vor der [InstallValidate](installvalidate-action.md) -Aktion sequenziert werden.

 

 



