---
title: Starten einer ausführbaren Datei, wenn eine Aufgabe registriert ist
description: Wenn Sie eine Aufgabe schreiben, die eine ausführbare Datei startet, wenn eine Aufgabe registriert wird, definieren Sie einen Registrierungs-und eine ausführbare Aktion.
ms.assetid: 426fa79d-7f0d-42fb-a8c4-15981d13be71
keywords:
- Taskplaner Beispiele Taskplaner, Registrierungs-Auslösung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8036b8bdff807ded582279e0ba7675bc2160811
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947829"
---
# <a name="starting-an-executable-when-a-task-is-registered"></a><span data-ttu-id="c191e-104">Starten einer ausführbaren Datei, wenn eine Aufgabe registriert ist</span><span class="sxs-lookup"><span data-stu-id="c191e-104">Starting an Executable When a Task is Registered</span></span>

<span data-ttu-id="c191e-105">Wenn Sie eine Aufgabe schreiben, die eine ausführbare Datei startet, wenn eine Aufgabe registriert wird, definieren Sie einen Registrierungs-und eine ausführbare Aktion.</span><span class="sxs-lookup"><span data-stu-id="c191e-105">Writing a task that starts an executable when a task is registered is done by defining a registration trigger and an executable action.</span></span>

## <a name="registration-trigger"></a><span data-ttu-id="c191e-106">Registrierungs-auslöst</span><span class="sxs-lookup"><span data-stu-id="c191e-106">Registration Trigger</span></span>

<span data-ttu-id="c191e-107">Registrierungs Trigger starten einen Task, sobald er registriert ist.</span><span class="sxs-lookup"><span data-stu-id="c191e-107">Registration triggers start a task as soon as it is registered.</span></span> <span data-ttu-id="c191e-108">Sie können auch eine Verzögerung für den Registrierungs-Auslösung angeben, die eine Aufgabe nach einem bestimmten Zeitraum (Verzögerung) nach der Registrierung des Tasks startet.</span><span class="sxs-lookup"><span data-stu-id="c191e-108">You can also specify a delay for the registration trigger, which starts a task after a specific amount of time (the delay) after the task is registered.</span></span> <span data-ttu-id="c191e-109">Die Verzögerung wird in der [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) -Eigenschaft der [**iregistration-auslöserschnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) angegeben ([**Registration-Auslösers**](registrationtrigger.md) für die Skripterstellung).</span><span class="sxs-lookup"><span data-stu-id="c191e-109">The delay is specified in the [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) property of the [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) interface ([**RegistrationTrigger**](registrationtrigger.md) for scripting).</span></span>

> [!Note]  
> <span data-ttu-id="c191e-110">Wenn eine Aufgabe mit einem Registrierungs-ausgelöst wird, wird die Aufgabe ausgeführt, nachdem das Update ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="c191e-110">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

## <a name="registration-trigger-examples"></a><span data-ttu-id="c191e-111">Beispiele für Registrierungs Beispiele</span><span class="sxs-lookup"><span data-stu-id="c191e-111">Registration Trigger Examples</span></span>

<span data-ttu-id="c191e-112">In den folgenden Beispielen wird Notepad gestartet, wenn ein Task registriert wird:</span><span class="sxs-lookup"><span data-stu-id="c191e-112">The following examples start Notepad when a task is registered:</span></span>

-   [<span data-ttu-id="c191e-113">Beispiel für Registrierungs Beispiel (Skripterstellung)</span><span class="sxs-lookup"><span data-stu-id="c191e-113">Registration Trigger Example (Scripting)</span></span>](registration-trigger-example--scripting-.md)
-   [<span data-ttu-id="c191e-114">Registrierungs auslöserbeispiel (C++)</span><span class="sxs-lookup"><span data-stu-id="c191e-114">Registration Trigger Example (C++)</span></span>](registration-trigger-example--c---.md)
-   [<span data-ttu-id="c191e-115">Registrierungs auslöserbeispiel (XML)</span><span class="sxs-lookup"><span data-stu-id="c191e-115">Registration Trigger Example (XML)</span></span>](registration-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="c191e-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c191e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c191e-117">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="c191e-117">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




