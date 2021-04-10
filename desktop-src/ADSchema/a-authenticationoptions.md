---
title: Authentication-Options-Attribut
description: Die Authentifizierungs Optionen, die in ADSI zum Binden an Verzeichnisdienst Objekte verwendet werden.
ms.assetid: a6dc4591-d825-456a-8f77-78cb3c91af9f
ms.tgt_platform: multiple
keywords:
- AD-Schema für Authentication-Options-Attribut
- AD-Schema des authenticationoptions-Attributs
topic_type:
- apiref
api_name:
- Authentication-Options
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cfa9c422dfe196ab002c02c361759461f43965d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107294"
---
# <a name="authentication-options-attribute"></a><span data-ttu-id="a8a51-105">Authentication-Options-Attribut</span><span class="sxs-lookup"><span data-stu-id="a8a51-105">Authentication-Options attribute</span></span>

<span data-ttu-id="a8a51-106">Die Authentifizierungs Optionen, die in ADSI zum Binden an Verzeichnisdienst Objekte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a8a51-106">The authentication options used in ADSI to bind to directory services objects.</span></span>



| <span data-ttu-id="a8a51-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8a51-107">Entry</span></span> | <span data-ttu-id="a8a51-108">Wert</span><span class="sxs-lookup"><span data-stu-id="a8a51-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8a51-109">CN</span><span class="sxs-lookup"><span data-stu-id="a8a51-109">CN</span></span>                | <span data-ttu-id="a8a51-110">Authentication-Options</span><span class="sxs-lookup"><span data-stu-id="a8a51-110">Authentication-Options</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="a8a51-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a8a51-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a8a51-112">authenticationoptions</span><span class="sxs-lookup"><span data-stu-id="a8a51-112">authenticationOptions</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a8a51-113">Size</span><span class="sxs-lookup"><span data-stu-id="a8a51-113">Size</span></span>              | <span data-ttu-id="a8a51-114">4 Bytes.</span><span class="sxs-lookup"><span data-stu-id="a8a51-114">4 bytes.</span></span> <span data-ttu-id="a8a51-115">In IADs. h: ADS \_ sichere \_ Authentifizierung 0x1 definierte Werte, ADS \_ verwenden \_ Verschlüsselung 0x2, ADS \_ verwenden \_ SSL 0x2, ADS Schreib geschützter \_ \_ Server 0x4, anzeigen \_ der \_ Anmelde Informationen 0x8, ADS \_ keine \_ Authentifizierung 0x10, ADS \_ schnelles \_ binden 0x20, anzeigen \_ \_ Signierung 0x40, anzeigen verwenden der \_ \_ Versiegelung 0x80</span><span class="sxs-lookup"><span data-stu-id="a8a51-115">Values defined in IADS.h: ADS\_SECURE\_AUTHENTICATION 0x1, ADS\_USE\_ENCRYPTION 0x2, ADS\_USE\_SSL 0x2, ADS\_READONLY\_SERVER 0x4, ADS\_PROMPT\_CREDENTIALS 0x8, ADS\_NO\_AUTHENTICATION 0x10, ADS\_FAST\_BIND 0x20, ADS\_USE\_SIGNING 0x40, ADS\_USE\_SEALING 0x80</span></span> |
| <span data-ttu-id="a8a51-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a8a51-116">Update Privilege</span></span>  | \-                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a8a51-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="a8a51-117">Update Frequency</span></span>  | \-                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a8a51-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a8a51-118">Attribute-Id</span></span>      | <span data-ttu-id="a8a51-119">1.2.840.113556.1.4.11</span><span class="sxs-lookup"><span data-stu-id="a8a51-119">1.2.840.113556.1.4.11</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a8a51-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a8a51-120">System-Id-Guid</span></span>    | <span data-ttu-id="a8a51-121">bf967928-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a8a51-121">bf967928-0de6-11d0-a285-00aa003049e2</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="a8a51-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8a51-122">Syntax</span></span>            | [<span data-ttu-id="a8a51-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="a8a51-123">**Enumeration**</span></span>](s-enumeration.md)                                                                                                                                                                                                                                         |



## <a name="implementations"></a><span data-ttu-id="a8a51-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="a8a51-124">Implementations</span></span>

-   [<span data-ttu-id="a8a51-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a8a51-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a8a51-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a8a51-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a8a51-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a8a51-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a8a51-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a8a51-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a8a51-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a8a51-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a8a51-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a8a51-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a8a51-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a8a51-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a8a51-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8a51-132">Entry</span></span> | <span data-ttu-id="a8a51-133">Wert</span><span class="sxs-lookup"><span data-stu-id="a8a51-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a8a51-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a8a51-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a8a51-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8a51-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a8a51-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8a51-136">System-Only</span></span>            | <span data-ttu-id="a8a51-137">False</span><span class="sxs-lookup"><span data-stu-id="a8a51-137">False</span></span>                                              |
| <span data-ttu-id="a8a51-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a8a51-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a8a51-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="a8a51-139">True</span></span>                                               |
| <span data-ttu-id="a8a51-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a8a51-140">Is Indexed</span></span>             | <span data-ttu-id="a8a51-141">False</span><span class="sxs-lookup"><span data-stu-id="a8a51-141">False</span></span>                                              |
| <span data-ttu-id="a8a51-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a8a51-142">In Global Catalog</span></span>      | <span data-ttu-id="a8a51-143">False</span><span class="sxs-lookup"><span data-stu-id="a8a51-143">False</span></span>                                              |
| <span data-ttu-id="a8a51-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8a51-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8a51-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a8a51-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a8a51-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8a51-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a8a51-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8a51-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a8a51-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8a51-148">Search-Flags</span></span>           | <span data-ttu-id="a8a51-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8a51-149">0x00000000</span></span>                                         |
| <span data-ttu-id="a8a51-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8a51-150">System-Flags</span></span>           | <span data-ttu-id="a8a51-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8a51-151">0x00000010</span></span>                                         |
| <span data-ttu-id="a8a51-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a8a51-152">Classes used in</span></span>        | [<span data-ttu-id="a8a51-153">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="a8a51-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a8a51-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a8a51-154">Windows Server 2003</span></span>



| <span data-ttu-id="a8a51-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8a51-155">Entry</span></span> | <span data-ttu-id="a8a51-156">Wert</span><span class="sxs-lookup"><span data-stu-id="a8a51-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a8a51-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a8a51-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a8a51-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8a51-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a8a51-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8a51-159">System-Only</span></span>            | <span data-ttu-id="a8a51-160">False</span><span class="sxs-lookup"><span data-stu-id="a8a51-160">False</span></span>                                              |
| <span data-ttu-id="a8a51-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a8a51-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a8a51-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="a8a51-162">True</span></span>                                               |
| <span data-ttu-id="a8a51-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a8a51-163">Is Indexed</span></span>             | <span data-ttu-id="a8a51-164">False</span><span class="sxs-lookup"><span data-stu-id="a8a51-164">False</span></span>                                              |
| <span data-ttu-id="a8a51-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a8a51-165">In Global Catalog</span></span>      | <span data-ttu-id="a8a51-166">False</span><span class="sxs-lookup"><span data-stu-id="a8a51-166">False</span></span>                                              |
| <span data-ttu-id="a8a51-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8a51-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8a51-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a8a51-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a8a51-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8a51-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a8a51-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8a51-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a8a51-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8a51-171">Search-Flags</span></span>           | <span data-ttu-id="a8a51-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8a51-172">0x00000000</span></span>                                         |
| <span data-ttu-id="a8a51-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8a51-173">System-Flags</span></span>           | <span data-ttu-id="a8a51-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8a51-174">0x00000010</span></span>                                         |
| <span data-ttu-id="a8a51-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a8a51-175">Classes used in</span></span>        | [<span data-ttu-id="a8a51-176">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="a8a51-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a8a51-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a8a51-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a8a51-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8a51-178">Entry</span></span> | <span data-ttu-id="a8a51-179">Wert</span><span class="sxs-lookup"><span data-stu-id="a8a51-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a8a51-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a8a51-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a8a51-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8a51-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a8a51-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8a51-182">System-Only</span></span>            | <span data-ttu-id="a8a51-183">False</span><span class="sxs-lookup"><span data-stu-id="a8a51-183">False</span></span>                                              |
| <span data-ttu-id="a8a51-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a8a51-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a8a51-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="a8a51-185">True</span></span>                                               |
| <span data-ttu-id="a8a51-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a8a51-186">Is Indexed</span></span>             | <span data-ttu-id="a8a51-187">False</span><span class="sxs-lookup"><span data-stu-id="a8a51-187">False</span></span>                                              |
| <span data-ttu-id="a8a51-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a8a51-188">In Global Catalog</span></span>      | <span data-ttu-id="a8a51-189">False</span><span class="sxs-lookup"><span data-stu-id="a8a51-189">False</span></span>                                              |
| <span data-ttu-id="a8a51-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8a51-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8a51-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a8a51-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a8a51-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8a51-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a8a51-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8a51-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a8a51-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8a51-194">Search-Flags</span></span>           | <span data-ttu-id="a8a51-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8a51-195">0x00000000</span></span>                                         |
| <span data-ttu-id="a8a51-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8a51-196">System-Flags</span></span>           | <span data-ttu-id="a8a51-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8a51-197">0x00000010</span></span>                                         |
| <span data-ttu-id="a8a51-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a8a51-198">Classes used in</span></span>        | [<span data-ttu-id="a8a51-199">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="a8a51-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a8a51-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8a51-200">Windows Server 2008</span></span>



| <span data-ttu-id="a8a51-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8a51-201">Entry</span></span> | <span data-ttu-id="a8a51-202">Wert</span><span class="sxs-lookup"><span data-stu-id="a8a51-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a8a51-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a8a51-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a8a51-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8a51-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a8a51-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8a51-205">System-Only</span></span>            | <span data-ttu-id="a8a51-206">False</span><span class="sxs-lookup"><span data-stu-id="a8a51-206">False</span></span>                                              |
| <span data-ttu-id="a8a51-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a8a51-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a8a51-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="a8a51-208">True</span></span>                                               |
| <span data-ttu-id="a8a51-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a8a51-209">Is Indexed</span></span>             | <span data-ttu-id="a8a51-210">False</span><span class="sxs-lookup"><span data-stu-id="a8a51-210">False</span></span>                                              |
| <span data-ttu-id="a8a51-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a8a51-211">In Global Catalog</span></span>      | <span data-ttu-id="a8a51-212">False</span><span class="sxs-lookup"><span data-stu-id="a8a51-212">False</span></span>                                              |
| <span data-ttu-id="a8a51-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8a51-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8a51-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a8a51-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a8a51-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8a51-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a8a51-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8a51-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a8a51-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8a51-217">Search-Flags</span></span>           | <span data-ttu-id="a8a51-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8a51-218">0x00000000</span></span>                                         |
| <span data-ttu-id="a8a51-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8a51-219">System-Flags</span></span>           | <span data-ttu-id="a8a51-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8a51-220">0x00000010</span></span>                                         |
| <span data-ttu-id="a8a51-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a8a51-221">Classes used in</span></span>        | [<span data-ttu-id="a8a51-222">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="a8a51-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a8a51-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a8a51-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a8a51-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8a51-224">Entry</span></span> | <span data-ttu-id="a8a51-225">Wert</span><span class="sxs-lookup"><span data-stu-id="a8a51-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a8a51-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a8a51-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a8a51-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8a51-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a8a51-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8a51-228">System-Only</span></span>            | <span data-ttu-id="a8a51-229">False</span><span class="sxs-lookup"><span data-stu-id="a8a51-229">False</span></span>                                              |
| <span data-ttu-id="a8a51-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a8a51-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a8a51-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="a8a51-231">True</span></span>                                               |
| <span data-ttu-id="a8a51-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a8a51-232">Is Indexed</span></span>             | <span data-ttu-id="a8a51-233">False</span><span class="sxs-lookup"><span data-stu-id="a8a51-233">False</span></span>                                              |
| <span data-ttu-id="a8a51-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a8a51-234">In Global Catalog</span></span>      | <span data-ttu-id="a8a51-235">False</span><span class="sxs-lookup"><span data-stu-id="a8a51-235">False</span></span>                                              |
| <span data-ttu-id="a8a51-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8a51-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8a51-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a8a51-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a8a51-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8a51-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a8a51-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8a51-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a8a51-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8a51-240">Search-Flags</span></span>           | <span data-ttu-id="a8a51-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8a51-241">0x00000000</span></span>                                         |
| <span data-ttu-id="a8a51-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8a51-242">System-Flags</span></span>           | <span data-ttu-id="a8a51-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8a51-243">0x00000010</span></span>                                         |
| <span data-ttu-id="a8a51-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a8a51-244">Classes used in</span></span>        | [<span data-ttu-id="a8a51-245">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="a8a51-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a8a51-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a8a51-246">Windows Server 2012</span></span>



| <span data-ttu-id="a8a51-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8a51-247">Entry</span></span> | <span data-ttu-id="a8a51-248">Wert</span><span class="sxs-lookup"><span data-stu-id="a8a51-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a8a51-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a8a51-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a8a51-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8a51-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a8a51-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8a51-251">System-Only</span></span>            | <span data-ttu-id="a8a51-252">False</span><span class="sxs-lookup"><span data-stu-id="a8a51-252">False</span></span>                                              |
| <span data-ttu-id="a8a51-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a8a51-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a8a51-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="a8a51-254">True</span></span>                                               |
| <span data-ttu-id="a8a51-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a8a51-255">Is Indexed</span></span>             | <span data-ttu-id="a8a51-256">False</span><span class="sxs-lookup"><span data-stu-id="a8a51-256">False</span></span>                                              |
| <span data-ttu-id="a8a51-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a8a51-257">In Global Catalog</span></span>      | <span data-ttu-id="a8a51-258">False</span><span class="sxs-lookup"><span data-stu-id="a8a51-258">False</span></span>                                              |
| <span data-ttu-id="a8a51-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8a51-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8a51-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a8a51-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a8a51-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8a51-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a8a51-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8a51-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a8a51-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8a51-263">Search-Flags</span></span>           | <span data-ttu-id="a8a51-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8a51-264">0x00000000</span></span>                                         |
| <span data-ttu-id="a8a51-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8a51-265">System-Flags</span></span>           | <span data-ttu-id="a8a51-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8a51-266">0x00000010</span></span>                                         |
| <span data-ttu-id="a8a51-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a8a51-267">Classes used in</span></span>        | [<span data-ttu-id="a8a51-268">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="a8a51-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





