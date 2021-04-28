---
description: Offlineregistrierungsbibliothek
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: Offlineregistrierungsbibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1aa5acdd7904516608413ff973e60e81c296c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089248"
---
# <a name="offline-registry-library"></a><span data-ttu-id="f0166-103">Offlineregistrierungsbibliothek</span><span class="sxs-lookup"><span data-stu-id="f0166-103">Offline Registry Library</span></span>

## <a name="purpose"></a><span data-ttu-id="f0166-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="f0166-104">Purpose</span></span>

<span data-ttu-id="f0166-105">Die Offlineregistrierungsbibliothek (Offreg.dll) wird verwendet, um eine Registrierungsstruktur außerhalb der aktiven Systemregistrierung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f0166-105">The offline registry library (Offreg.dll) is used to modify a registry hive outside the active system registry.</span></span> <span data-ttu-id="f0166-106">Diese Bibliothek ist für Registrierungsupdateszenarien wie die Wartung eines Betriebssystemimages vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="f0166-106">This library is intended for registry update scenarios such as servicing an operating system image.</span></span> <span data-ttu-id="f0166-107">Die Bibliothek unterstützt Registrierungsstrukturformate ab Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f0166-107">The library supports registry hive formats starting with Windows Vista.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="f0166-108">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="f0166-108">Developer audience</span></span>

<span data-ttu-id="f0166-109">Diese Technologie ist für Originalgerätehersteller (OEMs), Anbieter von Antiviren- und Antischadsoftware sowie für andere Anwendungsentwickler vorgesehen, die Registrierungsstrukturdateien analysieren müssen, ohne sie in die aktive Registrierung laden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="f0166-109">This technology is for original equipment manufacturers (OEMs), antivirus and antimalware software vendors, and other application developers who must be able to parse registry hive files without loading them into the active registry.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="f0166-110">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="f0166-110">Run-time requirements</span></span>

<span data-ttu-id="f0166-111">Die Offlineregistrierungsbibliothek wird als binäre verteilbare Dll (Dynamic Link Library) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f0166-111">The offline registry library is provided as a binary redistributable dynamic-link library (DLL).</span></span> <span data-ttu-id="f0166-112">Diese Bibliothek wird unter den folgenden Versionen von Windows ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="f0166-112">This library runs on the following versions of Windows:</span></span>

<dl> <span data-ttu-id="f0166-113">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f0166-113">Windows Server 2016</span></span>  
<span data-ttu-id="f0166-114">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f0166-114">Windows 10</span></span>  
<span data-ttu-id="f0166-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f0166-115">Windows 8.1</span></span>  
<span data-ttu-id="f0166-116">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f0166-116">Windows Server 2012 R2</span></span>  
<span data-ttu-id="f0166-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f0166-117">Windows 8</span></span>  
<span data-ttu-id="f0166-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f0166-118">Windows Server 2012</span></span>  
<span data-ttu-id="f0166-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f0166-119">Windows 7</span></span>  
<span data-ttu-id="f0166-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f0166-120">Windows Server 2008 R2</span></span>  
<span data-ttu-id="f0166-121">WindowsServer 2008</span><span class="sxs-lookup"><span data-stu-id="f0166-121">Windows Server 2008</span></span>  
<span data-ttu-id="f0166-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0166-122">Windows Vista</span></span>  
</dl>

<span data-ttu-id="f0166-123">Anwendungen sollten mithilfe dynamischer Verknüpfungen mit Offreg.dll verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="f0166-123">Applications should link to Offreg.dll using dynamic linking.</span></span>

<span data-ttu-id="f0166-124">Offreg.dll wird im Windows-Treiberkit (WDK) für Windows 10 und frühere Versionen des Windows-Betriebssystems bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f0166-124">Offreg.dll is provided in the Windows Driver Kit (WDK) for Windows 10 and earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="f0166-125">Informationen zum Abrufen des WDK finden Sie unter [How to Get the WDK and the WLK (Abrufen des WDK und des WLK)](/windows-hardware/drivers/download-the-wdk) oder auf der [MSDN-Abonnementwebsite.](https://msdn.microsoft.com/subscriptions/default.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0166-125">For information about obtaining the WDK, see [How to Get the WDK and the WLK](/windows-hardware/drivers/download-the-wdk) or visit the [MSDN Subscriptions](https://msdn.microsoft.com/subscriptions/default.aspx) website.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f0166-126">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="f0166-126">In this section</span></span>

-   [<span data-ttu-id="f0166-127">**Informationen zur Offlineregistrierungsbibliothek**</span><span class="sxs-lookup"><span data-stu-id="f0166-127">**About the Offline Registry Library**</span></span>](about-the-offline-registry-library.md)
-   [<span data-ttu-id="f0166-128">**Funktionen der Offlineregistrierungsbibliothek**</span><span class="sxs-lookup"><span data-stu-id="f0166-128">**Offline Registry Library Functions**</span></span>](offline-registry-library-functions.md)

 

 
