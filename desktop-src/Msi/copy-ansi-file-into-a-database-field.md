---
description: Die VBScript-Codebeispiel Datei WiTextIn.vbs in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt.
ms.assetid: ba6c6367-ebb1-4981-ae3a-bcff68aacdbf
title: ANSI-Datei in ein Datenbankfeld kopieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc6c4d3a945177581a35bf6b19d89855abb5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362547"
---
# <a name="copy-ansi-file-into-a-database-field"></a>ANSI-Datei in ein Datenbankfeld kopieren

Die VBScript-Codebeispiel Datei WiTextIn.vbs in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Das Beispiel zeigt, wie ein-Skript verwendet werden kann, um eine Datei in ein Textfeld einer Windows Installer-Datenbank zu kopieren und die Verarbeitung von Primärschlüssel Daten zu veranschaulichen.

Das Codebeispiel zeigt außerdem Folgendes:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md) und die [**lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [**Installer-Objekts**](installer-object.md)
-   [**OpenView-Methode**](database-openview.md), die [**Commit-Methode**](database-commit.md)und die [**primarykeys-Eigenschaft**](database-primarykeys.md) des Database- [**Objekts**](database-object.md)
-   [**Fetch-Methode**](view-fetch.md) und die [**Modify-Methode**](view-modify.md) des View- [**Objekts**](view-object.md)
-   [**StringData-Eigenschaft**](record-stringdata.md) und die Read [**Stream-Methode**](record-readstream.md) des [**Datensatz-Objekts**](record-object.md)

Um das Codebeispiel zu verwenden, benötigen Sie die CScript.exe oder WScript.exe Version von Windows Script Host.

**So verwenden Sie CScript.exe, um dieses Beispiel auszuführen**

-   Geben Sie an der Eingabeaufforderung die folgende Syntax ein:

    **cscript WiTextIn.vbs \[ Pfad zum Daten Bank \] \[ Tabellennamen \] \[ Primärschlüssel Werte \] \[ Spaltenname \] \[ Pfad zu Datei\]**

> [!Note]  
> Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden.

 

**So leiten Sie die Ausgabe in eine Datei um**

-   Beenden Sie die Befehlszeile mit folgendem: **VSB > \[ Pfad zur Datei \] . T**

> [!Note]  
> Im Beispiel wird der Wert 0 (null) für Erfolg zurückgegeben, 1 (eins), wenn die Hilfe aufgerufen wird, und 2 (zwei), wenn das Skript fehlschlägt.

 

In der folgenden Liste sind die Elemente aufgeführt, die Sie angeben müssen:

-   Geben Sie den Pfad für die Windows Installer-Datenbank an.
-   Geben Sie den Namen der Datenbanktabelle an.
-   Geben Sie alle Primärschlüssel Werte für die Zeile in der angegebenen Reihenfolge an, und verkettet mit Doppelpunkten.
-   Geben Sie einen Spaltennamen an, der keine Schlüssel Spalte ist. Dies ist die Spalte, die die Daten empfangen soll.
-   Geben Sie den Pfad zu der Textdatei an, die kopiert wird.

> [!Note]  
> Wenn das letzte Argument weggelassen wird, wird der aktuelle Wert im Feld angezeigt.

 

Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md). Beispiel Hilfsprogramme, die den Windows Script Host nicht benötigen, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

 

 



