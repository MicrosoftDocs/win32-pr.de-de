---
description: WMI-C++ Klassen, die Teil des WMI-Anbieter-Frameworks sind, werden nicht mehr zur Verwendung empfohlen.
ms.assetid: d2414a72-3435-4035-bcd9-b3ec87f5709c
ms.tgt_platform: multiple
title: Anbieter Framework-Hilfsprogrammklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab09c99fe2597cacd81e55a4ed18bd4e286ff16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352741"
---
# <a name="provider-framework-utility-classes"></a>Anbieter Framework-Hilfsprogrammklassen

\[WMI-C++-Klassen, die Teil des WMI-Anbieter-Frameworks sind und nun im Endzustand berücksichtigt werden, und keine weiteren Entwicklungen, Verbesserungen oder Updates sind für nicht sicherheitsrelevante Probleme verfügbar, die diese Bibliotheken betreffen. Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Die Anbieter Framework-Bibliotheken Framedyd.dll (Debugversion) und Framedyn.dll (Releaseversion) implementieren mehrere Anbieter-Hilfsklassen. Einige Funktionen in Framedyn.dll wurden aus den Header Dateien entfernt. Um diese Funktionen weiterhin zu verwenden, fügen Sie `#define FRAMEWORK_ALLOW_DEPRECATED` Ihrem Code hinzu, bevor Sie fwcommon. h einschließen.

Sie können einzelne Anbieter entladen, die nicht mehr benötigt werden.

Um diese Funktion verwenden zu können, müssen Sie die drei folgenden Änderungen am Anbieter in "maindll. cpp" vornehmen:

-   In der **DllMain** -Funktion, in der Sie [**cwbemproviderglue:: frameworklogindll**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong))aufrufen, müssen Sie einen zweiten Parameter hinzufügen, der ein Zeiger auf einen Long-Wert ist.
-   In der **DllCanUnloadNow** -Funktion, in der Sie [**cwbemproviderglue:: frameworklogoffdll**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong))aufrufen, müssen Sie einen zweiten Parameter hinzufügen, der ein Zeiger auf einen Long-Wert ist.
-   In der **DllGetClassObject** -Funktion, in der Sie eine Instanz von **cwbemgluefactory** erstellen, müssen Sie einen Parameter hinzufügen, der ein Zeiger auf einen Long-Wert ist.

In allen drei Fällen muss der Zeiger auf einen Long-Zeiger gleich sein.

> [!Note]  
> In "maindll. cpp" müssen die Routinen **DllGetClassObject**, **DllCanUnloadNow**, **DllRegisterServer**, **DllUnregisterServer** und **DllMain** in einem try/catch-Block eingeschlossen werden.

 

> [!Caution]  
> Anbieter-Debugbuilds sind für Framedyd.dll mit "framedyd. lib" verknüpft. Framedyd.dll befindet sich im bin-Verzeichnis von Microsoft Windows Software Development Kit (SDK) \\ , das nicht im Systempfad enthalten ist. Wenn ein Debugbuild eines Anbieters mit dem Windows-Verwaltungsdienst getestet wird, kann der frameworkanbieter nicht geladen werden, da Framedyd.dll oder eine seiner Abhängigkeiten nicht gefunden wird. Daher müssen Sie entweder Framedyd.dll aus dem Verzeichnis "Windows SDK \\ bin" in das \\ Verzeichnis "System32 \\ WBEM" Kopieren oder das Windows SDK \\ bin-Verzeichnis dem System Suchpfad hinzufügen.

 

In der folgenden Tabelle sind die Anbieter Framework-Dienstprogramm Klassen aufgeführt.



| Utility-Klasse                                          | BESCHREIBUNG                                                                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**Zeichenfolge**](chstring.md)                           | Stellt Zeichen folgen Vergleichs-und Bearbeitungsfunktionen für WMI bereit.                                                                  |
| [**Chstringarray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray)                 | Enthält zum Erstellen und Bearbeiten von Zeichen folgen Arrays.                                                                      |
| [**Treberpointercollection**](/windows/desktop/api/RefPtrCo/nl-refptrco-trefpointercollection) | Gewährt den Zugriff auf eine Container Klasse für Zeiger.                                                                                |
| [**Wbemtime**](wbemtime.md)                           | Ermöglicht Konvertierungen zwischen verschiedenen Windows-und ANSI C-Lauf Zeitformaten.                                               |
| [**Wbemtimespan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan)                   | Enthält Hilfsfunktionen, die verwendet werden, um den Zeitspannen Unterschied zwischen zwei [**wbemtime**](wbemtime.md) -Objekten zu berechnen und zu speichern. |



 

> [!Note]  
> Die Klassen " [**chstring**](chstring.md) " und " [**chstringarray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) " ähneln den Microsoft Foundation Classes (MFC) " **CString** " und " **cstringarray**". Die WMI-Versionen sind vorhanden, damit Entwickler auf Zeichen folgen Manipulation und Vergleichsmethoden zugreifen können, ohne auf MFC zugreifen zu müssen. Die Klassen [**wbemtime**](wbemtime.md) und [**wbemtimespan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) ähneln auch den Klassen MFC **ctime** und **CTimeSpan** . Die WMI-Versionen können Zeit bis zur Nanosekunden-Genauigkeit speichern und können auch in und aus **BSTR** konvertieren. Weitere Informationen zu den Klassen CString, cstringarray, ctime und CTimeSpan finden Sie in der [Microsoft Foundation Classes](https://msdn.microsoft.com/library/d06h2x6e(VS.71).aspx) auf MSDN.

 

Von [**wbemtime**](wbemtime.md) -Methoden zurückgegebene **BSTR** -Werte weisen das [Datums-und Uhrzeit Format](date-and-time-format.md)auf: "YYYYMMDDHHMMSS. mmmmmmsUUU"

Von [**wbemtimespan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) -Methoden zurückgegebene **BSTR** -Werte liegen im [Intervall Format](interval-format.md)vor: "ddddddddhhmmss. mmmmmm: 000"

Obwohl Zeiten und Zeitspannen intern als Nanosekunden gespeichert werden, werden Sie nicht notwendigerweise mit der Nanosekunden-Genauigkeit gespeichert. Dies liegt daran, dass [**wbemtime**](wbemtime.md) -Objekte mit Zeitformaten erstellt werden können, die auf eine Sekunde (**struct tm** und **time \_ t**) zutreffen. Durch das Hinzufügen künstlicher Dezimalstellen wird die Genauigkeit nicht erhöht.

 

 
