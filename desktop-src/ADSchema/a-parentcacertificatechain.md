---
title: Parent-CA-Certificate-Chain-Attribut
description: Der-codiertes X. 509v3-Zertifikat für die übergeordnete Zertifizierungsstelle.
ms.assetid: 37e04c7b-5350-4e48-b3fd-22f97959d26a
ms.tgt_platform: multiple
keywords:
- AD-Schema für übergeordnete Zertifizierungsstellen-Zertifikat Kette
- cschema für das Attribut "centcacertificatechain"
topic_type:
- apiref
api_name:
- Parent-CA-Certificate-Chain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62f27bacb77fb7ab3f1ae712920dace7cb525efc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479975"
---
# <a name="parent-ca-certificate-chain-attribute"></a><span data-ttu-id="6a1fb-105">Parent-CA-Certificate-Chain-Attribut</span><span class="sxs-lookup"><span data-stu-id="6a1fb-105">Parent-CA-Certificate-Chain attribute</span></span>

<span data-ttu-id="6a1fb-106">Der-codiertes X. 509v3-Zertifikat für die übergeordnete Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="6a1fb-106">DER-encoded X.509v3 certificate for the parent certification authority.</span></span>



| <span data-ttu-id="6a1fb-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6a1fb-107">Entry</span></span> | <span data-ttu-id="6a1fb-108">Wert</span><span class="sxs-lookup"><span data-stu-id="6a1fb-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="6a1fb-109">CN</span><span class="sxs-lookup"><span data-stu-id="6a1fb-109">CN</span></span>                | <span data-ttu-id="6a1fb-110">Übergeordnete Zertifizierungsstellen-Zertifikat Kette</span><span class="sxs-lookup"><span data-stu-id="6a1fb-110">Parent-CA-Certificate-Chain</span></span>                           |
| <span data-ttu-id="6a1fb-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6a1fb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6a1fb-112">parametricacertificatechain</span><span class="sxs-lookup"><span data-stu-id="6a1fb-112">parentCACertificateChain</span></span>                              |
| <span data-ttu-id="6a1fb-113">Size</span><span class="sxs-lookup"><span data-stu-id="6a1fb-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="6a1fb-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="6a1fb-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="6a1fb-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="6a1fb-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="6a1fb-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6a1fb-116">Attribute-Id</span></span>      | <span data-ttu-id="6a1fb-117">1.2.840.113556.1.4.685</span><span class="sxs-lookup"><span data-stu-id="6a1fb-117">1.2.840.113556.1.4.685</span></span>                                |
| <span data-ttu-id="6a1fb-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6a1fb-118">System-Id-Guid</span></span>    | <span data-ttu-id="6a1fb-119">963d2733-48be-11d1-a9c3-0000 C1</span><span class="sxs-lookup"><span data-stu-id="6a1fb-119">963d2733-48be-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="6a1fb-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a1fb-120">Syntax</span></span>            | [<span data-ttu-id="6a1fb-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="6a1fb-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="6a1fb-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="6a1fb-122">Implementations</span></span>

-   [<span data-ttu-id="6a1fb-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6a1fb-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6a1fb-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6a1fb-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6a1fb-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6a1fb-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6a1fb-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6a1fb-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6a1fb-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6a1fb-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6a1fb-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6a1fb-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6a1fb-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6a1fb-129">Windows 2000 Server</span></span>



| <span data-ttu-id="6a1fb-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6a1fb-130">Entry</span></span> | <span data-ttu-id="6a1fb-131">Wert</span><span class="sxs-lookup"><span data-stu-id="6a1fb-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="6a1fb-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6a1fb-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6a1fb-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a1fb-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6a1fb-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a1fb-134">System-Only</span></span>            | <span data-ttu-id="6a1fb-135">False</span><span class="sxs-lookup"><span data-stu-id="6a1fb-135">False</span></span>                                                                  |
| <span data-ttu-id="6a1fb-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6a1fb-136">Is-Single-Valued</span></span>       | <span data-ttu-id="6a1fb-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="6a1fb-137">True</span></span>                                                                   |
| <span data-ttu-id="6a1fb-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6a1fb-138">Is Indexed</span></span>             | <span data-ttu-id="6a1fb-139">False</span><span class="sxs-lookup"><span data-stu-id="6a1fb-139">False</span></span>                                                                  |
| <span data-ttu-id="6a1fb-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6a1fb-140">In Global Catalog</span></span>      | <span data-ttu-id="6a1fb-141">False</span><span class="sxs-lookup"><span data-stu-id="6a1fb-141">False</span></span>                                                                  |
| <span data-ttu-id="6a1fb-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6a1fb-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a1fb-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6a1fb-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="6a1fb-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a1fb-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="6a1fb-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a1fb-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="6a1fb-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a1fb-146">Search-Flags</span></span>           | <span data-ttu-id="6a1fb-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a1fb-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="6a1fb-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a1fb-148">System-Flags</span></span>           | <span data-ttu-id="6a1fb-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a1fb-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="6a1fb-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6a1fb-150">Classes used in</span></span>        | [<span data-ttu-id="6a1fb-151">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="6a1fb-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6a1fb-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6a1fb-152">Windows Server 2003</span></span>



| <span data-ttu-id="6a1fb-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6a1fb-153">Entry</span></span> | <span data-ttu-id="6a1fb-154">Wert</span><span class="sxs-lookup"><span data-stu-id="6a1fb-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="6a1fb-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6a1fb-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6a1fb-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a1fb-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6a1fb-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a1fb-157">System-Only</span></span>            | <span data-ttu-id="6a1fb-158">False</span><span class="sxs-lookup"><span data-stu-id="6a1fb-158">False</span></span>                                                                  |
| <span data-ttu-id="6a1fb-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6a1fb-159">Is-Single-Valued</span></span>       | <span data-ttu-id="6a1fb-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="6a1fb-160">True</span></span>                                                                   |
| <span data-ttu-id="6a1fb-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6a1fb-161">Is Indexed</span></span>             | <span data-ttu-id="6a1fb-162">False</span><span class="sxs-lookup"><span data-stu-id="6a1fb-162">False</span></span>                                                                  |
| <span data-ttu-id="6a1fb-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6a1fb-163">In Global Catalog</span></span>      | <span data-ttu-id="6a1fb-164">False</span><span class="sxs-lookup"><span data-stu-id="6a1fb-164">False</span></span>                                                                  |
| <span data-ttu-id="6a1fb-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6a1fb-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a1fb-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6a1fb-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="6a1fb-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a1fb-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="6a1fb-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a1fb-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="6a1fb-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a1fb-169">Search-Flags</span></span>           | <span data-ttu-id="6a1fb-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a1fb-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="6a1fb-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a1fb-171">System-Flags</span></span>           | <span data-ttu-id="6a1fb-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a1fb-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="6a1fb-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6a1fb-173">Classes used in</span></span>        | [<span data-ttu-id="6a1fb-174">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="6a1fb-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6a1fb-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6a1fb-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6a1fb-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6a1fb-176">Entry</span></span> | <span data-ttu-id="6a1fb-177">Wert</span><span class="sxs-lookup"><span data-stu-id="6a1fb-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="6a1fb-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6a1fb-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6a1fb-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a1fb-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6a1fb-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a1fb-180">System-Only</span></span>            | <span data-ttu-id="6a1fb-181">False</span><span class="sxs-lookup"><span data-stu-id="6a1fb-181">False</span></span>                                                                  |
| <span data-ttu-id="6a1fb-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6a1fb-182">Is-Single-Valued</span></span>       | <span data-ttu-id="6a1fb-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="6a1fb-183">True</span></span>                                                                   |
| <span data-ttu-id="6a1fb-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6a1fb-184">Is Indexed</span></span>             | <span data-ttu-id="6a1fb-185">False</span><span class="sxs-lookup"><span data-stu-id="6a1fb-185">False</span></span>                                                                  |
| <span data-ttu-id="6a1fb-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6a1fb-186">In Global Catalog</span></span>      | <span data-ttu-id="6a1fb-187">False</span><span class="sxs-lookup"><span data-stu-id="6a1fb-187">False</span></span>                                                                  |
| <span data-ttu-id="6a1fb-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6a1fb-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a1fb-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6a1fb-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="6a1fb-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a1fb-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="6a1fb-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a1fb-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="6a1fb-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a1fb-192">Search-Flags</span></span>           | <span data-ttu-id="6a1fb-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a1fb-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="6a1fb-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a1fb-194">System-Flags</span></span>           | <span data-ttu-id="6a1fb-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a1fb-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="6a1fb-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6a1fb-196">Classes used in</span></span>        | [<span data-ttu-id="6a1fb-197">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="6a1fb-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6a1fb-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a1fb-198">Windows Server 2008</span></span>



| <span data-ttu-id="6a1fb-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6a1fb-199">Entry</span></span> | <span data-ttu-id="6a1fb-200">Wert</span><span class="sxs-lookup"><span data-stu-id="6a1fb-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="6a1fb-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6a1fb-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6a1fb-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a1fb-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6a1fb-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a1fb-203">System-Only</span></span>            | <span data-ttu-id="6a1fb-204">False</span><span class="sxs-lookup"><span data-stu-id="6a1fb-204">False</span></span>                                                                  |
| <span data-ttu-id="6a1fb-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6a1fb-205">Is-Single-Valued</span></span>       | <span data-ttu-id="6a1fb-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="6a1fb-206">True</span></span>                                                                   |
| <span data-ttu-id="6a1fb-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6a1fb-207">Is Indexed</span></span>             | <span data-ttu-id="6a1fb-208">False</span><span class="sxs-lookup"><span data-stu-id="6a1fb-208">False</span></span>                                                                  |
| <span data-ttu-id="6a1fb-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6a1fb-209">In Global Catalog</span></span>      | <span data-ttu-id="6a1fb-210">False</span><span class="sxs-lookup"><span data-stu-id="6a1fb-210">False</span></span>                                                                  |
| <span data-ttu-id="6a1fb-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6a1fb-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a1fb-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6a1fb-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="6a1fb-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a1fb-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="6a1fb-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a1fb-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="6a1fb-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a1fb-215">Search-Flags</span></span>           | <span data-ttu-id="6a1fb-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a1fb-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="6a1fb-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a1fb-217">System-Flags</span></span>           | <span data-ttu-id="6a1fb-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a1fb-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="6a1fb-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6a1fb-219">Classes used in</span></span>        | [<span data-ttu-id="6a1fb-220">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="6a1fb-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6a1fb-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6a1fb-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6a1fb-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6a1fb-222">Entry</span></span> | <span data-ttu-id="6a1fb-223">Wert</span><span class="sxs-lookup"><span data-stu-id="6a1fb-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="6a1fb-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6a1fb-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6a1fb-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a1fb-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6a1fb-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a1fb-226">System-Only</span></span>            | <span data-ttu-id="6a1fb-227">False</span><span class="sxs-lookup"><span data-stu-id="6a1fb-227">False</span></span>                                                                  |
| <span data-ttu-id="6a1fb-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6a1fb-228">Is-Single-Valued</span></span>       | <span data-ttu-id="6a1fb-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="6a1fb-229">True</span></span>                                                                   |
| <span data-ttu-id="6a1fb-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6a1fb-230">Is Indexed</span></span>             | <span data-ttu-id="6a1fb-231">False</span><span class="sxs-lookup"><span data-stu-id="6a1fb-231">False</span></span>                                                                  |
| <span data-ttu-id="6a1fb-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6a1fb-232">In Global Catalog</span></span>      | <span data-ttu-id="6a1fb-233">False</span><span class="sxs-lookup"><span data-stu-id="6a1fb-233">False</span></span>                                                                  |
| <span data-ttu-id="6a1fb-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6a1fb-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a1fb-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6a1fb-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="6a1fb-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a1fb-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="6a1fb-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a1fb-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="6a1fb-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a1fb-238">Search-Flags</span></span>           | <span data-ttu-id="6a1fb-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a1fb-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="6a1fb-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a1fb-240">System-Flags</span></span>           | <span data-ttu-id="6a1fb-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a1fb-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="6a1fb-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6a1fb-242">Classes used in</span></span>        | [<span data-ttu-id="6a1fb-243">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="6a1fb-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6a1fb-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a1fb-244">Windows Server 2012</span></span>



| <span data-ttu-id="6a1fb-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6a1fb-245">Entry</span></span> | <span data-ttu-id="6a1fb-246">Wert</span><span class="sxs-lookup"><span data-stu-id="6a1fb-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="6a1fb-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6a1fb-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6a1fb-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a1fb-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="6a1fb-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a1fb-249">System-Only</span></span>            | <span data-ttu-id="6a1fb-250">False</span><span class="sxs-lookup"><span data-stu-id="6a1fb-250">False</span></span>                                                                  |
| <span data-ttu-id="6a1fb-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6a1fb-251">Is-Single-Valued</span></span>       | <span data-ttu-id="6a1fb-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="6a1fb-252">True</span></span>                                                                   |
| <span data-ttu-id="6a1fb-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6a1fb-253">Is Indexed</span></span>             | <span data-ttu-id="6a1fb-254">False</span><span class="sxs-lookup"><span data-stu-id="6a1fb-254">False</span></span>                                                                  |
| <span data-ttu-id="6a1fb-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6a1fb-255">In Global Catalog</span></span>      | <span data-ttu-id="6a1fb-256">False</span><span class="sxs-lookup"><span data-stu-id="6a1fb-256">False</span></span>                                                                  |
| <span data-ttu-id="6a1fb-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6a1fb-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a1fb-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6a1fb-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="6a1fb-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a1fb-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="6a1fb-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a1fb-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="6a1fb-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a1fb-261">Search-Flags</span></span>           | <span data-ttu-id="6a1fb-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a1fb-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="6a1fb-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a1fb-263">System-Flags</span></span>           | <span data-ttu-id="6a1fb-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a1fb-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="6a1fb-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6a1fb-265">Classes used in</span></span>        | [<span data-ttu-id="6a1fb-266">**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="6a1fb-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





