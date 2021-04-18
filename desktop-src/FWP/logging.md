---
title: Protokollierung (Windows-Filter Plattform)
description: Die Windows-Filter Plattform (WFP) ermöglicht das Protokollieren von Paket Ablage-und IKE/AuthIP-Fehlern.
ms.assetid: 607b7664-6be4-4ae6-991b-58ac9175405a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27868c76a643a8e1b7b478152c100a2026bfc20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106337481"
---
# <a name="logging-windows-filtering-platform"></a><span data-ttu-id="e3d2e-103">Protokollierung (Windows-Filter Plattform)</span><span class="sxs-lookup"><span data-stu-id="e3d2e-103">Logging (Windows Filtering Platform)</span></span>

<span data-ttu-id="e3d2e-104">Die Windows-Filter Plattform (Windows Filtering Platform, WFP) ermöglicht das Protokollieren von Paket Ablage-und IKE/AuthIP-Fehlern</span><span class="sxs-lookup"><span data-stu-id="e3d2e-104">The Windows Filtering Platform (WFP) provides logging of packet drops and IKE/AuthIP failures.</span></span>

<span data-ttu-id="e3d2e-105">Die protokollierten Ereignisse werden im enumerierten Typ des Typs "Typ des Typs [**" vom Typ \_ \_ \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) "Typ" definiert und lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="e3d2e-105">The logged events are defined in the [**FWPM\_NET\_EVENT\_TYPE**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) enumerated type and are as follows.</span></span>

-   <span data-ttu-id="e3d2e-106">IKE/AuthIP-hauptmodusfehler.</span><span class="sxs-lookup"><span data-stu-id="e3d2e-106">IKE/AuthIP main mode failures.</span></span>
-   <span data-ttu-id="e3d2e-107">IKE/AuthIP-Schnellmodus Fehler.</span><span class="sxs-lookup"><span data-stu-id="e3d2e-107">IKE/AuthIP quick mode failures.</span></span>
-   <span data-ttu-id="e3d2e-108">AuthIP-Fehler im erweiterten Modus.</span><span class="sxs-lookup"><span data-stu-id="e3d2e-108">AuthIP extended mode failures.</span></span>
-   <span data-ttu-id="e3d2e-109">Während der Klassifizierung gelöschte Pakete.</span><span class="sxs-lookup"><span data-stu-id="e3d2e-109">Packets dropped during classification.</span></span>
-   <span data-ttu-id="e3d2e-110">Von IPSec gelöschte Pakete.</span><span class="sxs-lookup"><span data-stu-id="e3d2e-110">Packets dropped by IPsec.</span></span>

<span data-ttu-id="e3d2e-111">Standardmäßig ist die Protokollierung für WFP für eingehende Unicastpakete und für alle ausgehenden Pakete (Unicast, Multicast und Broadcast) aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e3d2e-111">By default, logging for WFP is enabled for unicast inbound packets and for all outbound packets (unicast, multicast, and broadcast).</span></span> <span data-ttu-id="e3d2e-112">Mithilfe der [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) -Verwaltungsfunktion kann die Protokollierung für den Rest der Pakete aktiviert oder für alle Pakete deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="e3d2e-112">Logging can be enabled for the rest of the packets, or disabled for all packets, through the [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) management function.</span></span> <span data-ttu-id="e3d2e-113">Ereignis Einstellungen bleiben bei Neustarts erhalten.</span><span class="sxs-lookup"><span data-stu-id="e3d2e-113">Event settings persist across reboots.</span></span>

<span data-ttu-id="e3d2e-114">Protokollierte Ereignisse werden in einem Zirkel Protokoll gespeichert, d. h. neue Ereignisse überschreiben alte, wenn das Protokoll die maximale Größe erreicht, und können mithilfe der von WFP bereitgestellten [Ereignis Verwaltungs](fwp-mgmt-functions.md) Funktionen analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="e3d2e-114">Logged events are stored in a circular log, that is new events override old ones when the log reaches its maximum size, and can be analyzed using the [event management](fwp-mgmt-functions.md) functions provided by WFP.</span></span> <span data-ttu-id="e3d2e-115">Das Ereignisprotokoll hat eine maximale Größe von 128 KB und kann ungefähr 100 bis 150 Ereignisse enthalten.</span><span class="sxs-lookup"><span data-stu-id="e3d2e-115">The event log has a maximum size of 128 KB and it can hold about 100 to 150 events.</span></span>

<span data-ttu-id="e3d2e-116">Im Allgemeinen werden Enumerationsfunktionen und [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) / [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) insbesondere zum Zeitpunkt der Erstellung des enumerationshandles eine Momentaufnahme des Protokolls erstellt.</span><span class="sxs-lookup"><span data-stu-id="e3d2e-116">Enumeration functions in general, and [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0)/[**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) in particular, take a snapshot of the log at the time the enumeration handle is created.</span></span> <span data-ttu-id="e3d2e-117">Nachfolgende Aufrufe, die denselben enumerationshandle verwenden, geben den nächsten Satz von Elementen zurück, die dem letzten Ausgabepuffer folgen.</span><span class="sxs-lookup"><span data-stu-id="e3d2e-117">Subsequent calls using the same enumeration handle return the next set of items following those in the last output buffer.</span></span>

<span data-ttu-id="e3d2e-118">Wenn eine Anwendung die WFP-Protokollierung deaktiviert (durch Aufrufen von [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)), sind alle Anwendungen betroffen.</span><span class="sxs-lookup"><span data-stu-id="e3d2e-118">When an application disables WFP logging (by calling [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)) all applications are affected.</span></span> <span data-ttu-id="e3d2e-119">Das Ereignisprotokoll wird erst bereinigt, wenn eine Anwendung die WFP-Protokollierung erneut aktiviert, das Ereignisprotokoll aber vorher nicht abgefragt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e3d2e-119">The event log is not cleaned up until an application re-enables WFP logging, but the event log cannot be queried before then.</span></span>

<span data-ttu-id="e3d2e-120">Das WFP-Ereignisprotokoll wird nach einem Neustart geleert.</span><span class="sxs-lookup"><span data-stu-id="e3d2e-120">The WFP event log is emptied after a reboot.</span></span>

 

 




