---
description: Geben Sie Datensätze für die fünf benutzerdefinierten Beispielaktionen ein, die im vorherigen Abschnitt in der CustomAction-Tabelle erstellt wurden. Weitere Informationen zum Auffüllen der CustomAction-Tabelle für diese Art von benutzerdefinierter Aktion finden Sie unter Benutzerdefinierter Aktionstyp 1.
ms.assetid: 56828105-bd72-426d-833f-f756c577c77f
title: Erstellen der CustomAction-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b618da6e88718aa59483b3b25c007ff0b41eb89f6e1dc18a7eb31563632dc54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066080"
---
# <a name="authoring-the-customaction-table"></a>Erstellen der CustomAction-Tabelle

Geben Sie Datensätze für die fünf benutzerdefinierten Beispielaktionen ein, die im vorherigen Abschnitt in der [CustomAction-Tabelle erstellt wurden.](customaction-table.md) Weitere Informationen zum Auffüllen der CustomAction-Tabelle für diese Art von benutzerdefinierter Aktion finden Sie unter [Benutzerdefinierter Aktionstyp 1.](custom-action-type-1.md)

[CustomAction-Tabelle](customaction-table.md)



| Aktion            | type  | `Source`      | Ziel                |
|-------------------|-------|-------------|-----------------------|
| ProcessAccounts   | 1     | Process.dll | ProcessUserAccounts   |
| UninstallAccounts | 1     | Process.dll | UninstallUserAccounts |
| CreateAccount     | 11265 | Create.dll  | CreateUserAccount     |
| RemoveAccount     | 11265 | Remove.dll  | RemoveUserAccount     |
| RollbackAccount   | 9473  | Remove.dll  | RemoveUserAccount     |



 

Der C++-Quellcode für die Dynamic Link-Bibliotheken wird im Windows Installer SDK bereitgestellt. Verwenden Sie Process.cpp, um die Datei zu Process.dll. Verwenden Sie Create.cpp, um die Datei zu Create.dll. Verwenden Sie Remove.cpp, um Remove.dll. Fügen Sie diese Dynamic Link Library-Dateien der Binary-Tabelle hinzu.

[Binäre Tabelle](binary-table.md)



| Name        | Daten            |
|-------------|-----------------|
| Process.dll | {*binary data*} |
| Create.dll  | {*binary data*} |
| Remove.dll  | {*binary data*} |



 

Fahren Sie [mit Hinzufügen einer benutzerdefinierten CustomUserAccounts-Tabelle fort.](adding-a-custom-customuseraccounts-table.md)

 

 



