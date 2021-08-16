---
description: Die VBScript-WiDiffDb.vbs wird in den Windows SDK-Komponenten für Windows Installer-Entwickler bereitgestellt. Dieses Beispielskript generiert eine temporäre Transformationsdatei zwischen zwei Windows Installer-Datenbanken und zeigt die Transformation an.
ms.assetid: 9750ddc6-de8d-48e9-a984-892f0cf4ac3b
title: Anzeigen der Unterschiede zwischen zwei Datenbanken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbb04ad6ed1ecaa9d4d5be73708c5edc7dc8c84c9fe230a3725f971d949d335
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375913"
---
# <a name="view-differences-between-two-databases"></a>Anzeigen der Unterschiede zwischen zwei Datenbanken

Die VBScript-WiDiffDb.vbs wird in den Windows [SDK-Komponenten für Windows Installer-Entwickler bereitgestellt.](platform-sdk-components-for-windows-installer-developers.md) Dieses Beispielskript generiert eine temporäre Transformationsdatei zwischen zwei Windows Installer-Datenbanken und zeigt die Transformation an.

Das Beispiel veranschaulicht die Verwendung von:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)
-   [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)
-   [**OpenView-Methode**](database-openview.md)
-   [**SummaryInformation-Eigenschaft (Datenbankobjekt)**](database-summaryinformation.md)
-   [**GenerateTransform-Methode**](database-generatetransform.md)
-   [**ApplyTransform-Methode**](database-applytransform.md)
-   [**Datenbankobjekt**](database-object.md)
-   [**Fetch-Methode**](view-fetch.md) des [ **View-Objekts**](view-object.md)
-   [**IsNull-Eigenschaft**](record-isnull.md)
-   [**StringData-Eigenschaft**](record-stringdata.md) des [ **Datensatzobjekts**](record-object.md)
-   [\_TransformView-Tabelle](-transformview-table.md)

Die Verwendung dieses Beispiels erfordert die CScript.exe-Version Windows Skripthosts. Um dieses CScript.exe ausführen zu können, geben Sie an der Eingabeaufforderung einen Befehl mit der folgenden Syntax ein. Hilfe wird angezeigt, wenn das erste Argument /? ist. oder , wenn zu wenige Argumente angegeben werden. Um die Ausgabe an eine Datei umzuleiten, beenden Sie die Befehlszeile mit VBS > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für den Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiDiffDb.vbs** *\[ pfad zum ursprünglichen Datenbankpfad \] \[ zur überarbeiteten Datenbank \]*

Geben Sie den Pfad zur ursprünglichen Windows Installer-Datenbank an. Geben Sie den Pfad zur überarbeiteten Datenbank an. Das Beispielskript zeigt die Transformation an.

Weitere Skriptbeispiele finden Sie unter [Windows Installer Scripting Examples](windows-installer-scripting-examples.md). Beispielprogramme, für die kein Skripthost Windows ist, finden Sie unter [Windows Installer Development Tools](windows-installer-development-tools.md).

 

 



