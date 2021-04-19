---
description: Das Erstellen eines Erfassungs Filters, der mit Netzwerkmonitor funktioniert, ist ein fünfstufiger Prozess.
ms.assetid: 04be791c-43c5-44c2-8ab0-799a99974bf6
title: Erstellen eines Monitor Erfassungs Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097a8276bd6a1f311b343787b3f06175d9b7091f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347991"
---
# <a name="creating-a-monitor-capture-filter"></a><span data-ttu-id="265e7-103">Erstellen eines Monitor Erfassungs Filters</span><span class="sxs-lookup"><span data-stu-id="265e7-103">Creating a Monitor Capture Filter</span></span>

<span data-ttu-id="265e7-104">Das Erstellen eines Erfassungs Filters, der mit Netzwerkmonitor funktioniert, ist ein fünfstufiger Prozess:</span><span class="sxs-lookup"><span data-stu-id="265e7-104">Creating a capture filter that works with Network Monitor is a five-step process:</span></span>

-   [<span data-ttu-id="265e7-105">Festlegen von ETYPE oder SAP-Filter</span><span class="sxs-lookup"><span data-stu-id="265e7-105">Setting the Etype or SAP Filter</span></span>](writing-etypesap-filter-portion.md)
-   [<span data-ttu-id="265e7-106">Schreiben von adresstablem Filter</span><span class="sxs-lookup"><span data-stu-id="265e7-106">Writing ADDRESSTABLE Filter</span></span>](writing-addresstable-filter-portion.md)
-   [<span data-ttu-id="265e7-107">Schreiben des patternmatch-Filters</span><span class="sxs-lookup"><span data-stu-id="265e7-107">Writing the PATTERNMATCH Filter</span></span>](writing-the-patternmatch-filter.md)
-   [<span data-ttu-id="265e7-108">Clipping eines Frames</span><span class="sxs-lookup"><span data-stu-id="265e7-108">Clipping a Frame</span></span>](clipping-a-frame.md)
-   [<span data-ttu-id="265e7-109">Implementieren des Erfassungs Filter Codes</span><span class="sxs-lookup"><span data-stu-id="265e7-109">Implementing the Capture Filter Code</span></span>](implementing-the-capture-filter-code.md)

<span data-ttu-id="265e7-110">Ein [*Erfassungs Filter*](c.md) ist eine Reihe von Ergänzungen zum NPP-BLOB, die auswählen, welche Frames an den Monitor zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="265e7-110">A [*capture filter*](c.md) is a series of additions to the NPP BLOB that selects which frames are passed back to the monitor.</span></span> <span data-ttu-id="265e7-111">Wenn der NPP-BLOB von einem Monitor nicht geändert wird, wechselt der NPP in den Modus "gemischten" und sendet den gesamten Netzwerk Datenverkehr an den Monitor.</span><span class="sxs-lookup"><span data-stu-id="265e7-111">If a monitor does not alter the NPP BLOB, then the NPP will go into promiscuous mode and send all network traffic to the monitor.</span></span> <span data-ttu-id="265e7-112">Der npp ist am effizientesten, wenn er die an einen Treiber übergebenen Daten reduzieren kann, sodass ein Monitor einen Erfassungs Filter erstellen sollte.</span><span class="sxs-lookup"><span data-stu-id="265e7-112">The NPP is most efficient if it can reduce the data handed up to a driver, so a monitor should create a capture filter.</span></span> <span data-ttu-id="265e7-113">Ein Monitor legt den Erfassungs Filter fest, indem er im Aufrufe der [doconfigure](imonitor-doconfigure.md) -Funktion in das NPP-BLOB schreibt.</span><span class="sxs-lookup"><span data-stu-id="265e7-113">A monitor sets its capture filter by writing to the NPP BLOB in the call to the [DoConfigure](imonitor-doconfigure.md) function.</span></span> <span data-ttu-id="265e7-114">Anschließend ruft der mcsvc den NPP mit dem NPP-BLOB auf.</span><span class="sxs-lookup"><span data-stu-id="265e7-114">The MCSVC then calls the NPP with the NPP BLOB.</span></span> <span data-ttu-id="265e7-115">Weitere Informationen zum Erfassungs Filter, zu [Netzwerk Paket Anbietern](network-packet-providers.md) in NPPs und [Netzwerkmonitor BLOBs](network-monitor-blobs.md) für BLOB-Funktionen finden Sie unter [Erfassungs Filter](capture-filters.md) .</span><span class="sxs-lookup"><span data-stu-id="265e7-115">See [Capture Filters](capture-filters.md) for more details on the capture filter, [Network Packet Providers](network-packet-providers.md) on NPPs, and [Network Monitor Blobs](network-monitor-blobs.md) on BLOB functions.</span></span>

 

 



