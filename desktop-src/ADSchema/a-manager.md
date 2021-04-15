---
title: Manager-Attribut
description: Enthält den Distinguished Name des Benutzers, der der Manager des Benutzers ist. Das Benutzerobjekt des Managers enthält eine DirectReports-Eigenschaft, die Verweise auf alle Benutzer Objekte enthält, deren Manager-Eigenschaften auf diesen Distinguished Name festgelegt sind.
ms.assetid: 40743784-a99c-4ec0-9140-9f865c073244
ms.tgt_platform: multiple
keywords:
- AD-Schema für Manager-Attribut
- AD-Schema für Manager-Attribut
topic_type:
- apiref
api_name:
- Manager
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f42c659a436f9798861f5c37df19f8d10db91127
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104392288"
---
# <a name="manager-attribute"></a><span data-ttu-id="aa904-106">Manager-Attribut</span><span class="sxs-lookup"><span data-stu-id="aa904-106">Manager attribute</span></span>

<span data-ttu-id="aa904-107">Enthält den Distinguished Name des Benutzers, der der Manager des Benutzers ist.</span><span class="sxs-lookup"><span data-stu-id="aa904-107">Contains the distinguished name of the user who is the user's manager.</span></span> <span data-ttu-id="aa904-108">Das Benutzerobjekt des Managers enthält eine DirectReports-Eigenschaft, die Verweise auf alle Benutzer Objekte enthält, deren Manager-Eigenschaften auf diesen Distinguished Name festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="aa904-108">The manager's user object contains a directReports property that contains references to all user objects that have their manager properties set to this distinguished name.</span></span>



| <span data-ttu-id="aa904-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aa904-109">Entry</span></span> | <span data-ttu-id="aa904-110">Wert</span><span class="sxs-lookup"><span data-stu-id="aa904-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="aa904-111">CN</span><span class="sxs-lookup"><span data-stu-id="aa904-111">CN</span></span>                | <span data-ttu-id="aa904-112">Manager</span><span class="sxs-lookup"><span data-stu-id="aa904-112">Manager</span></span>                                                                     |
| <span data-ttu-id="aa904-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="aa904-113">Ldap-Display-Name</span></span> | <span data-ttu-id="aa904-114">manager</span><span class="sxs-lookup"><span data-stu-id="aa904-114">manager</span></span>                                                                     |
| <span data-ttu-id="aa904-115">Size</span><span class="sxs-lookup"><span data-stu-id="aa904-115">Size</span></span>              | \-                                                                          |
| <span data-ttu-id="aa904-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="aa904-116">Update Privilege</span></span>  | <span data-ttu-id="aa904-117">Domänen Administrator oder Konto Besitzer.</span><span class="sxs-lookup"><span data-stu-id="aa904-117">Domain administrator or account owner.</span></span>                                      |
| <span data-ttu-id="aa904-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="aa904-118">Update Frequency</span></span>  | <span data-ttu-id="aa904-119">Wenn der Benutzerdaten Satz erstellt und der Manager geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="aa904-119">When the user's record is created and whenever the manager needs to change.</span></span> |
| <span data-ttu-id="aa904-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="aa904-120">Attribute-Id</span></span>      | <span data-ttu-id="aa904-121">0.9.2342.19200300.100.1.10</span><span class="sxs-lookup"><span data-stu-id="aa904-121">0.9.2342.19200300.100.1.10</span></span>                                                  |
| <span data-ttu-id="aa904-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="aa904-122">System-Id-Guid</span></span>    | <span data-ttu-id="aa904-123">bf9679b5-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="aa904-123">bf9679b5-0de6-11d0-a285-00aa003049e2</span></span>                                        |
| <span data-ttu-id="aa904-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa904-124">Syntax</span></span>            | [<span data-ttu-id="aa904-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="aa904-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                                     |



## <a name="implementations"></a><span data-ttu-id="aa904-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="aa904-126">Implementations</span></span>

-   [<span data-ttu-id="aa904-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="aa904-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="aa904-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="aa904-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="aa904-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="aa904-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="aa904-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="aa904-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="aa904-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="aa904-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="aa904-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="aa904-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="aa904-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aa904-133">Windows 2000 Server</span></span>



| <span data-ttu-id="aa904-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aa904-134">Entry</span></span> | <span data-ttu-id="aa904-135">Wert</span><span class="sxs-lookup"><span data-stu-id="aa904-135">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="aa904-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aa904-136">Link-Id</span></span>                | <span data-ttu-id="aa904-137">42</span><span class="sxs-lookup"><span data-stu-id="aa904-137">42</span></span>                                                                 |
| <span data-ttu-id="aa904-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa904-138">MAPI-Id</span></span>                | <span data-ttu-id="aa904-139">0x8005</span><span class="sxs-lookup"><span data-stu-id="aa904-139">0x8005</span></span>                                                             |
| <span data-ttu-id="aa904-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa904-140">System-Only</span></span>            | <span data-ttu-id="aa904-141">False</span><span class="sxs-lookup"><span data-stu-id="aa904-141">False</span></span>                                                              |
| <span data-ttu-id="aa904-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aa904-142">Is-Single-Valued</span></span>       | <span data-ttu-id="aa904-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="aa904-143">True</span></span>                                                               |
| <span data-ttu-id="aa904-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aa904-144">Is Indexed</span></span>             | <span data-ttu-id="aa904-145">False</span><span class="sxs-lookup"><span data-stu-id="aa904-145">False</span></span>                                                              |
| <span data-ttu-id="aa904-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aa904-146">In Global Catalog</span></span>      | <span data-ttu-id="aa904-147">Richtig</span><span class="sxs-lookup"><span data-stu-id="aa904-147">True</span></span>                                                               |
| <span data-ttu-id="aa904-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aa904-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa904-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aa904-149">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="aa904-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa904-150">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="aa904-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa904-151">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="aa904-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa904-152">Search-Flags</span></span>           | <span data-ttu-id="aa904-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa904-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="aa904-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa904-154">System-Flags</span></span>           | <span data-ttu-id="aa904-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa904-155">0x00000010</span></span>                                                         |
| <span data-ttu-id="aa904-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aa904-156">Classes used in</span></span>        | [<span data-ttu-id="aa904-157">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="aa904-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="aa904-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aa904-158">Windows Server 2003</span></span>



| <span data-ttu-id="aa904-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aa904-159">Entry</span></span> | <span data-ttu-id="aa904-160">Wert</span><span class="sxs-lookup"><span data-stu-id="aa904-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa904-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aa904-161">Link-Id</span></span>                | <span data-ttu-id="aa904-162">42</span><span class="sxs-lookup"><span data-stu-id="aa904-162">42</span></span>                                                                                                                     |
| <span data-ttu-id="aa904-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa904-163">MAPI-Id</span></span>                | <span data-ttu-id="aa904-164">0x8005</span><span class="sxs-lookup"><span data-stu-id="aa904-164">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="aa904-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa904-165">System-Only</span></span>            | <span data-ttu-id="aa904-166">False</span><span class="sxs-lookup"><span data-stu-id="aa904-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="aa904-167">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aa904-167">Is-Single-Valued</span></span>       | <span data-ttu-id="aa904-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="aa904-168">True</span></span>                                                                                                                   |
| <span data-ttu-id="aa904-169">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aa904-169">Is Indexed</span></span>             | <span data-ttu-id="aa904-170">False</span><span class="sxs-lookup"><span data-stu-id="aa904-170">False</span></span>                                                                                                                  |
| <span data-ttu-id="aa904-171">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aa904-171">In Global Catalog</span></span>      | <span data-ttu-id="aa904-172">Richtig</span><span class="sxs-lookup"><span data-stu-id="aa904-172">True</span></span>                                                                                                                   |
| <span data-ttu-id="aa904-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aa904-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa904-174">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aa904-174">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="aa904-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa904-175">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="aa904-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa904-176">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="aa904-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa904-177">Search-Flags</span></span>           | <span data-ttu-id="aa904-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa904-178">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="aa904-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa904-179">System-Flags</span></span>           | <span data-ttu-id="aa904-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa904-180">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="aa904-181">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aa904-181">Classes used in</span></span>        | [<span data-ttu-id="aa904-182">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="aa904-182">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="aa904-183">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="aa904-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="aa904-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="aa904-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="aa904-185">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aa904-185">Entry</span></span> | <span data-ttu-id="aa904-186">Wert</span><span class="sxs-lookup"><span data-stu-id="aa904-186">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa904-187">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aa904-187">Link-Id</span></span>                | <span data-ttu-id="aa904-188">42</span><span class="sxs-lookup"><span data-stu-id="aa904-188">42</span></span>                                                                                                                     |
| <span data-ttu-id="aa904-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa904-189">MAPI-Id</span></span>                | <span data-ttu-id="aa904-190">0x8005</span><span class="sxs-lookup"><span data-stu-id="aa904-190">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="aa904-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa904-191">System-Only</span></span>            | <span data-ttu-id="aa904-192">False</span><span class="sxs-lookup"><span data-stu-id="aa904-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="aa904-193">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aa904-193">Is-Single-Valued</span></span>       | <span data-ttu-id="aa904-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="aa904-194">True</span></span>                                                                                                                   |
| <span data-ttu-id="aa904-195">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aa904-195">Is Indexed</span></span>             | <span data-ttu-id="aa904-196">False</span><span class="sxs-lookup"><span data-stu-id="aa904-196">False</span></span>                                                                                                                  |
| <span data-ttu-id="aa904-197">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aa904-197">In Global Catalog</span></span>      | <span data-ttu-id="aa904-198">Richtig</span><span class="sxs-lookup"><span data-stu-id="aa904-198">True</span></span>                                                                                                                   |
| <span data-ttu-id="aa904-199">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aa904-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa904-200">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aa904-200">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="aa904-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa904-201">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="aa904-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa904-202">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="aa904-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa904-203">Search-Flags</span></span>           | <span data-ttu-id="aa904-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa904-204">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="aa904-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa904-205">System-Flags</span></span>           | <span data-ttu-id="aa904-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa904-206">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="aa904-207">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aa904-207">Classes used in</span></span>        | [<span data-ttu-id="aa904-208">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="aa904-208">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="aa904-209">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="aa904-209">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="aa904-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa904-210">Windows Server 2008</span></span>



| <span data-ttu-id="aa904-211">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aa904-211">Entry</span></span> | <span data-ttu-id="aa904-212">Wert</span><span class="sxs-lookup"><span data-stu-id="aa904-212">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa904-213">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aa904-213">Link-Id</span></span>                | <span data-ttu-id="aa904-214">42</span><span class="sxs-lookup"><span data-stu-id="aa904-214">42</span></span>                                                                                                                     |
| <span data-ttu-id="aa904-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa904-215">MAPI-Id</span></span>                | <span data-ttu-id="aa904-216">0x8005</span><span class="sxs-lookup"><span data-stu-id="aa904-216">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="aa904-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa904-217">System-Only</span></span>            | <span data-ttu-id="aa904-218">False</span><span class="sxs-lookup"><span data-stu-id="aa904-218">False</span></span>                                                                                                                  |
| <span data-ttu-id="aa904-219">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aa904-219">Is-Single-Valued</span></span>       | <span data-ttu-id="aa904-220">Richtig</span><span class="sxs-lookup"><span data-stu-id="aa904-220">True</span></span>                                                                                                                   |
| <span data-ttu-id="aa904-221">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aa904-221">Is Indexed</span></span>             | <span data-ttu-id="aa904-222">False</span><span class="sxs-lookup"><span data-stu-id="aa904-222">False</span></span>                                                                                                                  |
| <span data-ttu-id="aa904-223">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aa904-223">In Global Catalog</span></span>      | <span data-ttu-id="aa904-224">Richtig</span><span class="sxs-lookup"><span data-stu-id="aa904-224">True</span></span>                                                                                                                   |
| <span data-ttu-id="aa904-225">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aa904-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa904-226">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aa904-226">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="aa904-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa904-227">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="aa904-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa904-228">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="aa904-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa904-229">Search-Flags</span></span>           | <span data-ttu-id="aa904-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa904-230">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="aa904-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa904-231">System-Flags</span></span>           | <span data-ttu-id="aa904-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa904-232">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="aa904-233">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aa904-233">Classes used in</span></span>        | [<span data-ttu-id="aa904-234">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="aa904-234">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="aa904-235">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="aa904-235">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="aa904-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aa904-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="aa904-237">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aa904-237">Entry</span></span> | <span data-ttu-id="aa904-238">Wert</span><span class="sxs-lookup"><span data-stu-id="aa904-238">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa904-239">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aa904-239">Link-Id</span></span>                | <span data-ttu-id="aa904-240">42</span><span class="sxs-lookup"><span data-stu-id="aa904-240">42</span></span>                                                                                                                     |
| <span data-ttu-id="aa904-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa904-241">MAPI-Id</span></span>                | <span data-ttu-id="aa904-242">0x8005</span><span class="sxs-lookup"><span data-stu-id="aa904-242">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="aa904-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa904-243">System-Only</span></span>            | <span data-ttu-id="aa904-244">False</span><span class="sxs-lookup"><span data-stu-id="aa904-244">False</span></span>                                                                                                                  |
| <span data-ttu-id="aa904-245">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aa904-245">Is-Single-Valued</span></span>       | <span data-ttu-id="aa904-246">Richtig</span><span class="sxs-lookup"><span data-stu-id="aa904-246">True</span></span>                                                                                                                   |
| <span data-ttu-id="aa904-247">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aa904-247">Is Indexed</span></span>             | <span data-ttu-id="aa904-248">False</span><span class="sxs-lookup"><span data-stu-id="aa904-248">False</span></span>                                                                                                                  |
| <span data-ttu-id="aa904-249">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aa904-249">In Global Catalog</span></span>      | <span data-ttu-id="aa904-250">Richtig</span><span class="sxs-lookup"><span data-stu-id="aa904-250">True</span></span>                                                                                                                   |
| <span data-ttu-id="aa904-251">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aa904-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa904-252">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aa904-252">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="aa904-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa904-253">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="aa904-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa904-254">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="aa904-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa904-255">Search-Flags</span></span>           | <span data-ttu-id="aa904-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa904-256">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="aa904-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa904-257">System-Flags</span></span>           | <span data-ttu-id="aa904-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa904-258">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="aa904-259">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aa904-259">Classes used in</span></span>        | [<span data-ttu-id="aa904-260">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="aa904-260">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="aa904-261">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="aa904-261">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="aa904-262">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aa904-262">Windows Server 2012</span></span>



| <span data-ttu-id="aa904-263">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aa904-263">Entry</span></span> | <span data-ttu-id="aa904-264">Wert</span><span class="sxs-lookup"><span data-stu-id="aa904-264">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa904-265">Link-ID</span><span class="sxs-lookup"><span data-stu-id="aa904-265">Link-Id</span></span>                | <span data-ttu-id="aa904-266">42</span><span class="sxs-lookup"><span data-stu-id="aa904-266">42</span></span>                                                                                                                     |
| <span data-ttu-id="aa904-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa904-267">MAPI-Id</span></span>                | <span data-ttu-id="aa904-268">0x8005</span><span class="sxs-lookup"><span data-stu-id="aa904-268">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="aa904-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa904-269">System-Only</span></span>            | <span data-ttu-id="aa904-270">False</span><span class="sxs-lookup"><span data-stu-id="aa904-270">False</span></span>                                                                                                                  |
| <span data-ttu-id="aa904-271">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="aa904-271">Is-Single-Valued</span></span>       | <span data-ttu-id="aa904-272">Richtig</span><span class="sxs-lookup"><span data-stu-id="aa904-272">True</span></span>                                                                                                                   |
| <span data-ttu-id="aa904-273">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="aa904-273">Is Indexed</span></span>             | <span data-ttu-id="aa904-274">False</span><span class="sxs-lookup"><span data-stu-id="aa904-274">False</span></span>                                                                                                                  |
| <span data-ttu-id="aa904-275">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="aa904-275">In Global Catalog</span></span>      | <span data-ttu-id="aa904-276">Richtig</span><span class="sxs-lookup"><span data-stu-id="aa904-276">True</span></span>                                                                                                                   |
| <span data-ttu-id="aa904-277">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aa904-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa904-278">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="aa904-278">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="aa904-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa904-279">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="aa904-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa904-280">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="aa904-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa904-281">Search-Flags</span></span>           | <span data-ttu-id="aa904-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa904-282">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="aa904-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa904-283">System-Flags</span></span>           | <span data-ttu-id="aa904-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa904-284">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="aa904-285">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="aa904-285">Classes used in</span></span>        | [<span data-ttu-id="aa904-286">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="aa904-286">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="aa904-287">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="aa904-287">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





