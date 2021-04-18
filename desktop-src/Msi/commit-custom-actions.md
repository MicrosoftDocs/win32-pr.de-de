---
description: Benutzerdefinierte COMMIT-Aktionen werden nach erfolgreichem Abschluss des Installations Skripts ausgeführt.
ms.assetid: ad766585-e8ac-44b6-9717-7979f803886c
title: Commit für benutzerdefinierte Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174af16a84f71ff90a1fc35c76054ee503449b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347075"
---
# <a name="commit-custom-actions"></a>Commit für benutzerdefinierte Aktionen

Benutzerdefinierte COMMIT-Aktionen werden nach erfolgreichem Abschluss des Installations Skripts ausgeführt. Wenn die [InstallFinalize-Aktion](installfinalize-action.md) erfolgreich ist, führt das Installationsprogramm alle benutzerdefinierten COMMIT-Aktionen aus. Der einzige Modusparameter, der vom Installer festgelegt wird, ist der msirunmode- \_ Commit. Unter [**msigetmode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) finden Sie eine Beschreibung der Parameter für den Testlauf.

Eine benutzerdefinierte Commit-Aktion kann angegeben werden, indem dem type-Feld der [CustomAction-Tabelle](customaction-table.md)ein Optionsflag hinzugefügt wird. Weitere Informationen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md) für das Optionsflag zum Festlegen einer benutzerdefinierten Commit-Aktion

Eine benutzerdefinierte Commit-Aktion ist die Ergänzung zu einer [benutzerdefinierten Rollback-Aktion](rollback-custom-actions.md) und kann mit einem Rollback von benutzerdefinierten Aktionen verwendet werden, um benutzerdefinierte Aktionen umzukehren, die Änderungen direkt am System vornehmen.

Beachten Sie, dass eine benutzerdefinierte Rollback-Aktion möglicherweise nicht alle Änderungen entfernt, die durch benutzerdefinierte COMMIT-Aktionen vorgenommen werden. Obwohl der Installer sowohl Rollback als auch Commit für benutzerdefinierte Aktionen in das Rollback-Skript schreibt, werden benutzerdefinierte Aktionen nur ausgeführt, nachdem das Installationsskript vom Installationsprogramm erfolgreich verarbeitet wurde. Commit für benutzerdefinierte Aktionen sind die ersten Aktionen, die im Rollback-Skript ausgeführt werden. Wenn bei einer benutzerdefinierten Commit-Aktion ein Fehler auftritt, wird ein Rollback vom Installationsprogramm initiiert Dies bedeutet, dass ein Rollback abhängig von der benutzerdefinierten Aktion "Commit" möglicherweise die von der Aktion vorgenommenen Änderungen nicht rückgängig machen kann. Sie können Fehler in benutzerdefinierten COMMIT-Aktionen ignorieren, indem Sie die benutzerdefinierte Aktion erstellen, um Rückgabecodes zu ignorieren.

Die benutzerdefinierten Aktionen Rollback und Commit werden nicht ausgeführt, wenn das Rollback deaktiviert ist. Wenn ein Paket Autor diese Art von benutzerdefinierten Aktionen für die ordnungsgemäße Installation erfordert, sollten Sie die [**rollbackdeaktiviert**](rollbackdisabled.md) -Eigenschaft in einer Bedingung verwenden, die verhindert, dass die Installation fortgesetzt wird, wenn das Rollback deaktiviert ist.

 

 



