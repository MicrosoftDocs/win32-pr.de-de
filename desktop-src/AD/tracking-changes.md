---
title: Nachverfolgen von Änderungen
description: Einige Anwendungen müssen die Konsistenz zwischen bestimmten Daten, die im Active Directory Directory-Dienst gespeichert sind, und anderen Daten beibehalten.
ms.assetid: f4539482-1170-4c0c-b817-b39e58049d39
ms.tgt_platform: multiple
keywords:
- Active Directory, verwenden, Nachverfolgen von Änderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dc772f883b97eb4e7305b39f0a582448a8bc021
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948540"
---
# <a name="tracking-changes"></a><span data-ttu-id="efc48-104">Nachverfolgen von Änderungen</span><span class="sxs-lookup"><span data-stu-id="efc48-104">Tracking Changes</span></span>

<span data-ttu-id="efc48-105">Einige Anwendungen müssen die Konsistenz zwischen bestimmten Daten, die im Active Directory Directory-Dienst gespeichert sind, und anderen Daten beibehalten.</span><span class="sxs-lookup"><span data-stu-id="efc48-105">Some applications must maintain consistency between specific data stored in the Active Directory directory service and other data.</span></span> <span data-ttu-id="efc48-106">Die anderen Daten können im Verzeichnis, in einer SQL Server Tabelle, in einer Datei oder in der Registrierung gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="efc48-106">The other data might be stored in the directory, in a SQL Server table, in a file, or in the registry.</span></span> <span data-ttu-id="efc48-107">Wenn sich im Verzeichnis gespeicherte Daten ändern, müssen die anderen Daten möglicherweise geändert werden, damit Sie konsistent bleiben.</span><span class="sxs-lookup"><span data-stu-id="efc48-107">When data stored in the directory changes, the other data may be required to change in order to remain consistent.</span></span> <span data-ttu-id="efc48-108">Anwendungen, die diese Anforderung erfüllen, umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="efc48-108">Applications that have this requirement include:</span></span>

<span data-ttu-id="efc48-109">In diesem Abschnitt werden die von der Überwachung von Anwendungen verwendeten Mechanismen nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="efc48-109">This section does not cover mechanisms used by monitoring applications.</span></span> <span data-ttu-id="efc48-110">Dabei handelt es sich um Anwendungen, die Verzeichnisänderungen überwachen, nicht um konsistente Daten zwischen separaten speichern zu verwalten, sondern als System Verwaltungs Tool.</span><span class="sxs-lookup"><span data-stu-id="efc48-110">These are applications that monitor directory changes not for the purpose of maintaining consistent data between separate stores, but as a system management tool.</span></span> <span data-ttu-id="efc48-111">Wenngleich Überwachungsanwendungen die gleichen Mechanismen verwenden können, die Anwendungen für die Änderungs Nachverfolgung unterstützen, sind die folgenden Mechanismen speziell für die Überwachung von Anwendungen konzipiert:</span><span class="sxs-lookup"><span data-stu-id="efc48-111">Although monitoring applications can use the same mechanisms that support change-tracking applications, the following mechanisms are specifically designed for monitoring applications:</span></span>

-   <span data-ttu-id="efc48-112">Sicherheitsüberwachung.</span><span class="sxs-lookup"><span data-stu-id="efc48-112">Security auditing.</span></span> <span data-ttu-id="efc48-113">Durch Ändern des Teils der System Zugriffs Steuerungs Liste (SACL) einer Objekt Sicherheits Beschreibung können Sie Zugriffe auf das-Objekt auf einem bestimmten Domänen Controller veranlassen, dass Überwachungsdaten Sätze im Sicherheits Ereignisprotokoll auf diesem Domänen Controller generiert werden.</span><span class="sxs-lookup"><span data-stu-id="efc48-113">By modifying the system access-control list (SACL) portion of an object security descriptor, you can cause accesses to the object on a given domain controller to generate audit records in the security event log on that DC.</span></span> <span data-ttu-id="efc48-114">Sie können Lese-und Schreibvorgänge oder beides überwachen. Sie können das gesamte Objekt oder bestimmte Attribute überwachen.</span><span class="sxs-lookup"><span data-stu-id="efc48-114">You can audit reads, writes, or both; you can audit the entire object or specific attributes.</span></span> <span data-ttu-id="efc48-115">Weitere Informationen finden Sie unter [Abrufen der SACL](retrieving-an-objectampaposs-sacl.md) -und Überwachungs [Generierung](/windows/desktop/SecAuthZ/audit-generation)eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="efc48-115">For more information, see [Retrieving an Object's SACL](retrieving-an-objectampaposs-sacl.md) and [Audit Generation](/windows/desktop/SecAuthZ/audit-generation).</span></span>
-   <span data-ttu-id="efc48-116">Ereignisprotokollierung</span><span class="sxs-lookup"><span data-stu-id="efc48-116">Event logging.</span></span> <span data-ttu-id="efc48-117">Durch Ändern der Registrierungs Einstellungen auf einem bestimmten Domänen Controller können Sie die Arten von Ereignissen ändern, die in das Verzeichnisdienst-Ereignisprotokoll protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="efc48-117">By modifying registry settings on a given domain controller, you can change the kinds of events logged to the directory service event log.</span></span> <span data-ttu-id="efc48-118">Um alle Änderungen zu protokollieren, legen Sie den **8-Verzeichniszugriffs** Wert unter dem folgenden Registrierungsschlüssel auf 4 fest.</span><span class="sxs-lookup"><span data-stu-id="efc48-118">Specifically, to log all modifications, set the **8 Directory Access** value under the following registry key to 4.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                NTDS
                   Diagnostics
    ```

    <span data-ttu-id="efc48-119">Weitere Informationen finden Sie unter [Ereignisprotokollierung](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="efc48-119">For more information, see [Event Logging](/windows/desktop/EventLog/event-logging).</span></span>

-   <span data-ttu-id="efc48-120">Ereignisablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="efc48-120">Event tracing.</span></span> <span data-ttu-id="efc48-121">In Windows 2000 wurde eine Ereignis Ablauf Verfolgungs-API für die Ablauf Verfolgung und Protokollierung interessanter Ereignisse in Software oder Hardware eingeführt.</span><span class="sxs-lookup"><span data-stu-id="efc48-121">Windows 2000 introduced an Event Tracing API for tracing and logging interesting events in software or hardware.</span></span> <span data-ttu-id="efc48-122">Das Windows-Betriebssystem und Active Directory Domain Services insbesondere die Verwendung der Ereignis Ablauf Verfolgung für die Kapazitätsplanung und detaillierte Leistungsanalyse unterstützen.</span><span class="sxs-lookup"><span data-stu-id="efc48-122">The Windows operating system, and Active Directory Domain Services in particular, support the use of event tracing for capacity planning and detailed performance analysis.</span></span> <span data-ttu-id="efc48-123">Weitere Informationen finden Sie unter [Ereignis Ablauf Verfolgung](/windows/desktop/ETW/event-tracing-portal) und [Ereignis Ablauf Verfolgung in ADSI](/windows/desktop/ADSI/adsi-and-etw).</span><span class="sxs-lookup"><span data-stu-id="efc48-123">For more information, see [Event Tracing](/windows/desktop/ETW/event-tracing-portal) and [Event Tracing in ADSI](/windows/desktop/ADSI/adsi-and-etw).</span></span>

<span data-ttu-id="efc48-124">Dieser Abschnitt schließt folgende Themen ein:</span><span class="sxs-lookup"><span data-stu-id="efc48-124">This section includes the following topics:</span></span>

-   [<span data-ttu-id="efc48-125">Übersicht über Änderungsnachverfolgung Techniken</span><span class="sxs-lookup"><span data-stu-id="efc48-125">Overview of Change Tracking Techniques</span></span>](overview-of-change-tracking-techniques.md)
-   [<span data-ttu-id="efc48-126">Ändern von Benachrichtigungen in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="efc48-126">Change Notifications in Active Directory Domain Services</span></span>](change-notifications-in-active-directory-domain-services.md)
-   [<span data-ttu-id="efc48-127">Abrufen von Änderungen mithilfe des Dirsync-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="efc48-127">Polling for Changes Using the DirSync Control</span></span>](polling-for-changes-using-the-dirsync-control.md)
-   [<span data-ttu-id="efc48-128">Abrufen von Änderungen mithilfe von ""</span><span class="sxs-lookup"><span data-stu-id="efc48-128">Polling for Changes Using USNChanged</span></span>](polling-for-changes-using-usnchanged.md)

 

 