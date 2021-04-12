---
description: Die VBScript-Datei WiDiffDb.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. Dieses Beispielskript generiert eine temporäre Transformations Datei zwischen zwei Windows Installer-Datenbanken und zeigt die Transformation an.
ms.assetid: 9750ddc6-de8d-48e9-a984-892f0cf4ac3b
title: Anzeigen von Unterschieden zwischen zwei Datenbanken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b0c97afc0bd7145170209ed87497b6af90e64d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525874"
---
# <a name="view-differences-between-two-databases"></a>Anzeigen von Unterschieden zwischen zwei Datenbanken

Die VBScript-Datei WiDiffDb.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Beispielskript generiert eine temporäre Transformations Datei zwischen zwei Windows Installer-Datenbanken und zeigt die Transformation an.

Das Beispiel veranschaulicht die Verwendung von:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)
-   [**Lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)
-   [**OpenView-Methode**](database-openview.md)
-   [**SummaryInformation (Eigenschaft) (Datenbankobjekt)**](database-summaryinformation.md)
-   [**GenerateTransform-Methode**](database-generatetransform.md)
-   [**Applytransform-Methode**](database-applytransform.md)
-   [**Datenbankobjekt**](database-object.md)
-   [**Fetch-Methode**](view-fetch.md) des [ **View-Objekts**](view-object.md)
-   [**IsNull-Eigenschaft**](record-isnull.md)
-   [**StringData-Eigenschaft**](record-stringdata.md) des [ **Datensatz-Objekts**](record-object.md)
-   [\_Transformview-Tabelle](-transformview-table.md)

Zum Verwenden dieses Beispiels ist die CScript.exe Version von Windows Script Host erforderlich. Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie einen Befehl an der Eingabeaufforderung ein, indem Sie die folgende Syntax verwenden. Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden. Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiDiffDb.vbs** *\[ Pfad zum ursprünglichen Daten Bank \] \[ Pfad zur über \] arbeiteten Datenbank*

Geben Sie den Pfad zur ursprünglichen Windows Installer Datenbank an. Geben Sie den Pfad zur überarbeiteten Datenbank an. Im Beispielskript wird die Transformation angezeigt.

Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md). Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

 

 



