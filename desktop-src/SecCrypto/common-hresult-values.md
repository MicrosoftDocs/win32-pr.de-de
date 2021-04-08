---
description: Die folgenden HRESULT-Werte sind am häufigsten. Weitere Werte sind in der Header Datei Winerror. h enthalten.
ms.assetid: ce52efc3-92c7-40e4-ac49-0c54049e169f
title: Allgemeine HRESULT-Werte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a64d042d9531d026cda548b2a699ed60c0bebd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863864"
---
# <a name="common-hresult-values"></a><span data-ttu-id="18728-104">Allgemeine HRESULT-Werte</span><span class="sxs-lookup"><span data-stu-id="18728-104">Common HRESULT Values</span></span>

<span data-ttu-id="18728-105">Die folgenden HRESULT-Werte sind am häufigsten.</span><span class="sxs-lookup"><span data-stu-id="18728-105">The following HRESULT values are the most common.</span></span> <span data-ttu-id="18728-106">Weitere Werte sind in der Header Datei Winerror. h enthalten.</span><span class="sxs-lookup"><span data-stu-id="18728-106">More values are contained in the header file Winerror.h.</span></span>

<span data-ttu-id="18728-107">Hier sind die Werte, die alphabetisch nach Namen aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="18728-107">Here are the values listed alphabetically by name.</span></span>



| <span data-ttu-id="18728-108">Name</span><span class="sxs-lookup"><span data-stu-id="18728-108">Name</span></span>            | <span data-ttu-id="18728-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18728-109">Description</span></span>                         | <span data-ttu-id="18728-110">Wert</span><span class="sxs-lookup"><span data-stu-id="18728-110">Value</span></span>      |
|-----------------|-------------------------------------|------------|
| <span data-ttu-id="18728-111">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="18728-111">S\_OK</span></span>           | <span data-ttu-id="18728-112">Vorgang erfolgreich</span><span class="sxs-lookup"><span data-stu-id="18728-112">Operation successful</span></span>                | <span data-ttu-id="18728-113">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18728-113">0x00000000</span></span> |
| <span data-ttu-id="18728-114">E \_ Abbrechen</span><span class="sxs-lookup"><span data-stu-id="18728-114">E\_ABORT</span></span>        | <span data-ttu-id="18728-115">Vorgang abgebrochen</span><span class="sxs-lookup"><span data-stu-id="18728-115">Operation aborted</span></span>                   | <span data-ttu-id="18728-116">0x80004004</span><span class="sxs-lookup"><span data-stu-id="18728-116">0x80004004</span></span> |
| <span data-ttu-id="18728-117">E \_ AccessDenied</span><span class="sxs-lookup"><span data-stu-id="18728-117">E\_ACCESSDENIED</span></span> | <span data-ttu-id="18728-118">Allgemeiner Zugriffs Verweigerungs Fehler</span><span class="sxs-lookup"><span data-stu-id="18728-118">General access denied error</span></span>         | <span data-ttu-id="18728-119">0x80070005</span><span class="sxs-lookup"><span data-stu-id="18728-119">0x80070005</span></span> |
| <span data-ttu-id="18728-120">E \_ fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="18728-120">E\_FAIL</span></span>         | <span data-ttu-id="18728-121">Nicht spezifizierter Fehler</span><span class="sxs-lookup"><span data-stu-id="18728-121">Unspecified failure</span></span>                 | <span data-ttu-id="18728-122">0x80004005</span><span class="sxs-lookup"><span data-stu-id="18728-122">0x80004005</span></span> |
| <span data-ttu-id="18728-123">E- \_ handle</span><span class="sxs-lookup"><span data-stu-id="18728-123">E\_HANDLE</span></span>       | <span data-ttu-id="18728-124">Handle, das ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="18728-124">Handle that is not valid</span></span>            | <span data-ttu-id="18728-125">0x80070006</span><span class="sxs-lookup"><span data-stu-id="18728-125">0x80070006</span></span> |
| <span data-ttu-id="18728-126">E \_ invalidArg</span><span class="sxs-lookup"><span data-stu-id="18728-126">E\_INVALIDARG</span></span>   | <span data-ttu-id="18728-127">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="18728-127">One or more arguments are not valid</span></span> | <span data-ttu-id="18728-128">0x80070057</span><span class="sxs-lookup"><span data-stu-id="18728-128">0x80070057</span></span> |
| <span data-ttu-id="18728-129">E \_ nointerface</span><span class="sxs-lookup"><span data-stu-id="18728-129">E\_NOINTERFACE</span></span>  | <span data-ttu-id="18728-130">Schnittstelle nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="18728-130">No such interface supported</span></span>         | <span data-ttu-id="18728-131">0x80004002</span><span class="sxs-lookup"><span data-stu-id="18728-131">0x80004002</span></span> |
| <span data-ttu-id="18728-132">E \_ notimpl</span><span class="sxs-lookup"><span data-stu-id="18728-132">E\_NOTIMPL</span></span>      | <span data-ttu-id="18728-133">Nicht implementiert</span><span class="sxs-lookup"><span data-stu-id="18728-133">Not implemented</span></span>                     | <span data-ttu-id="18728-134">0x80004001</span><span class="sxs-lookup"><span data-stu-id="18728-134">0x80004001</span></span> |
| <span data-ttu-id="18728-135">E \_ outo-Memory</span><span class="sxs-lookup"><span data-stu-id="18728-135">E\_OUTOFMEMORY</span></span>  | <span data-ttu-id="18728-136">Fehler beim Zuordnen des erforderlichen Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="18728-136">Failed to allocate necessary memory</span></span> | <span data-ttu-id="18728-137">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="18728-137">0x8007000E</span></span> |
| <span data-ttu-id="18728-138">E- \_ Zeiger</span><span class="sxs-lookup"><span data-stu-id="18728-138">E\_POINTER</span></span>      | <span data-ttu-id="18728-139">Ungültiger Zeiger</span><span class="sxs-lookup"><span data-stu-id="18728-139">Pointer that is not valid</span></span>           | <span data-ttu-id="18728-140">0x80004003</span><span class="sxs-lookup"><span data-stu-id="18728-140">0x80004003</span></span> |
| <span data-ttu-id="18728-141">E \_ unerwartet</span><span class="sxs-lookup"><span data-stu-id="18728-141">E\_UNEXPECTED</span></span>   | <span data-ttu-id="18728-142">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="18728-142">Unexpected failure</span></span>                  | <span data-ttu-id="18728-143">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="18728-143">0x8000FFFF</span></span> |



 

<span data-ttu-id="18728-144">Dies sind die Werte, die in numerischer Reihenfolge nach Wert aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="18728-144">Here are the values listed in numeric order by value.</span></span>



| <span data-ttu-id="18728-145">Wert</span><span class="sxs-lookup"><span data-stu-id="18728-145">Value</span></span>      | <span data-ttu-id="18728-146">Name</span><span class="sxs-lookup"><span data-stu-id="18728-146">Name</span></span>            | <span data-ttu-id="18728-147">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18728-147">Description</span></span>                         |
|------------|-----------------|-------------------------------------|
| <span data-ttu-id="18728-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18728-148">0x00000000</span></span> | <span data-ttu-id="18728-149">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="18728-149">S\_OK</span></span>           | <span data-ttu-id="18728-150">Vorgang erfolgreich</span><span class="sxs-lookup"><span data-stu-id="18728-150">Operation successful</span></span>                |
| <span data-ttu-id="18728-151">0x80004001</span><span class="sxs-lookup"><span data-stu-id="18728-151">0x80004001</span></span> | <span data-ttu-id="18728-152">E \_ notimpl</span><span class="sxs-lookup"><span data-stu-id="18728-152">E\_NOTIMPL</span></span>      | <span data-ttu-id="18728-153">Nicht implementiert</span><span class="sxs-lookup"><span data-stu-id="18728-153">Not implemented</span></span>                     |
| <span data-ttu-id="18728-154">0x80004002</span><span class="sxs-lookup"><span data-stu-id="18728-154">0x80004002</span></span> | <span data-ttu-id="18728-155">E \_ nointerface</span><span class="sxs-lookup"><span data-stu-id="18728-155">E\_NOINTERFACE</span></span>  | <span data-ttu-id="18728-156">Schnittstelle nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="18728-156">No such interface supported</span></span>         |
| <span data-ttu-id="18728-157">0x80004003</span><span class="sxs-lookup"><span data-stu-id="18728-157">0x80004003</span></span> | <span data-ttu-id="18728-158">E- \_ Zeiger</span><span class="sxs-lookup"><span data-stu-id="18728-158">E\_POINTER</span></span>      | <span data-ttu-id="18728-159">Ungültiger Zeiger</span><span class="sxs-lookup"><span data-stu-id="18728-159">Pointer that is not valid</span></span>           |
| <span data-ttu-id="18728-160">0x80004004</span><span class="sxs-lookup"><span data-stu-id="18728-160">0x80004004</span></span> | <span data-ttu-id="18728-161">E \_ Abbrechen</span><span class="sxs-lookup"><span data-stu-id="18728-161">E\_ABORT</span></span>        | <span data-ttu-id="18728-162">Vorgang abgebrochen</span><span class="sxs-lookup"><span data-stu-id="18728-162">Operation aborted</span></span>                   |
| <span data-ttu-id="18728-163">0x80004005</span><span class="sxs-lookup"><span data-stu-id="18728-163">0x80004005</span></span> | <span data-ttu-id="18728-164">E \_ fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="18728-164">E\_FAIL</span></span>         | <span data-ttu-id="18728-165">Nicht spezifizierter Fehler</span><span class="sxs-lookup"><span data-stu-id="18728-165">Unspecified failure</span></span>                 |
| <span data-ttu-id="18728-166">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="18728-166">0x8000FFFF</span></span> | <span data-ttu-id="18728-167">E \_ unerwartet</span><span class="sxs-lookup"><span data-stu-id="18728-167">E\_UNEXPECTED</span></span>   | <span data-ttu-id="18728-168">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="18728-168">Unexpected failure</span></span>                  |
| <span data-ttu-id="18728-169">0x80070005</span><span class="sxs-lookup"><span data-stu-id="18728-169">0x80070005</span></span> | <span data-ttu-id="18728-170">E \_ AccessDenied</span><span class="sxs-lookup"><span data-stu-id="18728-170">E\_ACCESSDENIED</span></span> | <span data-ttu-id="18728-171">Allgemeiner Zugriffs Verweigerungs Fehler</span><span class="sxs-lookup"><span data-stu-id="18728-171">General access denied error</span></span>         |
| <span data-ttu-id="18728-172">0x80070006</span><span class="sxs-lookup"><span data-stu-id="18728-172">0x80070006</span></span> | <span data-ttu-id="18728-173">E- \_ handle</span><span class="sxs-lookup"><span data-stu-id="18728-173">E\_HANDLE</span></span>       | <span data-ttu-id="18728-174">Handle, das ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="18728-174">Handle that is not valid</span></span>            |
| <span data-ttu-id="18728-175">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="18728-175">0x8007000E</span></span> | <span data-ttu-id="18728-176">E \_ outo-Memory</span><span class="sxs-lookup"><span data-stu-id="18728-176">E\_OUTOFMEMORY</span></span>  | <span data-ttu-id="18728-177">Fehler beim Zuordnen des erforderlichen Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="18728-177">Failed to allocate necessary memory</span></span> |
| <span data-ttu-id="18728-178">0x80070057</span><span class="sxs-lookup"><span data-stu-id="18728-178">0x80070057</span></span> | <span data-ttu-id="18728-179">E \_ invalidArg</span><span class="sxs-lookup"><span data-stu-id="18728-179">E\_INVALIDARG</span></span>   | <span data-ttu-id="18728-180">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="18728-180">One or more arguments are not valid</span></span> |



 

 

 



