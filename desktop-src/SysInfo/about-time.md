---
description: Zeitbezogene Funktionen geben eine Zeit in einem von mehreren Formaten zurück. Sie können die Zeitfunktionen für die Konvertierung zwischen einigen Zeitformaten verwenden, um den Vergleich und die Anzeige zu vereinfachen. In der folgenden Tabelle werden die Zeitformate zusammengefasst.
ms.assetid: 74feb158-ba45-4660-970b-3eb577b1ebf8
title: Informationen zu Zeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a95571637bb480920f82e90011a72f6eba9e8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042378"
---
# <a name="about-time"></a>Informationen zu Zeit

Zeitbezogene Funktionen geben eine Zeit in einem von mehreren Formaten zurück. Sie können die Zeitfunktionen für die Konvertierung zwischen einigen Zeitformaten verwenden, um den Vergleich und die Anzeige zu vereinfachen. In der folgenden Tabelle werden die Zeitformate zusammengefasst.



| Format          | type                                                                     | Beschreibung                                                                                                                         |
|-----------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| System          | [**System Time**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)                                     | Jahr, Monat, Tag, Stunde, Sekunde und Millisekunde, die von der internen Hardware Uhr entnommen werden.                                            |
| Lokal           | [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) oder [ **FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) | Eine Systemzeit-oder Dateizeit, die in die lokale Zeitzone des Systems konvertiert wurde.                                                               |
| File            | [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)                                         | Die Anzahl von 100-Nanosekunden-Intervallen seit dem 1. Januar 1601.                                                                       |
| MS-DOS          | **WORD**                                                                 | Ein gepacktes Wort für das Datum, ein weiteres für die Uhrzeit.                                                                                   |
| Windows         | **DWORD** oder **ULONGLONG**                                               | Die Anzahl der Millisekunden seit dem letzten Start des Systems. Beim Abrufen als DWORD-Wert wird Windows-Zeitzyklen alle 49,7 Tage fest. |
| Unterbrechungs Anzahl | **ULONGLONG**                                                            | Die Anzahl von 100-Nanosekunden-Intervallen seit dem letzten Start des Systems.                                                           |



 

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Systemzeit](system-time.md)
-   [Ortszeit](local-time.md)
-   [Datei Zeiten](file-times.md)
-   [Datum und Uhrzeit der MS-DOS](ms-dos-date-and-time.md)
-   [Windows-Zeitdienst](windows-time.md)
-   [Interruptzeit](interrupt-time.md)

 

 
