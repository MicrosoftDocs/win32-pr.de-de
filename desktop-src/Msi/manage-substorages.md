---
description: Die VBScript-WiSubStg.vbs wird in den sdk-Komponenten Windows für Windows Installer-Entwickler bereitgestellt.
ms.assetid: a0248dfb-e406-4ce6-ab11-1e428aa67af4
title: Verwalten von Unterstorages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f6d3a0716854755e595133771ede65b11212cdd0fd19b4502bab0c631a9d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945595"
---
# <a name="manage-substorages"></a>Verwalten von Unterstorages

Die VBScript-WiSubStg.vbs wird in den Windows [SDK-Komponenten für Windows Installer-Entwickler bereitgestellt.](platform-sdk-components-for-windows-installer-developers.md) In diesem Beispiel wird gezeigt, wie das Skript zum Verwalten von Unterstorages in einer Windows Installer-Datenbank verwendet werden kann. Eine Transformation kann einer vorhandenen Datenbank Windows Installer als Unterstorage hinzugefügt werden.

Das Beispiel veranschaulicht die Verwendung von:

-   [\_Tabelle "Speicher"](-storages-table.md)
-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)
-   [**CreateRecord-Methode**](installer-createrecord.md)
-   [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)
-   [**OpenView-Methode**](database-openview.md)
-   [**Commit-Methode**](database-commit.md) des [ **Database-Objekts**](database-object.md)
-   [**Fetch-Methode**](view-fetch.md)
-   [**Modify-Methode**](view-modify.md)
-   [**Execute-Methode**](view-execute.md) des [ **View-Objekts**](view-object.md)
-   [**StringData-Eigenschaft**](record-stringdata.md)
-   [**SetStream-Methode**](record-setstream.md) des [ **Record-Objekts**](record-object.md)

Sie benötigen die CScript.exe oder WScript.exe von Windows Script Host, um dieses Beispiel verwenden zu können. Um dieses CScript.exe ausführen zu können, geben Sie an der Eingabeaufforderung eine Befehlszeile mit der folgenden Syntax ein. Hilfe wird angezeigt, wenn das erste Argument /? ist. oder , wenn zu wenige Argumente angegeben werden. Um die Ausgabe an eine Datei umzuleiten, beenden Sie die Befehlszeile mit VBS > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für den Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiSubStg.vbs \[ pfad zum Datenbankpfad zu Dateioptionen Name des \] \[ \] \[ \] \[ Unterstorages\]**

Geben Sie den Pfad zur Windows Installer-Datenbank an, die Unterstorage hinzugefügt oder entfernt werden soll. Geben Sie einen Pfad zur Transformations- oder Datenbankdatei an, die als Unterstorage hinzugefügt wird. Wenn Sie die Unterstorages in der Windows Installer-Datenbank auflisten möchten, müssen Sie den Pfad zu dieser Datei weglassen. Sie können einen optionalen Namen für das Unterspeichern angeben. Wenn dies weggelassen wird, wird der Name des Unterspeichers standardmäßig auf den Dateinamen festgelegt.

Die folgende Option kann angegeben werden.



| Option              | Beschreibung                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| keine Option angegeben | Fügen Sie der Windows Installer-Datenbank einen Windows hinzu.                                                 |
| /d                  | Entfernen Sie ein Unterstorage. Auf dieses Optionsflag muss der Name des zu entfernenden Unterstorages folgen. |



 

Weitere Skriptbeispiele finden Sie unter [Windows Installer Scripting Examples](windows-installer-scripting-examples.md). Beispielprogramme, für die kein Skripthost Windows ist, finden Sie unter [Windows Installer Development Tools](windows-installer-development-tools.md).

Beachten Sie, [dass ein Lokalisierungsbeispiel](a-localization-example.md) [das Einbetten von Anpassungstransformationen als Unterstorage veranschaulicht.](embedding-customization-transforms-as-substorage.md)

 

 



