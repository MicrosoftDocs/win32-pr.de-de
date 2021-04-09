---
title: Entwickeln von RPC-Windows-Anwendungen
description: Wenn Sie das Platform Software Development Kit (SDK) installieren, werden die folgenden RPC-Entwicklungsumgebungen, die Laufzeitbibliotheken und Tools automatisch installiert.
ms.assetid: d5da3bca-5251-4ba4-b873-0817fe0f298d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b418358649d0cf7205b9a3bde236cf66d3ce81e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039497"
---
# <a name="developing-rpc-windows-applications"></a><span data-ttu-id="3adb2-103">Entwickeln von RPC-Windows-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="3adb2-103">Developing RPC Windows Applications</span></span>

<span data-ttu-id="3adb2-104">Wenn Sie das Platform Software Development Kit (SDK) installieren, werden die folgende RPC-Entwicklungsumgebung, die Laufzeitbibliotheken und-Tools automatisch installiert:</span><span class="sxs-lookup"><span data-stu-id="3adb2-104">When you install the Platform Software Development Kit (SDK), the following RPC development environment, the run-time libraries, and tools are automatically installed:</span></span>

-   <span data-ttu-id="3adb2-105">C/C++-sprach Header (. H) Dateien</span><span class="sxs-lookup"><span data-stu-id="3adb2-105">C/C++ language header (.H) files</span></span>
-   <span data-ttu-id="3adb2-106">RPC-Import Bibliotheken (. lib)</span><span class="sxs-lookup"><span data-stu-id="3adb2-106">RPC import libraries (.lib) files</span></span>
-   <span data-ttu-id="3adb2-107">Beispiel Programme</span><span class="sxs-lookup"><span data-stu-id="3adb2-107">Sample programs</span></span>
-   <span data-ttu-id="3adb2-108">RPC-Verweis Hilfedateien</span><span class="sxs-lookup"><span data-stu-id="3adb2-108">RPC reference Help files</span></span>
-   <span data-ttu-id="3adb2-109">Das Hilfsprogramm **"uuidgen**</span><span class="sxs-lookup"><span data-stu-id="3adb2-109">The **uuidgen** utility</span></span>

<span data-ttu-id="3adb2-110">Wenn Sie Windows installieren, werden Folgendes installiert:</span><span class="sxs-lookup"><span data-stu-id="3adb2-110">When you install Windows, the following are installed:</span></span>

-   <span data-ttu-id="3adb2-111">RPC-Lauf Zeit-DLLs</span><span class="sxs-lookup"><span data-stu-id="3adb2-111">RPC Run-time DLLs</span></span>
-   <span data-ttu-id="3adb2-112">Microsoft Locator (wird unter Windows Vista und höher nicht unterstützt)</span><span class="sxs-lookup"><span data-stu-id="3adb2-112">Microsoft Locator (not supported on Windows Vista and later)</span></span>
-   <span data-ttu-id="3adb2-113">RPC-Endpunkt-Mapping-Dienste</span><span class="sxs-lookup"><span data-stu-id="3adb2-113">RPC Endpoint-mapping services</span></span>

<span data-ttu-id="3adb2-114">Die folgenden RPC-Import Bibliotheken.</span><span class="sxs-lookup"><span data-stu-id="3adb2-114">The following RPC import libraries.</span></span>



| <span data-ttu-id="3adb2-115">Bibliothek importieren</span><span class="sxs-lookup"><span data-stu-id="3adb2-115">Import library</span></span> | <span data-ttu-id="3adb2-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3adb2-116">Description</span></span>                |
|----------------|----------------------------|
| <span data-ttu-id="3adb2-117">Rpcns4. lib</span><span class="sxs-lookup"><span data-stu-id="3adb2-117">Rpcns4.lib</span></span>     | <span data-ttu-id="3adb2-118">Name-Service-Funktionen</span><span class="sxs-lookup"><span data-stu-id="3adb2-118">Name-service functions</span></span>     |
| <span data-ttu-id="3adb2-119">Rpcrt4. lib</span><span class="sxs-lookup"><span data-stu-id="3adb2-119">Rpcrt4.lib</span></span>     | <span data-ttu-id="3adb2-120">Windows-Lauf Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="3adb2-120">Windows run-time functions</span></span> |



 

> [!Note]  
> <span data-ttu-id="3adb2-121">Rpcns4. lib ist veraltet und wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3adb2-121">Rpcns4.lib is obsolete and no longer supported.</span></span>

 

<span data-ttu-id="3adb2-122">Die folgenden RPC-Bibliotheken sind für die Unterstützung der untergeordneten Ebene enthalten.</span><span class="sxs-lookup"><span data-stu-id="3adb2-122">The following RPC libraries are included for down-level support.</span></span>



| <span data-ttu-id="3adb2-123">Dynamic Link Library</span><span class="sxs-lookup"><span data-stu-id="3adb2-123">Dynamic-link library</span></span> | <span data-ttu-id="3adb2-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3adb2-124">Description</span></span>                 | <span data-ttu-id="3adb2-125">Plattform</span><span class="sxs-lookup"><span data-stu-id="3adb2-125">Platform</span></span>                           |
|----------------------|-----------------------------|------------------------------------|
| <span data-ttu-id="3adb2-126">Rpcltc1.dll</span><span class="sxs-lookup"><span data-stu-id="3adb2-126">Rpcltc1.dll</span></span>          | <span data-ttu-id="3adb2-127">Client Named Pipe-Transport</span><span class="sxs-lookup"><span data-stu-id="3adb2-127">Client named-pipe transport</span></span> | <span data-ttu-id="3adb2-128">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="3adb2-128">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="3adb2-129">Rpclts1.dll</span><span class="sxs-lookup"><span data-stu-id="3adb2-129">Rpclts1.dll</span></span>          | <span data-ttu-id="3adb2-130">Server Named Pipe-Transport</span><span class="sxs-lookup"><span data-stu-id="3adb2-130">Server named-pipe transport</span></span> | <span data-ttu-id="3adb2-131">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="3adb2-131">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="3adb2-132">Rpcltc3.dll</span><span class="sxs-lookup"><span data-stu-id="3adb2-132">Rpcltc3.dll</span></span>          | <span data-ttu-id="3adb2-133">TCP/IP-Client Transport</span><span class="sxs-lookup"><span data-stu-id="3adb2-133">Client TCP/IP transport</span></span>     | <span data-ttu-id="3adb2-134">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="3adb2-134">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="3adb2-135">Rpclts3.dll</span><span class="sxs-lookup"><span data-stu-id="3adb2-135">Rpclts3.dll</span></span>          | <span data-ttu-id="3adb2-136">Server-TCP/IP-Transport</span><span class="sxs-lookup"><span data-stu-id="3adb2-136">Server TCP/IP transport</span></span>     | <span data-ttu-id="3adb2-137">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="3adb2-137">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="3adb2-138">Rpcltc5.dll</span><span class="sxs-lookup"><span data-stu-id="3adb2-138">Rpcltc5.dll</span></span>          | <span data-ttu-id="3adb2-139">Client-NetBIOS-Transport</span><span class="sxs-lookup"><span data-stu-id="3adb2-139">Client NetBIOS transport</span></span>    | <span data-ttu-id="3adb2-140">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="3adb2-140">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="3adb2-141">Rpclts5.dll</span><span class="sxs-lookup"><span data-stu-id="3adb2-141">Rpclts5.dll</span></span>          | <span data-ttu-id="3adb2-142">Server-NetBIOS-Transport</span><span class="sxs-lookup"><span data-stu-id="3adb2-142">Server NetBIOS transport</span></span>    | <span data-ttu-id="3adb2-143">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="3adb2-143">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="3adb2-144">Rpcltc6.dll</span><span class="sxs-lookup"><span data-stu-id="3adb2-144">Rpcltc6.dll</span></span>          | <span data-ttu-id="3adb2-145">Client-SPX-Transport</span><span class="sxs-lookup"><span data-stu-id="3adb2-145">Client SPX transport</span></span>        | <span data-ttu-id="3adb2-146">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="3adb2-146">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="3adb2-147">Rpclts6.dll</span><span class="sxs-lookup"><span data-stu-id="3adb2-147">Rpclts6.dll</span></span>          | <span data-ttu-id="3adb2-148">Server-SPX-Transport</span><span class="sxs-lookup"><span data-stu-id="3adb2-148">Server SPX transport</span></span>        | <span data-ttu-id="3adb2-149">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="3adb2-149">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="3adb2-150">Rpcdgc6.dll</span><span class="sxs-lookup"><span data-stu-id="3adb2-150">Rpcdgc6.dll</span></span>          | <span data-ttu-id="3adb2-151">IPX-Client Transport</span><span class="sxs-lookup"><span data-stu-id="3adb2-151">Client IPX transport</span></span>        | <span data-ttu-id="3adb2-152">Windows NT</span><span class="sxs-lookup"><span data-stu-id="3adb2-152">Windows NT</span></span>                         |
| <span data-ttu-id="3adb2-153">Rpcdgs6.dll</span><span class="sxs-lookup"><span data-stu-id="3adb2-153">Rpcdgs6.dll</span></span>          | <span data-ttu-id="3adb2-154">IPX-Server Transport</span><span class="sxs-lookup"><span data-stu-id="3adb2-154">Server IPX transport</span></span>        | <span data-ttu-id="3adb2-155">Windows NT</span><span class="sxs-lookup"><span data-stu-id="3adb2-155">Windows NT</span></span>                         |
| <span data-ttu-id="3adb2-156">Rpcdgc3.dll</span><span class="sxs-lookup"><span data-stu-id="3adb2-156">Rpcdgc3.dll</span></span>          | <span data-ttu-id="3adb2-157">UDP-Client Transport</span><span class="sxs-lookup"><span data-stu-id="3adb2-157">Client UDP transport</span></span>        | <span data-ttu-id="3adb2-158">Windows NT</span><span class="sxs-lookup"><span data-stu-id="3adb2-158">Windows NT</span></span>                         |
| <span data-ttu-id="3adb2-159">Rpcdgs3.dll</span><span class="sxs-lookup"><span data-stu-id="3adb2-159">Rpcdgs3.dll</span></span>          | <span data-ttu-id="3adb2-160">UDP-Server Transport</span><span class="sxs-lookup"><span data-stu-id="3adb2-160">Server UDP transport</span></span>        | <span data-ttu-id="3adb2-161">Windows NT</span><span class="sxs-lookup"><span data-stu-id="3adb2-161">Windows NT</span></span>                         |



 

<span data-ttu-id="3adb2-162">Außerdem benötigen Sie den Microsoft Interface Definition Language-Compiler (mittlerer l).</span><span class="sxs-lookup"><span data-stu-id="3adb2-162">You will also need the Microsoft Interface Definition Language (MIDL) compiler.</span></span> <span data-ttu-id="3adb2-163">Weitere Informationen finden Sie unter [using the Mittel l Compiler](/windows/desktop/Midl/using-the-midl-compiler-2).</span><span class="sxs-lookup"><span data-stu-id="3adb2-163">For more information, see [Using The MIDL Compiler](/windows/desktop/Midl/using-the-midl-compiler-2).</span></span>

 

 