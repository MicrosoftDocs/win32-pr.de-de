---
description: Zeitbezogene Funktionen geben Zeit in einem von mehreren Formaten zurück. Sie können die Zeitfunktionen verwenden, um zur Vereinfachung des Vergleichs und der Anzeige zwischen einigen Zeitformaten zu konvertieren. In der folgenden Tabelle sind die Zeitformate zusammengefasst.
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

Zeitbezogene Funktionen geben Zeit in einem von mehreren Formaten zurück. Sie können die Zeitfunktionen verwenden, um zur Vereinfachung des Vergleichs und der Anzeige zwischen einigen Zeitformaten zu konvertieren. In der folgenden Tabelle sind die Zeitformate zusammengefasst.



| Format          | type                                                                     | Beschreibung                                                                                                                         |
|-----------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| System          | [**Systemtime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)                                     | Jahr, Monat, Tag, Stunde, Sekunde und Millisekunde aus der internen Hardwareuhr.                                            |
| Lokal           | [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) oder [ **FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) | Eine Systemzeit oder Dateizeit, die in die lokale Zeitzone des Systems konvertiert wird.                                                               |
| Datei            | [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)                                         | Die Anzahl der Intervalle von 100 Nanosekunden seit dem 1. Januar 1601.                                                                       |
| MS-DOS          | **WORD**                                                                 | Ein gepacktes Wort für das Datum, ein anderes für die Uhrzeit.                                                                                   |
| Windows         | **DWORD** oder **ULONGLONG**                                               | Die Anzahl von Millisekunden seit dem letzten Start des Systems. Beim Abrufen als DWORD-Wert Windows Zeitzyklen alle 49,7 Tage. |
| Interruptanzahl | **ULONGLONG**                                                            | Die Anzahl von Intervallen von 100 Nanosekunden seit dem letzten Start des Systems.                                                           |



 

Weitere Informationen finden Sie in den folgenden Themen:

-   [Systemzeit](system-time.md)
-   [Ortszeit](local-time.md)
-   [Dateizeiten](file-times.md)
-   [Datum und Uhrzeit von MS-DOS](ms-dos-date-and-time.md)
-   [Windows-Zeitdienst](windows-time.md)
-   [Interruptzeit](interrupt-time.md)

 

 
