---
description: Die Windows SDK Komponenten für Windows Installer Entwickler enthalten VBScript-Dateien, die Ihnen zeigen, wie die Windows Installer Automation-Schnittstelle zum Ändern von Windows Installer Paketen verwendet wird.
ms.assetid: 93747a8d-32e0-4f31-a5cf-f95fb26b97df
title: Skript Beispiele für Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c2ad75411201cdbf74ef3aa035906d7e58aa7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959979"
---
# <a name="windows-installer-scripting-examples"></a>Skript Beispiele für Windows Installer

Die [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md) enthalten VBScript-Dateien, die Ihnen zeigen, wie die Windows Installer Automation-Schnittstelle zum Ändern von Windows Installer Paketen verwendet wird.

Die in diesem Thema identifizierten Skript Beispiele werden von der Microsoft Corporation nicht unterstützt, und Sie werden nur als potenziell nützliche Referenz bereitgestellt. Zum Ausführen dieser Beispiele ist der Windows Script Host erforderlich. Weitere Informationen zu Windows Script Host finden Sie im Abschnitt [Windows Script Host](/previous-versions//9bbdkx3k(v=vs.85)) des Microsoft Windows Software Development Kit (SDK).



| Beispielskript Datei | BESCHREIBUNG                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------|
| WiLstPrd.vbs       | [Auflisten von Produkten, Eigenschaften, Features und Komponenten](list-products-properties-features-and-components.md) |
| WiImport.vbs       | [Dateien importieren](import-files.md)                                                                            |
| WiExport.vbs       | [Dateien exportieren](export-files.md)                                                                            |
| WiSubStg.vbs       | [Verwalten von substorages](manage-substorages.md)                                                                |
| WiStream.vbs       | [Binäre Streams verwalten](manage-binary-streams.md)                                                          |
| WiMerge.vbs        | [Zwei Datenbanken zusammenführen](merge-two-databases.md)                                                              |
| WiGenXfm.vbs       | [Generieren einer Transformation](generate-a-transform.md)                                                            |
| WiUseXfm.vbs       | [Anwenden einer Transformation](apply-a-transform.md)                                                                  |
| WiLstXfm.vbs       | [Anzeigen einer Transformation](view-a-transform.md) (nur cscript)                                                     |
| WiDiffDb.vbs       | [Anzeigen von Unterschieden zwischen zwei Datenbanken](view-differences-between-two-databases.md) (nur cscript)         |
| WiLstScr.vbs       | [Installerskript anzeigen](view-installer-script.md) (nur cscript)                                           |
| WiSumInf.vbs       | [Zusammenfassende Informationen verwalten](manage-summary-information.md)                                                |
| WiPolicy.vbs       | [Verwalten von Richtlinieneinstellungen](manage-policy-settings.md)                                                        |
| WiLangId.vbs       | [Verwalten von Sprache und Codepage](manage-language-and-codepage.md)                                            |
| WiToAnsi.vbs       | [Kopieren einer Unicode-Datei in eine ANSI-Datei](copy-a-unicode-file-to-an-ansi-file.md)                              |
| WiFilVer.vbs       | [Verwalten von Dateigrößen und-Versionen](manage-file-sizes-and-versions.md)                                        |
| WiMakCab.vbs       | [Datei CAB-Datei generieren](generate-file-cabinet.md)                                                          |
| WiRunSQL.vbs       | [SQL-Anweisungen ausführen](execute-sql-statements.md)                                                        |
| WiTextIn.vbs       | [ANSI-Datei in ein Datenbankfeld kopieren](copy-ansi-file-into-a-database-field.md)                            |
| WiCompon.vbs       | [Komponenten auflisten](list-components.md)                                                                      |
| WiFeatur.vbs       | [Auflisten von Features](list-features.md)                                                                          |
| WiDialog.vbs       | [Vorschau der Benutzeroberfläche](preview-user-interface.md)                                                        |



 

Alle diese Skripts zeigen einen Hilfe Bildschirm an, in dem die Befehlszeilenargumente beschrieben werden. Zum Anzeigen des Hilfe Bildschirms in Windows Doppelklicken Sie auf die Datei. Wenn Sie den Hilfe Bildschirm über eine Befehlszeile anzeigen möchten, geben Sie ein? als erstes Argument, oder geben Sie weniger Argumente als erforderlich ein. Skripts geben den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2 bei einem Fehler.

Diese Beispiele erfordern das Ausführen von Windows Script Host. Windows Script Host ist tatsächlich zwei Hosts:

-   CScript.exe ist die Version, mit der Sie Skripts über die Eingabeaufforderung ausführen und Befehls Zeilenschalter für das Festlegen von Skript Eigenschaften bereitstellen können.
-   WScript.exe ist die Version von Windows Script Host, mit der Sie Skripts aus Windows ausführen können. Weitere Informationen finden Sie im Abschnitt [Windows Script Host](/previous-versions//9bbdkx3k(v=vs.85)) des Windows SDK.

Das Makecab.exe-Hilfsprogramm ist in den Beispielen für das Patchen in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)enthalten.

Weitere Informationen zu WMI finden [Sie unter Verwenden von Windows Installer mit WMI](using-windows-installer-with-wmi.md).

 

 
