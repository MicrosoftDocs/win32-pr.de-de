---
title: PKI-Überschneidungszeit Attribut
description: Der Zeitraum, nach dem das Zertifikat erneuert werden soll, bevor es abgelaufen ist.
ms.assetid: 394c78b2-7476-4c2d-9a95-f781c779ea4d
ms.tgt_platform: multiple
keywords:
- AD-Schema für PKI-Überschneidungs Zeitraum
- pkioverlapperiod-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- PKI-Overlap-Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad34a30086c4a6de8f96ae18e99c2f8a71682ef
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859588"
---
# <a name="pki-overlap-period-attribute"></a><span data-ttu-id="edbba-105">PKI-Überschneidungszeit Attribut</span><span class="sxs-lookup"><span data-stu-id="edbba-105">PKI-Overlap-Period attribute</span></span>

<span data-ttu-id="edbba-106">Der Zeitraum, nach dem das Zertifikat erneuert werden soll, bevor es abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="edbba-106">The period by when the certificate should be renewed before it is expired.</span></span>



| <span data-ttu-id="edbba-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="edbba-107">Entry</span></span> | <span data-ttu-id="edbba-108">Wert</span><span class="sxs-lookup"><span data-stu-id="edbba-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="edbba-109">CN</span><span class="sxs-lookup"><span data-stu-id="edbba-109">CN</span></span>                | <span data-ttu-id="edbba-110">PKI-Überlappung-Zeitraum</span><span class="sxs-lookup"><span data-stu-id="edbba-110">PKI-Overlap-Period</span></span>                                    |
| <span data-ttu-id="edbba-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="edbba-111">Ldap-Display-Name</span></span> | <span data-ttu-id="edbba-112">pkioverlapperiod</span><span class="sxs-lookup"><span data-stu-id="edbba-112">pKIOverlapPeriod</span></span>                                      |
| <span data-ttu-id="edbba-113">Size</span><span class="sxs-lookup"><span data-stu-id="edbba-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="edbba-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="edbba-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="edbba-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="edbba-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="edbba-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="edbba-116">Attribute-Id</span></span>      | <span data-ttu-id="edbba-117">1.2.840.113556.1.4.1332</span><span class="sxs-lookup"><span data-stu-id="edbba-117">1.2.840.113556.1.4.1332</span></span>                               |
| <span data-ttu-id="edbba-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="edbba-118">System-Id-Guid</span></span>    | <span data-ttu-id="edbba-119">1219a3ec-3b9e-11d2-90cc-00c04f d91ab1</span><span class="sxs-lookup"><span data-stu-id="edbba-119">1219a3ec-3b9e-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="edbba-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="edbba-120">Syntax</span></span>            | [<span data-ttu-id="edbba-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="edbba-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="edbba-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="edbba-122">Implementations</span></span>

-   [<span data-ttu-id="edbba-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="edbba-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="edbba-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="edbba-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="edbba-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="edbba-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="edbba-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="edbba-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="edbba-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="edbba-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="edbba-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="edbba-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="edbba-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="edbba-129">Windows 2000 Server</span></span>



| <span data-ttu-id="edbba-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="edbba-130">Entry</span></span> | <span data-ttu-id="edbba-131">Wert</span><span class="sxs-lookup"><span data-stu-id="edbba-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="edbba-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="edbba-132">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edbba-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edbba-133">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edbba-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="edbba-134">System-Only</span></span>            | <span data-ttu-id="edbba-135">False</span><span class="sxs-lookup"><span data-stu-id="edbba-135">False</span></span>                                                                   |
| <span data-ttu-id="edbba-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="edbba-136">Is-Single-Valued</span></span>       | <span data-ttu-id="edbba-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="edbba-137">True</span></span>                                                                    |
| <span data-ttu-id="edbba-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="edbba-138">Is Indexed</span></span>             | <span data-ttu-id="edbba-139">False</span><span class="sxs-lookup"><span data-stu-id="edbba-139">False</span></span>                                                                   |
| <span data-ttu-id="edbba-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="edbba-140">In Global Catalog</span></span>      | <span data-ttu-id="edbba-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="edbba-141">True</span></span>                                                                    |
| <span data-ttu-id="edbba-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="edbba-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="edbba-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="edbba-143">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="edbba-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edbba-144">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="edbba-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edbba-145">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="edbba-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edbba-146">Search-Flags</span></span>           | <span data-ttu-id="edbba-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edbba-147">0x00000000</span></span>                                                              |
| <span data-ttu-id="edbba-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edbba-148">System-Flags</span></span>           | <span data-ttu-id="edbba-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edbba-149">0x00000010</span></span>                                                              |
| <span data-ttu-id="edbba-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="edbba-150">Classes used in</span></span>        | [<span data-ttu-id="edbba-151">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="edbba-151">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="edbba-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="edbba-152">Windows Server 2003</span></span>



| <span data-ttu-id="edbba-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="edbba-153">Entry</span></span> | <span data-ttu-id="edbba-154">Wert</span><span class="sxs-lookup"><span data-stu-id="edbba-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="edbba-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="edbba-155">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edbba-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edbba-156">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edbba-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="edbba-157">System-Only</span></span>            | <span data-ttu-id="edbba-158">False</span><span class="sxs-lookup"><span data-stu-id="edbba-158">False</span></span>                                                                   |
| <span data-ttu-id="edbba-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="edbba-159">Is-Single-Valued</span></span>       | <span data-ttu-id="edbba-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="edbba-160">True</span></span>                                                                    |
| <span data-ttu-id="edbba-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="edbba-161">Is Indexed</span></span>             | <span data-ttu-id="edbba-162">False</span><span class="sxs-lookup"><span data-stu-id="edbba-162">False</span></span>                                                                   |
| <span data-ttu-id="edbba-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="edbba-163">In Global Catalog</span></span>      | <span data-ttu-id="edbba-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="edbba-164">True</span></span>                                                                    |
| <span data-ttu-id="edbba-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="edbba-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="edbba-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="edbba-166">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="edbba-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edbba-167">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="edbba-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edbba-168">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="edbba-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edbba-169">Search-Flags</span></span>           | <span data-ttu-id="edbba-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edbba-170">0x00000000</span></span>                                                              |
| <span data-ttu-id="edbba-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edbba-171">System-Flags</span></span>           | <span data-ttu-id="edbba-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edbba-172">0x00000010</span></span>                                                              |
| <span data-ttu-id="edbba-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="edbba-173">Classes used in</span></span>        | [<span data-ttu-id="edbba-174">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="edbba-174">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="edbba-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="edbba-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="edbba-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="edbba-176">Entry</span></span> | <span data-ttu-id="edbba-177">Wert</span><span class="sxs-lookup"><span data-stu-id="edbba-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="edbba-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="edbba-178">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edbba-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edbba-179">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edbba-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="edbba-180">System-Only</span></span>            | <span data-ttu-id="edbba-181">False</span><span class="sxs-lookup"><span data-stu-id="edbba-181">False</span></span>                                                                   |
| <span data-ttu-id="edbba-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="edbba-182">Is-Single-Valued</span></span>       | <span data-ttu-id="edbba-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="edbba-183">True</span></span>                                                                    |
| <span data-ttu-id="edbba-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="edbba-184">Is Indexed</span></span>             | <span data-ttu-id="edbba-185">False</span><span class="sxs-lookup"><span data-stu-id="edbba-185">False</span></span>                                                                   |
| <span data-ttu-id="edbba-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="edbba-186">In Global Catalog</span></span>      | <span data-ttu-id="edbba-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="edbba-187">True</span></span>                                                                    |
| <span data-ttu-id="edbba-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="edbba-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="edbba-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="edbba-189">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="edbba-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edbba-190">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="edbba-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edbba-191">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="edbba-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edbba-192">Search-Flags</span></span>           | <span data-ttu-id="edbba-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edbba-193">0x00000000</span></span>                                                              |
| <span data-ttu-id="edbba-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edbba-194">System-Flags</span></span>           | <span data-ttu-id="edbba-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edbba-195">0x00000010</span></span>                                                              |
| <span data-ttu-id="edbba-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="edbba-196">Classes used in</span></span>        | [<span data-ttu-id="edbba-197">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="edbba-197">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="edbba-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="edbba-198">Windows Server 2008</span></span>



| <span data-ttu-id="edbba-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="edbba-199">Entry</span></span> | <span data-ttu-id="edbba-200">Wert</span><span class="sxs-lookup"><span data-stu-id="edbba-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="edbba-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="edbba-201">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edbba-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edbba-202">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edbba-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="edbba-203">System-Only</span></span>            | <span data-ttu-id="edbba-204">False</span><span class="sxs-lookup"><span data-stu-id="edbba-204">False</span></span>                                                                   |
| <span data-ttu-id="edbba-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="edbba-205">Is-Single-Valued</span></span>       | <span data-ttu-id="edbba-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="edbba-206">True</span></span>                                                                    |
| <span data-ttu-id="edbba-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="edbba-207">Is Indexed</span></span>             | <span data-ttu-id="edbba-208">False</span><span class="sxs-lookup"><span data-stu-id="edbba-208">False</span></span>                                                                   |
| <span data-ttu-id="edbba-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="edbba-209">In Global Catalog</span></span>      | <span data-ttu-id="edbba-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="edbba-210">True</span></span>                                                                    |
| <span data-ttu-id="edbba-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="edbba-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="edbba-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="edbba-212">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="edbba-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edbba-213">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="edbba-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edbba-214">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="edbba-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edbba-215">Search-Flags</span></span>           | <span data-ttu-id="edbba-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edbba-216">0x00000000</span></span>                                                              |
| <span data-ttu-id="edbba-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edbba-217">System-Flags</span></span>           | <span data-ttu-id="edbba-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edbba-218">0x00000010</span></span>                                                              |
| <span data-ttu-id="edbba-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="edbba-219">Classes used in</span></span>        | [<span data-ttu-id="edbba-220">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="edbba-220">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="edbba-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="edbba-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="edbba-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="edbba-222">Entry</span></span> | <span data-ttu-id="edbba-223">Wert</span><span class="sxs-lookup"><span data-stu-id="edbba-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="edbba-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="edbba-224">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edbba-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edbba-225">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edbba-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="edbba-226">System-Only</span></span>            | <span data-ttu-id="edbba-227">False</span><span class="sxs-lookup"><span data-stu-id="edbba-227">False</span></span>                                                                   |
| <span data-ttu-id="edbba-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="edbba-228">Is-Single-Valued</span></span>       | <span data-ttu-id="edbba-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="edbba-229">True</span></span>                                                                    |
| <span data-ttu-id="edbba-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="edbba-230">Is Indexed</span></span>             | <span data-ttu-id="edbba-231">False</span><span class="sxs-lookup"><span data-stu-id="edbba-231">False</span></span>                                                                   |
| <span data-ttu-id="edbba-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="edbba-232">In Global Catalog</span></span>      | <span data-ttu-id="edbba-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="edbba-233">True</span></span>                                                                    |
| <span data-ttu-id="edbba-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="edbba-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="edbba-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="edbba-235">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="edbba-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edbba-236">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="edbba-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edbba-237">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="edbba-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edbba-238">Search-Flags</span></span>           | <span data-ttu-id="edbba-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edbba-239">0x00000000</span></span>                                                              |
| <span data-ttu-id="edbba-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edbba-240">System-Flags</span></span>           | <span data-ttu-id="edbba-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edbba-241">0x00000010</span></span>                                                              |
| <span data-ttu-id="edbba-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="edbba-242">Classes used in</span></span>        | [<span data-ttu-id="edbba-243">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="edbba-243">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="edbba-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="edbba-244">Windows Server 2012</span></span>



| <span data-ttu-id="edbba-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="edbba-245">Entry</span></span> | <span data-ttu-id="edbba-246">Wert</span><span class="sxs-lookup"><span data-stu-id="edbba-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="edbba-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="edbba-247">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edbba-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edbba-248">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edbba-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="edbba-249">System-Only</span></span>            | <span data-ttu-id="edbba-250">False</span><span class="sxs-lookup"><span data-stu-id="edbba-250">False</span></span>                                                                   |
| <span data-ttu-id="edbba-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="edbba-251">Is-Single-Valued</span></span>       | <span data-ttu-id="edbba-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="edbba-252">True</span></span>                                                                    |
| <span data-ttu-id="edbba-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="edbba-253">Is Indexed</span></span>             | <span data-ttu-id="edbba-254">False</span><span class="sxs-lookup"><span data-stu-id="edbba-254">False</span></span>                                                                   |
| <span data-ttu-id="edbba-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="edbba-255">In Global Catalog</span></span>      | <span data-ttu-id="edbba-256">Richtig</span><span class="sxs-lookup"><span data-stu-id="edbba-256">True</span></span>                                                                    |
| <span data-ttu-id="edbba-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="edbba-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="edbba-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="edbba-258">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="edbba-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edbba-259">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="edbba-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edbba-260">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="edbba-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edbba-261">Search-Flags</span></span>           | <span data-ttu-id="edbba-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edbba-262">0x00000000</span></span>                                                              |
| <span data-ttu-id="edbba-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edbba-263">System-Flags</span></span>           | <span data-ttu-id="edbba-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edbba-264">0x00000010</span></span>                                                              |
| <span data-ttu-id="edbba-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="edbba-265">Classes used in</span></span>        | [<span data-ttu-id="edbba-266">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="edbba-266">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





