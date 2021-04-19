---
description: Alle Benutzer haben Lesezugriff auf die Liste der Prozesse im System, und es gibt eine Reihe verschiedener Funktionen, mit denen die aktiven Prozesse aufgelistet werden. Die Funktion, die Sie verwenden sollten, hängt von Faktoren wie der Unterstützung gewünschter Plattformen ab.
ms.assetid: 4c73fb10-7ee8-4d8a-9cdb-a2ae59aef5bd
title: Process-Enumeration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911d11a50e898656b56fe89001811b939473c2e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358446"
---
# <a name="process-enumeration"></a><span data-ttu-id="e04ef-104">Process-Enumeration</span><span class="sxs-lookup"><span data-stu-id="e04ef-104">Process Enumeration</span></span>

<span data-ttu-id="e04ef-105">Alle Benutzer haben Lesezugriff auf die Liste der Prozesse im System, und es gibt eine Reihe verschiedener Funktionen, mit denen die aktiven Prozesse aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="e04ef-105">All users have read access to the list of processes in the system and there are a number of different functions that enumerate the active processes.</span></span> <span data-ttu-id="e04ef-106">Die Funktion, die Sie verwenden sollten, hängt von Faktoren wie der Unterstützung gewünschter Plattformen ab.</span><span class="sxs-lookup"><span data-stu-id="e04ef-106">The function you should use will depend on factors such as desired platform support.</span></span>

<span data-ttu-id="e04ef-107">Die folgenden Funktionen werden zum Auflisten von Prozessen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e04ef-107">The following functions are used to enumerate processes.</span></span>



| <span data-ttu-id="e04ef-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="e04ef-108">Function</span></span>                                                    | <span data-ttu-id="e04ef-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e04ef-109">Description</span></span>                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="e04ef-110">**EnumProcesses**</span><span class="sxs-lookup"><span data-stu-id="e04ef-110">**EnumProcesses**</span></span>](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | <span data-ttu-id="e04ef-111">Ruft den Prozess Bezeichner für jedes Prozess Objekt im System ab.</span><span class="sxs-lookup"><span data-stu-id="e04ef-111">Retrieves the process identifier for each process object in the system.</span></span>            |
| [<span data-ttu-id="e04ef-112">**Process32First**</span><span class="sxs-lookup"><span data-stu-id="e04ef-112">**Process32First**</span></span>](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | <span data-ttu-id="e04ef-113">Ruft Informationen zum ersten Prozess ab, der in einer System Momentaufnahme aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e04ef-113">Retrieves information about the first process encountered in a system snapshot.</span></span>    |
| [<span data-ttu-id="e04ef-114">**Process32Next**</span><span class="sxs-lookup"><span data-stu-id="e04ef-114">**Process32Next**</span></span>](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | <span data-ttu-id="e04ef-115">Ruft Informationen zum nächsten Prozess ab, der in einer System Momentaufnahme aufgezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="e04ef-115">Retrieves information about the next process recorded in a system snapshot.</span></span>        |
| [<span data-ttu-id="e04ef-116">**Wtsenum erateprocesses**</span><span class="sxs-lookup"><span data-stu-id="e04ef-116">**WTSEnumerateProcesses**</span></span>](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | <span data-ttu-id="e04ef-117">Ruft Informationen zu den aktiven Prozessen auf dem angegebenen Terminal Server ab.</span><span class="sxs-lookup"><span data-stu-id="e04ef-117">Retrieves information about the active processes on the specified terminal server.</span></span> |



 

<span data-ttu-id="e04ef-118">Die toolhelp-Funktionen [](/windows/win32/api/psapi/nf-psapi-enumprocesses) und enumerationsenumerationsenumerieren alle Prozesse.</span><span class="sxs-lookup"><span data-stu-id="e04ef-118">The toolhelp functions and [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) enumerate all process.</span></span> <span data-ttu-id="e04ef-119">Zum Auflisten der Prozesse, die in einem bestimmten Benutzerkonto ausgeführt werden, verwenden Sie [**wtsenumerateprocesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) und Filtern die Benutzer-SID.</span><span class="sxs-lookup"><span data-stu-id="e04ef-119">To list the processes that are running in a specific user account, use [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) and filter on the user SID.</span></span> <span data-ttu-id="e04ef-120">Sie können nach der Sitzungs-ID filtern, um Prozesse auszublenden, die in anderen Terminal Server Sitzungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e04ef-120">You can filter on the session ID to hide processes running in other terminal server sessions.</span></span>

<span data-ttu-id="e04ef-121">Sie können Prozesse unabhängig von der Enumerationsfunktion auch nach Benutzerkonto filtern, indem Sie [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess), [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)und [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) mit **tokenuser** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e04ef-121">You can also filter processes by user account, regardless of the enumeration function, by calling [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess), [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken), and [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) with **TokenUser**.</span></span> <span data-ttu-id="e04ef-122">Es ist jedoch nicht möglich, einen Prozess zu öffnen, der durch eine Sicherheits Beschreibung geschützt ist, es sei denn, Ihnen wurde der Zugriff gewährt.</span><span class="sxs-lookup"><span data-stu-id="e04ef-122">However, you cannot open a process that is protected by a security descriptor unless you have been granted access.</span></span>

 

 
