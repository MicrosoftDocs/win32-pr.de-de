---
title: 'PKI-Registrierung: Access-Attribut'
description: Das PKI-Registrierungs Zugriffs Attribut ist nur für die interne Verwendung vorgesehen.
ms.assetid: 09eab075-71a5-4a38-af34-dafedca9c2c6
ms.tgt_platform: multiple
keywords:
- PKI-Registrierung-AD-Schema des Zugriffs Attributs
- AD-Schema des pkienrollmentaccess-Attributs
topic_type:
- apiref
api_name:
- PKI-Enrollment-Access
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f974e1072810b902fa42d30f067a67e22236ca
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957328"
---
# <a name="pki-enrollment-access-attribute"></a><span data-ttu-id="da7f9-105">PKI-Registrierung: Access-Attribut</span><span class="sxs-lookup"><span data-stu-id="da7f9-105">PKI-Enrollment-Access attribute</span></span>

<span data-ttu-id="da7f9-106">Das **PKI-Registrierungs Zugriffs** Attribut ist nur für die interne Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="da7f9-106">The **PKI-Enrollment-Access** attribute is for internal use only.</span></span>



| <span data-ttu-id="da7f9-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da7f9-107">Entry</span></span> | <span data-ttu-id="da7f9-108">Wert</span><span class="sxs-lookup"><span data-stu-id="da7f9-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="da7f9-109">CN</span><span class="sxs-lookup"><span data-stu-id="da7f9-109">CN</span></span>                | <span data-ttu-id="da7f9-110">PKI-Registrierung-Zugriff</span><span class="sxs-lookup"><span data-stu-id="da7f9-110">PKI-Enrollment-Access</span></span>                               |
| <span data-ttu-id="da7f9-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="da7f9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="da7f9-112">pkienrollmentaccess</span><span class="sxs-lookup"><span data-stu-id="da7f9-112">pKIEnrollmentAccess</span></span>                                 |
| <span data-ttu-id="da7f9-113">Size</span><span class="sxs-lookup"><span data-stu-id="da7f9-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="da7f9-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="da7f9-114">Update Privilege</span></span>  | \-                                                  |
| <span data-ttu-id="da7f9-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="da7f9-115">Update Frequency</span></span>  | \-                                                  |
| <span data-ttu-id="da7f9-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="da7f9-116">Attribute-Id</span></span>      | <span data-ttu-id="da7f9-117">1.2.840.113556.1.4.1335</span><span class="sxs-lookup"><span data-stu-id="da7f9-117">1.2.840.113556.1.4.1335</span></span>                             |
| <span data-ttu-id="da7f9-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="da7f9-118">System-Id-Guid</span></span>    | <span data-ttu-id="da7f9-119">926be278-56b9-11d2-90d0-00c04f d91ab1</span><span class="sxs-lookup"><span data-stu-id="da7f9-119">926be278-56f9-11d2-90d0-00c04fd91ab1</span></span>                |
| <span data-ttu-id="da7f9-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="da7f9-120">Syntax</span></span>            | [<span data-ttu-id="da7f9-121">**String(NT-Sec-Desc)**</span><span class="sxs-lookup"><span data-stu-id="da7f9-121">**String(NT-Sec-Desc)**</span></span>](s-string-nt-sec-desc.md) |



## <a name="implementations"></a><span data-ttu-id="da7f9-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="da7f9-122">Implementations</span></span>

-   [<span data-ttu-id="da7f9-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="da7f9-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="da7f9-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="da7f9-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="da7f9-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="da7f9-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="da7f9-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="da7f9-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="da7f9-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="da7f9-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="da7f9-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="da7f9-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="da7f9-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="da7f9-129">Windows 2000 Server</span></span>



| <span data-ttu-id="da7f9-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da7f9-130">Entry</span></span> | <span data-ttu-id="da7f9-131">Wert</span><span class="sxs-lookup"><span data-stu-id="da7f9-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="da7f9-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da7f9-132">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="da7f9-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da7f9-133">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="da7f9-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="da7f9-134">System-Only</span></span>            | <span data-ttu-id="da7f9-135">False</span><span class="sxs-lookup"><span data-stu-id="da7f9-135">False</span></span>                                                                   |
| <span data-ttu-id="da7f9-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da7f9-136">Is-Single-Valued</span></span>       | <span data-ttu-id="da7f9-137">False</span><span class="sxs-lookup"><span data-stu-id="da7f9-137">False</span></span>                                                                   |
| <span data-ttu-id="da7f9-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da7f9-138">Is Indexed</span></span>             | <span data-ttu-id="da7f9-139">False</span><span class="sxs-lookup"><span data-stu-id="da7f9-139">False</span></span>                                                                   |
| <span data-ttu-id="da7f9-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da7f9-140">In Global Catalog</span></span>      | <span data-ttu-id="da7f9-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="da7f9-141">True</span></span>                                                                    |
| <span data-ttu-id="da7f9-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da7f9-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="da7f9-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da7f9-143">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="da7f9-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da7f9-144">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="da7f9-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da7f9-145">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="da7f9-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da7f9-146">Search-Flags</span></span>           | <span data-ttu-id="da7f9-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da7f9-147">0x00000000</span></span>                                                              |
| <span data-ttu-id="da7f9-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da7f9-148">System-Flags</span></span>           | <span data-ttu-id="da7f9-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da7f9-149">0x00000010</span></span>                                                              |
| <span data-ttu-id="da7f9-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da7f9-150">Classes used in</span></span>        | [<span data-ttu-id="da7f9-151">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="da7f9-151">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="da7f9-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="da7f9-152">Windows Server 2003</span></span>



| <span data-ttu-id="da7f9-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da7f9-153">Entry</span></span> | <span data-ttu-id="da7f9-154">Wert</span><span class="sxs-lookup"><span data-stu-id="da7f9-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="da7f9-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da7f9-155">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="da7f9-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da7f9-156">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="da7f9-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="da7f9-157">System-Only</span></span>            | <span data-ttu-id="da7f9-158">False</span><span class="sxs-lookup"><span data-stu-id="da7f9-158">False</span></span>                                                                   |
| <span data-ttu-id="da7f9-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da7f9-159">Is-Single-Valued</span></span>       | <span data-ttu-id="da7f9-160">False</span><span class="sxs-lookup"><span data-stu-id="da7f9-160">False</span></span>                                                                   |
| <span data-ttu-id="da7f9-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da7f9-161">Is Indexed</span></span>             | <span data-ttu-id="da7f9-162">False</span><span class="sxs-lookup"><span data-stu-id="da7f9-162">False</span></span>                                                                   |
| <span data-ttu-id="da7f9-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da7f9-163">In Global Catalog</span></span>      | <span data-ttu-id="da7f9-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="da7f9-164">True</span></span>                                                                    |
| <span data-ttu-id="da7f9-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da7f9-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="da7f9-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da7f9-166">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="da7f9-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da7f9-167">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="da7f9-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da7f9-168">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="da7f9-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da7f9-169">Search-Flags</span></span>           | <span data-ttu-id="da7f9-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da7f9-170">0x00000000</span></span>                                                              |
| <span data-ttu-id="da7f9-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da7f9-171">System-Flags</span></span>           | <span data-ttu-id="da7f9-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da7f9-172">0x00000010</span></span>                                                              |
| <span data-ttu-id="da7f9-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da7f9-173">Classes used in</span></span>        | [<span data-ttu-id="da7f9-174">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="da7f9-174">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="da7f9-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="da7f9-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="da7f9-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da7f9-176">Entry</span></span> | <span data-ttu-id="da7f9-177">Wert</span><span class="sxs-lookup"><span data-stu-id="da7f9-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="da7f9-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da7f9-178">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="da7f9-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da7f9-179">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="da7f9-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="da7f9-180">System-Only</span></span>            | <span data-ttu-id="da7f9-181">False</span><span class="sxs-lookup"><span data-stu-id="da7f9-181">False</span></span>                                                                   |
| <span data-ttu-id="da7f9-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da7f9-182">Is-Single-Valued</span></span>       | <span data-ttu-id="da7f9-183">False</span><span class="sxs-lookup"><span data-stu-id="da7f9-183">False</span></span>                                                                   |
| <span data-ttu-id="da7f9-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da7f9-184">Is Indexed</span></span>             | <span data-ttu-id="da7f9-185">False</span><span class="sxs-lookup"><span data-stu-id="da7f9-185">False</span></span>                                                                   |
| <span data-ttu-id="da7f9-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da7f9-186">In Global Catalog</span></span>      | <span data-ttu-id="da7f9-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="da7f9-187">True</span></span>                                                                    |
| <span data-ttu-id="da7f9-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da7f9-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="da7f9-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da7f9-189">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="da7f9-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da7f9-190">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="da7f9-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da7f9-191">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="da7f9-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da7f9-192">Search-Flags</span></span>           | <span data-ttu-id="da7f9-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da7f9-193">0x00000000</span></span>                                                              |
| <span data-ttu-id="da7f9-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da7f9-194">System-Flags</span></span>           | <span data-ttu-id="da7f9-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da7f9-195">0x00000010</span></span>                                                              |
| <span data-ttu-id="da7f9-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da7f9-196">Classes used in</span></span>        | [<span data-ttu-id="da7f9-197">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="da7f9-197">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="da7f9-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da7f9-198">Windows Server 2008</span></span>



| <span data-ttu-id="da7f9-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da7f9-199">Entry</span></span> | <span data-ttu-id="da7f9-200">Wert</span><span class="sxs-lookup"><span data-stu-id="da7f9-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="da7f9-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da7f9-201">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="da7f9-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da7f9-202">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="da7f9-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="da7f9-203">System-Only</span></span>            | <span data-ttu-id="da7f9-204">False</span><span class="sxs-lookup"><span data-stu-id="da7f9-204">False</span></span>                                                                   |
| <span data-ttu-id="da7f9-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da7f9-205">Is-Single-Valued</span></span>       | <span data-ttu-id="da7f9-206">False</span><span class="sxs-lookup"><span data-stu-id="da7f9-206">False</span></span>                                                                   |
| <span data-ttu-id="da7f9-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da7f9-207">Is Indexed</span></span>             | <span data-ttu-id="da7f9-208">False</span><span class="sxs-lookup"><span data-stu-id="da7f9-208">False</span></span>                                                                   |
| <span data-ttu-id="da7f9-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da7f9-209">In Global Catalog</span></span>      | <span data-ttu-id="da7f9-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="da7f9-210">True</span></span>                                                                    |
| <span data-ttu-id="da7f9-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da7f9-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="da7f9-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da7f9-212">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="da7f9-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da7f9-213">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="da7f9-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da7f9-214">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="da7f9-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da7f9-215">Search-Flags</span></span>           | <span data-ttu-id="da7f9-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da7f9-216">0x00000000</span></span>                                                              |
| <span data-ttu-id="da7f9-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da7f9-217">System-Flags</span></span>           | <span data-ttu-id="da7f9-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da7f9-218">0x00000010</span></span>                                                              |
| <span data-ttu-id="da7f9-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da7f9-219">Classes used in</span></span>        | [<span data-ttu-id="da7f9-220">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="da7f9-220">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="da7f9-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="da7f9-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="da7f9-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da7f9-222">Entry</span></span> | <span data-ttu-id="da7f9-223">Wert</span><span class="sxs-lookup"><span data-stu-id="da7f9-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="da7f9-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da7f9-224">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="da7f9-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da7f9-225">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="da7f9-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="da7f9-226">System-Only</span></span>            | <span data-ttu-id="da7f9-227">False</span><span class="sxs-lookup"><span data-stu-id="da7f9-227">False</span></span>                                                                   |
| <span data-ttu-id="da7f9-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da7f9-228">Is-Single-Valued</span></span>       | <span data-ttu-id="da7f9-229">False</span><span class="sxs-lookup"><span data-stu-id="da7f9-229">False</span></span>                                                                   |
| <span data-ttu-id="da7f9-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da7f9-230">Is Indexed</span></span>             | <span data-ttu-id="da7f9-231">False</span><span class="sxs-lookup"><span data-stu-id="da7f9-231">False</span></span>                                                                   |
| <span data-ttu-id="da7f9-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da7f9-232">In Global Catalog</span></span>      | <span data-ttu-id="da7f9-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="da7f9-233">True</span></span>                                                                    |
| <span data-ttu-id="da7f9-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da7f9-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="da7f9-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da7f9-235">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="da7f9-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da7f9-236">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="da7f9-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da7f9-237">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="da7f9-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da7f9-238">Search-Flags</span></span>           | <span data-ttu-id="da7f9-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da7f9-239">0x00000000</span></span>                                                              |
| <span data-ttu-id="da7f9-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da7f9-240">System-Flags</span></span>           | <span data-ttu-id="da7f9-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da7f9-241">0x00000010</span></span>                                                              |
| <span data-ttu-id="da7f9-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da7f9-242">Classes used in</span></span>        | [<span data-ttu-id="da7f9-243">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="da7f9-243">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="da7f9-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="da7f9-244">Windows Server 2012</span></span>



| <span data-ttu-id="da7f9-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da7f9-245">Entry</span></span> | <span data-ttu-id="da7f9-246">Wert</span><span class="sxs-lookup"><span data-stu-id="da7f9-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="da7f9-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="da7f9-247">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="da7f9-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da7f9-248">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="da7f9-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="da7f9-249">System-Only</span></span>            | <span data-ttu-id="da7f9-250">False</span><span class="sxs-lookup"><span data-stu-id="da7f9-250">False</span></span>                                                                   |
| <span data-ttu-id="da7f9-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="da7f9-251">Is-Single-Valued</span></span>       | <span data-ttu-id="da7f9-252">False</span><span class="sxs-lookup"><span data-stu-id="da7f9-252">False</span></span>                                                                   |
| <span data-ttu-id="da7f9-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="da7f9-253">Is Indexed</span></span>             | <span data-ttu-id="da7f9-254">False</span><span class="sxs-lookup"><span data-stu-id="da7f9-254">False</span></span>                                                                   |
| <span data-ttu-id="da7f9-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="da7f9-255">In Global Catalog</span></span>      | <span data-ttu-id="da7f9-256">Richtig</span><span class="sxs-lookup"><span data-stu-id="da7f9-256">True</span></span>                                                                    |
| <span data-ttu-id="da7f9-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da7f9-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="da7f9-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="da7f9-258">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="da7f9-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da7f9-259">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="da7f9-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da7f9-260">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="da7f9-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da7f9-261">Search-Flags</span></span>           | <span data-ttu-id="da7f9-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da7f9-262">0x00000000</span></span>                                                              |
| <span data-ttu-id="da7f9-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da7f9-263">System-Flags</span></span>           | <span data-ttu-id="da7f9-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da7f9-264">0x00000010</span></span>                                                              |
| <span data-ttu-id="da7f9-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="da7f9-265">Classes used in</span></span>        | [<span data-ttu-id="da7f9-266">**PKI-Zertifikat-Vorlage**</span><span class="sxs-lookup"><span data-stu-id="da7f9-266">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





