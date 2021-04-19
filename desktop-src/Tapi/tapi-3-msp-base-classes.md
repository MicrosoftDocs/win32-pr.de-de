---
description: In diesem Dokument werden das Design und die Verwendung der MSP-Basisklassen beschrieben. Die Verwendung dieser Klassen ist nicht erforderlich, aber die meisten Entwickler werden feststellen, dass Sie das Entwickeln eines DirectShow-basierten MSP für TAPI 3S New MSPi vereinfachen.
ms.assetid: 97597dcf-eb18-47aa-b0ed-a43286d5d134
title: TAPI 3-MSP-Basisklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb7c7958847ef7bf699cfe4810f7133ef0b4bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373299"
---
# <a name="tapi-3-msp-base-classes"></a><span data-ttu-id="2dc9e-104">TAPI 3-MSP-Basisklassen</span><span class="sxs-lookup"><span data-stu-id="2dc9e-104">TAPI 3 MSP Base Classes</span></span>

<span data-ttu-id="2dc9e-105">In diesem Dokument werden das Design und die Verwendung der MSP-Basisklassen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2dc9e-105">This document describes the design and use of the MSP Base Classes.</span></span> <span data-ttu-id="2dc9e-106">Die Verwendung dieser Klassen ist nicht erforderlich, aber die meisten Entwickler werden feststellen, dass Sie die Aufgabe der Entwicklung eines DirectShow-basierten MSP für die neue MSPi von TAPI 3 vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="2dc9e-106">Use of these classes is not required, but most developers will find they simplify the task of building a DirectShow-based MSP for TAPI 3's new MSPI.</span></span>

<span data-ttu-id="2dc9e-107">Quellcode für die MSP-Basisklassen finden Sie im Verzeichnis "Samples" des Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="2dc9e-107">Source code for the MSP base classes can be found in the Samples directory of the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="2dc9e-108">Es wird davon ausgegangen, dass Sie mit com, ATL, DirectShow und C++ vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="2dc9e-108">Familiarity with COM, ATL, DirectShow, and C++ is assumed.</span></span> <span data-ttu-id="2dc9e-109">Der Reader muss auch das allgemeine Material in [über den Media Service Provider (MSP)](about-the-media-service-provider-msp-.md) und in der [Media Service Provider Interface (MSPi)](media-service-provider-interface-mspi-.md)kennen.</span><span class="sxs-lookup"><span data-stu-id="2dc9e-109">The reader must also know the general material in [About the Media Service Provider (MSP)](about-the-media-service-provider-msp-.md) and in [Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md).</span></span>

<span data-ttu-id="2dc9e-110">ATL 2,1 ist für Windows 2000 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2dc9e-110">ATL 2.1 is required for Windows 2000.</span></span> <span data-ttu-id="2dc9e-111">Ab Windows XP werden sowohl ATL 2,1 als auch 3,0 kompiliert.</span><span class="sxs-lookup"><span data-stu-id="2dc9e-111">Starting with Windows XP, both ATL 2.1 and 3.0 will compile.</span></span>

<span data-ttu-id="2dc9e-112">MSP-Basisklassen Bibliotheken (verfügbar im SDK):</span><span class="sxs-lookup"><span data-stu-id="2dc9e-112">MSP Base Class Libraries (available in the SDK):</span></span>

-   <span data-ttu-id="2dc9e-113">Mspbase. lib</span><span class="sxs-lookup"><span data-stu-id="2dc9e-113">Mspbase.lib</span></span>
-   <span data-ttu-id="2dc9e-114">Mspid. lib</span><span class="sxs-lookup"><span data-stu-id="2dc9e-114">Mspid.lib</span></span>
-   <span data-ttu-id="2dc9e-115">"Ermbase. lib"</span><span class="sxs-lookup"><span data-stu-id="2dc9e-115">Strmbase.lib</span></span>
-   <span data-ttu-id="2dc9e-116">Tmuid. lib</span><span class="sxs-lookup"><span data-stu-id="2dc9e-116">Tmuid.lib</span></span>
    > [!Note]  
    > <span data-ttu-id="2dc9e-117">Es sollte dynamisch anstelle statischer Verknüpfungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2dc9e-117">Dynamic rather than static linking should be used.</span></span>

     

<span data-ttu-id="2dc9e-118">MSP-Basisklassen Header Dateien (verfügbar im SDK):</span><span class="sxs-lookup"><span data-stu-id="2dc9e-118">MSP Base Class Header Files (available in the SDK):</span></span>

-   <span data-ttu-id="2dc9e-119">Mspaddr. h</span><span class="sxs-lookup"><span data-stu-id="2dc9e-119">Mspaddr.h</span></span>
-   <span data-ttu-id="2dc9e-120">Mspbase. h</span><span class="sxs-lookup"><span data-stu-id="2dc9e-120">Mspbase.h</span></span>
-   <span data-ttu-id="2dc9e-121">"Mspcall. h"</span><span class="sxs-lookup"><span data-stu-id="2dc9e-121">Mspcall.h</span></span>
-   <span data-ttu-id="2dc9e-122">Msplog. h</span><span class="sxs-lookup"><span data-stu-id="2dc9e-122">Msplog.h</span></span>
-   <span data-ttu-id="2dc9e-123">Mspstraum. h</span><span class="sxs-lookup"><span data-stu-id="2dc9e-123">Mspstrm.h</span></span>
-   <span data-ttu-id="2dc9e-124">Mspterm. h</span><span class="sxs-lookup"><span data-stu-id="2dc9e-124">Mspterm.h</span></span>
-   <span data-ttu-id="2dc9e-125">Mspthrd. h</span><span class="sxs-lookup"><span data-stu-id="2dc9e-125">Mspthrd.h</span></span>
-   <span data-ttu-id="2dc9e-126">Msptmac. h</span><span class="sxs-lookup"><span data-stu-id="2dc9e-126">Msptmac.h</span></span>
-   <span data-ttu-id="2dc9e-127">Msptmvc. h</span><span class="sxs-lookup"><span data-stu-id="2dc9e-127">Msptmvc.h</span></span>
-   <span data-ttu-id="2dc9e-128">Msptrmvc. h</span><span class="sxs-lookup"><span data-stu-id="2dc9e-128">Msptrmvc.h</span></span>
-   <span data-ttu-id="2dc9e-129">Msptrmac. h</span><span class="sxs-lookup"><span data-stu-id="2dc9e-129">Msptrmac.h</span></span>
-   <span data-ttu-id="2dc9e-130">Msptrmar. h</span><span class="sxs-lookup"><span data-stu-id="2dc9e-130">Msptrmar.h</span></span>
-   <span data-ttu-id="2dc9e-131">Msputils. h</span><span class="sxs-lookup"><span data-stu-id="2dc9e-131">Msputils.h</span></span>

<span data-ttu-id="2dc9e-132">Quelldateien der MSP-Basisklasse (in den SDK-Beispielen verfügbar):</span><span class="sxs-lookup"><span data-stu-id="2dc9e-132">MSP Base Class Source Files (available in the SDK Samples):</span></span>

-   <span data-ttu-id="2dc9e-133">Mspaddr. cpp</span><span class="sxs-lookup"><span data-stu-id="2dc9e-133">Mspaddr.cpp</span></span>
-   <span data-ttu-id="2dc9e-134">Mspcall. cpp</span><span class="sxs-lookup"><span data-stu-id="2dc9e-134">Mspcall.cpp</span></span>
-   <span data-ttu-id="2dc9e-135">Msplog. cpp</span><span class="sxs-lookup"><span data-stu-id="2dc9e-135">Msplog.cpp</span></span>
-   <span data-ttu-id="2dc9e-136">Mspstraum. cpp</span><span class="sxs-lookup"><span data-stu-id="2dc9e-136">Mspstrm.cpp</span></span>
-   <span data-ttu-id="2dc9e-137">Mspterm. cpp</span><span class="sxs-lookup"><span data-stu-id="2dc9e-137">Mspterm.cpp</span></span>
-   <span data-ttu-id="2dc9e-138">Mspthrd. cpp</span><span class="sxs-lookup"><span data-stu-id="2dc9e-138">Mspthrd.cpp</span></span>
-   <span data-ttu-id="2dc9e-139">Msptrmac. cpp</span><span class="sxs-lookup"><span data-stu-id="2dc9e-139">Msptrmac.cpp</span></span>
-   <span data-ttu-id="2dc9e-140">Msptrmar. cpp</span><span class="sxs-lookup"><span data-stu-id="2dc9e-140">Msptrmar.cpp</span></span>
-   <span data-ttu-id="2dc9e-141">Msptrmvc. cpp</span><span class="sxs-lookup"><span data-stu-id="2dc9e-141">Msptrmvc.cpp</span></span>
-   <span data-ttu-id="2dc9e-142">Msputils. cpp</span><span class="sxs-lookup"><span data-stu-id="2dc9e-142">Msputils.cpp</span></span>

 

 



