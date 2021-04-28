---
description: Bewährte Methoden zum Minimieren von nicht reagierenden Diensten
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: Bewährte Methoden zum Minimieren von nicht reagierenden Diensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90416e8256383e16fd78c436dfaa8d6a2186c540
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087998"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a><span data-ttu-id="bf119-103">Bewährte Methoden zum Minimieren von nicht reagierenden Diensten</span><span class="sxs-lookup"><span data-stu-id="bf119-103">Best Practices for Minimizing Unresponsive Services</span></span>

## <a name="affected-platform"></a><span data-ttu-id="bf119-104">Betroffene Plattform</span><span class="sxs-lookup"><span data-stu-id="bf119-104">Affected Platform</span></span>

 <span data-ttu-id="bf119-105">**Clients** – Windows Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="bf119-105">**Clients** – Windows Vista \| Windows 7</span></span>  

## <a name="description"></a><span data-ttu-id="bf119-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf119-106">Description</span></span>

<span data-ttu-id="bf119-107">Nicht reagierende Dienste können zu Timeouts, beendeten Sitzungen und sogar zu Datenverlusten führen.</span><span class="sxs-lookup"><span data-stu-id="bf119-107">Unresponsive services can result in timeouts, terminated sessions, and even lost data.</span></span> <span data-ttu-id="bf119-108">Die Verwendung bewährter Methoden kann das Auftreten nicht reagierender Dienste erheblich reduzieren.</span><span class="sxs-lookup"><span data-stu-id="bf119-108">Employing best practices can greatly reduce the occurrence of unresponsive services.</span></span>

## <a name="best-practices"></a><span data-ttu-id="bf119-109">Bewährte Methoden</span><span class="sxs-lookup"><span data-stu-id="bf119-109">Best Practices</span></span>

<span data-ttu-id="bf119-110">Stellen Sie sicher, dass Ihre Anwendungen und alle abhängigen Dienste und Treiber auf Benachrichtigungen zum Ein- und Herunterfahren des Systems reagieren.</span><span class="sxs-lookup"><span data-stu-id="bf119-110">Make sure your applications and all of their dependent services and drivers respond to system power and shutdown notifications.</span></span>

-   <span data-ttu-id="bf119-111">Alle Anwendungen sollten sofort und angemessen auf Meldungen zum Herunterfahren reagieren, z. B. WM \_ QUERYENDSESSION und WM \_ ENDSESSION, die darauf hinweisen, dass ein Herunterfahren ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf119-111">All applications should respond promptly and appropriately to shutdown messages such as WM\_QUERYENDSESSION and WM\_ENDSESSION that indicate a shutdown is in progress.</span></span>
-   <span data-ttu-id="bf119-112">Alle Dienste sollten sofort auf Benachrichtigungen zum Herunterfahren des SCM reagieren.</span><span class="sxs-lookup"><span data-stu-id="bf119-112">All services should promptly respond to SCM shutdown notifications.</span></span> <span data-ttu-id="bf119-113">Wenn sie dies nicht tun, behandelt der Computer sie als nicht reagierend, initiiert ein Time out von 20 Sekunden und beendet sie, wodurch die Möglichkeit besteht, dass Daten verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="bf119-113">If they fail to do so, the machine treats them as unresponsive and initiates a 20-second time-out and stops them, opening up the possibility of lost data.</span></span> <span data-ttu-id="bf119-114">Dies erhöht auch die Zeit zum Herunterfahren eines Computers um 20 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="bf119-114">This also adds 20 seconds to the shutdown time of a machine shutdown.</span></span>
-   <span data-ttu-id="bf119-115">Alle Dienste mit Kernelgerätetreiberabhängigkeiten sollten in \_ ihren DispatchShutdown-Routinen umgehend und entsprechend auf die IRP MJ \_ SHUTDOWN-Benachrichtigung reagieren.</span><span class="sxs-lookup"><span data-stu-id="bf119-115">All services that have kernel device driver dependencies should respond promptly and appropriately to IRP\_MJ\_SHUTDOWN notification in their DispatchShutdown routines.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="bf119-116">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bf119-116">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="bf119-117">Windows Performance Toolkit</span><span class="sxs-lookup"><span data-stu-id="bf119-117">Windows Performance Toolkit</span></span>](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 



