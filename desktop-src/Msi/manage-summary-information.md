---
description: Die VBScript-WiSumInf.vbs wird in den Windows SDK-Komponenten für Windows Installer-Entwickler bereitgestellt. Dieses Beispielskript kann verwendet werden, um den Zusammenfassungsinformationsstream eines Pakets Windows Installer zu verwalten.
ms.assetid: f7f1cf89-f211-4511-8260-b48c898c1cf6
title: Verwalten von Zusammenfassungsinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf5ad72ee4f308831077ec2f732b92a70f407c560b204d10f2d3db63d1bb9bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926970"
---
# <a name="manage-summary-information"></a>Verwalten von Zusammenfassungsinformationen

Die VBScript-WiSumInf.vbs wird in den Windows [SDK-Komponenten für Windows Installer-Entwickler bereitgestellt.](platform-sdk-components-for-windows-installer-developers.md) Dieses Beispielskript kann verwendet werden, um den [Zusammenfassungsinformationsstream](summary-information-stream.md) eines Windows Installer-Pakets zu verwalten.

Das Beispiel veranschaulicht die Verwendung von:

-   [**SummaryInformation-Eigenschaft (Installer-Objekt)**](installer-summaryinformation.md)
-   [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)

Die Verwendung dieses Beispiels erfordert die CScript.exe oder WScript.exe version of Windows Script Host. Um dieses CScript.exe ausführen zu können, geben Sie an der Eingabeaufforderung einen Befehl mit der folgenden Syntax ein. Hilfe wird angezeigt, wenn das erste Argument /? ist. oder , wenn zu wenige Argumente angegeben werden. Um die Ausgabe an eine Datei umzuleiten, beenden Sie die Befehlszeile mit VBS > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für den Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiSumInf.vbs \[ zu database \] \[ Property=value\]**

Geben Sie den Pfad zur Windows Installer-Datenbank an. Wenn keine anderen Argumente angegeben werden, listet das Skript alle Zusammenfassungseigenschaften für das Paket auf. Geben Sie eine Liste der Zusammenfassungseigenschaften und -werte an, die mit dem Format Property=value aktualisiert werden sollen. Sie können die Eigenschaft entweder mit dem unten gezeigten Namen oder PID-Wert angeben. Datums- und Uhrzeitfelder verwenden das aktuelle Locale-Format oder "Now" oder "Date". Weitere Informationen finden Sie unter [Summary Information Stream Property Set](summary-information-stream-property-set.md).



| PID | Name        | BESCHREIBUNG                                                                                                                                                                                                                                                                                      |
|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | codepage    | ANSI-Codepage von Textzeichenfolgen in Zusammenfassungsinformationen. Weitere Informationen finden Sie unter [**Codepage Summary Property.**](codepage-summary.md)                                                                                                                                                           |
| 2   | Titel       | Typ des Windows Installer-Pakets. Weitere Informationen finden Sie unter [**Title Summary Property**](title-summary.md).                                                                                                                                                                                    |
| 3   | Gegenstand     | Vollständiger Produktname . Weitere Informationen finden Sie unter [**Subject Summary Property**](subject-summary.md).                                                                                                                                                                                               |
| 4   | Autor      | Creator, in der Regel Herstellername. Weitere Informationen finden Sie unter [**Author Summary Property**](author-summary.md).                                                                                                                                                                                     |
| 5   | Keywords    | Liste der Schlüsselwörter für die Verwendung durch den Dateibrowser. Weitere Informationen finden Sie unter [**Keywords Summary Property**](keywords-summary.md).                                                                                                                                                                       |
| 6   | Kommentare    | Beschreibung des Zwecks oder der Verwendung des Pakets. Weitere Informationen finden Sie unter [**Comments Summary Property**](comments-summary.md).                                                                                                                                                                       |
| 7   | Vorlage    | Unterstützte Plattformen und Sprachen. Weitere Informationen finden Sie unter [**Template Summary Property**](template-summary.md).                                                                                                                                                                              |
| 8   | LastAuthor  | Wird nur vom Installationsprogramm festgelegt. Weitere Informationen finden Sie unter [**Last Saved By Summary Property**](last-saved-by-summary.md).                                                                                                                                                                            |
| 9   | Revision    | Paketcode-GUID. Weitere Informationen finden Sie unter [**Revision Number Summary Property**](revision-number-summary.md).                                                                                                                                                                                |
| 11  | Gedruckt     | Datum und Uhrzeit des Installationsimages. Weitere Informationen finden Sie unter [**Last Printed Summary Property**](last-printed-summary.md).                                                                                                                                                                    |
| 12  | Erstellt     | Datum und Uhrzeit der Paketerstellung. Weitere Informationen finden Sie unter [**Create Time/Date Summary Property**](create-time-date-summary.md).                                                                                                                                                              |
| 13  | Gespeichert       | Datum und Uhrzeit der letzten Paketänderung. Weitere Informationen finden Sie unter [**Last Saved Time/Date Summary Property**](last-saved-time-date-summary.md).                                                                                                                                             |
| 14  | Seiten       | Mindestens erforderliche Version Windows Installer für dieses Paket. Weitere Informationen finden Sie unter [**Page Count Summary Property**](page-count-summary.md).                                                                                                                                             |
| 15  | Wörter       | Typ des Quelldateiimages. Weitere Informationen finden Sie unter [**Word Count Summary Property**](word-count-summary.md). Ab Windows Installer Version 4.0 unter Windows Vista und Windows Server 2008 enthält diese Eigenschaft Bits, um anzugeben, ob erhöhte Berechtigungen erforderlich sind.<br/> |
| 16  | Zeichen  | Wird nur für Transformationen verwendet. [**Zeichenanzahl**](character-count-summary.md).                                                                                                                                                                                                                    |
| 18  | Anwendung | Anwendung, die dieser Datei zugeordnet ist, d.h. "Windows Installer". Weitere Informationen finden Sie unter [**Erstellen der Anwendungszusammenfassungseigenschaft**](creating-application-summary.md).                                                                                                                        |
| 19  | Sicherheit    | Sicherheitseinstellung. Weitere Informationen finden Sie unter [**Security Summary Property**](security-summary.md).                                                                                                                                                                                               |



 

Weitere Skriptbeispiele finden Sie unter [Windows Installer Scripting Examples](windows-installer-scripting-examples.md). Beispielprogramme, für die kein Skripthost Windows ist, finden Sie unter [Windows Installer Development Tools](windows-installer-development-tools.md).

 

 




