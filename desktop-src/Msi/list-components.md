---
description: Die VBScript-Datei WiCompon.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. Dieses Beispielskript kann verwendet werden, um die Komponenten in einer Windows Installer Datenbank aufzulisten.
ms.assetid: 4e6cc6f4-821a-4a10-a897-5c6aace1f702
title: Komponenten auflisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b79fa34f62374632ec7fdf52a13c6da8ddbfd82a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751704"
---
# <a name="list-components"></a>Komponenten auflisten

Die VBScript-Datei WiCompon.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Beispielskript kann verwendet werden, um die Komponenten in einer Windows Installer Datenbank aufzulisten.

Dieses Beispiel veranschaulicht die Verwendung des verschiedenen Primärschlüssels in der [Component-Tabelle](component-table.md).

Das Beispiel veranschaulicht außerdem Folgendes:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md), die [**Methode**](installer-createrecord.md)"up-Methode" und die [**lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [**Installerobjekts**](installer-object.md).
-   [**OpenView-Methode**](database-openview.md), die [**tablepersistent-Eigenschaft**](database-tablepersistent.md)und die [**primarykeys-Eigenschaft**](database-primarykeys.md) des [**Datenbankobjekts**](database-object.md).
-   [**Execute-Methode**](view-execute.md) und die [**Fetch-Methode**](view-fetch.md) des View- [**Objekts**](view-object.md).
-   [**StringData-Eigenschaften**](record-stringdata.md) Eigenschaft des [**Datensatz-Objekts**](record-object.md).

Zum Verwenden dieses Beispiels ist die CScript.exe oder WScript.exe Version von Windows Script Host erforderlich. Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie einen Befehl an der Eingabeaufforderung ein, indem Sie die folgende Syntax verwenden. Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden. Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript-WiCompon.vbs \[ Pfad zum Daten Bank \] \[ Komponentennamen\]**

Geben Sie den Pfad für die Windows Installer-Datenbank an. Geben Sie den Namen der Komponente an. Der Name muss in der Component-Spalte der Component- [Tabelle](component-table.md)aufgeführt werden. Wenn der Name der Komponente weggelassen wird, werden alle Komponenten aufgelistet. Wenn ein Sternchen ( \* ) als Komponenten Name verwendet wird, wird WiCompon.vbs die Zusammensetzung aller Komponenten auflistet. Beachten Sie, dass große Datenbanken mithilfe von cscript anstelle von WScript besser angezeigt werden.

Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md). Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

 

 



