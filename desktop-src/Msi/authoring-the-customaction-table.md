---
description: Geben Sie Datensätze für die fünf benutzerdefinierten Beispiel Aktionen ein, die im vorherigen Abschnitt für die Tabelle CustomAction erstellt wurden. Weitere Informationen zum Auffüllen der CustomAction-Tabelle für diese Art von benutzerdefinierter Aktion finden Sie unter benutzerdefinierter Aktionstyp 1.
ms.assetid: 56828105-bd72-426d-833f-f756c577c77f
title: Erstellen der Tabelle "CustomAction"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fb7d8cf99a30200e6a5525e3516e2b888c1129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959509"
---
# <a name="authoring-the-customaction-table"></a>Erstellen der Tabelle "CustomAction"

Geben Sie Datensätze für die fünf benutzerdefinierten Beispiel Aktionen ein, die im vorherigen Abschnitt für die [Tabelle CustomAction](customaction-table.md)erstellt wurden. Weitere Informationen zum Auffüllen der CustomAction-Tabelle für diese Art von benutzerdefinierter Aktion finden Sie unter [benutzerdefinierter Aktionstyp 1](custom-action-type-1.md).

[Tabelle "CustomAction"](customaction-table.md)



| Aktion            | type  | `Source`      | Ziel                |
|-------------------|-------|-------------|-----------------------|
| Processaccounts   | 1     | Process.dll | Processuseraccounts   |
| Nicht installaccounts | 1     | Process.dll | Uninstalluseraccounts |
| CreateAccount     | 11265 | Create.dll  | "Kreateuseraccount"     |
| RemoveAccount     | 11265 | Remove.dll  | Removeuseraccount     |
| Rollbackaccount   | 9473  | Remove.dll  | Removeuseraccount     |



 

Der C++-Quellcode für die Dynamic-Link-Bibliotheken wird im Windows Installer SDK bereitgestellt. Verwenden Sie "Process. cpp", um die Datei Process.dll zu erstellen. Erstellen Sie die Datei Create.dll mit CREATE. cpp. Verwenden Sie Remove. cpp, um Remove.dll zu erstellen. Fügen Sie diese Dynamic-Link Library-Dateien der Binär Tabelle hinzu.

[Binäre Tabelle](binary-table.md)



| Name        | Daten            |
|-------------|-----------------|
| Process.dll | {*binäre Daten*} |
| Create.dll  | {*binäre Daten*} |
| Remove.dll  | {*binäre Daten*} |



 

Fügen Sie weiterhin [eine benutzerdefinierte customuseraccounts-Tabelle hinzu](adding-a-custom-customuseraccounts-table.md).

 

 



