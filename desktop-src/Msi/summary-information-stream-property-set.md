---
description: Die folgende Tabelle zeigt den Eigenschaftensatz für den Zusammenfassungsinformationsstream, der die Eigenschaften, die entsprechenden Eigenschaften-IDs, PIDs und Typen enthält.
ms.assetid: a5dd014f-21af-41f9-be75-1b139946179d
title: Summary Information Stream Property Set
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d41439e15a59ca1942fcbb49c06067251060935b165d6a34972df868fa7feac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627050"
---
# <a name="summary-information-stream-property-set"></a>Summary Information Stream Property Set

Die folgende Tabelle zeigt den Eigenschaftensatz für den Zusammenfassungsinformationsstream, der die Eigenschaften, die entsprechenden Eigenschaften-IDs, PIDs und Typen enthält. Weitere Informationen dazu, wie das Installationsprogramm diese Eigenschaften verwendet, finden Sie unter [Zusammenfassungseigenschaftenbeschreibungen](summary-property-descriptions.md). Informationen zu den Funktionen des Fensterinstallationsprogramms, die zum Konfigurieren der Zusammenfassungsinformationseigenschaften verwendet werden, finden Sie unter [Verwenden des Zusammenfassungsinformationsstreams.](using-the-summary-information-stream.md)



| Eigenschaftenname                                                | Eigenschafts-ID        | PID | Typ         |
|--------------------------------------------------------------|--------------------|-----|--------------|
| [**Codepage**](codepage-summary.md)                         | \_PID-CODEPAGE      | 1   | VT \_ I2       |
| [**Titel**](title-summary.md)                               | PID \_ TITLE         | 2   | VT \_ LPSTR    |
| [**Subject**](subject-summary.md)                           | PID \_ SUBJECT       | 3   | VT \_ LPSTR    |
| [**Autor**](author-summary.md)                             | PID \_ AUTHOR        | 4   | VT \_ LPSTR    |
| [**Keywords**](keywords-summary.md)                         | \_PID-SCHLÜSSELWÖRTER      | 5   | VT \_ LPSTR    |
| [**Kommentare**](comments-summary.md)                         | \_PID-KOMMENTARE      | 6   | VT \_ LPSTR    |
| [**Vorlage**](template-summary.md)                         | \_PID-VORLAGE      | 7   | VT \_ LPSTR    |
| [**Zuletzt gespeichert von**](last-saved-by-summary.md)               | PID \_ LASTAUTHOR    | 8   | VT \_ LPSTR    |
| [**Revisionsnummer**](revision-number-summary.md)           | PID \_ REVNUMBER     | 9   | VT \_ LPSTR    |
| [**Zuletzt gedruckt**](last-printed-summary.md)                 | PID \_ LASTPRINTED   | 11  | VT \_ FILETIME |
| [**Erstellen von Uhrzeit/Datum**](create-time-date-summary.md)         | PID \_ CREATE \_ DG   | 12  | VT \_ FILETIME |
| [**Zeitpunkt/Datum des letzten Speicherns**](last-saved-time-date-summary.md)  | PID \_ LASTSAVE \_ DG | 13  | VT \_ FILETIME |
| [**Seitenanzahl**](page-count-summary.md)                     | PID \_ PAGECOUNT     | 14  | VT \_ I4       |
| [**Wortanzahl**](word-count-summary.md)                     | PID \_ WORDCOUNT     | 15  | VT \_ I4       |
| [**Zeichenanzahl**](character-count-summary.md)           | PID \_ CHARCOUNT     | 16  | VT \_ I4       |
| [**Erstellen einer Anwendung**](creating-application-summary.md) | PID \_ APPNAME       | 18  | VT \_ LPSTR    |
| [**Security**](security-summary.md)                         | \_PID-SICHERHEIT      | 19  | VT \_ I4       |



 

Das Installationsprogramm verwaltet derzeit drei Speicherformate für Installationspakete, Transformationen und Patchpakete. Die CLSID für den Speicher wird unabhängig von den Zusammenfassungsinformationen für den Speicher auf die entsprechende Formatklasse für das bestimmte Format festgelegt.

 

 



