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
# <a name="error-handling-in-the-dll"></a><span data-ttu-id="e0698-103">Fehlerbehandlung in der dll</span><span class="sxs-lookup"><span data-stu-id="e0698-103">Error Handling in the DLL</span></span>

<span data-ttu-id="e0698-104">Verwenden Sie die Ereignisprotokollierung, um Fehler aufzuzeichnen, die in der Leistungs-dll auftreten.</span><span class="sxs-lookup"><span data-stu-id="e0698-104">Use event logging to record errors that occur in the performance DLL.</span></span> <span data-ttu-id="e0698-105">Das Protokollieren von Fehlerereignissen hilft bei der Problembehandlung bei Anwendungen, die während der Entwicklung und nach der Installation Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="e0698-105">Logging error events aids in troubleshooting applications that provide performance data during development and after installation.</span></span> <span data-ttu-id="e0698-106">Sie sollten die Menge der Fehler Protokollierung einschränken, die in der [**collectperformancedata**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) -Funktion auftritt, da die Datensammlung häufig vorkommen kann.</span><span class="sxs-lookup"><span data-stu-id="e0698-106">You should limit the amount of error logging that occurs in the [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) function because data collection can be frequent.</span></span>

<span data-ttu-id="e0698-107">Das System protokolliert die folgenden Fehler im Ereignisprotokoll, wenn Probleme mit der [**openperformancedata**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) -Funktion auftreten.</span><span class="sxs-lookup"><span data-stu-id="e0698-107">The system logs the following errors to the event log if there are problems with the [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function.</span></span> <span data-ttu-id="e0698-108">Wenn einer der folgenden Fehler auftritt, ruft das System die Leistungs-DLL nicht erneut auf.</span><span class="sxs-lookup"><span data-stu-id="e0698-108">If one of the following errors occurs, the system does not call the performance DLL again.</span></span> <span data-ttu-id="e0698-109">Stattdessen wird die DLL entladen.</span><span class="sxs-lookup"><span data-stu-id="e0698-109">Instead, the DLL is unloaded.</span></span>

-   <span data-ttu-id="e0698-110">**Perflib \_ Die geöffnete Prozedur wurde \_ \_ nicht \_ gefunden**– wird protokolliert, wenn der in der Registrierung definierte Prozedur Name in der dll nicht als exportierte Funktion gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="e0698-110">**PERFLIB\_OPEN\_PROC\_NOT\_FOUND**—Logged when the procedure name defined in the registry could not be found in the DLL as an exported function.</span></span> <span data-ttu-id="e0698-111">Dies tritt normalerweise auf, wenn die dll oder der Dienst nicht ordnungsgemäß installiert ist oder der Funktionsname umbenannt wurde, ohne die Installation zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e0698-111">This usually occurs when the DLL or the service is not installed correctly or the function name has been renamed without updating the installation procedure.</span></span>
-   <span data-ttu-id="e0698-112">**Perflib \_ Öffnen Sie den \_ proc \_**-Fehler – protokolliert, wenn die geöffnete Prozedur einen anderen Fehlerstatus als Fehler erfolgreich zurückgegeben hat \_ .</span><span class="sxs-lookup"><span data-stu-id="e0698-112">**PERFLIB\_OPEN\_PROC\_FAILURE**—Logged when the open procedure returned an error status other than ERROR\_SUCCESS.</span></span> <span data-ttu-id="e0698-113">Wenn dies der Fall ist, sollte die dll auch einen Ereignisprotokoll Eintrag eingegeben haben, der die Bedingungen beschreibt, die den Fehler verursacht haben.</span><span class="sxs-lookup"><span data-stu-id="e0698-113">Should this happen, the DLL should have also entered an event log entry describing the conditions that caused the failure.</span></span>
-   <span data-ttu-id="e0698-114">**Perflib \_ Öffnen Sie \_ proc \_ Exception**– protokolliert, wenn bei der geöffneten Prozedur eine nicht behandelte Ausnahme auftritt.</span><span class="sxs-lookup"><span data-stu-id="e0698-114">**PERFLIB\_OPEN\_PROC\_EXCEPTION**—Logged when the open procedure encounters an unhandled exception.</span></span> <span data-ttu-id="e0698-115">Dies ist normalerweise auf eine unerwartete Fehlerbedingung zurückzuführen, die in der geöffneten Prozedur aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e0698-115">This is usually due to an unexpected error condition encountered by the open procedure.</span></span>

 

 
