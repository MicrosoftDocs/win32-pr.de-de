---
description: Verwenden Sie die Ereignisprotokollierung, um Fehler zu erfassen, die in der Leistungs-DLL auftreten.
ms.assetid: 61bc4fa1-8185-4e07-a3b5-4bd357f0f75a
title: Fehlerbehandlung in der DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a64dcfdf360a1dcc2301b5496d3f4630631cd7bfbc3fffb0e2cd5408120351
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517470"
---
# <a name="error-handling-in-the-dll"></a>Fehlerbehandlung in der DLL

Verwenden Sie die Ereignisprotokollierung, um Fehler zu erfassen, die in der Leistungs-DLL auftreten. Die Protokollierung von Fehlerereignissen hilft bei der Problembehandlung von Anwendungen, die während der Entwicklung und nach der Installation Leistungsdaten bereitstellen. Sie sollten die Menge der Fehlerprotokollierung begrenzen, die in der [**CollectPerformanceData-Funktion**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) auftritt, da die Datensammlung häufig erfolgen kann.

Das System protokolliert die folgenden Fehler im Ereignisprotokoll, wenn Probleme mit der [**OpenPerformanceData-Funktion**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) vorliegen. Wenn einer der folgenden Fehler auftritt, wird die Leistungs-DLL vom System nicht erneut aufruft. Stattdessen wird die DLL entladen.

-   **PERFLIB \_ OPEN \_ PROC \_ NOT \_ FOUND**– Wird protokolliert, wenn der in der Registrierung definierte Prozedurname in der DLL nicht als exportierte Funktion gefunden werden konnte. Dies tritt in der Regel auf, wenn die DLL oder der Dienst nicht ordnungsgemäß installiert ist oder der Funktionsname umbenannt wurde, ohne den Installationsvorgang zu aktualisieren.
-   **PERFLIB \_ OPEN \_ PROC \_ FAILURE –** Wird protokolliert, wenn die geöffnete Prozedur einen anderen Fehlerstatus als ERROR SUCCESS zurückgegeben \_ hat. In diesem Fall sollte die DLL auch einen Ereignisprotokolleintrag eingegeben haben, der die Bedingungen beschreibt, die den Fehler verursacht haben.
-   **PERFLIB \_ OPEN \_ PROC \_ EXCEPTION**– Wird protokolliert, wenn die geöffnete Prozedur auf eine nicht behandelte Ausnahme trifft. Dies liegt in der Regel an einem unerwarteten Fehlerzustand, der von der geöffneten Prozedur aufgetreten ist.

 

 
