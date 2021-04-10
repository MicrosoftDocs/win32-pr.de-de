---
description: Bei einem Anbieter handelt es sich um eine Leistungs-DLL, die für Consumer Leistungsdaten liefert.
ms.assetid: bbb777fe-b97e-4777-b797-ec8525065610
title: Erstellen einer Leistungs Erweiterungs-DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d397f1581454aca1b25c447b35f250eefd215f57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865124"
---
# <a name="creating-a-performance-extension-dll"></a>Erstellen einer Leistungs Erweiterungs-DLL

> [!IMPORTANT]
> Aufgrund erheblicher Leistungs-und Zuverlässigkeits Beschränkungen ist die Methode zum Bereitstellen von Leistungsdaten, die in diesem Thema beschrieben werden, möglicherweise in Zukunft geändert oder nicht verfügbar. Stattdessen empfiehlt Microsoft die Verwendung der unter [Bereitstellen von Indikator Daten mit Version 2,0](providing-counter-data-using-version-2-0.md) beschriebenen Methode zum Erstellen neuer Leistungsindikatoren und die Migration vorhandener Leistungsindikatoren zur Verwendung dieser Methode.

Ein [v1-Anbieter](providing-counter-data.md) verwendet eine Leistungs-DLL, die Leistungsdaten für Consumer bereitstellt. Die Leistungs-DLL muss die [**openperformancedata**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))-, [**collectperformancedata**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)-und [**closeperformancedata**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) -Funktionen exportieren. In der Regel verwenden Sie eine Modul Definitionsdatei (. def), um die Funktionen aus der dll zu exportieren. Das System ruft diese Funktionen auf, wenn ein Consumer Leistungsdaten abfragt.

Wenn ein Consumer zum ersten Mal [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa)aufruft oder der Consumer die [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) -oder [**regconnectregistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) -Funktion zum Öffnen verwendet `HKEY_PERFORMANCE_DATA` , ruft das System die [**openperformancedata**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) -Funktion für jeden Anbieter auf, der auf dem Computer [registriert](adding-performance-counters.md) ist. Die Ausnahme ist, wenn der Anbieter die Liste der Objekte angibt, die er im- `[objects]` Abschnitt von unterstützt. INI-Datei. In diesem Fall ruft das System den Anbieter nur auf, wenn eines der abgefragten Objekte mit einem Objekt aus der Liste übereinstimmt.

Die [**openperformancedata**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) -Funktion gibt allen Anbietern die Möglichkeit, die Leistungsdaten Strukturen zu initialisieren. Wenn die **openperformancedata** -Funktion erfolgreich zurückgegeben wird, ruft das System die [**collectperformancedata**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) -Funktion des Anbieters auf. Nachfolgende Aufrufe von [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) bewirken, dass das System die **collectperformancedata** -Funktion aufruft.

Wenn der Consumer die Erfassung von Leistungsdaten abschließt, wird `HKEY_PERFORMANCE_DATA` in einem Rückruf der [**RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey) -Funktion angegeben. Dies bewirkt, dass das System die [**closeperformancedata**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) -Funktion für jeden Anbieter aufruft. Die Anbieter werden dann entladen.

Es ist möglich, dass mehrere Consumer gleichzeitig Leistungsdaten sammeln. Das System ruft [**openperformancedata**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) -und [**closeperformancedata**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) -Funktionen nur einmal auf, wenn die dll geladen oder entladen wird.

> [!Note]
> Stellen Sie sicher, dass Sie extern "C" in Ihren C++-Code einschließen, um zu verhindern, dass der Compiler ihren Funktionsnamen Dekorationen hinzufügt. Andernfalls kann das System die Funktionen nicht finden.

> [!Note]
> Wenn beim Laden der Leistungs-DLL, beim Suchen der Funktionen oder beim Aufrufen der Funktionen ein Fehler auftritt, wird der Anbieter für nachfolgende Auflistungen innerhalb desselben Prozesses vom System deaktiviert. Wenn dieses Problem bei der Ausführung in einem privilegierten Prozess auftritt, fügt das System den Leistungsindikator " **Leistungsindikatoren deaktivieren** " dem **Leistungs** Schlüssel hinzu, um zu verhindern, dass der Anbieter in Zukunft geladen wird.

Weitere Informationen zum Schreiben einer Leistungs-dll finden Sie in den folgenden Themen:

- [Implementieren der openperformancedata-Funktion](implementing-openperformancedata.md)
- [Implementieren der collectperformancedata-Funktion](implementing-collectperformancedata.md)
- [Fehlerbehandlung in der dll](error-handling-in-the-dll.md)
- [Einschränken des Zugriffs auf Leistungs Erweiterungs-DLLs](restricting-access-to-performance-extension--dlls.md)
- [Leistungs-DLL-Beispiele](performance-dll-samples.md)
