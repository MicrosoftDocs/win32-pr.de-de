---
description: Die VBScript-Datei WiSubStg.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt.
ms.assetid: a0248dfb-e406-4ce6-ab11-1e428aa67af4
title: Verwalten von substorages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01876efdb85bdc89df1b4d64332d44674e5e860e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348978"
---
# <a name="manage-substorages"></a>Verwalten von substorages

Die VBScript-Datei WiSubStg.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. In diesem Beispiel wird gezeigt, wie Sie mithilfe von Skripts substorages in einer Windows Installer Datenbank verwalten können. Eine Transformation kann zu einer vorhandenen Windows Installer Datenbank als unter Speicher hinzugefügt werden.

Das Beispiel veranschaulicht die Verwendung von:

-   [\_Tabelle "Storages"](-storages-table.md)
-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)
-   [**Methode "kreaterecord"**](installer-createrecord.md)
-   [**Lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)
-   [**OpenView-Methode**](database-openview.md)
-   [**Commit-Methode**](database-commit.md) des [ **Datenbankobjekts**](database-object.md)
-   [**FETCH-Methode**](view-fetch.md)
-   [**Modify-Methode**](view-modify.md)
-   [**Execute-Methode**](view-execute.md) des [ **View-Objekts**](view-object.md)
-   [**StringData (Eigenschaft)**](record-stringdata.md)
-   [**SetStream-Methode**](record-setstream.md) des [ **Datensatz-Objekts**](record-object.md)

Sie benötigen die CScript.exe oder WScript.exe Version von Windows Script Host, um dieses Beispiel zu verwenden. Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie mithilfe der folgenden Syntax eine Befehlszeile an der Eingabeaufforderung ein. Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden. Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiSubStg.vbs \[ Pfad zu Daten Bank \] \[ Pfad zu Datei \] \[ Optionen \] \[ unter Speicher Name\]**

Geben Sie den Pfad zur Windows Installer Datenbank an, um unter Speicher hinzuzufügen oder zu entfernen. Geben Sie einen Pfad zur Transformation oder Datenbankdatei an, die als unter Speicher hinzugefügt wird. Zum Auflisten der substorages in der Windows Installer-Datenbank lassen Sie den Pfad zu dieser Datei aus. Sie können einen optionalen unter Speicher Namen angeben. Wenn dieser Wert ausgelassen wird, wird der Name des unter Speichers standardmäßig auf den Dateinamen festgelegt.

Die folgende Option kann angegeben werden.



| Option              | BESCHREIBUNG                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| keine Option angegeben. | Fügen Sie der Windows Installer Datenbank einen unter Speicher hinzu.                                                 |
| /d                  | Entfernen Sie einen unter Speicher. Auf dieses Optionsflag muss der Name des zu entfernenden subspeichers folgen. |



 

Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md). Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

Beachten Sie, dass [ein Beispiel für eine Lokalisierung](a-localization-example.md) die [Einbettung von Anpassungs Transformationen als unter Speicher](embedding-customization-transforms-as-substorage.md)veranschaulicht.

 

 



