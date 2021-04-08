---
description: Verwenden Sie die Ereignisprotokollierung, um Fehler aufzuzeichnen, die in der Leistungs-dll auftreten.
ms.assetid: 61bc4fa1-8185-4e07-a3b5-4bd357f0f75a
title: Fehlerbehandlung in der dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd21f0b9338600012d65aa19801ee57794fac294
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959764"
---
# <a name="error-handling-in-the-dll"></a>Fehlerbehandlung in der dll

Verwenden Sie die Ereignisprotokollierung, um Fehler aufzuzeichnen, die in der Leistungs-dll auftreten. Das Protokollieren von Fehlerereignissen hilft bei der Problembehandlung bei Anwendungen, die während der Entwicklung und nach der Installation Leistungsdaten Sie sollten die Menge der Fehler Protokollierung einschränken, die in der [**collectperformancedata**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) -Funktion auftritt, da die Datensammlung häufig vorkommen kann.

Das System protokolliert die folgenden Fehler im Ereignisprotokoll, wenn Probleme mit der [**openperformancedata**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) -Funktion auftreten. Wenn einer der folgenden Fehler auftritt, ruft das System die Leistungs-DLL nicht erneut auf. Stattdessen wird die DLL entladen.

-   **Perflib \_ Die geöffnete Prozedur wurde \_ \_ nicht \_ gefunden**– wird protokolliert, wenn der in der Registrierung definierte Prozedur Name in der dll nicht als exportierte Funktion gefunden wurde. Dies tritt normalerweise auf, wenn die dll oder der Dienst nicht ordnungsgemäß installiert ist oder der Funktionsname umbenannt wurde, ohne die Installation zu aktualisieren.
-   **Perflib \_ Öffnen Sie den \_ proc \_**-Fehler – protokolliert, wenn die geöffnete Prozedur einen anderen Fehlerstatus als Fehler erfolgreich zurückgegeben hat \_ . Wenn dies der Fall ist, sollte die dll auch einen Ereignisprotokoll Eintrag eingegeben haben, der die Bedingungen beschreibt, die den Fehler verursacht haben.
-   **Perflib \_ Öffnen Sie \_ proc \_ Exception**– protokolliert, wenn bei der geöffneten Prozedur eine nicht behandelte Ausnahme auftritt. Dies ist normalerweise auf eine unerwartete Fehlerbedingung zurückzuführen, die in der geöffneten Prozedur aufgetreten ist.

 

 
