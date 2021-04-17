---
title: Starten einer ausführbaren Datei, wenn sich ein Benutzer anmeldet
description: Wenn Sie eine Aufgabe schreiben, die eine ausführbare Datei startet, wenn sich ein Benutzer anmeldet, definieren Sie einen LOGON-und eine ausführbare Aktion.
ms.assetid: 0c5912aa-913d-42ce-a01b-b1359b49bb2f
keywords:
- Taskplaner Beispiele Taskplaner, LOGON-Auslösung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa758546dbd08b6ccf27412f38891589cb9643
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387952"
---
# <a name="starting-an-executable-when-a-user-logs-on"></a><span data-ttu-id="0a6be-104">Starten einer ausführbaren Datei, wenn sich ein Benutzer anmeldet</span><span class="sxs-lookup"><span data-stu-id="0a6be-104">Starting an Executable When a User Logs On</span></span>

<span data-ttu-id="0a6be-105">Wenn Sie eine Aufgabe schreiben, die eine ausführbare Datei startet, wenn sich ein Benutzer anmeldet, definieren Sie einen LOGON-und eine ausführbare Aktion.</span><span class="sxs-lookup"><span data-stu-id="0a6be-105">Writing a task that starts an executable when a user logs on is done by defining a logon trigger and an executable action.</span></span>

## <a name="logon-trigger"></a><span data-ttu-id="0a6be-106">Logon-Auslösung</span><span class="sxs-lookup"><span data-stu-id="0a6be-106">Logon Trigger</span></span>

<span data-ttu-id="0a6be-107">LOGON-Trigger werden über die Start Grenze aktiviert, starten die ausführbare Datei jedoch erst, wenn sich ein angegebener Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="0a6be-107">Logon triggers are activated by their start boundary but they do not start the executable until a specified user logs on.</span></span> <span data-ttu-id="0a6be-108">Sie können den Logon-Zeitpunkt angeben, der gestartet werden soll, wenn sich ein bestimmter Benutzer anmeldet, indem Sie den Benutzer in der [**UserID**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) -Eigenschaft der [**iLogon-**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) Schnittstelle angeben ([**Logon-**](logontrigger.md) Auslösung für Skripterstellung).</span><span class="sxs-lookup"><span data-stu-id="0a6be-108">You can specify the logon trigger to start when a certain user logs on by specifying the user in the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property of the [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) interface ([**LogonTrigger**](logontrigger.md) for scripting).</span></span>

## <a name="logontrigger-examples"></a><span data-ttu-id="0a6be-109">Logon-auslöserbeispiele</span><span class="sxs-lookup"><span data-stu-id="0a6be-109">LogonTrigger Examples</span></span>

<span data-ttu-id="0a6be-110">In den folgenden Beispielen wird Notepad gestartet, nachdem sich ein Benutzer angemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="0a6be-110">The following examples start Notepad after a user logs on.</span></span>

-   [<span data-ttu-id="0a6be-111">Beispiel für LOGON-Auslösung (Skripterstellung)</span><span class="sxs-lookup"><span data-stu-id="0a6be-111">Logon Trigger Example (Scripting)</span></span>](logon-trigger-example--scripting-.md)
-   [<span data-ttu-id="0a6be-112">Beispiel eines LOGON-Auslösers (C++)</span><span class="sxs-lookup"><span data-stu-id="0a6be-112">Logon Trigger Example (C++)</span></span>](logon-trigger-example--c---.md)
-   [<span data-ttu-id="0a6be-113">Beispiel eines LOGON-Auslösers (XML)</span><span class="sxs-lookup"><span data-stu-id="0a6be-113">Logon Trigger Example (XML)</span></span>](logon-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="0a6be-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0a6be-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a6be-115">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="0a6be-115">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




