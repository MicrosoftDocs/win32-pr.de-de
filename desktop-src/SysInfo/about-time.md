---
description: Zeitbezogene Funktionen geben die Zeit in einem von mehreren Formaten zurück. Sie können die Zeitfunktionen verwenden, um zwischen einigen Zeitformaten zu konvertieren, um den Vergleich und die Anzeige zu erleichtern. In der folgenden Tabelle werden die Zeitformate zusammengefasst.
ms.assetid: 74feb158-ba45-4660-970b-3eb577b1ebf8
title: Na endlich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22cb2cd140ada7033ebe7bf672e654dbf7227385509c676176ee8e936ff590ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765031"
---
# <a name="about-time"></a>Na endlich

Zeitbezogene Funktionen geben die Zeit in einem von mehreren Formaten zurück. Sie können die Zeitfunktionen verwenden, um zwischen einigen Zeitformaten zu konvertieren, um den Vergleich und die Anzeige zu erleichtern. In der folgenden Tabelle werden die Zeitformate zusammengefasst.



| Format          | type                                                                     | Beschreibung                                                                                                                         |
|-----------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| System          | [**Systemtime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)                                     | Jahr, Monat, Tag, Stunde, Sekunde und Millisekunde aus der internen Hardwareuhr.                                            |
| Lokal           | [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) oder [ **FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) | Eine Systemzeit oder Dateizeit, die in die lokale Zeitzone des Systems konvertiert wurde.                                                               |
| Datei            | [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)                                         | Die Anzahl von 100-Nanosekunden-Intervallen seit dem 1. Januar 1601.                                                                       |
| MS-DOS          | **WORD**                                                                 | Ein gepacktes Wort für das Datum, ein anderes für die Uhrzeit.                                                                                   |
| Windows         | **DWORD** oder **ULONGLONG**                                               | Die Anzahl von Millisekunden seit dem letzten Start des Systems. Wenn sie als DWORD-Wert abgerufen wird, Windows alle 49,7 Tage zeitzyklen. |
| Interruptanzahl | **ULONGLONG**                                                            | Die Anzahl von 100-Nanosekunden-Intervallen seit dem letzten Start des Systems.                                                           |



 

Weitere Informationen finden Sie in den folgenden Themen:

-   [Systemzeit](system-time.md)
-   [Ortszeit](local-time.md)
-   [Dateizeiten](file-times.md)
-   [MS-DOS-Datum und -Uhrzeit](ms-dos-date-and-time.md)
-   [Windows-Zeitdienst](windows-time.md)
-   [Interruptzeit](interrupt-time.md)

 

 
