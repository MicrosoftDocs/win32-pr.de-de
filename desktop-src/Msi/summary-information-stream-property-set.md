---
description: In der folgenden Tabelle wird der Eigenschafts Satz für Zusammenfassungs Informationsdaten Ströme angezeigt, der die Eigenschaften, die entsprechenden Eigenschaften-IDs, PIDs und Typen enthält.
ms.assetid: a5dd014f-21af-41f9-be75-1b139946179d
title: Eigenschaften Satz für Zusammenfassungs Informationsdaten Strom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3929e4180a85a8f154c0a0352ddd1f9a052769ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363858"
---
# <a name="summary-information-stream-property-set"></a>Eigenschaften Satz für Zusammenfassungs Informationsdaten Strom

In der folgenden Tabelle wird der Eigenschafts Satz für Zusammenfassungs Informationsdaten Ströme angezeigt, der die Eigenschaften, die entsprechenden Eigenschaften-IDs, PIDs und Typen enthält. Weitere Informationen zur Verwendung dieser Eigenschaften durch das Installationsprogramm finden Sie unter [Zusammenfassungs Eigenschafts Beschreibungen](summary-property-descriptions.md). Informationen zu den Windows Installer-Funktionen, die zum Konfigurieren der Eigenschaften für Zusammenfassungs Informationen verwendet werden, finden [Sie unter Verwenden des Datenstroms für Zusammenfassungs Informationen](using-the-summary-information-stream.md).



| Eigenschaftenname                                                | Eigenschafts-ID        | PID | type         |
|--------------------------------------------------------------|--------------------|-----|--------------|
| [**Codepage**](codepage-summary.md)                         | PID- \_ Codepage      | 1   | VT \_ I2       |
| [**Titel**](title-summary.md)                               | PID- \_ Titel         | 2   | VT \_ LPSTR    |
| [**Subject**](subject-summary.md)                           | PID- \_ Betreff       | 3   | VT \_ LPSTR    |
| [**Autor**](author-summary.md)                             | PID- \_ Autor        | 4   | VT \_ LPSTR    |
| [**Keywords**](keywords-summary.md)                         | PID- \_ Schlüsselwörter      | 5   | VT \_ LPSTR    |
| [**Kommentare**](comments-summary.md)                         | PID- \_ Kommentare      | 6   | VT \_ LPSTR    |
| [**Vorlage**](template-summary.md)                         | PID- \_ Vorlage      | 7   | VT \_ LPSTR    |
| [**Zuletzt gespeichert von**](last-saved-by-summary.md)               | PID \_ lastauthor    | 8   | VT \_ LPSTR    |
| [**Revisionsnummer**](revision-number-summary.md)           | PID- \_ revnumber     | 9   | VT \_ LPSTR    |
| [**Zuletzt gedruckt**](last-printed-summary.md)                 | PID \_ lastprint   | 11  | VT \_ FILETIME |
| [**Uhrzeit/Datum erstellen**](create-time-date-summary.md)         | PID \_ Erstellen von \_ DTM   | 12  | VT \_ FILETIME |
| [**Zeitpunkt der letzten Speicherung/Datum**](last-saved-time-date-summary.md)  | PID \_ lastsave \_ DTM | 13  | VT \_ FILETIME |
| [**Seitenanzahl**](page-count-summary.md)                     | PID- \_ PageCount     | 14  | VT \_ I4       |
| [**Wort Anzahl**](word-count-summary.md)                     | PID- \_ WordCount     | 15  | VT \_ I4       |
| [**Zeichen Anzahl**](character-count-summary.md)           | PID- \_ Anzahl     | 16  | VT \_ I4       |
| [**Anwendung wird erstellt**](creating-application-summary.md) | PID- \_ appname       | 18  | VT \_ LPSTR    |
| [**Sicherheit**](security-summary.md)                         | PID- \_ Sicherheit      | 19  | VT \_ I4       |



 

Das Installationsprogramm verwaltet derzeit dreispeicher Formate für Installationspakete, Transformationen und Patchpakete. Die CLSID für den Speicher ist unabhängig von den Zusammenfassungs Informationen für den Speicher auf die entsprechende Formatklasse für das jeweilige Format festgelegt.

 

 



