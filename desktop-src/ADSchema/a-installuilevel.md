---
title: Install-Attribute auf Benutzeroberflächen Ebene
description: Dieses Attribut enthält Informationen für den Typ (Ebene) der Installation, die für die Benutzeroberfläche verwendet wird.
ms.assetid: 718e04c7-ea96-4519-b312-12534ffd66df
ms.tgt_platform: multiple
keywords:
- AD-Schema für die Installation auf Benutzeroberflächen Ebene
- AD-Schema des installuilevel-Attributs
topic_type:
- apiref
api_name:
- Install-Ui-Level
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b93900bb401d1bdcd72f8881fb78026745c4e8f6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957338"
---
# <a name="install-ui-level-attribute"></a><span data-ttu-id="227eb-105">Install-Attribute auf Benutzeroberflächen Ebene</span><span class="sxs-lookup"><span data-stu-id="227eb-105">Install-Ui-Level attribute</span></span>

<span data-ttu-id="227eb-106">Dieses Attribut enthält Informationen für den Typ (Ebene) der Installation, die für die Benutzeroberfläche verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="227eb-106">This attribute contains information for the type (level) of installation that is used for the user interface.</span></span> <span data-ttu-id="227eb-107">Folgende Installations Ebenen sind möglich: 2 installuilevel \_ None (unbeaufsichtigte Installation) 3 installuilevel \_ Basic (einfache Installation mit Fehlerbehandlung) 4 installuilevel \_ Reduced (erstellte Benutzeroberfläche, unterdrückte Dialogfelder für Assistenten) 5 installuilevel \_ Full (erstellte Benutzeroberfläche mit Assistenten, Status, Fehler)</span><span class="sxs-lookup"><span data-stu-id="227eb-107">Possible installation levels are as follows: 2 INSTALLUILEVEL\_NONE (silent installation) 3 INSTALLUILEVEL\_BASIC (simple installation with error handling) 4 INSTALLUILEVEL\_REDUCED (authored UI, wizard dialog boxes suppressed) 5 INSTALLUILEVEL\_FULL (authored UI with wizards, progress, errors)</span></span>



| <span data-ttu-id="227eb-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="227eb-108">Entry</span></span> | <span data-ttu-id="227eb-109">Wert</span><span class="sxs-lookup"><span data-stu-id="227eb-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="227eb-110">CN</span><span class="sxs-lookup"><span data-stu-id="227eb-110">CN</span></span>                | <span data-ttu-id="227eb-111">Install-UI-Level</span><span class="sxs-lookup"><span data-stu-id="227eb-111">Install-Ui-Level</span></span>                     |
| <span data-ttu-id="227eb-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="227eb-112">Ldap-Display-Name</span></span> | <span data-ttu-id="227eb-113">installuilevel</span><span class="sxs-lookup"><span data-stu-id="227eb-113">installUiLevel</span></span>                       |
| <span data-ttu-id="227eb-114">Size</span><span class="sxs-lookup"><span data-stu-id="227eb-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="227eb-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="227eb-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="227eb-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="227eb-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="227eb-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="227eb-117">Attribute-Id</span></span>      | <span data-ttu-id="227eb-118">1.2.840.113556.1.4.847</span><span class="sxs-lookup"><span data-stu-id="227eb-118">1.2.840.113556.1.4.847</span></span>               |
| <span data-ttu-id="227eb-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="227eb-119">System-Id-Guid</span></span>    | <span data-ttu-id="227eb-120">96a7dd64-9118-11d1-AEbc-0000f 80367c1</span><span class="sxs-lookup"><span data-stu-id="227eb-120">96a7dd64-9118-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="227eb-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="227eb-121">Syntax</span></span>            | [<span data-ttu-id="227eb-122">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="227eb-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="227eb-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="227eb-123">Implementations</span></span>

-   [<span data-ttu-id="227eb-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="227eb-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="227eb-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="227eb-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="227eb-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="227eb-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="227eb-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="227eb-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="227eb-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="227eb-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="227eb-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="227eb-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="227eb-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="227eb-130">Windows 2000 Server</span></span>



| <span data-ttu-id="227eb-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="227eb-131">Entry</span></span> | <span data-ttu-id="227eb-132">Wert</span><span class="sxs-lookup"><span data-stu-id="227eb-132">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="227eb-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="227eb-133">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="227eb-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="227eb-134">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="227eb-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="227eb-135">System-Only</span></span>            | <span data-ttu-id="227eb-136">False</span><span class="sxs-lookup"><span data-stu-id="227eb-136">False</span></span>                                                            |
| <span data-ttu-id="227eb-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="227eb-137">Is-Single-Valued</span></span>       | <span data-ttu-id="227eb-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="227eb-138">True</span></span>                                                             |
| <span data-ttu-id="227eb-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="227eb-139">Is Indexed</span></span>             | <span data-ttu-id="227eb-140">False</span><span class="sxs-lookup"><span data-stu-id="227eb-140">False</span></span>                                                            |
| <span data-ttu-id="227eb-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="227eb-141">In Global Catalog</span></span>      | <span data-ttu-id="227eb-142">False</span><span class="sxs-lookup"><span data-stu-id="227eb-142">False</span></span>                                                            |
| <span data-ttu-id="227eb-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="227eb-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="227eb-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="227eb-144">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="227eb-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="227eb-145">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="227eb-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="227eb-146">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="227eb-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="227eb-147">Search-Flags</span></span>           | <span data-ttu-id="227eb-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="227eb-148">0x00000000</span></span>                                                       |
| <span data-ttu-id="227eb-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="227eb-149">System-Flags</span></span>           | <span data-ttu-id="227eb-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="227eb-150">0x00000010</span></span>                                                       |
| <span data-ttu-id="227eb-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="227eb-151">Classes used in</span></span>        | [<span data-ttu-id="227eb-152">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="227eb-152">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="227eb-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="227eb-153">Windows Server 2003</span></span>



| <span data-ttu-id="227eb-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="227eb-154">Entry</span></span> | <span data-ttu-id="227eb-155">Wert</span><span class="sxs-lookup"><span data-stu-id="227eb-155">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="227eb-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="227eb-156">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="227eb-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="227eb-157">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="227eb-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="227eb-158">System-Only</span></span>            | <span data-ttu-id="227eb-159">False</span><span class="sxs-lookup"><span data-stu-id="227eb-159">False</span></span>                                                            |
| <span data-ttu-id="227eb-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="227eb-160">Is-Single-Valued</span></span>       | <span data-ttu-id="227eb-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="227eb-161">True</span></span>                                                             |
| <span data-ttu-id="227eb-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="227eb-162">Is Indexed</span></span>             | <span data-ttu-id="227eb-163">False</span><span class="sxs-lookup"><span data-stu-id="227eb-163">False</span></span>                                                            |
| <span data-ttu-id="227eb-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="227eb-164">In Global Catalog</span></span>      | <span data-ttu-id="227eb-165">False</span><span class="sxs-lookup"><span data-stu-id="227eb-165">False</span></span>                                                            |
| <span data-ttu-id="227eb-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="227eb-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="227eb-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="227eb-167">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="227eb-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="227eb-168">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="227eb-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="227eb-169">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="227eb-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="227eb-170">Search-Flags</span></span>           | <span data-ttu-id="227eb-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="227eb-171">0x00000000</span></span>                                                       |
| <span data-ttu-id="227eb-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="227eb-172">System-Flags</span></span>           | <span data-ttu-id="227eb-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="227eb-173">0x00000010</span></span>                                                       |
| <span data-ttu-id="227eb-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="227eb-174">Classes used in</span></span>        | [<span data-ttu-id="227eb-175">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="227eb-175">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="227eb-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="227eb-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="227eb-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="227eb-177">Entry</span></span> | <span data-ttu-id="227eb-178">Wert</span><span class="sxs-lookup"><span data-stu-id="227eb-178">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="227eb-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="227eb-179">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="227eb-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="227eb-180">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="227eb-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="227eb-181">System-Only</span></span>            | <span data-ttu-id="227eb-182">False</span><span class="sxs-lookup"><span data-stu-id="227eb-182">False</span></span>                                                            |
| <span data-ttu-id="227eb-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="227eb-183">Is-Single-Valued</span></span>       | <span data-ttu-id="227eb-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="227eb-184">True</span></span>                                                             |
| <span data-ttu-id="227eb-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="227eb-185">Is Indexed</span></span>             | <span data-ttu-id="227eb-186">False</span><span class="sxs-lookup"><span data-stu-id="227eb-186">False</span></span>                                                            |
| <span data-ttu-id="227eb-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="227eb-187">In Global Catalog</span></span>      | <span data-ttu-id="227eb-188">False</span><span class="sxs-lookup"><span data-stu-id="227eb-188">False</span></span>                                                            |
| <span data-ttu-id="227eb-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="227eb-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="227eb-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="227eb-190">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="227eb-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="227eb-191">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="227eb-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="227eb-192">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="227eb-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="227eb-193">Search-Flags</span></span>           | <span data-ttu-id="227eb-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="227eb-194">0x00000000</span></span>                                                       |
| <span data-ttu-id="227eb-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="227eb-195">System-Flags</span></span>           | <span data-ttu-id="227eb-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="227eb-196">0x00000010</span></span>                                                       |
| <span data-ttu-id="227eb-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="227eb-197">Classes used in</span></span>        | [<span data-ttu-id="227eb-198">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="227eb-198">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="227eb-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="227eb-199">Windows Server 2008</span></span>



| <span data-ttu-id="227eb-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="227eb-200">Entry</span></span> | <span data-ttu-id="227eb-201">Wert</span><span class="sxs-lookup"><span data-stu-id="227eb-201">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="227eb-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="227eb-202">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="227eb-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="227eb-203">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="227eb-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="227eb-204">System-Only</span></span>            | <span data-ttu-id="227eb-205">False</span><span class="sxs-lookup"><span data-stu-id="227eb-205">False</span></span>                                                            |
| <span data-ttu-id="227eb-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="227eb-206">Is-Single-Valued</span></span>       | <span data-ttu-id="227eb-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="227eb-207">True</span></span>                                                             |
| <span data-ttu-id="227eb-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="227eb-208">Is Indexed</span></span>             | <span data-ttu-id="227eb-209">False</span><span class="sxs-lookup"><span data-stu-id="227eb-209">False</span></span>                                                            |
| <span data-ttu-id="227eb-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="227eb-210">In Global Catalog</span></span>      | <span data-ttu-id="227eb-211">False</span><span class="sxs-lookup"><span data-stu-id="227eb-211">False</span></span>                                                            |
| <span data-ttu-id="227eb-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="227eb-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="227eb-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="227eb-213">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="227eb-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="227eb-214">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="227eb-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="227eb-215">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="227eb-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="227eb-216">Search-Flags</span></span>           | <span data-ttu-id="227eb-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="227eb-217">0x00000000</span></span>                                                       |
| <span data-ttu-id="227eb-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="227eb-218">System-Flags</span></span>           | <span data-ttu-id="227eb-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="227eb-219">0x00000010</span></span>                                                       |
| <span data-ttu-id="227eb-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="227eb-220">Classes used in</span></span>        | [<span data-ttu-id="227eb-221">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="227eb-221">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="227eb-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="227eb-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="227eb-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="227eb-223">Entry</span></span> | <span data-ttu-id="227eb-224">Wert</span><span class="sxs-lookup"><span data-stu-id="227eb-224">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="227eb-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="227eb-225">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="227eb-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="227eb-226">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="227eb-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="227eb-227">System-Only</span></span>            | <span data-ttu-id="227eb-228">False</span><span class="sxs-lookup"><span data-stu-id="227eb-228">False</span></span>                                                            |
| <span data-ttu-id="227eb-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="227eb-229">Is-Single-Valued</span></span>       | <span data-ttu-id="227eb-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="227eb-230">True</span></span>                                                             |
| <span data-ttu-id="227eb-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="227eb-231">Is Indexed</span></span>             | <span data-ttu-id="227eb-232">False</span><span class="sxs-lookup"><span data-stu-id="227eb-232">False</span></span>                                                            |
| <span data-ttu-id="227eb-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="227eb-233">In Global Catalog</span></span>      | <span data-ttu-id="227eb-234">False</span><span class="sxs-lookup"><span data-stu-id="227eb-234">False</span></span>                                                            |
| <span data-ttu-id="227eb-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="227eb-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="227eb-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="227eb-236">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="227eb-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="227eb-237">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="227eb-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="227eb-238">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="227eb-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="227eb-239">Search-Flags</span></span>           | <span data-ttu-id="227eb-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="227eb-240">0x00000000</span></span>                                                       |
| <span data-ttu-id="227eb-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="227eb-241">System-Flags</span></span>           | <span data-ttu-id="227eb-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="227eb-242">0x00000010</span></span>                                                       |
| <span data-ttu-id="227eb-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="227eb-243">Classes used in</span></span>        | [<span data-ttu-id="227eb-244">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="227eb-244">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="227eb-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="227eb-245">Windows Server 2012</span></span>



| <span data-ttu-id="227eb-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="227eb-246">Entry</span></span> | <span data-ttu-id="227eb-247">Wert</span><span class="sxs-lookup"><span data-stu-id="227eb-247">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="227eb-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="227eb-248">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="227eb-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="227eb-249">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="227eb-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="227eb-250">System-Only</span></span>            | <span data-ttu-id="227eb-251">False</span><span class="sxs-lookup"><span data-stu-id="227eb-251">False</span></span>                                                            |
| <span data-ttu-id="227eb-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="227eb-252">Is-Single-Valued</span></span>       | <span data-ttu-id="227eb-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="227eb-253">True</span></span>                                                             |
| <span data-ttu-id="227eb-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="227eb-254">Is Indexed</span></span>             | <span data-ttu-id="227eb-255">False</span><span class="sxs-lookup"><span data-stu-id="227eb-255">False</span></span>                                                            |
| <span data-ttu-id="227eb-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="227eb-256">In Global Catalog</span></span>      | <span data-ttu-id="227eb-257">False</span><span class="sxs-lookup"><span data-stu-id="227eb-257">False</span></span>                                                            |
| <span data-ttu-id="227eb-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="227eb-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="227eb-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="227eb-259">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="227eb-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="227eb-260">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="227eb-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="227eb-261">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="227eb-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="227eb-262">Search-Flags</span></span>           | <span data-ttu-id="227eb-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="227eb-263">0x00000000</span></span>                                                       |
| <span data-ttu-id="227eb-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="227eb-264">System-Flags</span></span>           | <span data-ttu-id="227eb-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="227eb-265">0x00000010</span></span>                                                       |
| <span data-ttu-id="227eb-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="227eb-266">Classes used in</span></span>        | [<span data-ttu-id="227eb-267">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="227eb-267">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





