---
title: Starten einer ausführbaren Datei beim System Start
description: Wenn Sie eine Aufgabe schreiben, die eine ausführbare Datei startet, wenn ein System gestartet wird, definieren Sie einen Start-und eine ausführbare Aktion.
ms.assetid: 9e2359df-a223-4a0c-9051-01b73a83c1f7
keywords:
- Taskplaner Beispiele Taskplaner, Start-Auslösers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d41c39e9c80d3fc8f14c0bc9b9d9305de38e16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712576"
---
# <a name="starting-an-executable-on-system-boot"></a><span data-ttu-id="93b71-104">Starten einer ausführbaren Datei beim System Start</span><span class="sxs-lookup"><span data-stu-id="93b71-104">Starting an Executable on System Boot</span></span>

<span data-ttu-id="93b71-105">Wenn Sie eine Aufgabe schreiben, die eine ausführbare Datei startet, wenn ein System gestartet wird, definieren Sie einen Start-und eine ausführbare Aktion.</span><span class="sxs-lookup"><span data-stu-id="93b71-105">Writing a task that starts an executable when a system is booted is done by defining a boot trigger and an executable action.</span></span>

## <a name="boot-trigger"></a><span data-ttu-id="93b71-106">Start-auslöst</span><span class="sxs-lookup"><span data-stu-id="93b71-106">Boot Trigger</span></span>

<span data-ttu-id="93b71-107">Start Trigger werden über die Start Grenze aktiviert, starten die ausführbare Datei jedoch erst, wenn das System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="93b71-107">Boot triggers are activated by their start boundary but they do not start the executable until the system is booted.</span></span> <span data-ttu-id="93b71-108">Sie können auch eine Verzögerungszeit im Start-Fehler angeben, die den Zeitraum zwischen dem Start des Systems und dem Start der Aufgabe angibt.</span><span class="sxs-lookup"><span data-stu-id="93b71-108">You can also specify a delay time in the boot trigger that specifies the amount of time between when the system is booted and when the task is started.</span></span> <span data-ttu-id="93b71-109">Dies wird durch die [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) -Eigenschaft in der [**iboottrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) -Schnittstelle ([**boottrigger**](boottrigger.md) -Objekt für die Skripterstellung) definiert.</span><span class="sxs-lookup"><span data-stu-id="93b71-109">This is defined by the [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) property in the [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) interface ([**BootTrigger**](boottrigger.md) object for scripting).</span></span>

## <a name="boot-trigger-examples"></a><span data-ttu-id="93b71-110">Beispiele für Start Beispiele</span><span class="sxs-lookup"><span data-stu-id="93b71-110">Boot Trigger Examples</span></span>

<span data-ttu-id="93b71-111">In den folgenden Beispielen wird Notepad gestartet, nachdem das System gestartet wurde:</span><span class="sxs-lookup"><span data-stu-id="93b71-111">The following examples start Notepad after the system is booted:</span></span>

-   [<span data-ttu-id="93b71-112">Beispiel für einen Start-Beispiel (Skripterstellung)</span><span class="sxs-lookup"><span data-stu-id="93b71-112">Boot Trigger Example (Scripting)</span></span>](boot-trigger-example--scripting-.md)
-   [<span data-ttu-id="93b71-113">Beispiel für einen Start Auslösers (C++)</span><span class="sxs-lookup"><span data-stu-id="93b71-113">Boot Trigger Example (C++)</span></span>](boot-trigger-example--c---.md)
-   [<span data-ttu-id="93b71-114">Beispiel für einen Start Auslösers (XML)</span><span class="sxs-lookup"><span data-stu-id="93b71-114">Boot Trigger Example (XML)</span></span>](boot-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="93b71-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="93b71-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93b71-116">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="93b71-116">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




