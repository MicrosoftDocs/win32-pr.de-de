---
description: Benutzerdefinierte Aktionen werden in Sequenztabellen auf die gleiche Weise wie Standardaktionen geplant.
ms.assetid: 1aea75b1-a498-405e-9208-91672455496b
title: Sequenzieren benutzerdefinierter Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26d86449b67809f782560e35d32b1b1e42434153ced776a27fd479a7b80a25a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039970"
---
# <a name="sequencing-custom-actions"></a>Sequenzieren benutzerdefinierter Aktionen

Benutzerdefinierte Aktionen werden in Sequenztabellen auf die gleiche Weise wie Standardaktionen geplant.

**So planen Sie eine benutzerdefinierte Aktion in einer Sequenztabelle**

1.  Geben Sie den Namen der benutzerdefinierten Aktion (der der Primärschlüssel der [CustomAction-Tabelle](customaction-table.md)ist) in die Spalte Aktion der [Sequenztabelle](sequence-table-detailed-example.md) ein.
2.  Geben Sie die Sequenz der benutzerdefinierten Aktion relativ zu den anderen Aktionen in der Tabelle in die Spalte Sequenz der [Sequenztabelle](sequence-table-detailed-example.md) ein. Weitere Informationen zu Sequenztabellen finden Sie unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md)
3.  Um die Aktion bedingt zu überspringen, geben Sie einen bedingten Ausdruck in die Spalte Bedingung der [Sequenztabelle](sequence-table-detailed-example.md) ein. Das Installationsprogramm überspringt diese Aktion, wenn der Ausdruck als FALSE ausgewertet wird.

Wie bei Standardaktionen werden benutzerdefinierte Aktionen, die in [InstallUISequence](installuisequence-table.md) oder [AdminUISequence](adminuisequence-table.md) geplant sind, nur ausgeführt, wenn die interne Benutzeroberfläche auf die vollständige Ebene festgelegt ist. Die Benutzeroberflächenebene wird mithilfe der [**MsiSetInternalUI-Funktion**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) festgelegt.

Standardaktionen und benutzerdefinierte Aktionen, die in den Tabellen [InstallExecuteSequence,](installexecutesequence-table.md) [AdminExecuteSequence](adminexecutesequence-table.md)oder [AdvtExecuteSequence](advtexecutesequence-table.md) geplant sind, nehmen keine Systemänderungen vor. Stattdessen reiht das Installationsprogramm Ausführungsdatensätze in einem Skript für die nachfolgende Ausführung während des Installationsdiensts in die Warteschlange ein. Wenn kein Installationsdienst vorhanden ist, werden die in diesen Tabellen geplanten Aktionen im gleichen Kontext wie die Ui-Sequenz ausgeführt.

Wenn der Installationsserver nicht registriert ist, werden die benutzerdefinierten Aktionen auf der Clientseite ausgeführt. Wenn der Server registriert ist und den vollständigen Benutzeroberflächenmodus verwendet, werden die benutzerdefinierten Aktionen auf serverseitiger Seite ausgeführt.

Wenn Sie die vollständige Benutzeroberfläche mit dem Server verwenden, werden die ersten Aktionen vor der [InstallValidate-Aktion](installvalidate-action.md) auf dem Client ausgeführt, um eine vollständige Interaktion zu ermöglichen. Die Ausführung wird dann auf den Server umgestellt, der diese Aktionen wiederholt und die Skriptausführungsaktionen ausführt. Darauf folgt eine Rückgabe an den Client für die endgültigen Aktionen.

Beachten Sie, dass die [**REMOVE-Eigenschaft**](remove.md) möglicherweise erst nach der [InstallValidate-Aktion](installvalidate-action.md) gleich ALL ist, wenn ein Produkt entfernt wird, indem sein oberstes Feature auf absent festgelegt wird. Dies bedeutet, dass alle benutzerdefinierten Aktionen, die von REMOVE=ALL abhängen, nach der InstallValidate-Aktion sequenziert werden müssen. Eine benutzerdefinierte Aktion kann REMOVE überprüfen, um zu bestimmen, ob ein Produkt so festgelegt wurde, dass es vollständig deinstalliert wird.

Benutzerdefinierte Aktionen, die auf eine installierte Datei als Quelle verweisen, z. B. benutzerdefinierter Aktionstyp 17 (DLL), benutzerdefinierter Aktionstyp 18 (EXE), benutzerdefinierter Aktionstyp 21 (JScript) und benutzerdefinierter Aktionstyp 22 (VBScript), müssen die folgenden Sequenzeinschränkungen einhalten.

-   Die benutzerdefinierte Aktion muss nach der [CostFinalize-Aktion](costfinalize-action.md) sequenziert werden, damit der Pfad zur Datei, auf die verwiesen wird, aufgelöst werden kann.
-   Wenn die Quelldatei noch nicht auf dem Computer installiert ist, müssen verzögerte (skriptbasierte) benutzerdefinierte Aktionen nach [installFiles](installfiles-action.md)sequenziert werden.
-   Wenn die Quelldatei nicht bereits auf dem Computer installiert ist, müssen nicht abgeleitete benutzerdefinierte Aktionen nach der [InstallInitialize-Aktion](installinitialize-action.md) sequenziert werden.

Die folgenden Sequenzierungseinschränkungen gelten für benutzerdefinierte Aktionen, die ein Windows Installer-Paket ändern oder aktualisieren.

-   Wenn die benutzerdefinierte Aktion das Paket ändert, z. B. durch Hinzufügen von Zeilen zu einer Tabelle, muss die Aktion vor der [InstallInitialize-Aktion](installinitialize-action.md) sequenziert werden.
-   Wenn die benutzerdefinierte Aktion Änderungen vornimmt, die sich auf die Kosten auswirken würden, sollte sie vor der [CostInitialize-Aktion](costfinalize-action.md) sequenziert werden.
-   Wenn die benutzerdefinierte Aktion den Installationsstatus von Features oder Komponenten ändert, muss sie vor der [InstallValidate-Aktion](installvalidate-action.md) sequenziert werden.

 

 



