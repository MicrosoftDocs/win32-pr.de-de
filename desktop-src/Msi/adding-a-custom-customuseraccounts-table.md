---
description: Eine Spezifikation des Beispiels besteht darin, dass Benutzerkontoinformationen aus einer benutzerdefinierten Tabelle in der Installations Datenbank gelesen und nicht in die benutzerdefinierte Aktion hart codiert werden.
ms.assetid: 1545b4f1-3ccf-4745-90d8-15f1f79d8455
title: Hinzufügen einer benutzerdefinierten customuseraccounts-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58366c725ecc135b9583c926a16383a5ad5a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351639"
---
# <a name="adding-a-custom-customuseraccounts-table"></a>Hinzufügen einer benutzerdefinierten customuseraccounts-Tabelle

Eine Spezifikation des Beispiels besteht darin, dass Benutzerkontoinformationen aus einer benutzerdefinierten Tabelle in der Installations Datenbank gelesen und nicht in die benutzerdefinierte Aktion hart codiert werden.

Fügen Sie der Beispiel Installations Datenbank eine benutzerdefinierte Tabelle mit dem Namen customuseraccounts hinzu, um die Benutzerkontoinformationen zu speichern. Ein Beispiel für das Hinzufügen einer benutzerdefinierten Tabelle finden Sie unter [Beispiele für Datenbankabfragen mithilfe von SQL und Skript](examples-of-database-queries-using-sql-and-script.md) . Verwenden Sie das folgende Schema für die customuseraccounts-Tabelle. Eine Erläuterung der Spaltentypen finden Sie unter [Spalten Definitions Format](column-definition-format.md) .



| Spalte     | Typ | Schlüssel | Nullwerte zulässig | BESCHREIBUNG                                                                                                                                                                                                                                                                                                |
|------------|------|-----|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UserName   | S72  | J   | N        | Der Name des Benutzerkontos, das erstellt wird.                                                                                                                                                                                                                                                                        |
| Kennwort   | S72  |     | N        | Name der Eigenschaft, die das Kennwort für das Konto enthält. Dabei handelt es sich um eine [öffentliche Eigenschaft](public-properties.md) , die in der Befehlszeile oder über ein [Bearbeitungs Steuer](edit-control.md) Element in der Benutzeroberfläche festgelegt wird. Dieses Bearbeitungs Steuerelement muss über das [Attribut "Password Control](password-control-attribute.md)" verfügen. |
| Attribute | i4   |     | J        | Attribute für das Konto. Diese werden als **DWORD** -Werte für den usri1 \_ Flags-Member der Struktur "User \_ Info 1" definiert \_ .                                                                                                                                                                              |



 

Nachdem die Tabelle customuseraccounts der Datenbank hinzugefügt wurde, können Sie diese Tabelle mithilfe von Orca, einem Tabellen-Editor, der mit dem Windows Installer SDK bereitgestellt wird, oder einem anderen Editor bearbeiten. Geben Sie den folgenden Datensatz in der Tabelle "customuseraccounts" ein, um ein Kenn Wort geschütztes Benutzerkonto für einen Benutzernamens "testuser" zu erstellen. Beachten Sie, dass 512 der numerische Wert für das Standardkonto "UF" ist \_ \_ .

Tabelle "customuseraccounts"



| UserName | Kennwort         | Attribute |
|----------|------------------|------------|
| TestUser | Testuserpassword | 512        |



 

Fügen Sie der Überprüfungs \_ Tabelle für die benutzerdefinierte Tabelle die folgenden Datensätze hinzu.

[\_Validierungs Tabelle](-validation-table.md)



| Tabelle              | Spalte     | Nullwerte zulässig | MinValue | MaxValue   | KeyTable | KeyColumn | Category                     | Set | BESCHREIBUNG |
|--------------------|------------|----------|----------|------------|----------|-----------|------------------------------|-----|-------------|
| Customuseraccounts | UserName   | N        |          |            |          |           | [Text](text.md)             |     |             |
| Customuseraccounts | Kennwort   | N        |          |            |          |           | [Bezeichner](identifier.md) |     |             |
| Customuseraccounts | Attribute | J        | 0        | 2147483647 |          |           | NULL                         |     |             |



 

Fahren Sie mit [dem Erstellen der Aktions Text-und Fehler Tabellen](authoring-the-actiontext-and-error-tables.md)fort.

 

 



