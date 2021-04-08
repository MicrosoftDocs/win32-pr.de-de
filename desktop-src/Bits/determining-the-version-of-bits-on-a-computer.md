---
title: Bestimmen der Bits-Version auf einem Computer
description: Überprüfen Sie die Version von QMgr.dll, um die Bits-Version auf dem Client Computer zu ermitteln.
ms.assetid: b6057ae4-3bf0-4304-ae50-5da5e82a0bed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c94e151608511ec59e52befdef6e4f63e44476e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707860"
---
# <a name="determining-the-version-of-bits-on-a-computer"></a><span data-ttu-id="0dfe1-103">Bestimmen der Bits-Version auf einem Computer</span><span class="sxs-lookup"><span data-stu-id="0dfe1-103">Determining the Version of BITS on a Computer</span></span>

<span data-ttu-id="0dfe1-104">Überprüfen Sie die Version von QMgr.dll, um die Bits-Version auf dem Client Computer zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="0dfe1-104">To determine the version of BITS on the client computer, check the version of QMgr.dll.</span></span> <span data-ttu-id="0dfe1-105">So ermitteln Sie die Versionsnummer der dll:</span><span class="sxs-lookup"><span data-stu-id="0dfe1-105">To find the version number of the DLL:</span></span>

-   <span data-ttu-id="0dfe1-106">Suchen Sie in% windir% \\ system32 nach QMgr.dll.</span><span class="sxs-lookup"><span data-stu-id="0dfe1-106">Locate QMgr.dll in %windir%\\System32.</span></span>
-   <span data-ttu-id="0dfe1-107">Klicken Sie mit der rechten Maustaste auf QMgr.dll und dann auf **Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="0dfe1-107">Right-click QMgr.dll and click **Properties**.</span></span>
-   <span data-ttu-id="0dfe1-108">Klicken Sie auf die Registerkarte **Version** .</span><span class="sxs-lookup"><span data-stu-id="0dfe1-108">Click the **Version** tab.</span></span>
-   <span data-ttu-id="0dfe1-109">Beachten Sie die Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="0dfe1-109">Note the version number.</span></span>

<span data-ttu-id="0dfe1-110">Sie können auch den folgenden PowerShell-Code verwenden, um die Version der DLL-Datei auf Ihrem System zu ermitteln:</span><span class="sxs-lookup"><span data-stu-id="0dfe1-110">You can also use the following PowerShell code to determine the version of the .dll on your system:</span></span>

`get-item "C:\Windows\System32\qmgr.dll" | Select-Object -ExpandProperty VersionInfo`

<span data-ttu-id="0dfe1-111">Wenn die dll auch in% windir% \\ system32 \\ Bits vorhanden ist, wiederholen Sie die vorherigen Schritte.</span><span class="sxs-lookup"><span data-stu-id="0dfe1-111">If the DLL also exists in %windir%\\System32\\Bits, repeat the previous steps.</span></span> <span data-ttu-id="0dfe1-112">Bits verwendet die DLL mit der höheren Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="0dfe1-112">BITS uses the DLL with the higher version number.</span></span>

<span data-ttu-id="0dfe1-113">In der folgenden Tabelle sind die Versionen von Bits und ihre entsprechenden QMgr.dll Dateiversionsnummern aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0dfe1-113">The following table lists the versions of BITS and their corresponding QMgr.dll file version numbers.</span></span>



| <span data-ttu-id="0dfe1-114">BITS-Version</span><span class="sxs-lookup"><span data-stu-id="0dfe1-114">BITS version</span></span> | <span data-ttu-id="0dfe1-115">Versionsnummer der QMgr.dll Datei</span><span class="sxs-lookup"><span data-stu-id="0dfe1-115">QMgr.dll file version number</span></span> |
|--------------|------------------------------|
| <span data-ttu-id="0dfe1-116">Bits 10,1</span><span class="sxs-lookup"><span data-stu-id="0dfe1-116">BITS 10.1</span></span>    | <span data-ttu-id="0dfe1-117">7.8. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="0dfe1-117">7.8.xxxx.xxxx</span></span>                |
| <span data-ttu-id="0dfe1-118">Bits 5,0</span><span class="sxs-lookup"><span data-stu-id="0dfe1-118">BITS 5.0</span></span>     | <span data-ttu-id="0dfe1-119">7.7. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="0dfe1-119">7.7.xxxx.xxxx</span></span>                |
| <span data-ttu-id="0dfe1-120">Bits 4,0</span><span class="sxs-lookup"><span data-stu-id="0dfe1-120">BITS 4.0</span></span>     | <span data-ttu-id="0dfe1-121">7.5. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="0dfe1-121">7.5.xxxx.xxxx</span></span>                |
| <span data-ttu-id="0dfe1-122">Bits 3,0</span><span class="sxs-lookup"><span data-stu-id="0dfe1-122">BITS 3.0</span></span>     | <span data-ttu-id="0dfe1-123">7.0. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="0dfe1-123">7.0.xxxx.xxxx</span></span>                |
| <span data-ttu-id="0dfe1-124">BITS 2.5</span><span class="sxs-lookup"><span data-stu-id="0dfe1-124">BITS 2.5</span></span>     | <span data-ttu-id="0dfe1-125">6.7. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="0dfe1-125">6.7.xxxx.xxxx</span></span>                |
| <span data-ttu-id="0dfe1-126">BITS 2,0</span><span class="sxs-lookup"><span data-stu-id="0dfe1-126">BITS 2.0</span></span>     | <span data-ttu-id="0dfe1-127">6.6. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="0dfe1-127">6.6.xxxx.xxxx</span></span>                |
| <span data-ttu-id="0dfe1-128">Bits 1,5</span><span class="sxs-lookup"><span data-stu-id="0dfe1-128">BITS 1.5</span></span>     | <span data-ttu-id="0dfe1-129">6.5. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="0dfe1-129">6.5.xxxx.xxxx</span></span>                |
| <span data-ttu-id="0dfe1-130">Bits 1,2</span><span class="sxs-lookup"><span data-stu-id="0dfe1-130">BITS 1.2</span></span>     | <span data-ttu-id="0dfe1-131">6.2. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="0dfe1-131">6.2.xxxx.xxxx</span></span>                |
| <span data-ttu-id="0dfe1-132">Bits 1,0</span><span class="sxs-lookup"><span data-stu-id="0dfe1-132">BITS 1.0</span></span>     | <span data-ttu-id="0dfe1-133">6.0. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="0dfe1-133">6.0.xxxx.xxxx</span></span>                |



 

<span data-ttu-id="0dfe1-134">Mit den symbolischen Klassen Bezeichners können Sie auch die Version von Bits ermitteln, die auf dem Computer registriert ist.</span><span class="sxs-lookup"><span data-stu-id="0dfe1-134">You can also use the symbolic class identifiers to determine the version of BITS that is registered on the computer.</span></span> <span data-ttu-id="0dfe1-135">In der folgenden Tabelle werden die Versionen von Bits und ihre entsprechenden symbolischen Klassen Bezeichner aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0dfe1-135">The following table lists the versions of BITS and their corresponding symbolic class identifiers.</span></span> <span data-ttu-id="0dfe1-136">Die **cokreateinstance** -Funktion gibt **RegDB \_ E \_ classnotreg** zurück, wenn die Klasse nicht registriert ist.</span><span class="sxs-lookup"><span data-stu-id="0dfe1-136">The **CoCreateInstance** function returns **REGDB\_E\_CLASSNOTREG** if the class is not registered.</span></span>



| <span data-ttu-id="0dfe1-137">BITS-Version</span><span class="sxs-lookup"><span data-stu-id="0dfe1-137">BITS version</span></span>  | <span data-ttu-id="0dfe1-138">Symbolischer Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0dfe1-138">Symbolic class identifier</span></span>         |
|---------------|-----------------------------------|
| <span data-ttu-id="0dfe1-139">Bits 10,1</span><span class="sxs-lookup"><span data-stu-id="0dfe1-139">BITS 10.1</span></span>     | <span data-ttu-id="0dfe1-140">CLSID \_ BackgroundCopyManager10 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0dfe1-140">CLSID\_BackgroundCopyManager10\_1</span></span> |
| <span data-ttu-id="0dfe1-141">Bits 5,0</span><span class="sxs-lookup"><span data-stu-id="0dfe1-141">BITS 5.0</span></span>      | <span data-ttu-id="0dfe1-142">CLSID \_ BackgroundCopyManager5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0dfe1-142">CLSID\_BackgroundCopyManager5\_0</span></span>  |
| <span data-ttu-id="0dfe1-143">Bits 4,0</span><span class="sxs-lookup"><span data-stu-id="0dfe1-143">BITS 4.0</span></span>      | <span data-ttu-id="0dfe1-144">CLSID \_ BackgroundCopyManager4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0dfe1-144">CLSID\_BackgroundCopyManager4\_0</span></span>  |
| <span data-ttu-id="0dfe1-145">Bits 3,0</span><span class="sxs-lookup"><span data-stu-id="0dfe1-145">BITS 3.0</span></span>      | <span data-ttu-id="0dfe1-146">CLSID \_ BackgroundCopyManager3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0dfe1-146">CLSID\_BackgroundCopyManager3\_0</span></span>  |
| <span data-ttu-id="0dfe1-147">BITS 2.5</span><span class="sxs-lookup"><span data-stu-id="0dfe1-147">BITS 2.5</span></span>      | <span data-ttu-id="0dfe1-148">CLSID \_ BackgroundCopyManager2 \_ 5</span><span class="sxs-lookup"><span data-stu-id="0dfe1-148">CLSID\_BackgroundCopyManager2\_5</span></span>  |
| <span data-ttu-id="0dfe1-149">BITS 2,0</span><span class="sxs-lookup"><span data-stu-id="0dfe1-149">BITS 2.0</span></span>      | <span data-ttu-id="0dfe1-150">CLSID \_ BackgroundCopyManager2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0dfe1-150">CLSID\_BackgroundCopyManager2\_0</span></span>  |
| <span data-ttu-id="0dfe1-151">Bits 1,5</span><span class="sxs-lookup"><span data-stu-id="0dfe1-151">BITS 1.5</span></span>      | <span data-ttu-id="0dfe1-152">CLSID \_ BackgroundCopyManager1 \_ 5</span><span class="sxs-lookup"><span data-stu-id="0dfe1-152">CLSID\_BackgroundCopyManager1\_5</span></span>  |
| <span data-ttu-id="0dfe1-153">Bits 1,2, 1,0</span><span class="sxs-lookup"><span data-stu-id="0dfe1-153">BITS 1.2, 1.0</span></span> | <span data-ttu-id="0dfe1-154">CLSID- \_ backgroundcopymanager</span><span class="sxs-lookup"><span data-stu-id="0dfe1-154">CLSID\_BackgroundCopyManager</span></span>      |



 

 

 




