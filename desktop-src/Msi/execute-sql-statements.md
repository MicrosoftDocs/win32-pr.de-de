---
description: Die VBScript-Datei WiRunSQL.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt.
ms.assetid: 1027b187-1237-43d1-9905-8fcdaec63903
title: SQL-Anweisungen ausführen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99da54f85b02ee867003b140d505f5754f58cc00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358841"
---
# <a name="execute-sql-statements"></a>SQL-Anweisungen ausführen

Die VBScript-Datei WiRunSQL.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Beispiel zeigt, wie das Skript zum Ausführen von SQL-Abfragen und-Updates für eine Windows Installer Datenbank verwendet wird. Weitere Informationen finden Sie unter [SQL-Syntax](sql-syntax.md) und [Beispiele für Datenbankabfragen mithilfe von SQL und Skript](examples-of-database-queries-using-sql-and-script.md).

Das Beispielskript veranschaulicht Folgendes:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md) und die [**lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [**Installer-Objekts**](installer-object.md)
-   [**OpenView-Methode**](database-openview.md)und die [**Commit-Methode**](database-commit.md) des [**Datenbankobjekts**](database-object.md)
-   [**Execute-Methode**](view-execute.md) des [ **View-Objekts**](view-object.md)
-   Eigenschaften [**Eigenschaft von StringData**](record-stringdata.md) des [ **Datensatz-Objekts**](record-object.md)

Zum Verwenden dieses Beispiels ist die CScript.exe oder WScript.exe Version von Windows Script Host erforderlich. Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie einen Befehl an der Eingabeaufforderung ein, indem Sie die folgende Syntax verwenden. Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden. Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript-WiRunSQL.vbs \[ Pfad zu SQL-Daten Bank \] \[ Abfragen\]**

Geben Sie den Pfad zu einer Windows Installer-Datenbank an. Geben Sie die SQL-Abfragen an, die ausgeführt werden sollen. Beachten Sie, dass die SQL-Abfrage in doppelte Anführungszeichen eingeschlossen werden muss. SELECT Queries zeigt die Zeilen der in der Abfrage angegebenen Ergebnisliste an. Von einer Abfrage ausgewählte binäre Datenspalten werden nicht angezeigt.

Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md). Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

Weitere Informationen finden Sie unter [Arbeiten mit Abfragen](working-with-queries.md) und [Beispielen für Datenbankabfragen mithilfe von SQL und Skript](examples-of-database-queries-using-sql-and-script.md). Im [Beispiel eines Lokalisierungs Beispiels](a-localization-example.md) wird die Verwendung von SQL zum [Lokalisieren von Daten Bank Spalten](localizing-database-columns.md) und [Aktualisieren eines Zusammenfassungs Datenstroms](updating-a-summary-information-stream.md)veranschaulicht.

 

 



