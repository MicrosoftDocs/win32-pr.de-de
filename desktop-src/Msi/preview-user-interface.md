---
description: Die VBScript-WiDialog.vbs wird in den sdk-Komponenten Windows für Windows Installer-Entwickler bereitgestellt. Dieses Beispiel zeigt, wie das Skript verwendet wird, um eine Vorschau der Dialoge in einer Windows Installer-Datenbank anzuzeigen.
ms.assetid: b3d72ba1-1d19-4460-8b9b-94f72214e8b1
title: Vorschauversion Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572ab444cc2f6acb6ec426f842318201187336121aa9c2a0557fca8cab94a3ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074710"
---
# <a name="preview-user-interface"></a>Vorschauversion Benutzeroberfläche

Die VBScript-WiDialog.vbs wird in den Windows [SDK-Komponenten für Windows Installer-Entwickler bereitgestellt.](platform-sdk-components-for-windows-installer-developers.md) Dieses Beispiel zeigt, wie das Skript verwendet wird, um eine Vorschau der Dialoge in einer Windows Installer-Datenbank anzuzeigen.

In diesem Beispiel wird Folgendes veranschaulicht:

-   [**OpenDatabase-Methode (Installer-Objekt),**](installer-opendatabase.md) [**die CreateRecord-Methode**](installer-createrecord.md)und die [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) des [**Installer-Objekts**](installer-object.md)
-   [**OpenView-Methode**](database-openview.md) und [**enableUIpreview-Methode**](database-enableuipreview.md) des [**Datenbankobjekts**](database-object.md)
-   [**Execute-Methode**](view-execute.md) und [**fetch-Methode**](view-fetch.md) des [**View-Objekts**](view-object.md)
-   [**StringData-Eigenschaft**](record-stringdata.md) des [ **Datensatzobjekts**](record-object.md)

Für dieses Beispiel ist die CScript.exe oder WScript.exe version of Windows Script Host erforderlich. Um die CScript.exe Beispiel zu verwenden, geben Sie an der Eingabeaufforderung einen Befehl mit der folgenden Syntax ein. Hilfe wird angezeigt, wenn das erste Argument /? ist. oder , wenn zu wenige Argumente angegeben werden. Um die Ausgabe an eine Datei umzuleiten, beenden Sie die Befehlszeile mit VBS > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für den Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiDialog.vbs** *\[ zu Datenbankdialogfeldnamen \] \[ \]*

Geben Sie den Pfad zu einer Windows Installer-Datenbank an. Geben Sie den Namen eines Dialogfelds an. Dieser Name muss in der Spalte Dialog der Tabelle [Dialog aufgeführt werden.](dialog-table.md) Um ein Schild anzuzeigen, fügen Sie den Namen des Dialogfelds mit dem Namen des Steuerelements aus der [Tabelle Control](control-table.md) an, und fügen Sie diesen an den Namen der Tafel in der [Tabelle "Wird" an.](billboard-table.md) Wenn keine Dialoge angegeben werden, werden alle Dialoge in der Dialogtabelle sequenziell angezeigt.

Weitere Skriptbeispiele finden Sie unter [Windows Installer Scripting Examples](windows-installer-scripting-examples.md). Beispielprogramme, für die kein Skripthost Windows ist, finden Sie unter [Windows Installer Development Tools](windows-installer-development-tools.md).

 

 



