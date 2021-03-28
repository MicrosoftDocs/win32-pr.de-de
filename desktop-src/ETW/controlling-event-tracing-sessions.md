---
description: Ereignis Ablauf Verfolgungs Sitzungen zeichnen Ereignisse von einem oder mehreren Anbietern auf.
ms.assetid: 43841d2f-5a4c-493d-9531-21941311ffbc
title: Steuern von Ereignis Ablauf Verfolgungs Sitzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03f1917354679e7a68f9dbd001fc3aa10f09db0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977720"
---
# <a name="controlling-event-tracing-sessions"></a><span data-ttu-id="f9354-103">Steuern von Ereignis Ablauf Verfolgungs Sitzungen</span><span class="sxs-lookup"><span data-stu-id="f9354-103">Controlling Event Tracing Sessions</span></span>

<span data-ttu-id="f9354-104">Ereignis Ablauf Verfolgungs Sitzungen zeichnen Ereignisse von einem oder mehreren [Anbietern](providing-events.md)auf.</span><span class="sxs-lookup"><span data-stu-id="f9354-104">Event tracing sessions record events from one or more [providers](providing-events.md).</span></span> <span data-ttu-id="f9354-105">Der Controller definiert die Sitzung und aktiviert die Anbieter.</span><span class="sxs-lookup"><span data-stu-id="f9354-105">The controller defines the session and enables the providers.</span></span> <span data-ttu-id="f9354-106">Das Definieren der Sitzung umfasst in der Regel die Angabe von Sitzungs-und Protokoll Dateiname, Typ der zu verwendenden Protokolldatei und die Auflösung des Zeitstempels, der zum Aufzeichnen der Ereignisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f9354-106">Defining the session typically includes specifying the session and log file name, type of log file to use, and the resolution of the time stamp used to record the events.</span></span> <span data-ttu-id="f9354-107">Controller können auch Ereignis Ablauf Verfolgungs Sitzungen aktualisieren und Abfragen.</span><span class="sxs-lookup"><span data-stu-id="f9354-107">Controllers can also update and query event tracing sessions.</span></span>

<span data-ttu-id="f9354-108">In den folgenden Themen wird gezeigt, wie Sie eine Sitzung definieren und aktualisieren und Ereignis Ablauf Verfolgungs Anbieter aktivieren:</span><span class="sxs-lookup"><span data-stu-id="f9354-108">The following topics demonstrate how to define and update a session, and enable event trace providers:</span></span>

-   [<span data-ttu-id="f9354-109">Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung</span><span class="sxs-lookup"><span data-stu-id="f9354-109">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
-   [<span data-ttu-id="f9354-110">Konfigurieren und Starten einer systemtraceprovider-Sitzung</span><span class="sxs-lookup"><span data-stu-id="f9354-110">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
-   [<span data-ttu-id="f9354-111">Konfigurieren und Starten einer autologger-Sitzung</span><span class="sxs-lookup"><span data-stu-id="f9354-111">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
-   [<span data-ttu-id="f9354-112">Konfigurieren und Starten einer Sitzung für private Logger</span><span class="sxs-lookup"><span data-stu-id="f9354-112">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
-   [<span data-ttu-id="f9354-113">Aktualisieren einer Ereignis Ablauf Verfolgungs Sitzung</span><span class="sxs-lookup"><span data-stu-id="f9354-113">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
-   [<span data-ttu-id="f9354-114">Abrufen von zusätzlichen Ereignis Ablauf Verfolgungs Daten</span><span class="sxs-lookup"><span data-stu-id="f9354-114">Retrieving Additional Event Tracing Data</span></span>](retrieving-additional-event-tracing-data.md)

<span data-ttu-id="f9354-115">Informationen zum leeren und Abfragen von Sitzungen finden Sie unter [**controltrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) bzw. [**queryalltraces**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa).</span><span class="sxs-lookup"><span data-stu-id="f9354-115">For information on flushing and querying sessions, see [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) and [**QueryAllTraces**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa), respectively.</span></span>

<span data-ttu-id="f9354-116">Nur Benutzer, die mit erhöhten Administratorrechten ausgeführt werden, Benutzer in der Gruppe der Leistungs Protokoll Benutzer und Anwendungen, die als LocalSystem, LocalService oder Network Service ausgeführt werden, können Ereignisse für die Ereignis Ablauf Verfolgung steuern.</span><span class="sxs-lookup"><span data-stu-id="f9354-116">Only users running with elevated administrative privileges, users in the Performance Log Users group, and applications running as LocalSystem, LocalService or NetworkService can control event tracing sessions.</span></span> <span data-ttu-id="f9354-117">Um einem eingeschränkten Benutzer die Möglichkeit zu geben, Ablauf Verfolgungs Sitzungen zu steuern, fügen Sie diese der Gruppe Leistungs Protokoll Benutzer hinzu.</span><span class="sxs-lookup"><span data-stu-id="f9354-117">To grant a restricted user the ability to control trace sessions, add them to the Performance Log Users group.</span></span>

<span data-ttu-id="f9354-118">**Windows XP und Windows 2000:** Jeder kann eine Ablauf Verfolgungs Sitzung steuern.</span><span class="sxs-lookup"><span data-stu-id="f9354-118">**Windows XP and Windows 2000:** Anyone can control a trace session.</span></span>

 

 
