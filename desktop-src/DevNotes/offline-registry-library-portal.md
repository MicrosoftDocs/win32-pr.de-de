---
description: .
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: Offline-Registrierungs Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a473bde729a0047a56d7ad0fdec1c0e3133ea103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345425"
---
# <a name="offline-registry-library"></a><span data-ttu-id="04499-103">Offline-Registrierungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="04499-103">Offline Registry Library</span></span>

## <a name="purpose"></a><span data-ttu-id="04499-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="04499-104">Purpose</span></span>

<span data-ttu-id="04499-105">Die Offline Registrierungs Bibliothek (Offreg.dll) wird verwendet, um eine Registrierungs Struktur außerhalb der aktiven Systemregistrierung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="04499-105">The offline registry library (Offreg.dll) is used to modify a registry hive outside the active system registry.</span></span> <span data-ttu-id="04499-106">Diese Bibliothek ist für Registrierungs Aktualisierungs Szenarien wie die Wartung eines Betriebssystem Abbilds vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="04499-106">This library is intended for registry update scenarios such as servicing an operating system image.</span></span> <span data-ttu-id="04499-107">Die Bibliothek unterstützt Registrierungs Struktur Formate ab Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="04499-107">The library supports registry hive formats starting with Windows Vista.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="04499-108">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="04499-108">Developer audience</span></span>

<span data-ttu-id="04499-109">Diese Technologie ist für Originalgerätehersteller (OEMs), Antiviren-und antischadsoftwarehersteller und andere Anwendungsentwickler gedacht, die in der Lage sein müssen, Registrierungs-Hive-Dateien zu analysieren, ohne Sie in die aktive Registrierung zu laden.</span><span class="sxs-lookup"><span data-stu-id="04499-109">This technology is for original equipment manufacturers (OEMs), antivirus and antimalware software vendors, and other application developers who must be able to parse registry hive files without loading them into the active registry.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="04499-110">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="04499-110">Run-time requirements</span></span>

<span data-ttu-id="04499-111">Die Offline Registrierungs Bibliothek wird als binäre verteilbare dll (Dynamic-Link Library) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="04499-111">The offline registry library is provided as a binary redistributable dynamic-link library (DLL).</span></span> <span data-ttu-id="04499-112">Diese Bibliothek wird unter den folgenden Versionen von Windows ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="04499-112">This library runs on the following versions of Windows:</span></span>

<dl> <span data-ttu-id="04499-113">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="04499-113">Windows Server 2016</span></span>  
<span data-ttu-id="04499-114">Windows 10</span><span class="sxs-lookup"><span data-stu-id="04499-114">Windows 10</span></span>  
<span data-ttu-id="04499-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="04499-115">Windows 8.1</span></span>  
<span data-ttu-id="04499-116">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="04499-116">Windows Server 2012 R2</span></span>  
<span data-ttu-id="04499-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="04499-117">Windows 8</span></span>  
<span data-ttu-id="04499-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="04499-118">Windows Server 2012</span></span>  
<span data-ttu-id="04499-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="04499-119">Windows 7</span></span>  
<span data-ttu-id="04499-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="04499-120">Windows Server 2008 R2</span></span>  
<span data-ttu-id="04499-121">WindowsServer 2008</span><span class="sxs-lookup"><span data-stu-id="04499-121">Windows Server 2008</span></span>  
<span data-ttu-id="04499-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04499-122">Windows Vista</span></span>  
</dl>

<span data-ttu-id="04499-123">Anwendungen sollten mithilfe dynamischer Verknüpfungen mit Offreg.dll verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="04499-123">Applications should link to Offreg.dll using dynamic linking.</span></span>

<span data-ttu-id="04499-124">Offreg.dll wird im Windows-Treiberkit (WDK) für Windows 10 und frühere Versionen des Windows-Betriebssystems bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="04499-124">Offreg.dll is provided in the Windows Driver Kit (WDK) for Windows 10 and earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="04499-125">Weitere Informationen zum Abrufen des WDK finden Sie unter Abrufen [des WDK und der WLK](/windows-hardware/drivers/download-the-wdk) , oder besuchen Sie die Website für [MSDN-Abonnements](https://msdn.microsoft.com/subscriptions/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="04499-125">For information about obtaining the WDK, see [How to Get the WDK and the WLK](/windows-hardware/drivers/download-the-wdk) or visit the [MSDN Subscriptions](https://msdn.microsoft.com/subscriptions/default.aspx) website.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="04499-126">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="04499-126">In this section</span></span>

-   [<span data-ttu-id="04499-127">**Informationen zur Offline Registrierungs Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="04499-127">**About the Offline Registry Library**</span></span>](about-the-offline-registry-library.md)
-   [<span data-ttu-id="04499-128">**Funktionen der Offline-Registrierungs Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="04499-128">**Offline Registry Library Functions**</span></span>](offline-registry-library-functions.md)

 

 
