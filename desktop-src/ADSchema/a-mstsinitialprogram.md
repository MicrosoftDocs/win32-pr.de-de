---
title: MS-TS-Initial-Program-Attribut
description: Terminal Dienste-Sitzungsstart Programm gibt den Pfad und den Dateinamen der Anwendung an, die der Benutzer automatisch starten möchte, wenn sich der Benutzer am Terminal Server anmeldet.
ms.assetid: c886209b-725b-4e49-a802-58be9ed5e92e
ms.tgt_platform: multiple
keywords:
- "\"MS-TS-Initial-Program\"-Attribut, AD-Schema"
- AD-Schema des mstsinitialprogram-Attributs
topic_type:
- apiref
api_name:
- ms-TS-Initial-Program
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2a4796a97722f2d26142a2ff374414ca3ca1cf2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104392272"
---
# <a name="ms-ts-initial-program-attribute"></a><span data-ttu-id="b677a-105">MS-TS-Initial-Program-Attribut</span><span class="sxs-lookup"><span data-stu-id="b677a-105">ms-TS-Initial-Program attribute</span></span>

<span data-ttu-id="b677a-106">Terminal Dienste-Sitzungsstart Programm gibt den Pfad und den Dateinamen der Anwendung an, die der Benutzer automatisch starten möchte, wenn sich der Benutzer am Terminal Server anmeldet.</span><span class="sxs-lookup"><span data-stu-id="b677a-106">Terminal Services Session Initial Program specifies the path and file name of the application that the user wants to start automatically when the user logs on to the Terminal Server.</span></span>



| <span data-ttu-id="b677a-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b677a-107">Entry</span></span> | <span data-ttu-id="b677a-108">Wert</span><span class="sxs-lookup"><span data-stu-id="b677a-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b677a-109">CN</span><span class="sxs-lookup"><span data-stu-id="b677a-109">CN</span></span>                | <span data-ttu-id="b677a-110">MS-TS-Initial-Program</span><span class="sxs-lookup"><span data-stu-id="b677a-110">ms-TS-Initial-Program</span></span>                       |
| <span data-ttu-id="b677a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b677a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b677a-112">mstsinitialprogram</span><span class="sxs-lookup"><span data-stu-id="b677a-112">msTSInitialProgram</span></span>                          |
| <span data-ttu-id="b677a-113">Size</span><span class="sxs-lookup"><span data-stu-id="b677a-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="b677a-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b677a-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="b677a-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="b677a-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="b677a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b677a-116">Attribute-Id</span></span>      | <span data-ttu-id="b677a-117">1.2.840.113556.1.4.1990</span><span class="sxs-lookup"><span data-stu-id="b677a-117">1.2.840.113556.1.4.1990</span></span>                     |
| <span data-ttu-id="b677a-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b677a-118">System-Id-Guid</span></span>    | <span data-ttu-id="b677a-119">9201ac6l-1d69-4dfb-802e-d95510109599</span><span class="sxs-lookup"><span data-stu-id="b677a-119">9201ac6f-1d69-4dfb-802e-d95510109599</span></span>        |
| <span data-ttu-id="b677a-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="b677a-120">Syntax</span></span>            | [<span data-ttu-id="b677a-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b677a-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b677a-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="b677a-122">Implementations</span></span>

-   [<span data-ttu-id="b677a-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b677a-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b677a-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b677a-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b677a-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b677a-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="b677a-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b677a-126">Windows Server 2008</span></span>



| <span data-ttu-id="b677a-127">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b677a-127">Entry</span></span> | <span data-ttu-id="b677a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="b677a-128">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b677a-129">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b677a-129">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b677a-130">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b677a-130">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b677a-131">System-Only</span><span class="sxs-lookup"><span data-stu-id="b677a-131">System-Only</span></span>            | <span data-ttu-id="b677a-132">False</span><span class="sxs-lookup"><span data-stu-id="b677a-132">False</span></span>                             |
| <span data-ttu-id="b677a-133">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b677a-133">Is-Single-Valued</span></span>       | <span data-ttu-id="b677a-134">Richtig</span><span class="sxs-lookup"><span data-stu-id="b677a-134">True</span></span>                              |
| <span data-ttu-id="b677a-135">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b677a-135">Is Indexed</span></span>             | <span data-ttu-id="b677a-136">False</span><span class="sxs-lookup"><span data-stu-id="b677a-136">False</span></span>                             |
| <span data-ttu-id="b677a-137">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b677a-137">In Global Catalog</span></span>      | <span data-ttu-id="b677a-138">False</span><span class="sxs-lookup"><span data-stu-id="b677a-138">False</span></span>                             |
| <span data-ttu-id="b677a-139">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b677a-139">NT-Security-Descriptor</span></span> | <span data-ttu-id="b677a-140">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b677a-140">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b677a-141">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b677a-141">Range-Lower</span></span>            | <span data-ttu-id="b677a-142">0</span><span class="sxs-lookup"><span data-stu-id="b677a-142">0</span></span>                                 |
| <span data-ttu-id="b677a-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b677a-143">Range-Upper</span></span>            | <span data-ttu-id="b677a-144">32767</span><span class="sxs-lookup"><span data-stu-id="b677a-144">32767</span></span>                             |
| <span data-ttu-id="b677a-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b677a-145">Search-Flags</span></span>           | <span data-ttu-id="b677a-146">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b677a-146">0x00000000</span></span>                        |
| <span data-ttu-id="b677a-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b677a-147">System-Flags</span></span>           | <span data-ttu-id="b677a-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b677a-148">0x00000010</span></span>                        |
| <span data-ttu-id="b677a-149">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b677a-149">Classes used in</span></span>        | [<span data-ttu-id="b677a-150">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="b677a-150">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b677a-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b677a-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b677a-152">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b677a-152">Entry</span></span> | <span data-ttu-id="b677a-153">Wert</span><span class="sxs-lookup"><span data-stu-id="b677a-153">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b677a-154">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b677a-154">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b677a-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b677a-155">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b677a-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="b677a-156">System-Only</span></span>            | <span data-ttu-id="b677a-157">False</span><span class="sxs-lookup"><span data-stu-id="b677a-157">False</span></span>                             |
| <span data-ttu-id="b677a-158">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b677a-158">Is-Single-Valued</span></span>       | <span data-ttu-id="b677a-159">Richtig</span><span class="sxs-lookup"><span data-stu-id="b677a-159">True</span></span>                              |
| <span data-ttu-id="b677a-160">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b677a-160">Is Indexed</span></span>             | <span data-ttu-id="b677a-161">False</span><span class="sxs-lookup"><span data-stu-id="b677a-161">False</span></span>                             |
| <span data-ttu-id="b677a-162">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b677a-162">In Global Catalog</span></span>      | <span data-ttu-id="b677a-163">False</span><span class="sxs-lookup"><span data-stu-id="b677a-163">False</span></span>                             |
| <span data-ttu-id="b677a-164">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b677a-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="b677a-165">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b677a-165">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b677a-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b677a-166">Range-Lower</span></span>            | <span data-ttu-id="b677a-167">0</span><span class="sxs-lookup"><span data-stu-id="b677a-167">0</span></span>                                 |
| <span data-ttu-id="b677a-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b677a-168">Range-Upper</span></span>            | <span data-ttu-id="b677a-169">32767</span><span class="sxs-lookup"><span data-stu-id="b677a-169">32767</span></span>                             |
| <span data-ttu-id="b677a-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b677a-170">Search-Flags</span></span>           | <span data-ttu-id="b677a-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b677a-171">0x00000000</span></span>                        |
| <span data-ttu-id="b677a-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b677a-172">System-Flags</span></span>           | <span data-ttu-id="b677a-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b677a-173">0x00000010</span></span>                        |
| <span data-ttu-id="b677a-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b677a-174">Classes used in</span></span>        | [<span data-ttu-id="b677a-175">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="b677a-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b677a-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b677a-176">Windows Server 2012</span></span>



| <span data-ttu-id="b677a-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b677a-177">Entry</span></span> | <span data-ttu-id="b677a-178">Wert</span><span class="sxs-lookup"><span data-stu-id="b677a-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="b677a-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b677a-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="b677a-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b677a-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="b677a-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="b677a-181">System-Only</span></span>            | <span data-ttu-id="b677a-182">False</span><span class="sxs-lookup"><span data-stu-id="b677a-182">False</span></span>                             |
| <span data-ttu-id="b677a-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b677a-183">Is-Single-Valued</span></span>       | <span data-ttu-id="b677a-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="b677a-184">True</span></span>                              |
| <span data-ttu-id="b677a-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b677a-185">Is Indexed</span></span>             | <span data-ttu-id="b677a-186">False</span><span class="sxs-lookup"><span data-stu-id="b677a-186">False</span></span>                             |
| <span data-ttu-id="b677a-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b677a-187">In Global Catalog</span></span>      | <span data-ttu-id="b677a-188">False</span><span class="sxs-lookup"><span data-stu-id="b677a-188">False</span></span>                             |
| <span data-ttu-id="b677a-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b677a-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="b677a-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b677a-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="b677a-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b677a-191">Range-Lower</span></span>            | <span data-ttu-id="b677a-192">0</span><span class="sxs-lookup"><span data-stu-id="b677a-192">0</span></span>                                 |
| <span data-ttu-id="b677a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b677a-193">Range-Upper</span></span>            | <span data-ttu-id="b677a-194">32767</span><span class="sxs-lookup"><span data-stu-id="b677a-194">32767</span></span>                             |
| <span data-ttu-id="b677a-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b677a-195">Search-Flags</span></span>           | <span data-ttu-id="b677a-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b677a-196">0x00000000</span></span>                        |
| <span data-ttu-id="b677a-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b677a-197">System-Flags</span></span>           | <span data-ttu-id="b677a-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b677a-198">0x00000010</span></span>                        |
| <span data-ttu-id="b677a-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b677a-199">Classes used in</span></span>        | [<span data-ttu-id="b677a-200">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="b677a-200">**User**</span></span>](c-user.md)<br/> |



 

 





