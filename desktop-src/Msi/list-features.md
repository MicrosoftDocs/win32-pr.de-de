---
description: Die VBScript-Datei WiFeatur.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt.
ms.assetid: 797cb383-22c0-42b4-82c1-d5bcc3a8bafb
title: Auflisten von Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e166401b514f1beec9c14c74aba7ca0601f446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345058"
---
# <a name="list-features"></a>Auflisten von Features

Die VBScript-Datei WiFeatur.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Beispiel zeigt, wie das Skript zum Auflisten der Funktionen in einer Windows Installer Datenbank verwendet wird. In diesem Beispiel wird veranschaulicht, wie einer schreibgeschützten Windows Installer-Datenbank temporäre Spalten hinzugefügt werden.

In diesem Beispiel wird Folgendes veranschaulicht:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md), die [**Methode "samaterecord**](installer-createrecord.md)" und die [**Methode "lasterrorrecord**](installer-lasterrorrecord.md) " des [**Installerobjekts**](installer-object.md)
-   [**Execute-Methode**](view-execute.md) und die [**Fetch-Methode**](view-fetch.md) des View- [**Objekts**](view-object.md)
-   [**OpenView-Methode**](database-openview.md), die [**tablepersistent-Eigenschaft**](database-tablepersistent.md)und die [**primarykeys-Eigenschaft**](database-primarykeys.md) des Database- [**Objekts**](database-object.md)
-   [**FieldCount-Eigenschaft**](record-fieldcount.md), [**IntegerData-Eigenschaft**](record-integerdata.md)und [**StringData-Eigenschaft**](record-stringdata.md) des [**Datensatz-Objekts**](record-object.md)

Zum Verwenden dieses Beispiels ist die CScript.exe oder WScript.exe Version von Windows Script Host erforderlich. Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie einen Befehl an der Eingabeaufforderung ein, indem Sie die folgende Syntax verwenden. Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden. Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript-WiFeatur.vbs \[ Pfad zum Namen der Daten Bank \] \[ Funktion\]**

Geben Sie den Pfad für die Windows Installer-Datenbank an. Geben Sie den Namen der Funktion an. Dies muss in der featurespalte der [Funktions Tabelle](feature-table.md)aufgeführt werden. Wenn der Name der Funktion weggelassen wird, werden alle Funktionen als Funktionsstruktur aufgeführt. Wenn ein Sternchen ( \* ) als Funktionsname verwendet wird, wird WiFeatur.vbs die Zusammensetzung aller Features auflistet. Beachten Sie, dass große Datenbanken mithilfe von cscript anstelle von WScript besser angezeigt werden.

Weitere Informationen finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md) für weitere Skript Beispiele. Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

 

 



