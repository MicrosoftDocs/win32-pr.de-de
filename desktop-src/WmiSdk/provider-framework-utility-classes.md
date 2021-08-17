---
description: WMI-C++-Klassen, die Teil des WMI-Anbieterframework sind, werden nicht mehr für die Verwendung empfohlen.
ms.assetid: d2414a72-3435-4035-bcd9-b3ec87f5709c
ms.tgt_platform: multiple
title: Anbieterframework-Hilfsprogrammklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 254a1321ab835c86e7b4bf0e5cb14048be0352290707a61aaf993a9a6cc6e8dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130982"
---
# <a name="provider-framework-utility-classes"></a>Anbieterframework-Hilfsprogrammklassen

\[WMI-C++-Klassen, die Teil des WMI-Anbieterframework sind, das jetzt im endgültigen Zustand betrachtet wird, und keine weiteren Entwicklungen, Erweiterungen oder Updates für nicht sich sicherheitsbezogene Probleme, die diese Bibliotheken betreffen, verfügbar sind. Die [MI-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Die Frameworkbibliotheken des Anbieters Framedyd.dll (Debugversion) und Framedyn.dll (Releaseversion) implementieren mehrere Anbieter-Hilfsklassen. Einige Funktionen in Framedyn.dll aus den Headerdateien entfernt. Um diese Funktionen weiterhin zu verwenden, fügen Sie `#define FRAMEWORK_ALLOW_DEPRECATED` dem Code hinzu, bevor Sie Fwcommon.h hinzufügen.

Sie können einzelne Anbieter entladen, die nicht mehr benötigt werden.

Um diese Funktion verwenden zu können, müssen Sie die drei folgenden Änderungen an Ihrem Anbieter in MainDll.cpp vornehmen:

-   In der **DllMain-Funktion,** in der [**Sie CWbemProviderGlue::FrameworkLoginDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong))aufrufen, müssen Sie einen zweiten Parameter hinzufügen, der ein Zeiger auf ein long-Objekt ist.
-   In der **DllCanUnloadNow-Funktion,** in der [**Sie CWbemProviderGlue::FrameworkLogoffDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong))aufrufen, müssen Sie einen zweiten Parameter hinzufügen, bei dem es sich um einen Zeiger auf einen long handelt.
-   In der **DllGetClassObject-Funktion,** in der Sie eine Instanz von **CWbemGlueFactory** erstellen, müssen Sie einen Parameter hinzufügen, der ein Zeiger auf ein long-Objekt ist.

In allen drei Fällen muss der Zeiger auf einen long-Zeiger identisch sein.

> [!Note]  
> In maindll.cpp müssen **die Routinen "DllGetClassObject",** **"DllCanUnloadNow",** **"DllRegisterServer",** **"DllUnregisterServer"** und **"DllMain"** in einen try/catch-Block umschlossen werden.

 

> [!Caution]  
> Der Debugbuildlink des Anbieters mit Framedyd.lib Framedyd.dll. Framedyd.dll befindet sich im Bin-Verzeichnis des Microsoft Windows Software Development Kit \\ (SDK), das nicht im Systempfad enthalten ist. Wenn ein Debugbuild eines Anbieters mit dem Windows Management-Dienst getestet wird, kann der Frameworkanbieter nicht geladen werden, da Framedyd.dll oder eine seiner Abhängigkeiten nicht gefunden wird. Daher müssen Sie entweder Framedyd.dll aus dem bin-Verzeichnis des Windows SDK in das \\ \\ Verzeichnis system32 wbem kopieren oder dem Systemsuchpfad das verzeichnis Windows \\ SDK \\ bin hinzufügen.

 

In der folgenden Tabelle sind die Anbieterframework-Hilfsprogrammklassen aufgeführt.



| Hilfsprogrammklasse                                          | Beschreibung                                                                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**CHString**](chstring.md)                           | Stellt Zeichenfolgenvergleichs- und Bearbeitungsfunktionen für WMI zur Verfügung.                                                                  |
| [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray)                 | Enthält zum Erstellen und Bearbeiten von ARRAYS von CHString.                                                                      |
| [**TRefPointerCollection**](/windows/desktop/api/RefPtrCo/nl-refptrco-trefpointercollection) | Gewährt Zeigern Zugriff auf eine Containerklasse.                                                                                |
| [**WBEMTime**](wbemtime.md)                           | Erleichtert Konvertierungen zwischen verschiedenen Windows und ANSI C-Laufzeitformaten.                                               |
| [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan)                   | Enthält Hilfsfunktionen, die verwendet werden, um die Zeitspannendifferenz zwischen zwei [**WBEMTime-Objekten zu**](wbemtime.md) berechnen und zu halten. |



 

> [!Note]  
> Die [**Klassen CHString**](chstring.md) und [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) ähneln den **CString-** und **CStringArray-Klassen** Microsoft Foundation Classes (MFC). Die WMI-Versionen sind vorhanden, sodass Entwickler auf Zeichenfolgenbearbeitungs- und Vergleichsmethoden zugreifen können, ohne auf MFC zugreifen zu müssen. Die [**Klassen WBEMTime**](wbemtime.md) und [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) ähneln auch den Klassen MFC **CTime** und **CTimeSpan.** Die WMI-Versionen sind in der Lage, die Genauigkeit von Zeit bis Nanosekunden zu speichern, und können auch in und aus **BSTR konvertieren.** Weitere Informationen zu den Klassen CString, CStringArray, CTime und CTimeSpan finden Sie Microsoft Foundation Classes [MSDN.](https://msdn.microsoft.com/library/d06h2x6e(VS.71).aspx)

 

Von [**WBEMTime-Methoden**](wbemtime.md) zurückgegebene **BSTR-Werte** liegen im Datums- und [Uhrzeitformat](date-and-time-format.md)vor: "yyyymmddHHMMSS.mmmmmmsUUU".

Von [**WBEMTimeSpan-Methoden**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) zurückgegebene **BSTR-Werte** liegen im [Intervallformat](interval-format.md)vor: "dddddddHHMMSS.mmmmmm:000"

Obwohl Zeiten und Zeitspannen intern als Nanosekunden gespeichert werden, werden sie nicht unbedingt mit Nanosekundengenauigkeit gespeichert. Dies liegt [**daran, dass WBEMTime-Objekte**](wbemtime.md) mit Zeitformaten erstellt werden können, die auf eine Sekunde genau sind (**struct tm** und **time \_ t**). Das Hinzufügen künstlicher Dezimalstellen erhöht die Genauigkeit nicht.

 

 
