---
description: Fehler Isolation und FailFast-Richtlinie
ms.assetid: 219c417c-a8a1-49eb-bc5a-702a16994d66
title: Fehler Isolation und FailFast-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc097a6d45f10d4ef8a8d059b1376862edd785ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523432"
---
# <a name="fault-isolation-and-failfast-policy"></a><span data-ttu-id="9a26e-103">Fehler Isolation und FailFast-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="9a26e-103">Fault Isolation and Failfast Policy</span></span>

<span data-ttu-id="9a26e-104">Com+ führt umfassende interne Integritäts-und Konsistenzprüfungen durch.</span><span class="sxs-lookup"><span data-stu-id="9a26e-104">COM+ performs extensive internal integrity and consistency checks.</span></span> <span data-ttu-id="9a26e-105">Wenn com+ eine unerwartete interne Fehlerbedingung feststellt, wird der Prozess sofort beendet.</span><span class="sxs-lookup"><span data-stu-id="9a26e-105">If COM+ encounters an unexpected internal error condition, it immediately terminates the process.</span></span> <span data-ttu-id="9a26e-106">Diese Richtlinie mit dem Namen " *FailFast*" vereinfacht die Fehler Aufnahme und führt zu zuverlässigeren und robusten Systemen.</span><span class="sxs-lookup"><span data-stu-id="9a26e-106">This policy, called *failfast*, facilitates fault containment and results in more reliable and robust systems.</span></span>

<span data-ttu-id="9a26e-107">Stellen Sie sich einen Fall vor, in dem com+ erkennt, dass eine der Datenstrukturen in einem beschädigten Zustand ist.</span><span class="sxs-lookup"><span data-stu-id="9a26e-107">Consider a case in which COM+ detects that one of its data structures is in a corrupted state.</span></span> <span data-ttu-id="9a26e-108">An diesem Punkt sind sowohl die Ursache als auch die Größe der Beschädigung unbekannt, sodass com+ leider nicht erkennen kann, wie weit sich der Schaden verbreitet hat.</span><span class="sxs-lookup"><span data-stu-id="9a26e-108">At this point, both the cause and the magnitude of the corruption are unknown and, unfortunately, COM+ cannot tell how far the damage has spread.</span></span> <span data-ttu-id="9a26e-109">Obwohl com+ sich in einem unbestimmten Zustand befindet, wird es jedoch nicht isoliert ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a26e-109">However, even though COM+ is in an indeterminate state, it does not run in isolation.</span></span> <span data-ttu-id="9a26e-110">Wie andere DLLs werden Sie in einer Prozessumgebung gehostet und teilen sich einen einzelnen Adressraum mit der ausführbaren Hauptprogramm Datei und vielen anderen DLLs.</span><span class="sxs-lookup"><span data-stu-id="9a26e-110">Like other DLLs, it is hosted in a process environment and shares a single address space with the main program executable and many other DLLs.</span></span> <span data-ttu-id="9a26e-111">Daher geht com+ davon aus, dass der gesamte Prozess beschädigt wurde, und der Prozess wird sofort beendet, um zu verhindern, dass er potenziell beschädigte Informationen an andere Prozesse zuweist oder noch schlimmer ist, dass beschädigte Daten committet und dauerhaft gemacht werden können.</span><span class="sxs-lookup"><span data-stu-id="9a26e-111">Therefore, COM+ assumes that the entire process has been corrupted, and the process is immediately terminated to prevent it from spreading potentially corrupted information to other processes or, worse yet, from allowing corrupted data to be committed and made durable.</span></span>

<span data-ttu-id="9a26e-112">Die Weitergabe von Ausnahmen außerhalb eines Kontexts ist in com+ nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="9a26e-112">COM+ does not allow exceptions to propagate outside of a context.</span></span> <span data-ttu-id="9a26e-113">Wenn eine Ausnahme während der Ausführung innerhalb eines com+-Kontexts auftritt und die Anwendung die Ausnahme nicht abfängt, bevor Sie aus dem Kontext zurückkehrt, fängt com+ die Ausnahme ab und beendet den Prozess.</span><span class="sxs-lookup"><span data-stu-id="9a26e-113">If an exception occurs while executing within a COM+ context and the application doesn't catch the exception before returning from the context, COM+ catches the exception and terminates the process.</span></span> <span data-ttu-id="9a26e-114">Die Verwendung der FailFast-Richtlinie basiert in diesem Fall auf der Annahme, dass die Ausnahme den Prozess in einen unbestimmten Zustand versetzt hat. Es ist nicht sicher, die Verarbeitung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="9a26e-114">Using the failfast policy in this case is based on the assumption that the exception has put the process into an indeterminate state; it is not safe to continue processing.</span></span>

<span data-ttu-id="9a26e-115">Als Entwickler oder Administrator sollten Sie das Ereignisanzeige-Anwendungsprotokoll überprüfen, um Details zu allen FailFast-Aktionen oder schwerwiegenden Anwendungsfehlern zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9a26e-115">As a developer or administrator, you should inspect the Event Viewer application log for details on any failfast action or serious application errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a26e-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9a26e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a26e-117">Ermitteln der Fehlerquelle</span><span class="sxs-lookup"><span data-stu-id="9a26e-117">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="9a26e-118">Ändern der Rückgabewerte durch com+</span><span class="sxs-lookup"><span data-stu-id="9a26e-118">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="9a26e-119">Interpretieren von Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="9a26e-119">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="9a26e-120">Strategien für die Behandlung von Fehlern in com+</span><span class="sxs-lookup"><span data-stu-id="9a26e-120">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="9a26e-121">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="9a26e-121">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



