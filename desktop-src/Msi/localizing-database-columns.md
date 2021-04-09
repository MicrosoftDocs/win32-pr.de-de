---
description: Ändern Sie alle anderen lokalisierbaren Spalten in der MNPFren.msi Datenbank mit einem Tabellen-Editor wie z. b. Orca-oder SQL-Abfragen.
ms.assetid: b62cf529-71a0-47ff-99ea-a182c0fe4479
title: Lokalisieren von Daten Bank Spalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed36b1adb2c496c9019b482c929e449187b1e0bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042533"
---
# <a name="localizing-database-columns"></a>Lokalisieren von Daten Bank Spalten

Ändern Sie alle anderen lokalisierbaren Spalten in der MNPFren.msi Datenbank mit einem Tabellen-Editor wie z. b. Orca-oder SQL-Abfragen. Informationen dazu, welche Spalten einer bestimmten Tabelle möglicherweise in einer anderen Sprache lokalisiert werden, finden Sie im Referenz Thema für diese Datenbanktabelle. Eine Liste aller Datenbanktabellen finden Sie unter [Datenbanktabellen](database-tables.md) .

Beispielsweise muss das Textfeld einiger Datensätze in der [Steuerelement Tabelle](control-table.md) möglicherweise in Französisch lokalisiert werden. Die Zeichenfolge "möchten Sie die \[ Installation von ProductName wirklich abbrechen \] ?" im [Dialog Feld Abbrechen](cancel-dialog.md) kann in dieser Tabelle geändert werden, damit Sie in Französisch angezeigt wird. Der ursprüngliche Datensatz in der MSI-Datei sieht wie folgt aus.

[Steuerungs Tabelle](control-table.md) (teilweise) der ursprünglichen MSI-Datei



| Dialog\_  | Control | type | X   | J   | Breite | Höhe | Attribute | Eigenschaft | Text                                                          | Nächstes Steuerelement \_ | Hilfe |
|-----------|---------|------|-----|-----|-------|--------|------------|----------|---------------------------------------------------------------|---------------|------|
| Canceldlg | Text    | Text | 48  | 15  | 194   | 30     | 3          |          | Möchten Sie die \[ ProductName-Installation wirklich abbrechen \] ? |               |      |



 

Sie können einen Tabellen-Editor verwenden, um das Textfeld zu ändern, z. b. den mit dem SDK oder einem anderen Tabellen-Editor bereitgestellten Hash-Tabellen-Editor, oder eine SQL-Abfrage verwenden, um das Textfeld des Steuerelement Tabellendaten Satzes zu ändern Ein Beispiel für Skript gesteuerte Datenbankabfragen wird im Windows Installer SDK als Dienstprogramm WiRunSQL.vbs bereitgestellt. Verwenden Sie die folgende Befehlszeile, um das Feld mit WiRunSQL.vbs und dem Windows Script Host zu ändern. Siehe auch [Beispiele für Datenbankabfragen, die SQL und Skripts verwenden](examples-of-database-queries-using-sql-and-script.md).

**Cscript-WiRunSQL.vbs MNPFren.msi "Steuerelement Satz-Steuerelement aktualisieren. Text = ' ETEs-dir sur de bürloir annuler l Installation de \[ ProductName \] ?" Where Control. Dialog \_ = ' canceldlg ' und Control. Control = ' Text ' '**

[Steuerelement Tabelle](control-table.md) (partiell) in MNPFren.msi



| Dialog\_  | Control | type | X   | J   | Breite | Höhe | Attribute | Eigenschaft | Text                                                                | Nächstes Steuerelement \_ | Hilfe |
|-----------|---------|------|-----|-----|-------|--------|------------|----------|---------------------------------------------------------------------|---------------|------|
| Canceldlg | Text    | Text | 48  | 15  | 194   | 30     | 3          |          | "Êtes-you sûr de bürloir localier l Installation de \[ ProductName" \] |               |      |



 

Wenn die Installation von MNPFren.msi vom Benutzer abgebrochen wird, wird das **Dialog Feld Abbrechen** mit dem folgenden Text angezeigt: "êtes-you sûr de bürloir Canceler l Installation de MNP2000?"

Wenn diese Methode verwendet wird, um den Benutzeroberflächen Text in eine andere Sprache zu lokalisieren, muss die lokalisierte Benutzeroberfläche getestet werden, um sicherzustellen, dass die Größe der Steuerelemente groß genug ist, um den gesamten lokalisierten Text anzuzeigen. Dies sollte mit allen Schriftart Größen Einstellungen getestet werden, die zur Anzeige verfügbar sind. Lokalisierter Text erfordert mehr Speicherplatz als der ursprüngliche Text und kann abgeschnitten werden, wenn er in einem zu kleinen Steuerelement angezeigt wird.

[Fortsetzen](updating-productlanguage-and-productcode-properties.md)

 

 



