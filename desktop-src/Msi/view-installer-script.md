---
description: Die VBScript-WiLstScr.vbs wird in den sdk-Komponenten Windows für Windows Installer-Entwickler bereitgestellt. Dieses Beispielskript veranschaulicht den Windows Installer-Skript-Viewer.
ms.assetid: 18989c16-e0c8-4d11-b915-730951b6845b
title: Anzeigen des Installationsskripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4797d73c4c90266b94a02b9d73657fb95de75e153617ef1e34797f28035ee701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803981"
---
# <a name="view-installer-script"></a>Anzeigen des Installationsskripts

Die VBScript-WiLstScr.vbs wird in den Windows [SDK-Komponenten für Windows Installer-Entwickler bereitgestellt.](platform-sdk-components-for-windows-installer-developers.md) Dieses Beispielskript veranschaulicht den Windows Installer-Skript-Viewer.

Das Beispiel veranschaulicht die Verwendung von:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)
-   [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) des [**Installer-Objekts**](installer-object.md)
-   [**OpenView-Methode**](database-openview.md) des [**Database-Objekts**](database-object.md)
-   [**Fetch-Methode**](view-fetch.md) des [**View-Objekts**](view-object.md)
-   [**FormatText-Methode**](record-formattext.md)
-   [**FieldCount-Eigenschaft**](record-fieldcount.md)
-   [**StringData-Eigenschaft**](record-stringdata.md) des [**Datensatzobjekts**](record-object.md)
-   [\_TransformView-Tabelle](-transformview-table.md)

Die Verwendung dieses Beispiels erfordert die CScript.exe-Version Windows Skripthosts. Um dieses CScript.exe ausführen zu können, geben Sie an der Eingabeaufforderung einen Befehl mit der folgenden Syntax ein. Hilfe wird angezeigt, wenn das erste Argument /? ist. oder , wenn zu wenige Argumente angegeben werden. Um die Ausgabe an eine Datei umzuleiten, beenden Sie die Befehlszeile mit VBS > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für den Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiLstScr.vbs** *\[ pfad zum Windows Installer-Ausführungsskript \]*

Geben Sie den Pfad zum Installationsausführungsskript an.

Weitere Skriptbeispiele finden Sie unter [Windows Installer Scripting Examples](windows-installer-scripting-examples.md). Beispielprogramme, für die kein Skripthost Windows ist, finden Sie unter [Windows Installer Development Tools](windows-installer-development-tools.md).

 

 



