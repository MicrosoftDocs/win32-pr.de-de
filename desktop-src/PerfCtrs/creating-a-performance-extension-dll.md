---
description: Ein Anbieter ist eine Leistungs-DLL, die Leistungsindikatordaten für Verbraucher zur Hand hat.
ms.assetid: bbb777fe-b97e-4777-b797-ec8525065610
title: Erstellen einer Leistungserweiterungs-DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1ef4509af77bcc1a4016e494a2834d40162305a837349e32a573cbf36d994d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011318"
---
# <a name="creating-a-performance-extension-dll"></a>Erstellen einer Leistungserweiterungs-DLL

> [!IMPORTANT]
> Aufgrund von erheblichen Leistungs- und Zuverlässigkeitseinschränkungen kann die In diesem Thema beschriebene Methode zum Bereitstellen von Leistungsindikatordaten in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft, die in Bereitstellen von Indikatordaten mit Version [2.0](providing-counter-data-using-version-2-0.md) beschriebene Methode zum Erstellen neuer Leistungsindikatoren zu verwenden und vorhandene Leistungsindikatoren zu migrieren, um diese Methode auch zu verwenden.

Ein [V1-Anbieter verwendet](providing-counter-data.md) eine Leistungs-DLL, die Leistungsindikatordaten für Verbraucher bietet. Die Leistungs-DLL muss die [**Funktionen OpenPerformanceData,**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)und [**ClosePerformanceData exportieren.**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) In der Regel verwenden Sie eine Moduldefinitionsdatei (DEF), um die Funktionen aus der DLL zu exportieren. Das System ruft diese Funktionen auf, wenn ein Consumer Leistungsdaten abfragt.

Wenn ein Consumer zum ersten Mal [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa)aufruft oder wenn der Consumer die [**RegOpenKey-**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) oder [**RegConnectRegistry-Funktion**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) zum Öffnen verwendet, ruft das System die `HKEY_PERFORMANCE_DATA` [**OpenPerformanceData-Funktion**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) für jeden Anbieter auf, der auf dem Computer registriert ist. [](adding-performance-counters.md) Die Ausnahme ist, wenn der Anbieter die Liste der Objekte angibt, die er im Abschnitt der .INI `[objects]` unterstützt. In diesem Fall ruft das System den Anbieter nur auf, wenn eines der abgefragten Objekte einem Objekt aus der Liste entspricht.

Die [**OpenPerformanceData-Funktion**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) bietet jedem Anbieter die Möglichkeit, seine Leistungsdatenstrukturen zu initialisieren. Wenn dann die **OpenPerformanceData-Funktion** erfolgreich zurückgegeben wird, ruft das System die [**CollectPerformanceData-Funktion**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) des Anbieters auf. Nachfolgende Aufrufe von [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) bewirken, dass das System die **CollectPerformanceData-Funktion** aufruft.

Wenn der Consumer das Sammeln von Leistungsdaten abgeschlossen hat, gibt er in einem Aufruf der `HKEY_PERFORMANCE_DATA` [**RegCloseKey-Funktion**](/windows/desktop/api/winreg/nf-winreg-regclosekey) an. Dies bewirkt, dass das System die [**ClosePerformanceData-Funktion**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) für jeden Anbieter aufruft. Die Anbieter werden dann entladen.

Es ist möglich, dass mehrere Benutzer gleichzeitig Leistungsdaten sammeln. Das System ruft [**die Funktionen OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) und [**ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) nur einmal auf, wenn die DLL geladen oder entladen wird.

> [!Note]
> Schließen Sie extern "C" in Ihren C++-Code ein, um zu verhindern, dass der Compiler Ihren Funktionsnamen Erweiterungen hinzufügung. Andernfalls kann das System Ihre Funktionen möglicherweise nicht finden.

> [!Note]
> Wenn beim Laden ihrer Leistungs-DLL, beim Suchen Ihrer Funktionen oder beim Aufrufen Ihrer Funktionen ein Fehler auftritt, deaktiviert das System den Anbieter für nachfolgende Sammlungen innerhalb desselben Prozesses. Wenn **dies** während der Ausführung in einem privilegierten Prozess auftritt, fügt  das System ihrem Leistungsschlüssel außerdem den Wert Leistungsindikatoren deaktivieren hinzu, um zu verhindern, dass der Anbieter in Zukunft geladen wird.

Weitere Informationen zum Schreiben einer Leistungs-DLL finden Sie in den folgenden Themen:

- [Implementieren der OpenPerformanceData-Funktion](implementing-openperformancedata.md)
- [Implementieren der CollectPerformanceData-Funktion](implementing-collectperformancedata.md)
- [Fehlerbehandlung in der DLL](error-handling-in-the-dll.md)
- [Einschränken des Zugriffs auf Leistungserweiterungs-DLLs](restricting-access-to-performance-extension--dlls.md)
- [Leistungs-DLL-Beispiele](performance-dll-samples.md)
