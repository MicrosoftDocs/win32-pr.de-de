---
description: Die Windows SDK-Komponenten für Windows Installer-Entwickler enthalten VBScript-Dateien, die zeigen, wie die Windows Installer-Automatisierungsschnittstelle verwendet wird, um Windows Installer-Pakete zu ändern.
ms.assetid: 93747a8d-32e0-4f31-a5cf-f95fb26b97df
title: Windows Beispiele für Skripterstellung für Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3addf648460418daad783b6c5dbcc71078f9904c4a0bba1324f025896692cd37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065770"
---
# <a name="windows-installer-scripting-examples"></a>Windows Beispiele für Skripterstellung für Installer

Die [Windows SDK-Komponenten für Windows Installer-Entwickler](platform-sdk-components-for-windows-installer-developers.md) enthält VBScript-Dateien, die zeigen, wie die Windows Installer-Automatisierungsschnittstelle verwendet wird, um Windows Installer-Pakete zu ändern.

Die in diesem Thema identifizierten Skriptbeispiele werden von Microsoft Corporation nicht unterstützt und werden nur als potenziell nützlicher Verweis bereitgestellt. Zum Ausführen dieser Beispiele ist der Windows Script Host erforderlich. Weitere Informationen zu Windows Script Host finden Sie im Abschnitt [Windows Script Host](/previous-versions//9bbdkx3k(v=vs.85)) des Microsoft Windows Software Development Kit (SDK).



| Beispielskriptdatei | Beschreibung                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------|
| WiLstPrd.vbs       | [Auflisten von Produkten, Eigenschaften, Features und Komponenten](list-products-properties-features-and-components.md) |
| WiImport.vbs       | [Importieren von Dateien](import-files.md)                                                                            |
| WiExport.vbs       | [Exportieren von Dateien](export-files.md)                                                                            |
| WiSubStg.vbs       | [Verwalten von Untertoragen](manage-substorages.md)                                                                |
| WiStream.vbs       | [Verwalten von binären Streams](manage-binary-streams.md)                                                          |
| WiMerge.vbs        | [Zusammenführen von zwei Datenbanken](merge-two-databases.md)                                                              |
| WiGenXfm.vbs       | [Generieren einer Transformation](generate-a-transform.md)                                                            |
| WiUseXfm.vbs       | [Anwenden einer Transformation](apply-a-transform.md)                                                                  |
| WiLstXfm.vbs       | [Anzeigen einer Transformation](view-a-transform.md) (nur CSCRIPT)                                                     |
| WiDiffDb.vbs       | [Anzeigen von Unterschieden zwischen zwei Datenbanken](view-differences-between-two-databases.md) (nur CSCRIPT)         |
| WiLstScr.vbs       | [Installer-Skript anzeigen](view-installer-script.md) (nur CSCRIPT)                                           |
| WiSumInf.vbs       | [Verwalten von Zusammenfassungsinformationen](manage-summary-information.md)                                                |
| WiPolicy.vbs       | [Verwalten von Richtlinieneinstellungen](manage-policy-settings.md)                                                        |
| WiLangId.vbs       | [Verwalten von Sprache und Codepage](manage-language-and-codepage.md)                                            |
| WiToAnsi.vbs       | [Kopieren einer Unicode-Datei in eine Ansi-Datei](copy-a-unicode-file-to-an-ansi-file.md)                              |
| WiFilVer.vbs       | [Verwalten von Dateigrößen und -versionen](manage-file-sizes-and-versions.md)                                        |
| WiMakCab.vbs       | [Generieren eines Dateischränks](generate-file-cabinet.md)                                                          |
| WiRunSQL.vbs       | [Ausführen von SQL-Anweisungen](execute-sql-statements.md)                                                        |
| WiTextIn.vbs       | [Kopieren einer ANSI-Datei in ein Datenbankfeld](copy-ansi-file-into-a-database-field.md)                            |
| WiCompon.vbs       | [Komponenten auflisten](list-components.md)                                                                      |
| WiFeatur.vbs       | [Auflisten von Features](list-features.md)                                                                          |
| WiDialog.vbs       | [Vorschau Benutzeroberfläche](preview-user-interface.md)                                                        |



 

Alle diese Skripts zeigen einen Hilfebildschirm an, der ihre Befehlszeilenargumente beschreibt. Doppelklicken Sie auf die Datei, um den Hilfebildschirm in Windows anzuzeigen. Um den Hilfebildschirm über eine Befehlszeile anzuzeigen, geben Sie ein ? als erstes Argument, oder geben Sie weniger Argumente als erforderlich ein. Skripts geben bei Erfolg den Wert 0 zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn ein Fehler vorliegt.

Für diese Beispiele muss Windows Skripthost ausgeführt werden. Windows Der Skripthost besteht eigentlich aus zwei Hosts:

-   CScript.exe ist die Version, mit der Sie Skripts über die Eingabeaufforderung ausführen können, und bietet Befehlszeilenschalter zum Festlegen von Skripteigenschaften.
-   WScript.exe ist die Version von Windows Script Host, mit der Sie Skripts aus Windows ausführen können. Weitere Informationen finden Sie im Abschnitt [Windows Script Host](/previous-versions//9bbdkx3k(v=vs.85)) im Windows SDK.

Das hilfsprogramm Makecab.exe ist in den Patchbeispielen in den [Windows SDK-Komponenten für Windows Installer-Entwickler](platform-sdk-components-for-windows-installer-developers.md)enthalten.

Weitere Informationen zu WMI finden Sie unter [Using Windows Installer with WMI (Verwenden von Windows Installer mit WMI).](using-windows-installer-with-wmi.md)

 

 
