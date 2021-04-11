---
description: Windows Sockets 2 unterstützt weiterhin alle Semantik-und Funktionsaufrufe von Windows Sockets 1,1, mit Ausnahme derjenigen, die mit der Pseudo Blockierung arbeiten.
ms.assetid: e4dc4019-d421-49b8-825a-faa6d5f5fcae
title: Windows Sockets-Kompatibilitätsprobleme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495db7ff504b68d0db41104fe0fff79b93f985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214989"
---
# <a name="windows-sockets-compatibility-issues"></a><span data-ttu-id="86447-103">Windows Sockets-Kompatibilitätsprobleme</span><span class="sxs-lookup"><span data-stu-id="86447-103">Windows Sockets Compatibility Issues</span></span>

<span data-ttu-id="86447-104">Windows Sockets 2 unterstützt weiterhin alle Semantik-und Funktionsaufrufe von Windows Sockets 1,1, mit Ausnahme derjenigen, die mit der Pseudo Blockierung arbeiten.</span><span class="sxs-lookup"><span data-stu-id="86447-104">Windows Sockets 2 continues to support all of the Windows Sockets 1.1 semantics and function calls except for those dealing with pseudo-blocking.</span></span> <span data-ttu-id="86447-105">Da Windows Sockets 2 nur in den in 32-Bit-Umgebungen, in der voremptiv geplanten Umgebungen, ausgeführt wird, ist es nicht erforderlich, die in Windows Sockets 1,1 gefundene Pseudo Blockierung zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="86447-105">Since Windows Sockets 2 runs only in 32-bit, preemptively scheduled environments, there is no need to implement the pseudo-blocking found in Windows Sockets 1.1.</span></span> <span data-ttu-id="86447-106">Dies bedeutet, dass der wsaan Progress-Fehlercode nie angezeigt wird und dass die folgenden Windows Sockets 1,1-Funktionen für Windows Sockets 2-Anwendungen nicht verfügbar sind:</span><span class="sxs-lookup"><span data-stu-id="86447-106">This means that the WSAEINPROGRESS error code will never be indicated and that the following Windows Sockets 1.1 functions are not available to Windows Sockets 2 applications:</span></span>

-   <span data-ttu-id="86447-107">Wsacancelblockingcall</span><span class="sxs-lookup"><span data-stu-id="86447-107">WSACancelBlockingCall</span></span>
-   <span data-ttu-id="86447-108">Wsais-Blockierung</span><span class="sxs-lookup"><span data-stu-id="86447-108">WSAIsBlocking</span></span>
-   <span data-ttu-id="86447-109">Wsasetblockinghook</span><span class="sxs-lookup"><span data-stu-id="86447-109">WSASetBlockingHook</span></span>
-   <span data-ttu-id="86447-110">Wsaunhuokblockinghook</span><span class="sxs-lookup"><span data-stu-id="86447-110">WSAUnhookBlockingHook</span></span>

<span data-ttu-id="86447-111">Windows Sockets 1,1-Programme, die zur Verwendung von Pseudo Blockierungen geschrieben werden, funktionieren weiterhin ordnungsgemäß, da Sie mit Winsock.dll oder Wsock32.dll verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="86447-111">Windows Sockets 1.1 programs that are written to utilize pseudo-blocking will continue to operate correctly since they link to either Winsock.dll or Wsock32.dll.</span></span> <span data-ttu-id="86447-112">Beide unterstützen weiterhin den kompletten Satz von Windows Sockets 1,1-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="86447-112">Both continue to support the complete set of Windows Sockets 1.1 functions.</span></span> <span data-ttu-id="86447-113">Damit Programme zu Windows Sockets 2-Anwendungen werden können, muss eine Änderung des Codes erfolgen.</span><span class="sxs-lookup"><span data-stu-id="86447-113">In order for programs to become Windows Sockets 2 applications, some code modification must occur.</span></span> <span data-ttu-id="86447-114">In den meisten Fällen kann die kluge Verwendung von Threads durch die Verarbeitung der Verarbeitung ersetzt werden, die mit einer blockierenden Hook-Funktion erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="86447-114">In most cases, the judicious use of threads can be substituted to accommodate processing that was being accomplished with a blocking hook function.</span></span>

 

 



