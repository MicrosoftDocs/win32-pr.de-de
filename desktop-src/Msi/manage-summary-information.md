---
description: Die VBScript-Datei WiSumInf.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. Dieses Beispielskript kann verwendet werden, um den Zusammenfassungs Informationsdaten Strom eines Windows Installer Pakets zu verwalten.
ms.assetid: f7f1cf89-f211-4511-8260-b48c898c1cf6
title: Zusammenfassende Informationen verwalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02ff360bd56dabc57b3a7ffccdba8c4f90346193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041835"
---
# <a name="manage-summary-information"></a>Zusammenfassende Informationen verwalten

Die VBScript-Datei WiSumInf.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Beispielskript kann verwendet werden, um den [Zusammenfassungs Informationsdaten Strom](summary-information-stream.md) eines Windows Installer Pakets zu verwalten.

Das Beispiel veranschaulicht die Verwendung von:

-   [**SummaryInformation-Eigenschaft (Installer-Objekt)**](installer-summaryinformation.md)
-   [**Lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)

Zum Verwenden dieses Beispiels ist die CScript.exe oder WScript.exe Version von Windows Script Host erforderlich. Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie einen Befehl an der Eingabeaufforderung ein, indem Sie die folgende Syntax verwenden. Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden. Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiSumInf.vbs \[ Pfad zur Daten Bank \] \[ Eigenschaft = Wert\]**

Geben Sie den Pfad für die Windows Installer-Datenbank an. Wenn keine anderen Argumente angegeben werden, listet das Skript alle Zusammenfassungs Eigenschaften für das Paket auf. Geben Sie eine Liste der zusammen zufassenden Eigenschaften und Werte an, die mit der Format Eigenschaft = Value aktualisiert werden sollen. Sie können die Eigenschaft entweder nach dem unten gezeigten Namen oder PID-Wert angeben. Datums-und Uhrzeit Felder verwenden das aktuelle Gebiets Schema Format oder "Now" oder "Date". Weitere Informationen finden Sie unter [Summary Information Stream-Eigenschaften Satz](summary-information-stream-property-set.md).



| PID | Name        | BESCHREIBUNG                                                                                                                                                                                                                                                                                      |
|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | codepage    | ANSI-Codepage von Text Zeichenfolgen in Zusammenfassungs Informationen. Weitere Informationen finden Sie unter [**Codepage Summary**](codepage-summary.md) -Eigenschaft.                                                                                                                                                           |
| 2   | Titel       | Der Typ des Windows Installer Pakets. Weitere Informationen finden Sie unter [**Titel Zusammenfassungs Eigenschaft**](title-summary.md).                                                                                                                                                                                    |
| 3   | Subject     | Der vollständige Produktname. Weitere Informationen finden Sie [**unter Subject Summary Property**](subject-summary.md).                                                                                                                                                                                               |
| 4   | Autor      | Ersteller, in der Regel Herstellername. Weitere Informationen finden Sie unter [**Zusammenfassungs Eigenschaft des Autors**](author-summary.md).                                                                                                                                                                                     |
| 5   | Keywords    | Liste der Schlüsselwörter, die vom Dateibrowser verwendet werden sollen. Weitere Informationen finden Sie unter [**Schlüsselwort Zusammenfassungs Eigenschaft**](keywords-summary.md).                                                                                                                                                                       |
| 6   | Kommentare    | Die Beschreibung des zwecks oder der Verwendung des Pakets. Weitere Informationen finden Sie unter [**comments Summary-Eigenschaft**](comments-summary.md).                                                                                                                                                                       |
| 7   | Vorlage    | Unterstützte Plattformen und Sprachen. Weitere Informationen finden Sie unter [**Template Summary-Eigenschaft**](template-summary.md).                                                                                                                                                                              |
| 8   | Lastauthor  | Wird nur vom Installationsprogramm festgelegt. Weitere Informationen finden Sie unter [**letzte gespeicherte Eigenschaft mit Zusammenfassung**](last-saved-by-summary.md).                                                                                                                                                                            |
| 9   | Revision    | Paket Code-GUID. Weitere Informationen finden Sie unter [**Übersicht über die Revisionsnummern Eigenschaft**](revision-number-summary.md).                                                                                                                                                                                |
| 11  | Drucken     | Datum und Uhrzeit des Installations Abbilds. Weitere Informationen finden Sie unter [**zuletzt gedruckte Summary-Eigenschaft**](last-printed-summary.md).                                                                                                                                                                    |
| 12  | Erstellt     | Datum und Uhrzeit der Paket Erstellung. Weitere Informationen finden Sie unter [**Create time/date Summary Property**](create-time-date-summary.md).                                                                                                                                                              |
| 13  | Gespeichert       | Datum und Uhrzeit der letzten Paket Änderung. Weitere Informationen finden Sie unter " [**zuletzt gespeicherte Zeit-/datezusammenfassungs-Eigenschaft**](last-saved-time-date-summary.md)".                                                                                                                                             |
| 14  | Seiten       | Mindestens erforderliche Version von Windows Installer für dieses Paket erforderlich. Weitere Informationen finden Sie unter [**Zusammenfassungs Eigenschaft für Seitenanzahl**](page-count-summary.md).                                                                                                                                             |
| 15  | Dankes       | Typ des Quelldatei Bilds. Weitere Informationen finden Sie unter [**Zusammenfassung der Wort Zählung**](word-count-summary.md). Ab Windows Installer Version 4,0 unter Windows Vista und Windows Server 2008 umfasst diese Eigenschaft Bits, um anzugeben, ob erhöhte Rechte erforderlich sind.<br/> |
| 16  | Zeichen  | Wird nur für Transformationen verwendet. [**Zeichen Anzahl**](character-count-summary.md).                                                                                                                                                                                                                    |
| 18  | Application | Die dieser Datei zugeordnete Anwendung, d. h. "Windows Installer". Weitere Informationen finden Sie unter [**Erstellen einer Anwendungs Zusammenfassungs Eigenschaft**](creating-application-summary.md).                                                                                                                        |
| 19  | Sicherheit    | Sicherheitseinstellung. Weitere Informationen finden Sie unter [**Sicherheits Zusammenfassungs Eigenschaft**](security-summary.md).                                                                                                                                                                                               |



 

Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md). Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

 

 




