---
description: Wenn das Installationsskript vom Installationsprogramm verarbeitet wird, wird gleichzeitig ein Rollback-Skript generiert.
ms.assetid: 5b9bfc5a-6a78-4b0e-aed8-f25aba089af1
title: Zurücksetzen von benutzerdefinierten Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c4ad91f8f94145399d51ed2ef53999ab0a91d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863540"
---
# <a name="rollback-custom-actions"></a>Zurücksetzen von benutzerdefinierten Aktionen

Wenn das Installationsskript vom Installationsprogramm verarbeitet wird, wird gleichzeitig ein Rollback-Skript generiert. Zusätzlich zum Rollback-Skript speichert das Installationsprogramm eine Kopie jeder Datei, die während der Installation gelöscht wird. Diese Dateien werden in einem verborgenen System Verzeichnis gespeichert. Nach Abschluss der Installation werden das Rollback-Skript und die gespeicherten Dateien gelöscht. Wenn eine Installation nicht erfolgreich ist, versucht das Installationsprogramm, die während der Installation vorgenommenen Änderungen zurückzusetzen und den ursprünglichen Zustand des Computers wiederherzustellen.

Obwohl benutzerdefinierte Aktionen, durch die System Vorgänge durch Einfügen von Zeilen in die Datenbanktabelle geplant werden, durch ein Rollback der Installation rückgängig gemacht werden, können benutzerdefinierte Aktionen, die das System direkt ändern oder Befehle an andere Systemdienste ausgeben, nicht durch ein Rollback umgekehrt werden. Eine benutzerdefinierte Rollback-Aktion ist eine Aktion, die vom Installationsprogramm nur während eines Installations Rollbacks ausgeführt wird, und der Zweck besteht darin, eine benutzerdefinierte Aktion umzukehren, die Änderungen am System vorgenommen hat.

Bei einer benutzerdefinierten Rollback-Aktion handelt es sich um eine [benutzerdefinierte Aktion der verzögerten Ausführung](deferred-execution-custom-actions.md), da ihre Ausführung verzögert wird, wenn Sie während der Installations Sequenz aufgerufen wird. Dies unterscheidet sich von einer regulären verzögerten benutzerdefinierten Aktion darin, dass Sie nur während eines Rollbacks ausgeführt wird. Eine benutzerdefinierte Rollback-Aktion muss immer vor der verzögerten benutzerdefinierten Aktion stehen, die in der Aktions Sequenz zurückgesetzt wird. Eine benutzerdefinierte Rollback-Aktion sollte auch den Fall behandeln, in dem die verzögerte benutzerdefinierte Aktion während der Ausführung unterbrochen wird. Beispielsweise, wenn der Benutzer die Schaltfläche Abbrechen beim Ausführen der benutzerdefinierten Aktion gedrückt hat.

Beachten Sie, dass benutzerdefinierte Rollbacks-Aktionen nicht asynchron ausgeführt werden können. Siehe [synchrone und asynchrone benutzerdefinierte Aktionen](synchronous-and-asynchronous-custom-actions.md).

Die Ergänzung zu einer benutzerdefinierten Rollback-Aktion ist eine [benutzerdefinierte Commit-Aktion](commit-custom-actions.md). Der Installer führt während der Installations Sequenz eine benutzerdefinierte Commit-Aktion aus, kopiert die benutzerdefinierte Aktion in das Rollback-Skript, führt die Aktion während des Rollbacks jedoch nicht aus.

Beachten Sie, dass eine benutzerdefinierte Rollback-Aktion möglicherweise nicht alle Änderungen entfernt, die durch benutzerdefinierte COMMIT-Aktionen vorgenommen werden. Obwohl der Installer sowohl Rollback als auch Commit für benutzerdefinierte Aktionen in das Rollback-Skript schreibt, werden benutzerdefinierte Aktionen nur ausgeführt, nachdem das Installationsskript vom Installationsprogramm erfolgreich verarbeitet wurde. Commit für benutzerdefinierte Aktionen sind die ersten Aktionen, die im Rollback-Skript ausgeführt werden. Wenn bei einer benutzerdefinierten Commit-Aktion ein Fehler auftritt, wird ein Rollback vom Installationsprogramm initiiert Dies bedeutet, dass ein Rollback abhängig von der benutzerdefinierten Aktion "Commit" möglicherweise die von der Aktion vorgenommenen Änderungen nicht rückgängig machen kann. Sie können Fehler in benutzerdefinierten COMMIT-Aktionen ignorieren, indem Sie die benutzerdefinierte Aktion erstellen, um Rückgabecodes zu ignorieren.

Wenn das Installationsprogramm eine benutzerdefinierte Rollback-Aktion ausführt, wird der einzige Mode-Parameter, der festgelegt wird, das msirunmode- \_ Rollback. Unter [**msigetmode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) finden Sie eine Beschreibung der Parameter für den Testlauf.

Eine benutzerdefinierte Rollback-Aktion kann angegeben werden, indem dem type-Feld der [CustomAction-Tabelle](customaction-table.md)ein Optionsflag hinzugefügt wird. Weitere Informationen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md) für das Optionsflag zum Festlegen einer benutzerdefinierten Aktion Zurücksetzen.

Die benutzerdefinierten Aktionen Rollback und Commit werden nicht ausgeführt, wenn das Rollback deaktiviert ist. Wenn ein Paket Autor diese Art von benutzerdefinierten Aktionen für die ordnungsgemäße Installation erfordert, sollten Sie die [**rollbackdeaktiviert**](rollbackdisabled.md) -Eigenschaft in einer Bedingung verwenden, die verhindert, dass die Installation fortgesetzt wird, wenn das Rollback deaktiviert ist. Weitere Informationen zum Deaktivieren des Rollbacks finden Sie unter [Rollback Installation (Windows Installer)](rollback-installation.md).

 

 



