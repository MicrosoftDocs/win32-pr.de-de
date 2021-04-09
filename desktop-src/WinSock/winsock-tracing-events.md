---
description: Details der Winsock-Ablauf Verfolgungs Ereignisse.
ms.assetid: 246AE0BE-E8E2-4291-8BF4-577F889F055B
title: Winsock-Ablauf Verfolgungs Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeabd2d06741f8dfa1f47b513a09c941ee1490b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129104"
---
# <a name="winsock-tracing-events"></a><span data-ttu-id="69573-103">Winsock-Ablauf Verfolgungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="69573-103">Winsock Tracing Events</span></span>

<span data-ttu-id="69573-104">In diesem Abschnitt werden ausführliche Informationen zu bestimmten Details der Winsock-Ablauf Verfolgungs Ereignisse beschrieben.</span><span class="sxs-lookup"><span data-stu-id="69573-104">This section describes detailed information on specific Winsock Tracing Events details.</span></span>

<span data-ttu-id="69573-105">Die Winsock-Ablauf Verfolgung ist ein Feature zur Problembehandlung, das in Binärdateien im Einzelhandel aktiviert werden kann, um bestimmte Windows Socket-Ereignisse mit minimalem mehr Aufwand</span><span class="sxs-lookup"><span data-stu-id="69573-105">Winsock tracing is a troubleshooting feature that can be enabled in retail binaries to trace certain Windows socket events with minimal overhead.</span></span> <span data-ttu-id="69573-106">Diese Funktion ermöglicht bessere Diagnosefunktionen für Entwickler und den Produktsupport.</span><span class="sxs-lookup"><span data-stu-id="69573-106">This feature allows for better diagnostic capabilities for developers and product support.</span></span> <span data-ttu-id="69573-107">Die Winsock-Netzwerk Ereignis Ablauf Verfolgung unterstützt Ablaufverfolgungs-Socketvorgänge für IPv4-und IPv6</span><span class="sxs-lookup"><span data-stu-id="69573-107">Winsock network event tracing supports tracing socket operations for IPv4 and IPv6 applications.</span></span> <span data-ttu-id="69573-108">Die Ablauf Verfolgung der Winsock-Katalog Änderung unterstützt die Ablauf Verfolgung von Änderungen, die an den Winsock-Katalog durch mehrstufige Dienstanbieter (LSPs</span><span class="sxs-lookup"><span data-stu-id="69573-108">Winsock catalog change tracing supports tracing changes made to the Winsock catalog by layered service providers (LSPs).</span></span>

> [!Note]  
> <span data-ttu-id="69573-109">Mehrstufige Dienstanbieter sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="69573-109">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="69573-110">Ab Windows 8 und Windows Server 2012 verwenden Sie die [Windows-Filter Plattform](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="69573-110">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="69573-111">Die Winsock-Ablauf Verfolgung verwendet die Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw), eine allgemeine, hoch Geschwindigkeits Ablauf Verfolgungs Funktion des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="69573-111">Winsock tracing uses Event Tracing for Windows (ETW), a general-purpose, high-speed tracing facility provided by the operating system.</span></span> <span data-ttu-id="69573-112">Etw bietet einen Ablauf Verfolgungs Mechanismus für Ereignisse, die von Anwendungen im Benutzermodus und im Kernel Modus-Gerätetreibern ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="69573-112">ETW provides a tracing mechanism for events raised by both user-mode applications and kernel-mode device drivers.</span></span> <span data-ttu-id="69573-113">Etw kann die Protokollierung dynamisch aktivieren und deaktivieren, sodass eine ausführliche Ablauf Verfolgung in Produktionsumgebungen ohne Neustarts oder Anwendungs Neustarts problemlos durchgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="69573-113">ETW can enable and disable logging dynamically, making it easy to perform detailed tracing in production environments without requiring reboots or application restarts.</span></span> <span data-ttu-id="69573-114">Unterstützung für die Winsock-Ablauf Verfolgung mit etw wurde unter Windows Vista und höher hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="69573-114">Support for Winsock tracing using ETW was added on Windows Vista and later.</span></span> <span data-ttu-id="69573-115">Allgemeine Informationen zu etw finden Sie unter verbessertes [Debugging und Leistungsoptimierung mit etw](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span><span class="sxs-lookup"><span data-stu-id="69573-115">For general information on ETW, see [Improve Debugging And Performance Tuning With ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span></span>

<span data-ttu-id="69573-116">In der folgenden Liste finden Sie ausführliche Informationen zu den einzelnen Winsock-Ablauf Verfolgungs Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="69573-116">The following list provides detailed information for each Winsock tracing event.</span></span> <span data-ttu-id="69573-117">Klicken Sie auf den Ereignis Namen, um weitere Informationen zu einem beliebigen Ereignis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="69573-117">For additional information on any event, click the event name.</span></span>



| <span data-ttu-id="69573-118">Veranstaltungsname</span><span class="sxs-lookup"><span data-stu-id="69573-118">Event Name</span></span>                                                            | <span data-ttu-id="69573-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69573-119">Description</span></span>                                                                               |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69573-120">**AFD- \_ Ereignis \_ Erstellung**</span><span class="sxs-lookup"><span data-stu-id="69573-120">**AFD\_EVENT\_CREATE**</span></span>](afd-event-create.md)                        | <span data-ttu-id="69573-121">Winsock-Netzwerk Ablauf Verfolgungs Ereignis für einen Socket-Erstellungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="69573-121">Winsock network tracing event for a socket creation operation.</span></span>                            |
| [<span data-ttu-id="69573-122">**AFD- \_ Ereignis \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="69573-122">**AFD\_EVENT\_CLOSE**</span></span>](afd-event-close.md)                          | <span data-ttu-id="69573-123">Winsock-Netzwerkablaufverfolgungs-Ereignis für SocketClose.</span><span class="sxs-lookup"><span data-stu-id="69573-123">Winsock network tracing event for socket close operation.</span></span>                                 |
| [<span data-ttu-id="69573-124">**Winsock \_ WS2HELP \_ LSP- \_ Installation**</span><span class="sxs-lookup"><span data-stu-id="69573-124">**WINSOCK\_WS2HELP\_LSP\_INSTALL**</span></span>](winsock-ws2help-lsp-install.md) | <span data-ttu-id="69573-125">Änderungs Ereignis für den Winsock-Katalog für einen mehrstufigen Dienstanbieter (LSP).</span><span class="sxs-lookup"><span data-stu-id="69573-125">Winsock catalog change event for a layered service provider (LSP) installation operation.</span></span> |
| [<span data-ttu-id="69573-126">**Winsock \_ WS2HELP \_ LSP \_ Entfernen**</span><span class="sxs-lookup"><span data-stu-id="69573-126">**WINSOCK\_WS2HELP\_LSP\_REMOVE**</span></span>](winsock-ws2help-lsp-remove.md)   | <span data-ttu-id="69573-127">Änderungs Ereignis für den Winsock-Katalog für einen mehrstufigen Dienstanbieter (LSP).</span><span class="sxs-lookup"><span data-stu-id="69573-127">Winsock catalog change event for a layered service provider (LSP) removal operation.</span></span>      |
| [<span data-ttu-id="69573-128">**Winsock \_ WS2HELP \_ LSP \_ Deaktivieren**</span><span class="sxs-lookup"><span data-stu-id="69573-128">**WINSOCK\_WS2HELP\_LSP\_DISABLE**</span></span>](winsock-ws2help-lsp-disable.md) | <span data-ttu-id="69573-129">Änderungs Ereignis für den Winsock-Katalog für einen mehrstufigen Dienstanbieter (LSP).</span><span class="sxs-lookup"><span data-stu-id="69573-129">Winsock catalog change event for a layered service provider (LSP) disable operation.</span></span>      |
| [<span data-ttu-id="69573-130">**Winsock \_ WS2HELP \_ LSP \_ Reset**</span><span class="sxs-lookup"><span data-stu-id="69573-130">**WINSOCK\_WS2HELP\_LSP\_RESET**</span></span>](winsock-ws2help-lsp-reset.md)     | <span data-ttu-id="69573-131">Das Änderungs Ereignis für den Winsock-Katalog für einen Winsock-Katalog Zurücksetzungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="69573-131">Winsock catalog change event for a Winsock catalog reset operation.</span></span>                       |



 

## <a name="related-topics"></a><span data-ttu-id="69573-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="69573-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69573-133">Verbessertes Debugging und Leistungsoptimierung mit ETW</span><span class="sxs-lookup"><span data-stu-id="69573-133">Improve Debugging And Performance Tuning With ETW</span></span>](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[<span data-ttu-id="69573-134">Winsock-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="69573-134">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="69573-135">Winsock-Ablauf Verfolgungs Ebenen</span><span class="sxs-lookup"><span data-stu-id="69573-135">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="69573-136">Kontrolle über die Winsock-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="69573-136">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="69573-137">Details der Winsock-Netzwerk Ereignis Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="69573-137">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="69573-138">Details zur Änderung der Winsock-Katalog Änderung</span><span class="sxs-lookup"><span data-stu-id="69573-138">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
