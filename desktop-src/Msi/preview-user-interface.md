---
description: Die VBScript-Datei WiDialog.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. Dieses Beispiel zeigt, wie das Skript zum Anzeigen einer Vorschau von Dialogfeldern in einer Windows Installer Datenbank verwendet wird.
ms.assetid: b3d72ba1-1d19-4460-8b9b-94f72214e8b1
title: Vorschau der Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7736c442cdfcb22034326ff459eb89fc28b0c9af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368806"
---
# <a name="preview-user-interface"></a>Vorschau der Benutzeroberfläche

Die VBScript-Datei WiDialog.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Beispiel zeigt, wie das Skript zum Anzeigen einer Vorschau von Dialogfeldern in einer Windows Installer Datenbank verwendet wird.

In diesem Beispiel wird Folgendes veranschaulicht:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md), die [**Methode "samaterecord**](installer-createrecord.md)" und die [**Methode "lasterrorrecord**](installer-lasterrorrecord.md) " des [**Installerobjekts**](installer-object.md)
-   [**OpenView-Methode**](database-openview.md) und die [**enableuipreview-Methode**](database-enableuipreview.md) des Database- [**Objekts**](database-object.md)
-   [**Execute-Methode**](view-execute.md) und die [**Fetch-Methode**](view-fetch.md) des View- [**Objekts**](view-object.md)
-   Eigenschaften [**Eigenschaft von StringData**](record-stringdata.md) des [ **Datensatz-Objekts**](record-object.md)

Für dieses Beispiel ist die CScript.exe oder WScript.exe Version von Windows Script Host erforderlich. Wenn Sie CScript.exe für dieses Beispiel verwenden möchten, geben Sie mithilfe der folgenden Syntax einen Befehl an der Eingabeaufforderung ein. Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden. Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript-WiDialog.vbs** *\[ Pfad zu Daten Bank \] \[ dialogamen \]*

Geben Sie den Pfad zu einer Windows Installer-Datenbank an. Geben Sie den Namen eines Dialogs an. Dieser Name muss in der Dialogfeld Spalte der Dialogfeld [Tabelle](dialog-table.md)aufgeführt werden. Zum Anzeigen eines Billboard fügen Sie den Namen des Dialog Felds mit dem Namen des Steuer Elements aus der [Tabelle "Control](control-table.md) " an, und fügen Sie diesen an den Namen des Billboard in der Tabelle " [Billboard](billboard-table.md)" an. Wenn keine Dialoge angegeben sind, werden alle Dialogfelder in der Dialog Feld Tabelle sequenziell angezeigt.

Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md). Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

 

 



