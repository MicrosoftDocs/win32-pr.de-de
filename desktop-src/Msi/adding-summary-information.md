---
description: Die folgenden Eigenschaften für Zusammenfassungs Informationen müssen in jedem Installationspaket definiert werden, wobei ein Software Tool für den Zugriff auf die IStream-Schnittstelle des Zusammenfassungs Informationsdaten Stroms verwendet wird.
ms.assetid: 9775959f-5ab2-43cd-8cc8-9d81945b4ec6
title: Hinzufügen von Übersichts Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd26486e0082a05b05fbdc9609881083e10cddb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131501"
---
# <a name="adding-summary-information"></a>Hinzufügen von Übersichts Informationen

Die folgenden Eigenschaften für Zusammenfassungs Informationen müssen in jedem Installationspaket definiert werden, wobei ein Software Tool für den Zugriff auf die **IStream** -Schnittstelle des [Zusammenfassungs Informationsdaten Stroms](summary-information-stream.md)verwendet wird. Beispielsweise können Sie das Msiinfo.exe Tool verwenden, das mit dem Windows Installer SDK bereitgestellt wird, um diese Eigenschaften festzulegen. Wenn diese Eigenschaften nicht festgelegt sind, übergibt das Paket die [Paket](package-validation.md)Überprüfung nicht.



| Eigenschaft für Zusammenfassungs Informationen                                                   | Daten                                   | Notizen                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Vorlage**](template-summary.md)(Plattform und Sprache)<br/>         | ; 1033                                  | Plattform und Sprache, die von der Datenbank verwendet werden. Wenn die Platt Form Spezifikation im Eigenschafts Wert für die [**Vorlagen**](template-summary.md) Zusammenfassung fehlt, nimmt das Installationsprogramm die Intel-Architektur an. Die [**productlanguage**](productlanguage.md) -Eigenschaft aus der Datenbank wird in der Regel für diese Zusammenfassungs Eigenschaft verwendet. Die Sprach-ID des Beispiels gibt an, dass das Paket US-Englisch verwendet. |
| [**Revisionsnummer**](revision-number-summary.md)(Paketcode)<br/>    | {4966aec4-3c59-4b07-9b98-1b6a7103c0d3} | Dies ist die Paket Code- [GUID](guid.md) , die das Beispiel Paket eindeutig identifiziert. Wenn Sie dieses Beispiel reproduzieren, verwenden Sie ein Dienstprogramm wie z. b. GUIDGEN, um eine andere GUID für das Paket zu generieren. Die Ergebnisse von Guidgen enthalten Kleinbuchstaben. Beachten Sie, dass Sie alle Kleinbuchstaben für einen gültigen Paketcode in Großbuchstaben ändern müssen. Siehe [Paket Codes](package-codes.md).             |
| [**Seitenanzahl**](page-count-summary.md)(minimale Installerversion)<br/> | 200                                    | Für einen minimalen Windows Installer 2,0 sollte diese Eigenschaft auf die ganze Zahl 200 festgelegt werden.                                                                                                                                                                                                                                                                                                                 |
| [**Wort Anzahl**](word-count-summary.md)(Quelltyp)<br/>            | 0                                      | Der globale Quelltyp für das Paket ist lange Dateinamen und unkomprimiert. Weitere Informationen finden Sie unter [komprimierte und nicht komprimierte Quellen](compressed-and-uncompressed-sources.md) und in der Beschreibung der Spalte Attribute der [Dateitabelle](file-table.md) .                                                                                                                                |



 

Die verbleibenden Eigenschaften des Zusammenfassungs Informationsdaten Stroms sind nicht erforderlich, sollten jedoch für das MNP2000.msi Beispiel festgelegt werden.



| Eigenschaft für Zusammenfassungs Informationen                                 | Daten                                                                             | Notizen                                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**Titel**](title-summary.md)                               | Installations Datenbank                                                            | Teilt den Benutzern mit, dass es sich bei dieser Datenbank um eine Installation anstelle einer Transformation oder eines Patches handelt.                        |
| [**Subject**](subject-summary.md)                           | MNP2000                                                                          | Dateibrowser können dies als Produktanzeigen, das mit dieser Datenbank installiert werden soll.                                  |
| [**Keywords**](keywords-summary.md)                         | Installer, MSI, Datenbank                                                         | Dateibrowser, die für die Suche nach Schlüsselwörtern geeignet sind, können nach diesen Wörtern suchen.                                    |
| [**Autor**](author-summary.md)                             | Microsoft Corporation                                                            | Der Name des Herstellers des Produkts.                                                                                |
| [**Kommentare**](comments-summary.md)                         | Diese Installerdatenbank enthält die Logik und die Daten, die zum Installieren von Notepad erforderlich sind. | Informiert Benutzer über den Zweck dieser Datenbank.                                                                  |
| [**Anwendung wird erstellt**](creating-application-summary.md) | Orca                                                                             | Anwendung, die zum Erstellen der Installations Datenbank verwendet wird. Das Beispiel gibt den Orca-Datenbank-Editor als Beispiel an. |
| [**Sicherheit**](security-summary.md)                         | 0                                                                                | Die Beispieldatenbank weist uneingeschränkten Lese-/Schreibzugriff auf.                                                                    |



 

Zum Vervollständigen dieser Beispieldatenbank benötigen Sie nicht die Eigenschaften für das Datum der [**letzten**](last-saved-by-summary.md)Speicherung, das Datum und die Uhrzeit der letzten [**Speicherung, das**](create-time-date-summary.md)Datum und die Uhrzeit der letzten [**gedruckten**](last-printed-summary.md) [**-**](last-saved-time-date-summary.md), [**Zeichen Anzahl**](character-count-summary.md)und die [**Codepage**](codepage-summary.md) -Zusammenfassung. Das Beispiel basiert auf dem Tool zum Bearbeiten von Datenbanken, um diese optionalen Eigenschaften festzulegen und zu aktualisieren.

Wenn Sie z. b. Msiinfo zum Hinzufügen der Zusammenfassungs Informationen zum Beispiel verwenden möchten, wechseln Sie in das Verzeichnis mit der Datenbank, und verwenden Sie die folgende Befehlszeile. Verwenden Sie die unten gezeigte Beispiel Paket-ID nicht.

**Msiinfo.exe MNP2000.msi-T-Installations Datenbank "-J Subject-A" Microsoft Corporation "-K" Installer, MSI, Datenbank "-O" Diese Installerdatenbank enthält die Logik und die Daten, die erforderlich sind, um Notepad zu installieren. "-P; 1033-V {4966aec4-3c59-4b07-9b98-1b6a7103c0d3}-G 200-W 0-N Orca-U 0**

Weitere Informationen zu Zusammenfassungs Informationen finden Sie unter Informationen zum [Zusammenfassungs Informationsdaten Strom](about-the-summary-information-stream.md) [mit dem Zusammenfassungs Informations](using-the-summary-information-stream.md)Datenstrom und [Datenstrom Referenz für Zusammenfassungs Informationen](summary-information-stream-reference.md).

Eine vollständige Liste aller Eigenschaften der Zusammenfassungs Informationen und [Beschreibungen](summary-property-descriptions.md) der Eigenschaften für die Beschreibung finden Sie unter Übersicht über Zusammenfassungs [Informationsdaten Ströme](summary-information-stream-property-set.md) .

[Fortsetzen](importing-the-user-interface.md)

 

 




