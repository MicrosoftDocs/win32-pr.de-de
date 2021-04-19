---
description: Die VBScript-Datei WiLangID.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt.
ms.assetid: 319e9ffd-ff9f-4b4c-913e-2c571f2ec9ee
title: Verwalten von Sprache und Codepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbfb96f04d75ed79f32c8a49fe58b8dcc86f184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369044"
---
# <a name="manage-language-and-codepage"></a>Verwalten von Sprache und Codepage

Die VBScript-Datei WiLangID.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Beispiel zeigt, wie mithilfe des Skripts auf die Sprachinformationen und Codepage eines Pakets zugegriffen werden kann. Weitere Informationen finden Sie unter [lokalisieren eines Windows Installer Pakets](localizing-a-windows-installer-package.md) und [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).

Das Beispiel veranschaulicht die Verwendung von:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)
-   [**Methode "kreaterecord"**](installer-createrecord.md)
-   [**Lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)
-   [**OpenView-Methode**](database-openview.md)
-   [**SummaryInformation-Eigenschaft (Datenbankobjekt)**](database-summaryinformation.md) des [ **Datenbankobjekts**](database-object.md)

Zum Verwenden dieses Beispiels ist die CScript.exe oder WScript.exe Version von Windows Script Host erforderlich. Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie einen Befehl an der Eingabeaufforderung ein, indem Sie die folgende Syntax verwenden. Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden. Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript-WiLangID.vbs \[ Pfad zu Datenbank- \] \[ Schlüsselwort \] \[ Wert\]**

Geben Sie den Pfad für die Windows Installer-Datenbank an. Um einen Wert zu ändern, geben Sie eines der folgenden Schlüsselwörter gefolgt vom neuen Wert an. Wenn kein Wert angegeben ist, gibt das Beispiel den aktuellen Wert zurück.



| Schlüsselwort      | BESCHREIBUNG                                                                                                                                                                                |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Paket**  | Die Sprachversionen, die von der Datenbank unterstützt werden. Weitere Informationen finden Sie unter [**Template Summary**](template-summary.md) -Eigenschaft.                                                               |
| **Produkt**  | Die Sprache, die das Installationsprogramm für alle Zeichen folgen in der Benutzeroberfläche verwenden soll, die nicht in der Datenbank erstellt wurden. Weitere Informationen finden Sie unter [**productlanguage**](productlanguage.md) -Eigenschaft. |
| **Codepage** | Einzelne ANSI-Codepage für den Zeichen folgen Pool. Weitere Informationen finden Sie unter [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).                                       |



 

Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md). Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

Weitere Informationen finden Sie unter [bestimmen der Codepage einer Installations Datenbank](determining-an-installation-database-s-code-page.md) und [Festlegen der Codepage einer Datenbank](setting-the-code-page-of-a-database.md).

 

 



