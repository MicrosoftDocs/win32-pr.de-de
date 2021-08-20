---
description: Ein Beispiel für die Verwendung skriptgesteuerter Datenbankabfragen finden Sie im Windows Installer Software Development Kit (SDK) als Hilfsprogramm WiRunSQL.vbs.
ms.assetid: aa38dbe5-411d-432e-b3fe-09994fc59c75
title: Beispiele für Datenbankabfragen mit SQL und Skripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f137927ba47c4fae5eef4534b7dfab1fa5c8fa1af2ba28d27669cc4605f836b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947068"
---
# <a name="examples-of-database-queries-using-sql-and-script"></a>Beispiele für Datenbankabfragen mit SQL und Skripts

Ein Beispiel für die Verwendung skriptgesteuerter Datenbankabfragen finden Sie im Windows [Installer Software Development Kit](platform-sdk-components-for-windows-installer-developers.md) (SDK) als Hilfsprogramm WiRunSQL.vbs. Dieses Hilfsprogramm verarbeitet Datenbankabfragen mithilfe der Windows Installer-Version von SQL, die im Abschnitt [SQL Syntax](sql-syntax.md)beschrieben wird.

**Löschen eines Datensatzes aus einer Tabelle**

Die folgende Befehlszeile löscht den Datensatz mit dem Primärschlüssel RED aus der [Tabelle Feature](feature-table.md) der Test.msi Datenbank.

**Cscript WiRunSQL.vbs Test.msi "DELETE FROM \` Feature WHERE Feature \` \` \` . \` Feature \` ='RED'"**

**Hinzufügen einer Tabelle zu einer Datenbank**

Über die folgende Befehlszeile wird die [Directory-Tabelle](directory-table.md) der Test.msi-Datenbank hinzugefügt.

**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \` Directory ( \` Directory \` \` CHAR(72) NOT NULL, \` Directory Parent \_ \` CHAR(72), \` DefaultDir \` CHAR(255) NOT NULL LOCALIZABLE PRIMARY KEY \` Directory \` )"**

**Entfernen einer Tabelle aus einer Datenbank**

Die folgende Befehlszeile entfernt die [Tabelle Feature](feature-table.md) aus der Test.msi Datenbank.

**Cscript WiRunSQL.vbs Test.msi "DROP \` \` TABLE-Feature"**

**Hinzufügen einer neuen Spalte zu einer Tabelle**

Über die folgende Befehlszeile wird die Spalte Test der [CustomAction-Tabelle](customaction-table.md) der Test.msi-Datenbank hinzugefügt.

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` CustomAction \` ADD \` Test \` INTEGER"**

**Einfügen eines neuen Datensatzes in eine Tabelle**

Die folgende Befehlszeile fügt einen neuen Datensatz in die [Tabelle Feature](feature-table.md) der Test.msi-Datenbank ein.

**Cscript WiRunSQL.vbs Test.msi "INSERT INTO \` Feature ( Feature \` \` \` . \` Feature \` , \` Feature \` . \` Übergeordnetes \_ \` Feature, \` Feature \` . \` Titel \` , \` Feature \` . \` Beschreibung, \` \` Feature \` . \` Anzeigen \` von , Feature \` \` . \` Ebene \` , \` Feature \` . \` Verzeichnis \_ \` , Feature \` \` . \` Attributes \` ) VALUES ('Soll','Sport','Soll','Select',25,3,'SPORTDIR',2)"**

Dadurch wird der folgende Datensatz in die [Tabelle Feature](feature-table.md) von Test.msi eingefügt.

[Feature](feature-table.md) Tabelle



| Komponente | \_Übergeordnetes Feature | Titel  | BESCHREIBUNG | Anzeige | Ebene | Verzeichnis\_ | Attribute |
|---------|-----------------|--------|-------------|---------|-------|-------------|------------|
| Tennis  | Sport           | Tennis | Turnier  | 25      | 3     | SPORTDIR    | 2          |



 

Beachten Sie, dass binäre Daten nicht direkt mithilfe der ABFRAGEN INSERT INTO oder UPDATE SQL in eine Tabelle eingefügt werden können. Weitere Informationen finden Sie unter [Hinzufügen von Binärdaten zu einer Tabelle mit SQL](adding-binary-data-to-a-table-using-sql.md).

**Ändern eines vorhandenen Datensatzes in einer Tabelle**

Über die folgende Befehlszeile wird der vorhandene Wert im Feld Titel in "Performance" geändert. Der aktualisierte Datensatz verfügt über "Soll" als Primärschlüssel und befindet sich in der Tabelle Feature der Test.msi-Datenbank.

**Cscript WiRunSQL.vbs Test.msi "UPDATE \` Feature \` SET Feature \` \` . \` Title \` ='Performance' WHERE \` Feature \` . \` Feature \` ='Soll'"**

**Auswählen einer Gruppe von Datensätzen**

Die folgende Befehlszeile wählt den Namen und typ aller Steuerelemente aus, die zum ErrorDialog in der Test.msi-Datenbank gehören.

**CScript WiRunSQL.vbs Test.msi "SELECT \` Control \` , Type FROM Control WHERE Dialog \` \` \` \` \` \_ \` ='ErrorDialog' "**

**Speichern einer Tabelle im Arbeitsspeicher**

Die folgende Befehlszeile sperrt die [Tabelle Komponente](component-table.md) der Test.msi Datenbank im Arbeitsspeicher.

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` Component \` HOLD"**

**Freigeben einer Tabelle im Arbeitsspeicher**

Die folgende Befehlszeile gibt die [Tabelle Component](component-table.md) der Test.msi-Datenbank aus dem Arbeitsspeicher frei.

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` Component \` FREE"**

 

 



