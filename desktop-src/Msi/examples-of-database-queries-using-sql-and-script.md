---
description: Ein Beispiel für die Verwendung von Skript gesteuerten Datenbankabfragen finden Sie im Windows Installer Software Development Kit (SDK) als Dienst WiRunSQL.vbs.
ms.assetid: aa38dbe5-411d-432e-b3fe-09994fc59c75
title: Beispiele für Datenbankabfragen mit SQL und Skript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd839151b40ddd5e9a265c6c370c27a4a9fd125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755625"
---
# <a name="examples-of-database-queries-using-sql-and-script"></a>Beispiele für Datenbankabfragen mit SQL und Skript

Ein Beispiel für die Verwendung von Skript gesteuerten Datenbankabfragen finden Sie im Windows [Installer Software Development Kit](platform-sdk-components-for-windows-installer-developers.md) (SDK) als Dienstprogramm WiRunSQL.vbs. Dieses Hilfsprogramm verarbeitet Datenbankabfragen mithilfe der Windows Installer SQL-Version, die im Abschnitt [SQL-Syntax](sql-syntax.md)beschrieben wird.

**Löschen eines Datensatzes aus einer Tabelle**

Mit der folgenden Befehlszeile wird der Datensatz mit dem Primärschlüssel aus der [Funktions](feature-table.md) Tabelle der Test.msi Datenbank gelöscht.

**Cscript WiRunSQL.vbs Test.msi "DELETE FROM \` Feature \` \` \` . \` Feature \` = ' red ' "**

**Hinzufügen einer Tabelle zu einer Datenbank**

Mit der folgenden Befehlszeile wird die [Verzeichnis](directory-table.md) Tabelle der Test.msi Datenbank hinzugefügt.

**Cscript-WiRunSQL.vbs Test.msi "Create Table \` Directory \` ( \` Verzeichnis \` char (72) nicht NULL, \` Verzeichnis \_ Parent \` char (72), \` DefaultDir \` char (255) NOT NULL localisierbares Primärschlüssel \` Verzeichnis \` )"**

**Entfernen einer Tabelle aus einer Datenbank**

Mit der folgenden Befehlszeile wird die [Funktions](feature-table.md) Tabelle aus der Test.msi-Datenbank entfernt.

**Cscript-WiRunSQL.vbs Test.msi "Drop Table- \` Funktion \` "**

**Hinzufügen einer neuen Spalte zu einer Tabelle**

Mit der folgenden Befehlszeile wird die Test Spalte der Tabelle " [CustomAction](customaction-table.md) " der Test.msi Datenbank hinzugefügt.

**Cscript-WiRunSQL.vbs Test.msi "alter Table \` CustomAction \` Add \` Test \` Integer"**

**Einfügen eines neuen Datensatzes in eine Tabelle**

Mit der folgenden Befehlszeile wird ein neuer Datensatz in die [Funktions](feature-table.md) Tabelle der Test.msi-Datenbank eingefügt.

**Cscript WiRunSQL.vbs Test.msi "INSERT INTO- \` Funktion \` ( \` Feature \` . \` Feature \` , \` Feature \` . \` Über \_ geordnetes Element \` , \` Feature \` . \` Titel \` , \` Feature \` . \` Beschreibung \` , \` Feature \` . \` Anzeigen \` , \` Feature \` . \` Ebene \` , \` Funktion \` . \` Verzeichnis \_ \` , \` Feature \` . \` Attribute \` ) Werte ("Tennis", "Sport", "Tennis", "Turnier", 25, 3, "sportdir", 2) "**

Dadurch wird der folgende Datensatz in die [Featuretabelle Test.msi](feature-table.md) eingefügt.

[Feature](feature-table.md) Glaub



| Funktion | Über \_ geordnetes Element | Titel  | BESCHREIBUNG | Anzeige | Ebene | Verzeichnis\_ | Attribute |
|---------|-----------------|--------|-------------|---------|-------|-------------|------------|
| Tennis  | Sport           | Tennis | Turnier  | 25      | 3     | Sportdir    | 2          |



 

Beachten Sie, dass Binärdaten nicht direkt mithilfe der INSERT INTO-oder Update SQL-Abfragen in eine Tabelle eingefügt werden können. Weitere Informationen finden [Sie unter Hinzufügen von Binärdaten zu einer Tabelle mithilfe von SQL](adding-binary-data-to-a-table-using-sql.md).

**Ändern eines vorhandenen Datensatzes in einer Tabelle**

Mit der folgenden Befehlszeile wird der vorhandene Wert im Feld "Title" in "Performance" geändert. Der aktualisierte Datensatz weist "Arts" als Primärschlüssel auf und befindet sich in der Featuretabelle der Test.msi Datenbank.

**Cscript-WiRunSQL.vbs Test.msi Feature "Featuresatz aktualisieren" \` \` \` \` . \` Title \` = ' Performance ' in der \` Funktion \` . \` Feature \` = ' Arts '**

**Gruppe von Datensätzen auswählen**

Die folgende Befehlszeile wählt den Namen und den Typ aller Steuerelemente aus, die zum ErrorDialog in der Test.msi-Datenbank gehören.

**Cscript-WiRunSQL.vbs Test.msi "Select- \` Steuerelement \` , \` Typ \` von \` Control \` Where \` Dialog \_ \` = ' ErrorDialog '"**

**Speichern einer Tabelle im Arbeitsspeicher**

Die folgende Befehlszeile sperrt die [Komponenten](component-table.md) Tabelle der Test.msi-Datenbank im Arbeitsspeicher.

**Cscript-WiRunSQL.vbs Test.msi "alter Table \` Component \` Hold"**

**Freigeben einer Tabelle im Arbeitsspeicher**

Mit der folgenden Befehlszeile wird die [Komponenten](component-table.md) Tabelle der Test.msi Datenbank aus dem Arbeitsspeicher freigegeben.

**Cscript-WiRunSQL.vbs Test.msi "alter Table \` Component \` Free"**

 

 



