---
title: ZS-Web-URL-Attribut
description: URL für die HTTP-Verbindung mit einer Zertifizierungsstelle.
ms.assetid: 148bab57-25ae-467a-86a2-dbf83e69979e
ms.tgt_platform: multiple
keywords:
- AD-Schema für ZS-Web-URL-Attribut
- caweburl-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- CA-WEB-URL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42b49efb851b0720499f5b641770279c12cb9563
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107270"
---
# <a name="ca-web-url-attribute"></a><span data-ttu-id="1fed8-105">ZS-Web-URL-Attribut</span><span class="sxs-lookup"><span data-stu-id="1fed8-105">CA-WEB-URL attribute</span></span>

<span data-ttu-id="1fed8-106">URL für die HTTP-Verbindung mit einer Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="1fed8-106">URL for http connection to a certification authority.</span></span>



| <span data-ttu-id="1fed8-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1fed8-107">Entry</span></span> | <span data-ttu-id="1fed8-108">Wert</span><span class="sxs-lookup"><span data-stu-id="1fed8-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="1fed8-109">CN</span><span class="sxs-lookup"><span data-stu-id="1fed8-109">CN</span></span>                | <span data-ttu-id="1fed8-110">ZS-Web-URL</span><span class="sxs-lookup"><span data-stu-id="1fed8-110">CA-WEB-URL</span></span>                                  |
| <span data-ttu-id="1fed8-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1fed8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1fed8-112">caweburl</span><span class="sxs-lookup"><span data-stu-id="1fed8-112">cAWEBURL</span></span>                                    |
| <span data-ttu-id="1fed8-113">Size</span><span class="sxs-lookup"><span data-stu-id="1fed8-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="1fed8-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="1fed8-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="1fed8-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="1fed8-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="1fed8-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1fed8-116">Attribute-Id</span></span>      | <span data-ttu-id="1fed8-117">1.2.840.113556.1.4.688</span><span class="sxs-lookup"><span data-stu-id="1fed8-117">1.2.840.113556.1.4.688</span></span>                      |
| <span data-ttu-id="1fed8-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1fed8-118">System-Id-Guid</span></span>    | <span data-ttu-id="1fed8-119">963d2736-48be-11d1-a9c3-0000 C1</span><span class="sxs-lookup"><span data-stu-id="1fed8-119">963d2736-48be-11d1-a9c3-0000f80367c1</span></span>        |
| <span data-ttu-id="1fed8-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fed8-120">Syntax</span></span>            | [<span data-ttu-id="1fed8-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="1fed8-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="1fed8-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="1fed8-122">Implementations</span></span>

-   [<span data-ttu-id="1fed8-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1fed8-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1fed8-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1fed8-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1fed8-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1fed8-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1fed8-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1fed8-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1fed8-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1fed8-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1fed8-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1fed8-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1fed8-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1fed8-129">Windows 2000 Server</span></span>



| <span data-ttu-id="1fed8-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1fed8-130">Entry</span></span> | <span data-ttu-id="1fed8-131">Wert</span><span class="sxs-lookup"><span data-stu-id="1fed8-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="1fed8-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1fed8-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1fed8-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fed8-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1fed8-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fed8-134">System-Only</span></span>            | <span data-ttu-id="1fed8-135">False</span><span class="sxs-lookup"><span data-stu-id="1fed8-135">False</span></span>                                                                  |
| <span data-ttu-id="1fed8-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1fed8-136">Is-Single-Valued</span></span>       | <span data-ttu-id="1fed8-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="1fed8-137">True</span></span>                                                                   |
| <span data-ttu-id="1fed8-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1fed8-138">Is Indexed</span></span>             | <span data-ttu-id="1fed8-139">False</span><span class="sxs-lookup"><span data-stu-id="1fed8-139">False</span></span>                                                                  |
| <span data-ttu-id="1fed8-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1fed8-140">In Global Catalog</span></span>      | <span data-ttu-id="1fed8-141">False</span><span class="sxs-lookup"><span data-stu-id="1fed8-141">False</span></span>                                                                  |
| <span data-ttu-id="1fed8-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1fed8-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fed8-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1fed8-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="1fed8-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fed8-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="1fed8-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fed8-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="1fed8-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fed8-146">Search-Flags</span></span>           | <span data-ttu-id="1fed8-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fed8-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="1fed8-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fed8-148">System-Flags</span></span>           | <span data-ttu-id="1fed8-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1fed8-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="1fed8-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1fed8-150">Classes used in</span></span>        | [<span data-ttu-id="1fed8-151">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="1fed8-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1fed8-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1fed8-152">Windows Server 2003</span></span>



| <span data-ttu-id="1fed8-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1fed8-153">Entry</span></span> | <span data-ttu-id="1fed8-154">Wert</span><span class="sxs-lookup"><span data-stu-id="1fed8-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="1fed8-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1fed8-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1fed8-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fed8-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1fed8-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fed8-157">System-Only</span></span>            | <span data-ttu-id="1fed8-158">False</span><span class="sxs-lookup"><span data-stu-id="1fed8-158">False</span></span>                                                                  |
| <span data-ttu-id="1fed8-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1fed8-159">Is-Single-Valued</span></span>       | <span data-ttu-id="1fed8-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="1fed8-160">True</span></span>                                                                   |
| <span data-ttu-id="1fed8-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1fed8-161">Is Indexed</span></span>             | <span data-ttu-id="1fed8-162">False</span><span class="sxs-lookup"><span data-stu-id="1fed8-162">False</span></span>                                                                  |
| <span data-ttu-id="1fed8-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1fed8-163">In Global Catalog</span></span>      | <span data-ttu-id="1fed8-164">False</span><span class="sxs-lookup"><span data-stu-id="1fed8-164">False</span></span>                                                                  |
| <span data-ttu-id="1fed8-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1fed8-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fed8-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1fed8-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="1fed8-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fed8-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="1fed8-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fed8-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="1fed8-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fed8-169">Search-Flags</span></span>           | <span data-ttu-id="1fed8-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fed8-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="1fed8-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fed8-171">System-Flags</span></span>           | <span data-ttu-id="1fed8-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1fed8-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="1fed8-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1fed8-173">Classes used in</span></span>        | [<span data-ttu-id="1fed8-174">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="1fed8-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1fed8-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1fed8-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1fed8-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1fed8-176">Entry</span></span> | <span data-ttu-id="1fed8-177">Wert</span><span class="sxs-lookup"><span data-stu-id="1fed8-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="1fed8-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1fed8-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1fed8-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fed8-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1fed8-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fed8-180">System-Only</span></span>            | <span data-ttu-id="1fed8-181">False</span><span class="sxs-lookup"><span data-stu-id="1fed8-181">False</span></span>                                                                  |
| <span data-ttu-id="1fed8-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1fed8-182">Is-Single-Valued</span></span>       | <span data-ttu-id="1fed8-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="1fed8-183">True</span></span>                                                                   |
| <span data-ttu-id="1fed8-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1fed8-184">Is Indexed</span></span>             | <span data-ttu-id="1fed8-185">False</span><span class="sxs-lookup"><span data-stu-id="1fed8-185">False</span></span>                                                                  |
| <span data-ttu-id="1fed8-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1fed8-186">In Global Catalog</span></span>      | <span data-ttu-id="1fed8-187">False</span><span class="sxs-lookup"><span data-stu-id="1fed8-187">False</span></span>                                                                  |
| <span data-ttu-id="1fed8-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1fed8-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fed8-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1fed8-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="1fed8-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fed8-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="1fed8-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fed8-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="1fed8-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fed8-192">Search-Flags</span></span>           | <span data-ttu-id="1fed8-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fed8-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="1fed8-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fed8-194">System-Flags</span></span>           | <span data-ttu-id="1fed8-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1fed8-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="1fed8-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1fed8-196">Classes used in</span></span>        | [<span data-ttu-id="1fed8-197">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="1fed8-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1fed8-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1fed8-198">Windows Server 2008</span></span>



| <span data-ttu-id="1fed8-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1fed8-199">Entry</span></span> | <span data-ttu-id="1fed8-200">Wert</span><span class="sxs-lookup"><span data-stu-id="1fed8-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="1fed8-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1fed8-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1fed8-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fed8-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1fed8-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fed8-203">System-Only</span></span>            | <span data-ttu-id="1fed8-204">False</span><span class="sxs-lookup"><span data-stu-id="1fed8-204">False</span></span>                                                                  |
| <span data-ttu-id="1fed8-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1fed8-205">Is-Single-Valued</span></span>       | <span data-ttu-id="1fed8-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="1fed8-206">True</span></span>                                                                   |
| <span data-ttu-id="1fed8-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1fed8-207">Is Indexed</span></span>             | <span data-ttu-id="1fed8-208">False</span><span class="sxs-lookup"><span data-stu-id="1fed8-208">False</span></span>                                                                  |
| <span data-ttu-id="1fed8-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1fed8-209">In Global Catalog</span></span>      | <span data-ttu-id="1fed8-210">False</span><span class="sxs-lookup"><span data-stu-id="1fed8-210">False</span></span>                                                                  |
| <span data-ttu-id="1fed8-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1fed8-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fed8-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1fed8-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="1fed8-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fed8-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="1fed8-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fed8-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="1fed8-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fed8-215">Search-Flags</span></span>           | <span data-ttu-id="1fed8-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fed8-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="1fed8-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fed8-217">System-Flags</span></span>           | <span data-ttu-id="1fed8-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1fed8-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="1fed8-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1fed8-219">Classes used in</span></span>        | [<span data-ttu-id="1fed8-220">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="1fed8-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1fed8-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1fed8-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1fed8-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1fed8-222">Entry</span></span> | <span data-ttu-id="1fed8-223">Wert</span><span class="sxs-lookup"><span data-stu-id="1fed8-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="1fed8-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1fed8-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1fed8-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fed8-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1fed8-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fed8-226">System-Only</span></span>            | <span data-ttu-id="1fed8-227">False</span><span class="sxs-lookup"><span data-stu-id="1fed8-227">False</span></span>                                                                  |
| <span data-ttu-id="1fed8-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1fed8-228">Is-Single-Valued</span></span>       | <span data-ttu-id="1fed8-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="1fed8-229">True</span></span>                                                                   |
| <span data-ttu-id="1fed8-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1fed8-230">Is Indexed</span></span>             | <span data-ttu-id="1fed8-231">False</span><span class="sxs-lookup"><span data-stu-id="1fed8-231">False</span></span>                                                                  |
| <span data-ttu-id="1fed8-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1fed8-232">In Global Catalog</span></span>      | <span data-ttu-id="1fed8-233">False</span><span class="sxs-lookup"><span data-stu-id="1fed8-233">False</span></span>                                                                  |
| <span data-ttu-id="1fed8-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1fed8-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fed8-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1fed8-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="1fed8-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fed8-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="1fed8-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fed8-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="1fed8-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fed8-238">Search-Flags</span></span>           | <span data-ttu-id="1fed8-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fed8-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="1fed8-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fed8-240">System-Flags</span></span>           | <span data-ttu-id="1fed8-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1fed8-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="1fed8-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1fed8-242">Classes used in</span></span>        | [<span data-ttu-id="1fed8-243">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="1fed8-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1fed8-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1fed8-244">Windows Server 2012</span></span>



| <span data-ttu-id="1fed8-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1fed8-245">Entry</span></span> | <span data-ttu-id="1fed8-246">Wert</span><span class="sxs-lookup"><span data-stu-id="1fed8-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="1fed8-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1fed8-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1fed8-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fed8-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="1fed8-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fed8-249">System-Only</span></span>            | <span data-ttu-id="1fed8-250">False</span><span class="sxs-lookup"><span data-stu-id="1fed8-250">False</span></span>                                                                  |
| <span data-ttu-id="1fed8-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1fed8-251">Is-Single-Valued</span></span>       | <span data-ttu-id="1fed8-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="1fed8-252">True</span></span>                                                                   |
| <span data-ttu-id="1fed8-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1fed8-253">Is Indexed</span></span>             | <span data-ttu-id="1fed8-254">False</span><span class="sxs-lookup"><span data-stu-id="1fed8-254">False</span></span>                                                                  |
| <span data-ttu-id="1fed8-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1fed8-255">In Global Catalog</span></span>      | <span data-ttu-id="1fed8-256">False</span><span class="sxs-lookup"><span data-stu-id="1fed8-256">False</span></span>                                                                  |
| <span data-ttu-id="1fed8-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1fed8-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fed8-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1fed8-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="1fed8-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fed8-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="1fed8-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fed8-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="1fed8-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fed8-261">Search-Flags</span></span>           | <span data-ttu-id="1fed8-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fed8-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="1fed8-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fed8-263">System-Flags</span></span>           | <span data-ttu-id="1fed8-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1fed8-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="1fed8-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1fed8-265">Classes used in</span></span>        | [<span data-ttu-id="1fed8-266">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="1fed8-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





