---
description: Eine Anwendung, die als Standardbenutzer ausgeführt wird, führt Vorgänge aus, die Administratorrechte erfordern, indem eine geplante Aufgabe gestartet wird.
ms.assetid: cd7485b3-6be5-4163-9a86-7892dbc59181
title: Modell mit erhöhten Rechten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27006e32210cfea05de5c2b3b9adf36613dc4f5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348929"
---
# <a name="elevated-task-model"></a><span data-ttu-id="670ba-103">Modell mit erhöhten Rechten</span><span class="sxs-lookup"><span data-stu-id="670ba-103">Elevated Task Model</span></span>

<span data-ttu-id="670ba-104">Im Modell mit erhöhten Rechten führt eine Anwendung, die als Standardbenutzer ausgeführt wird, Vorgänge durch, die Administratorrechte erfordern, indem eine geplante Aufgabe gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="670ba-104">In the elevated task model, an application running as a standard user performs operations that require administrator privilege by starting a scheduled task.</span></span>

<span data-ttu-id="670ba-105">**Windows Server 2003 und Windows XP:** Das Modell mit erhöhten Rechten wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="670ba-105">**Windows Server 2003 and Windows XP:** The elevated task model is not supported.</span></span>

<span data-ttu-id="670ba-106">Tasks verbrauchen nicht so viele Systemressourcen wie Dienste, und Aufgaben werden nach Abschluss des Vorgangs automatisch geschlossen.</span><span class="sxs-lookup"><span data-stu-id="670ba-106">Tasks do not consume as many system resources as services, and tasks automatically close when finished.</span></span> <span data-ttu-id="670ba-107">Sie sollten dieses Modell anstelle des [Betriebs System-Dienst Modells](operating-system-service-model.md) verwenden, es sei denn, es ist Abwärtskompatibilität mit früheren Betriebssystemen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="670ba-107">Consider using this model instead of the [Operating System Service Model](operating-system-service-model.md) unless backward compatibility with earlier operating systems is necessary.</span></span>

<span data-ttu-id="670ba-108">Die folgenden Bedingungen müssen erfüllt sein, um eine Aufgabe zum Ausführen privilegierter Vorgänge für eine Standardbenutzer Anwendung zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="670ba-108">To use a task to perform privileged operations for a standard user application, the following conditions must be met:</span></span>

-   <span data-ttu-id="670ba-109">Der Task muss auf " **System** ausführen" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="670ba-109">The task must be set to run as **SYSTEM**.</span></span>
-   <span data-ttu-id="670ba-110">Die [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) , die dem Task zugeordnet ist, muss so konfiguriert werden, dass Standardbenutzer die Aufgabe starten können.</span><span class="sxs-lookup"><span data-stu-id="670ba-110">The [*security descriptor*](/windows/desktop/SecGloss/s-gly) associated with the task must be configured to allow standard users to start the task.</span></span>
-   <span data-ttu-id="670ba-111">Der Taskplaner-Dienst muss ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="670ba-111">The task scheduler service must be running.</span></span>

<span data-ttu-id="670ba-112">Weitere Informationen zum Erstellen und starten von Aufgaben finden Sie unter [Taskplaner](/windows/desktop/TaskSchd/task-scheduler-start-page).</span><span class="sxs-lookup"><span data-stu-id="670ba-112">For information about how to create and start tasks, see [Task Scheduler](/windows/desktop/TaskSchd/task-scheduler-start-page).</span></span>

## <a name="related-topics"></a><span data-ttu-id="670ba-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="670ba-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="670ba-114">Entwickeln von Anwendungen, für die Administrator Rechte erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="670ba-114">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="670ba-115">Administrator Broker Modell</span><span class="sxs-lookup"><span data-stu-id="670ba-115">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="670ba-116">COM-Objektmodell für Administratoren</span><span class="sxs-lookup"><span data-stu-id="670ba-116">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="670ba-117">Betriebs System-Dienstmodell</span><span class="sxs-lookup"><span data-stu-id="670ba-117">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> </dl>

 

 
