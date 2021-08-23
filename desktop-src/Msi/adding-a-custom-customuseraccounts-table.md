---
description: Eine Spezifikation des Beispiels ist, dass Benutzerkontoinformationen aus einer benutzerdefinierten Tabelle in der Installationsdatenbank gelesen und nicht in die benutzerdefinierte Aktion hart codiert werden.
ms.assetid: 1545b4f1-3ccf-4745-90d8-15f1f79d8455
title: Hinzufügen einer benutzerdefinierten CustomUserAccounts-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede08ad733e2870e970416da3de345bfc89b7e63147bc848f3d36ffe66721585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066460"
---
# <a name="adding-a-custom-customuseraccounts-table"></a>Hinzufügen einer benutzerdefinierten CustomUserAccounts-Tabelle

Eine Spezifikation des Beispiels ist, dass Benutzerkontoinformationen aus einer benutzerdefinierten Tabelle in der Installationsdatenbank gelesen und nicht in die benutzerdefinierte Aktion hart codiert werden.

Fügen Sie der Beispielinstallationsdatenbank eine benutzerdefinierte Tabelle mit dem Namen CustomUserAccounts hinzu, um Benutzerkontoinformationen zu speichern. Ein Beispiel zum Hinzufügen einer [benutzerdefinierten Tabelle finden](examples-of-database-queries-using-sql-and-script.md) SQL Beispiele für Datenbankabfragen mithilfe von SQL und Skripts. Verwenden Sie das folgende Schema für die CustomUserAccounts-Tabelle. Eine [Erläuterung der Spaltentypen](column-definition-format.md) finden Sie unter Spaltendefinitionsformat.



| Spalte     | Typ | Key | Nullwerte zulässig | BESCHREIBUNG                                                                                                                                                                                                                                                                                                |
|------------|------|-----|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UserName   | s72  | J   | N        | Name des Benutzerkontos, das erstellt wird.                                                                                                                                                                                                                                                                        |
| Kennwort   | s72  |     | N        | Name der Eigenschaft, die das Kennwort für das Konto enthält. Dies ist [eine öffentliche Eigenschaft,](public-properties.md) die in der Befehlszeile oder über ein [Bearbeitungssteuer](edit-control.md) steuerelement in der Benutzeroberfläche festgelegt wird. Dieses Bearbeitungssteuer steuerelement sollte über das [Kennwortsteuerungsattribut verfügen.](password-control-attribute.md) |
| Attribute | i4   |     | J        | Attribute für account. Diese werden als **DWORD-Werte** für den usri1-Flags-Member \_ der USER INFO \_ \_ 1-Struktur definiert.                                                                                                                                                                              |



 

Nachdem die Tabelle CustomUserAccounts der Datenbank hinzugefügt wurde, können Sie diese Tabelle mithilfe von Orca, einem Tabellen-Editor, der mit dem Windows Installer SDK bereitgestellt wird, oder einem anderen Editor bearbeiten. Geben Sie den folgenden Datensatz in die Tabelle CustomUserAccounts ein, um ein kennwortgeschütztes Benutzerkonto für einen Benutzer namens TestUser zu erstellen. Beachten Sie, dass 512 der numerische Wert für UF \_ NORMAL \_ ACCOUNT ist.

CustomUserAccounts-Tabelle



| UserName | Kennwort         | Attribute |
|----------|------------------|------------|
| TestUser | TESTUSERPASSWORD | 512        |



 

Fügen Sie der Tabelle Validation für die \_ benutzerdefinierte Tabelle die folgenden Datensätze hinzu.

[\_Validierungstabelle](-validation-table.md)



| Tabelle              | Spalte     | Nullwerte zulässig | Minvalue | MaxValue   | KeyTable | KeyColumn | Category                     | Set | Beschreibung |
|--------------------|------------|----------|----------|------------|----------|-----------|------------------------------|-----|-------------|
| CustomUserAccounts | UserName   | N        |          |            |          |           | [Text](text.md)             |     |             |
| CustomUserAccounts | Kennwort   | N        |          |            |          |           | [Identifier](identifier.md) |     |             |
| CustomUserAccounts | Attribute | J        | 0        | 2147483647 |          |           | NULL                         |     |             |



 

Fahren Sie mit [Dem Erstellen der ActionText- und Fehlertabellen fort.](authoring-the-actiontext-and-error-tables.md)

 

 



