---
description: .
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: Bewährte Methoden zum minimieren nicht reagierender Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e1fbad7fe60c4165ebb97847c303482314f68e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868595"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a><span data-ttu-id="fab7c-103">Bewährte Methoden zum minimieren nicht reagierender Dienste</span><span class="sxs-lookup"><span data-stu-id="fab7c-103">Best Practices for Minimizing Unresponsive Services</span></span>

## <a name="affected-platform"></a><span data-ttu-id="fab7c-104">Betroffene Plattform</span><span class="sxs-lookup"><span data-stu-id="fab7c-104">Affected Platform</span></span>

 <span data-ttu-id="fab7c-105">**Clients** – Windows Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="fab7c-105">**Clients** – Windows Vista \| Windows 7</span></span>  

## <a name="description"></a><span data-ttu-id="fab7c-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fab7c-106">Description</span></span>

<span data-ttu-id="fab7c-107">Nicht reagierende Dienste können zu Timeouts, beendeten Sitzungen und sogar zum Verlust von Daten führen.</span><span class="sxs-lookup"><span data-stu-id="fab7c-107">Unresponsive services can result in timeouts, terminated sessions, and even lost data.</span></span> <span data-ttu-id="fab7c-108">Die Verwendung bewährter Methoden kann das Vorkommen nicht reagierender Dienste erheblich verringern.</span><span class="sxs-lookup"><span data-stu-id="fab7c-108">Employing best practices can greatly reduce the occurrence of unresponsive services.</span></span>

## <a name="best-practices"></a><span data-ttu-id="fab7c-109">Bewährte Methoden</span><span class="sxs-lookup"><span data-stu-id="fab7c-109">Best Practices</span></span>

<span data-ttu-id="fab7c-110">Stellen Sie sicher, dass Ihre Anwendungen und alle abhängigen Dienste und Treiber auf die Systemleistung und das Herunterfahren von Benachrichtigungen reagieren.</span><span class="sxs-lookup"><span data-stu-id="fab7c-110">Make sure your applications and all of their dependent services and drivers respond to system power and shutdown notifications.</span></span>

-   <span data-ttu-id="fab7c-111">Alle Anwendungen sollten umgehend und ordnungsgemäß auf das Herunterfahren von Nachrichten wie WM \_ queryendsession und WM \_ EndSession reagieren, die darauf hinweisen, dass ein Herunterfahren ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fab7c-111">All applications should respond promptly and appropriately to shutdown messages such as WM\_QUERYENDSESSION and WM\_ENDSESSION that indicate a shutdown is in progress.</span></span>
-   <span data-ttu-id="fab7c-112">Alle Dienste sollten umgehend auf SCM-Shutdown-Benachrichtigungen reagieren.</span><span class="sxs-lookup"><span data-stu-id="fab7c-112">All services should promptly respond to SCM shutdown notifications.</span></span> <span data-ttu-id="fab7c-113">Wenn dies nicht der Fall ist, werden Sie vom Computer als nicht reagierend behandelt, und es wird ein Timeout von 20 Sekunden initiiert, und der Computer wird beendet, und es wird die Gefahr verlorener Daten geöffnet.</span><span class="sxs-lookup"><span data-stu-id="fab7c-113">If they fail to do so, the machine treats them as unresponsive and initiates a 20-second time-out and stops them, opening up the possibility of lost data.</span></span> <span data-ttu-id="fab7c-114">Dadurch wird dem Herunterfahren eines Computers auch 20 Sekunden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fab7c-114">This also adds 20 seconds to the shutdown time of a machine shutdown.</span></span>
-   <span data-ttu-id="fab7c-115">Alle Dienste, die über Kernel-Gerätetreiber Abhängigkeiten verfügen, sollten umgehend und ordnungsgemäß auf die Benachrichtigung zum Herunterfahren von "Iran" \_ \_ in ihren dispatchshutdown-Routinen reagieren</span><span class="sxs-lookup"><span data-stu-id="fab7c-115">All services that have kernel device driver dependencies should respond promptly and appropriately to IRP\_MJ\_SHUTDOWN notification in their DispatchShutdown routines.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="fab7c-116">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fab7c-116">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="fab7c-117">Windows Performance Toolkit</span><span class="sxs-lookup"><span data-stu-id="fab7c-117">Windows Performance Toolkit</span></span>](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 



