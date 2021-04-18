---
title: MS-TAPI-Conference-BLOB-Attribut
description: Ein binäres Blob von Daten, das verschiedene Eigenschaften einer TAPI-Multicast Konferenz beschreibt. Das Format und der Inhalt werden durch den Wert des Attributs Protocol-Id im selben Objekt bestimmt. Die Daten in diesem BLOB entsprechen in der Regel RFC2327.
ms.assetid: f1d5baed-df3f-423e-aa2f-005e77e79725
ms.tgt_platform: multiple
keywords:
- MS-TAPI-Conference-BLOB-Attribut AD-Schema
- AD-Schema des MSTAPI-conferenceblob-Attributs
topic_type:
- apiref
api_name:
- ms-TAPI-Conference-Blob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f4e3ec8b74144daca7af1788c08270d998c139c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106340046"
---
# <a name="ms-tapi-conference-blob-attribute"></a><span data-ttu-id="4f449-107">MS-TAPI-Conference-BLOB-Attribut</span><span class="sxs-lookup"><span data-stu-id="4f449-107">ms-TAPI-Conference-Blob attribute</span></span>

<span data-ttu-id="4f449-108">Ein binäres Blob von Daten, das verschiedene Eigenschaften einer TAPI-Multicast Konferenz beschreibt.</span><span class="sxs-lookup"><span data-stu-id="4f449-108">A binary BLOB of data that describes various properties of a TAPI multicast conference.</span></span> <span data-ttu-id="4f449-109">Das Format und der Inhalt werden durch den Wert des Attributs Protocol-Id im selben Objekt bestimmt.</span><span class="sxs-lookup"><span data-stu-id="4f449-109">Its format and content are determined by the value of the attribute Protocol-Id in the same object.</span></span> <span data-ttu-id="4f449-110">Die Daten in diesem BLOB entsprechen in der Regel RFC2327.</span><span class="sxs-lookup"><span data-stu-id="4f449-110">Typically, the data in this BLOB conforms to RFC2327.</span></span>



| <span data-ttu-id="4f449-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4f449-111">Entry</span></span> | <span data-ttu-id="4f449-112">Wert</span><span class="sxs-lookup"><span data-stu-id="4f449-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f449-113">CN</span><span class="sxs-lookup"><span data-stu-id="4f449-113">CN</span></span>                | <span data-ttu-id="4f449-114">MS-TAPI-Conference-BLOB</span><span class="sxs-lookup"><span data-stu-id="4f449-114">ms-TAPI-Conference-Blob</span></span>                                                                                      |
| <span data-ttu-id="4f449-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4f449-115">Ldap-Display-Name</span></span> | <span data-ttu-id="4f449-116">MSTAPI-confererceblob</span><span class="sxs-lookup"><span data-stu-id="4f449-116">msTAPI-ConferenceBlob</span></span>                                                                                        |
| <span data-ttu-id="4f449-117">Size</span><span class="sxs-lookup"><span data-stu-id="4f449-117">Size</span></span>              | <span data-ttu-id="4f449-118">Kann eine beliebige Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4f449-118">Can be of arbitrary length.</span></span>                                                                                  |
| <span data-ttu-id="4f449-119">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="4f449-119">Update Privilege</span></span>  | <span data-ttu-id="4f449-120">Es sind keine besonderen Berechtigungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4f449-120">No special privileges required.</span></span>                                                                              |
| <span data-ttu-id="4f449-121">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="4f449-121">Update Frequency</span></span>  | <span data-ttu-id="4f449-122">Kann nach dem Ermessen eines TAPI-Konferenz Besitzers geändert werden, wenn sich einige Daten über die Konferenz ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="4f449-122">Can change at the discretion of a TAPI conference owner when some data about the conference needs to change.</span></span> |
| <span data-ttu-id="4f449-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4f449-123">Attribute-Id</span></span>      | <span data-ttu-id="4f449-124">1.2.840.113556.1.4.1700</span><span class="sxs-lookup"><span data-stu-id="4f449-124">1.2.840.113556.1.4.1700</span></span>                                                                                      |
| <span data-ttu-id="4f449-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4f449-125">System-Id-Guid</span></span>    | <span data-ttu-id="4f449-126">4cc4601e-7201-4141-abc8-3e529ae88863</span><span class="sxs-lookup"><span data-stu-id="4f449-126">4cc4601e-7201-4141-abc8-3e529ae88863</span></span>                                                                         |
| <span data-ttu-id="4f449-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f449-127">Syntax</span></span>            | [<span data-ttu-id="4f449-128">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="4f449-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                                        |



## <a name="implementations"></a><span data-ttu-id="4f449-129">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="4f449-129">Implementations</span></span>

-   [<span data-ttu-id="4f449-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4f449-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4f449-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4f449-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4f449-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4f449-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4f449-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4f449-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4f449-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4f449-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="4f449-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4f449-135">Windows Server 2003</span></span>



| <span data-ttu-id="4f449-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4f449-136">Entry</span></span> | <span data-ttu-id="4f449-137">Wert</span><span class="sxs-lookup"><span data-stu-id="4f449-137">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="4f449-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4f449-138">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4f449-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f449-139">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4f449-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f449-140">System-Only</span></span>            | <span data-ttu-id="4f449-141">False</span><span class="sxs-lookup"><span data-stu-id="4f449-141">False</span></span>                                                             |
| <span data-ttu-id="4f449-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4f449-142">Is-Single-Valued</span></span>       | <span data-ttu-id="4f449-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="4f449-143">True</span></span>                                                              |
| <span data-ttu-id="4f449-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4f449-144">Is Indexed</span></span>             | <span data-ttu-id="4f449-145">False</span><span class="sxs-lookup"><span data-stu-id="4f449-145">False</span></span>                                                             |
| <span data-ttu-id="4f449-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4f449-146">In Global Catalog</span></span>      | <span data-ttu-id="4f449-147">False</span><span class="sxs-lookup"><span data-stu-id="4f449-147">False</span></span>                                                             |
| <span data-ttu-id="4f449-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f449-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f449-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4f449-149">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="4f449-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f449-150">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="4f449-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f449-151">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="4f449-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f449-152">Search-Flags</span></span>           | <span data-ttu-id="4f449-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f449-153">0x00000000</span></span>                                                        |
| <span data-ttu-id="4f449-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f449-154">System-Flags</span></span>           | <span data-ttu-id="4f449-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f449-155">0x00000010</span></span>                                                        |
| <span data-ttu-id="4f449-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4f449-156">Classes used in</span></span>        | [<span data-ttu-id="4f449-157">**MS-TAPI-RT-Konferenz**</span><span class="sxs-lookup"><span data-stu-id="4f449-157">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4f449-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4f449-158">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4f449-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4f449-159">Entry</span></span> | <span data-ttu-id="4f449-160">Wert</span><span class="sxs-lookup"><span data-stu-id="4f449-160">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="4f449-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4f449-161">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4f449-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f449-162">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4f449-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f449-163">System-Only</span></span>            | <span data-ttu-id="4f449-164">False</span><span class="sxs-lookup"><span data-stu-id="4f449-164">False</span></span>                                                             |
| <span data-ttu-id="4f449-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4f449-165">Is-Single-Valued</span></span>       | <span data-ttu-id="4f449-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="4f449-166">True</span></span>                                                              |
| <span data-ttu-id="4f449-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4f449-167">Is Indexed</span></span>             | <span data-ttu-id="4f449-168">False</span><span class="sxs-lookup"><span data-stu-id="4f449-168">False</span></span>                                                             |
| <span data-ttu-id="4f449-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4f449-169">In Global Catalog</span></span>      | <span data-ttu-id="4f449-170">False</span><span class="sxs-lookup"><span data-stu-id="4f449-170">False</span></span>                                                             |
| <span data-ttu-id="4f449-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f449-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f449-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4f449-172">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="4f449-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f449-173">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="4f449-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f449-174">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="4f449-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f449-175">Search-Flags</span></span>           | <span data-ttu-id="4f449-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f449-176">0x00000000</span></span>                                                        |
| <span data-ttu-id="4f449-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f449-177">System-Flags</span></span>           | <span data-ttu-id="4f449-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f449-178">0x00000010</span></span>                                                        |
| <span data-ttu-id="4f449-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4f449-179">Classes used in</span></span>        | [<span data-ttu-id="4f449-180">**MS-TAPI-RT-Konferenz**</span><span class="sxs-lookup"><span data-stu-id="4f449-180">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4f449-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f449-181">Windows Server 2008</span></span>



| <span data-ttu-id="4f449-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4f449-182">Entry</span></span> | <span data-ttu-id="4f449-183">Wert</span><span class="sxs-lookup"><span data-stu-id="4f449-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="4f449-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4f449-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4f449-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f449-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4f449-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f449-186">System-Only</span></span>            | <span data-ttu-id="4f449-187">False</span><span class="sxs-lookup"><span data-stu-id="4f449-187">False</span></span>                                                             |
| <span data-ttu-id="4f449-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4f449-188">Is-Single-Valued</span></span>       | <span data-ttu-id="4f449-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="4f449-189">True</span></span>                                                              |
| <span data-ttu-id="4f449-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4f449-190">Is Indexed</span></span>             | <span data-ttu-id="4f449-191">False</span><span class="sxs-lookup"><span data-stu-id="4f449-191">False</span></span>                                                             |
| <span data-ttu-id="4f449-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4f449-192">In Global Catalog</span></span>      | <span data-ttu-id="4f449-193">False</span><span class="sxs-lookup"><span data-stu-id="4f449-193">False</span></span>                                                             |
| <span data-ttu-id="4f449-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f449-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f449-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4f449-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="4f449-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f449-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="4f449-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f449-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="4f449-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f449-198">Search-Flags</span></span>           | <span data-ttu-id="4f449-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f449-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="4f449-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f449-200">System-Flags</span></span>           | <span data-ttu-id="4f449-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f449-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="4f449-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4f449-202">Classes used in</span></span>        | [<span data-ttu-id="4f449-203">**MS-TAPI-RT-Konferenz**</span><span class="sxs-lookup"><span data-stu-id="4f449-203">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4f449-204">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4f449-204">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4f449-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4f449-205">Entry</span></span> | <span data-ttu-id="4f449-206">Wert</span><span class="sxs-lookup"><span data-stu-id="4f449-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="4f449-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4f449-207">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4f449-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f449-208">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4f449-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f449-209">System-Only</span></span>            | <span data-ttu-id="4f449-210">False</span><span class="sxs-lookup"><span data-stu-id="4f449-210">False</span></span>                                                             |
| <span data-ttu-id="4f449-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4f449-211">Is-Single-Valued</span></span>       | <span data-ttu-id="4f449-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="4f449-212">True</span></span>                                                              |
| <span data-ttu-id="4f449-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4f449-213">Is Indexed</span></span>             | <span data-ttu-id="4f449-214">False</span><span class="sxs-lookup"><span data-stu-id="4f449-214">False</span></span>                                                             |
| <span data-ttu-id="4f449-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4f449-215">In Global Catalog</span></span>      | <span data-ttu-id="4f449-216">False</span><span class="sxs-lookup"><span data-stu-id="4f449-216">False</span></span>                                                             |
| <span data-ttu-id="4f449-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f449-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f449-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4f449-218">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="4f449-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f449-219">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="4f449-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f449-220">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="4f449-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f449-221">Search-Flags</span></span>           | <span data-ttu-id="4f449-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f449-222">0x00000000</span></span>                                                        |
| <span data-ttu-id="4f449-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f449-223">System-Flags</span></span>           | <span data-ttu-id="4f449-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f449-224">0x00000010</span></span>                                                        |
| <span data-ttu-id="4f449-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4f449-225">Classes used in</span></span>        | [<span data-ttu-id="4f449-226">**MS-TAPI-RT-Konferenz**</span><span class="sxs-lookup"><span data-stu-id="4f449-226">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4f449-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4f449-227">Windows Server 2012</span></span>



| <span data-ttu-id="4f449-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4f449-228">Entry</span></span> | <span data-ttu-id="4f449-229">Wert</span><span class="sxs-lookup"><span data-stu-id="4f449-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="4f449-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="4f449-230">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4f449-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f449-231">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4f449-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f449-232">System-Only</span></span>            | <span data-ttu-id="4f449-233">False</span><span class="sxs-lookup"><span data-stu-id="4f449-233">False</span></span>                                                             |
| <span data-ttu-id="4f449-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="4f449-234">Is-Single-Valued</span></span>       | <span data-ttu-id="4f449-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="4f449-235">True</span></span>                                                              |
| <span data-ttu-id="4f449-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="4f449-236">Is Indexed</span></span>             | <span data-ttu-id="4f449-237">False</span><span class="sxs-lookup"><span data-stu-id="4f449-237">False</span></span>                                                             |
| <span data-ttu-id="4f449-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4f449-238">In Global Catalog</span></span>      | <span data-ttu-id="4f449-239">False</span><span class="sxs-lookup"><span data-stu-id="4f449-239">False</span></span>                                                             |
| <span data-ttu-id="4f449-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f449-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f449-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="4f449-241">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="4f449-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f449-242">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="4f449-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f449-243">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="4f449-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f449-244">Search-Flags</span></span>           | <span data-ttu-id="4f449-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f449-245">0x00000000</span></span>                                                        |
| <span data-ttu-id="4f449-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f449-246">System-Flags</span></span>           | <span data-ttu-id="4f449-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f449-247">0x00000010</span></span>                                                        |
| <span data-ttu-id="4f449-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="4f449-248">Classes used in</span></span>        | [<span data-ttu-id="4f449-249">**MS-TAPI-RT-Konferenz**</span><span class="sxs-lookup"><span data-stu-id="4f449-249">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



 

 





