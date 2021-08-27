---
description: Die VBScript-WiCompon.vbs wird in den Windows SDK-Komponenten für Windows Installer-Entwickler bereitgestellt. Dieses Beispielskript kann verwendet werden, um die Komponenten in einer Windows Installer-Datenbank auflisten.
ms.assetid: 4e6cc6f4-821a-4a10-a897-5c6aace1f702
title: Auflisten von Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec396e66ed55d78131c74b85432b2f01829cdb5400fc5c00a6ced5725edadeae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129320"
---
# <a name="list-components"></a>Auflisten von Komponenten

Die VBScript-WiCompon.vbs wird in den Windows [SDK-Komponenten für Windows Installer-Entwickler bereitgestellt.](platform-sdk-components-for-windows-installer-developers.md) Dieses Beispielskript kann verwendet werden, um die Komponenten in einer Windows Installer-Datenbank auflisten.

In diesem Beispiel wird die Verwendung des verschiedenen Primärschlüssels in der [Component-Tabelle veranschaulicht.](component-table.md)

Das Beispiel veranschaulicht außerdem:

-   [**OpenDatabase-Methode (Installer-Objekt),**](installer-opendatabase.md) [**die CreateRecord-Methode**](installer-createrecord.md)und die [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) des [**Installer-Objekts**](installer-object.md).
-   [**OpenView-Methode,**](database-openview.md) [**die TablePersistent-Eigenschaft**](database-tablepersistent.md)und die [**PrimaryKeys-Eigenschaft**](database-primarykeys.md) des [**Datenbankobjekts**](database-object.md).
-   [**Führen Sie die -Methode**](view-execute.md) und [**die Fetch-Methode**](view-fetch.md) des [**View-Objekts aus.**](view-object.md)
-   [**StringData-Eigenschaft**](record-stringdata.md) des [**Datensatzobjekts.**](record-object.md)

Die Verwendung dieses Beispiels erfordert die CScript.exe oder WScript.exe version of Windows Script Host. Um dieses CScript.exe ausführen zu können, geben Sie an der Eingabeaufforderung einen Befehl mit der folgenden Syntax ein. Hilfe wird angezeigt, wenn das erste Argument /? ist. oder , wenn zu wenige Argumente angegeben werden. Um die Ausgabe an eine Datei umzuleiten, beenden Sie die Befehlszeile mit VBS > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für den Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiCompon.vbs \[ zum Namen der \] \[ Datenbankkomponente\]**

Geben Sie den Pfad zur Windows Installer-Datenbank an. Geben Sie den Namen der Komponente an. Der Name muss in der Spalte Komponente der Komponententabelle [aufgeführt werden.](component-table.md) Wenn der Name der Komponente weggelassen wird, werden alle Komponenten aufgelistet. Wenn ein Sternchen ( ) als Komponentenname verwendet wird, WiCompon.vbs \* die Zusammensetzung aller Komponenten auf. Beachten Sie, dass große Datenbanken besser mit CScript anstelle von WScript angezeigt werden.

Weitere Skriptbeispiele finden Sie unter [Windows Installer Scripting Examples](windows-installer-scripting-examples.md). Beispielprogramme, für die kein Skripthost Windows ist, finden Sie unter [Windows Installer Development Tools](windows-installer-development-tools.md).

 

 



