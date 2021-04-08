---
title: Registrieren einer Hook-Funktion
description: Client Anwendungen empfangen WinEvents in einer wineventproc-Rückruffunktion. Die von der Rückruffunktion ausgeführten Aktionen werden von der Anwendung definiert, aber die Syntax muss wie im Prototyp angegeben angegeben werden.
ms.assetid: 7e999335-6a41-4d22-82ef-1a8dd6cb656e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b1f39a535b366af72b1034cc9344171d253ea0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855779"
---
# <a name="registering-a-hook-function"></a><span data-ttu-id="90379-104">Registrieren einer Hook-Funktion</span><span class="sxs-lookup"><span data-stu-id="90379-104">Registering a Hook Function</span></span>

<span data-ttu-id="90379-105">Client Anwendungen empfangen WinEvents in einer [*wineventproc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) -Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="90379-105">Client applications receive WinEvents in a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function.</span></span> <span data-ttu-id="90379-106">Die von der Rückruffunktion ausgeführten Aktionen werden von der Anwendung definiert, aber die Syntax muss wie im Prototyp angegeben angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="90379-106">The actions performed by the callback function are defined by the application, but the syntax must be as specified in the prototype.</span></span>

<span data-ttu-id="90379-107">Bevor Ereignisse empfangen werden können, muss die Funktion durch Aufrufen von [**setwineventhook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)registriert werden.</span><span class="sxs-lookup"><span data-stu-id="90379-107">Before it can receive events, the function must be registered by calling [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook).</span></span> <span data-ttu-id="90379-108">Der Client kann **setwineventhook** mehrmals aufrufen, um unterschiedliche Hook-Funktionen zu registrieren oder zusätzliche Ereignisse für eine zuvor registrierte Hook-Funktion festzulegen.</span><span class="sxs-lookup"><span data-stu-id="90379-108">The client can call **SetWinEventHook** more than once to register different hook functions, or to set additional events for a previously registered hook function.</span></span>

<span data-ttu-id="90379-109">Beim Aufrufen von [**setwineventhook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) gibt der Client an, welche Ereignisse empfangen werden sollen und wie diese empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="90379-109">When calling [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) the client specifies which events to receive and how to receive them.</span></span> <span data-ttu-id="90379-110">Der Client kann Folgendes auswählen:</span><span class="sxs-lookup"><span data-stu-id="90379-110">The client can choose to:</span></span>

-   <span data-ttu-id="90379-111">Empfangen Sie alle Ereignisse oder einen bestimmten Satz von Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="90379-111">Receive all events or a specific set of events.</span></span>
-   <span data-ttu-id="90379-112">Empfangen von Ereignissen von allen Threads oder von einem bestimmten Thread.</span><span class="sxs-lookup"><span data-stu-id="90379-112">Receive events from all threads or from a specific thread.</span></span>
-   <span data-ttu-id="90379-113">Empfangen von Ereignissen von allen Prozessen oder von einem bestimmten Prozess.</span><span class="sxs-lookup"><span data-stu-id="90379-113">Receive events from all processes or from a specific process.</span></span>
-   <span data-ttu-id="90379-114">Behandeln von Ereignissen in Prozessen oder außerhalb des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="90379-114">Handle events in process or out of process.</span></span>

<span data-ttu-id="90379-115">Wenn ein Ereignis generiert wird, das den angegebenen Kriterien entspricht, ruft das System die [*wineventproc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) -Rückruffunktion (oder "Hook Procedure") des Clients auf.</span><span class="sxs-lookup"><span data-stu-id="90379-115">When an event is generated that matches the specified criteria, the system calls the client's [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function (or "hook procedure").</span></span> <span data-ttu-id="90379-116">Die Parameter, die die Hook-Funktion empfängt, informieren den Client über das Fenster, das Objekt und das mögliche untergeordnete Element, das das Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="90379-116">The parameters that the hook function receives tell the client about the window, object, and possible child element that generated the event.</span></span> <span data-ttu-id="90379-117">Ein Client verwendet diese Parameter in einem Objekt Abruf Aufrufs, z. [**b. accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span><span class="sxs-lookup"><span data-stu-id="90379-117">A client uses these parameters in an object retrieval call, such as [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span></span>

 

 




