---
description: Die VBScript-Datei WiLstScr.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. In diesem Beispielskript wird der Windows Installer Skript-Viewer veranschaulicht.
ms.assetid: 18989c16-e0c8-4d11-b915-730951b6845b
title: Installerskript anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56888f478bb7cdd43ebcee817c86f6f9f163840e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343372"
---
# <a name="view-installer-script"></a>Installerskript anzeigen

Die VBScript-Datei WiLstScr.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. In diesem Beispielskript wird der Windows Installer Skript-Viewer veranschaulicht.

Das Beispiel veranschaulicht die Verwendung von:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)
-   [**Lasterrorrecord**](installer-lasterrorrecord.md) -Methode des [**Installer**](installer-object.md) -Objekts
-   [**OpenView**](database-openview.md) -Methode des [**Daten Bank**](database-object.md) Objekts
-   [**Fetch**](view-fetch.md) -Methode des [**View**](view-object.md) -Objekts
-   [**Formattext**](record-formattext.md) -Methode
-   [**FieldCount**](record-fieldcount.md) (Eigenschaft)
-   [**StringData**](record-stringdata.md) -Eigenschaft des [**Datensatz**](record-object.md) -Objekts
-   [\_Transformview-Tabelle](-transformview-table.md)

Zum Verwenden dieses Beispiels ist die CScript.exe Version von Windows Script Host erforderlich. Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie einen Befehl an der Eingabeaufforderung ein, indem Sie die folgende Syntax verwenden. Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden. Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript-WiLstScr.vbs** *\[ Pfad zum Windows Installer Ausführungs \] Skript*

Geben Sie den Pfad zum Ausführungs Skript des Installers an.

Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md). Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

 

 



