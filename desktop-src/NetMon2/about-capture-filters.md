---
description: Ein Erfassungs Filter ist ein Element einer NPP-Anwendung, das den Netzwerkmonitor Treiber (Nmnt.sys) anweist, welche Frames von Netzwerkdaten beibehalten werden sollen und welche Frames ignoriert werden sollen.
ms.assetid: 6ab17e18-bd97-42a8-b569-b205ac19ffd1
title: Informationen zu Erfassungs Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7226bb7dc5bc214ab2e09504cc232e1bf591840f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359021"
---
# <a name="about-capture-filters"></a><span data-ttu-id="6aeaf-103">Informationen zu Erfassungs Filtern</span><span class="sxs-lookup"><span data-stu-id="6aeaf-103">About Capture Filters</span></span>

<span data-ttu-id="6aeaf-104">Ein Erfassungs Filter ist ein Element einer NPP-Anwendung, das den Netzwerkmonitor Treiber (Nmnt.sys) anweist, welche Frames von Netzwerkdaten beibehalten werden sollen und welche Frames ignoriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6aeaf-104">A capture filter is an element of an NPP application that instructs the Network Monitor driver (Nmnt.sys) which frames of network data to retain and which frames to ignore.</span></span> <span data-ttu-id="6aeaf-105">Der Vorteil der Festlegung eines Erfassungs Filters ist eine höhere Effizienz.</span><span class="sxs-lookup"><span data-stu-id="6aeaf-105">The advantage of setting a capture filter is greater efficiency.</span></span> <span data-ttu-id="6aeaf-106">Sie müssen keine aufgezeichneten Frames untersuchen. Diese werden vom Netzwerkmonitor Treiber untersucht.</span><span class="sxs-lookup"><span data-stu-id="6aeaf-106">You do not have to examine captured frames; the Network Monitor driver examines them.</span></span> <span data-ttu-id="6aeaf-107">Durch diese Vorgehensweise wird das Kopieren von Frames vermieden</span><span class="sxs-lookup"><span data-stu-id="6aeaf-107">This approach eliminates frame copying, which provides a memory use advantage.</span></span>

## <a name="capture-filter-structure"></a><span data-ttu-id="6aeaf-108">Erfassungs Filter Struktur</span><span class="sxs-lookup"><span data-stu-id="6aeaf-108">Capture Filter Structure</span></span>

<span data-ttu-id="6aeaf-109">Erfassungs Filter bestehen aus drei Elementen:</span><span class="sxs-lookup"><span data-stu-id="6aeaf-109">Capture filters consist of three elements:</span></span>

-   <span data-ttu-id="6aeaf-110">ETYPE/SAP-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="6aeaf-110">Etype/SAP settings</span></span>
-   <span data-ttu-id="6aeaf-111">Adresse</span><span class="sxs-lookup"><span data-stu-id="6aeaf-111">Address</span></span>
-   <span data-ttu-id="6aeaf-112">Muster Übereinstimmung</span><span class="sxs-lookup"><span data-stu-id="6aeaf-112">Pattern match</span></span>

<span data-ttu-id="6aeaf-113">In dieser Weise Werten diese Elemente logisch aus, welche Frames während der Ausführung einer NPP-Anwendung eingeschlossen oder ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6aeaf-113">Together, these elements logically evaluate which frames to include, or exclude, during the operation of an NPP application.</span></span> <span data-ttu-id="6aeaf-114">Der Erfassungs Filter liefert komplexe Übereinstimmungen und Ausschlüsse von Frame Elementen für die NPP-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6aeaf-114">The capture filter supplies complex matches and exclusions of frame elements to the NPP application.</span></span>

<span data-ttu-id="6aeaf-115">Netzwerkmonitor implementiert den Erfassungs Filter über eine Datenstruktur ( [**capturefilter**](the-capturefilter-structure.md)), die an den NPP weitergegeben und beim Start der Erfassung an den Netzwerkmonitor Treiber weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="6aeaf-115">Network Monitor implements the capture filter through a data structure, [**CAPTUREFILTER**](the-capturefilter-structure.md), passed to the NPP and then passed on to the Network Monitor driver when the capture starts.</span></span>

<span data-ttu-id="6aeaf-116">Weitere Informationen zu NPP-Vorgängen und BLOB-Funktionen finden Sie unter [Netzwerk Paketanbieter](network-packet-providers.md) und [Netzwerkmonitor BLOBs](network-monitor-blobs.md).</span><span class="sxs-lookup"><span data-stu-id="6aeaf-116">For more information about NPP operations and BLOB functionality, see [Network Packet Providers](network-packet-providers.md) and [Network Monitor BLOBS](network-monitor-blobs.md).</span></span>

 

 



