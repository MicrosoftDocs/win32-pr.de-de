---
description: Ändern Sie alle anderen lokalisierbaren Spalten in der MNPFren.msi-Datenbank mithilfe eines Tabellen-Editors wie Orca oder SQL Abfragen.
ms.assetid: b62cf529-71a0-47ff-99ea-a182c0fe4479
title: Lokalisieren von Datenbankspalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a72d4d4d82f45be66f41710dea7294a63051d69750ade49ae3b66761964b579f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629455"
---
# <a name="localizing-database-columns"></a>Lokalisieren von Datenbankspalten

Ändern Sie alle anderen lokalisierbaren Spalten in der MNPFren.msi-Datenbank mithilfe eines Tabellen-Editors wie Orca oder SQL Abfragen. Informationen dazu, welche Spalten einer bestimmten Tabelle in einer anderen Sprache lokalisiert werden können, finden Sie im Referenzthema für diese Datenbanktabelle. Eine [Liste aller Datenbanktabellen](database-tables.md) finden Sie unter Datenbanktabellen.

Beispielsweise muss das Textfeld einiger Datensätze in der [Control-Tabelle](control-table.md) möglicherweise in Französisch lokalisiert werden. Die Zeichenfolge "Möchten Sie die Installation von \[ ProductName \] abbrechen?" im [Dialogfeld Abbrechen](cancel-dialog.md) kann in dieser Tabelle so geändert werden, dass sie auf Französisch angezeigt wird. Der ursprüngliche Datensatz in .msi datei wird wie folgt angezeigt.

[Steuertabelle](control-table.md) (partiell) der ursprünglichen .msi Datei



| Dialog\_  | Control | type | X   | J   | Breite | Höhe | Attribute | Eigenschaft | Text                                                          | Weiter \_ steuern | Hilfe |
|-----------|---------|------|-----|-----|-------|--------|------------|----------|---------------------------------------------------------------|---------------|------|
| CancelDlg | Text    | Text | 48  | 15  | 194   | 30     | 3          |          | Möchten Sie die Installation von \[ ProductName \] wirklich abbrechen? |               |      |



 

Sie können einen Tabellen-Editor verwenden, um das Textfeld zu ändern, z. B. den Orca-Tabellen-Editor, der mit dem SDK oder einem anderen Tabellen-Editor bereitgestellt wird, oder eine SQL-Abfrage verwenden, um das Textfeld des Datensatzes Control table zu ändern. Ein Beispiel für skriptgesteuerte Datenbankabfragen finden Sie im Windows Installer SDK als WiRunSQL.vbs. Verwenden Sie die folgende Befehlszeile, um das Feld mit WiRunSQL.vbs und dem Windows Skripthost zu ändern. Siehe auch [Beispiele für Datenbankabfragen mit SQL und Skript](examples-of-database-queries-using-sql-and-script.md).

**Cscript WiRunSQL.vbs MNPFren.msi "UPDATE Control SET Control.Text='Etes-vous sur de voätzir annuler l'installation de \[ \] ProductName?' WHERE Control.Dialog \_ ='CancelDlg' AND Control.Control='Text'"**

[Control Table](control-table.md) (partial) in MNPFren.msi



| Dialog\_  | Control | type | X   | J   | Breite | Höhe | Attribute | Eigenschaft | Text                                                                | Weiter \_ steuern | Hilfe |
|-----------|---------|------|-----|-----|-------|--------|------------|----------|---------------------------------------------------------------------|---------------|------|
| CancelDlg | Text    | Text | 48  | 15  | 194   | 30     | 3          |          | Gnotes-vous s vovocir annuler l'installation de \[ ProductName \] ? |               |      |



 

Wenn die Installation von MNPFren.msi durch den Benutzer  abgebrochen wird, wird im Dialogfeld Abbrechen der Text "Gnos-vous s de vovocir annuler l'installation de MNP2000?" angezeigt.

Wenn Sie diese Methode verwenden, um Benutzeroberflächentext in einer anderen Sprache zu lokalisieren, muss die lokalisierte Benutzeroberfläche getestet werden, um sicherzustellen, dass die Größe der Steuerelemente groß genug ist, um den gesamten lokalisierten Text anzuzeigen. Dies sollte mit allen Schriftgradeinstellungen getestet werden, die für die Anzeige verfügbar sind. Lokalisierter Text kann mehr Platz als der ursprüngliche Text erfordern und abgeschnitten werden, wenn er in einem zu kleinen Steuerelement angezeigt wird.

[Fortsetzen](updating-productlanguage-and-productcode-properties.md)

 

 



