---
title: SD-Rechte effektives Attribut
description: Dieses konstruierte Attribut gibt einen einzelnen DWORD-Wert zurück, der bis zu drei Bits festgelegt werden kann Sicherheits \_ \_ Informationen Sicherheits \_ \_ informationsacl Sicherheits informationsacl \_ Sicherheits \_ Informationen wenn ein Bit festgelegt ist, dann verfügt der Benutzer über Schreibzugriff auf den entsprechenden Teil der Sicherheits Beschreibung. Owner bedeutet Besitzer und Gruppe.
ms.assetid: 66d1aefb-49be-42fc-b144-3fb95c59dd0f
ms.tgt_platform: multiple
keywords:
- AD-Schema für SD-Rights-effektive Attribute
- AD-Schema des sdrightseffective-Attributs
topic_type:
- apiref
api_name:
- SD-Rights-Effective
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac449cd18b3fb75a61f04fffc266c290b7763295
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859575"
---
# <a name="sd-rights-effective-attribute"></a><span data-ttu-id="53e71-106">SD-Rechte effektives Attribut</span><span class="sxs-lookup"><span data-stu-id="53e71-106">SD-Rights-Effective attribute</span></span>

<span data-ttu-id="53e71-107">Dieses konstruierte Attribut gibt einen einzelnen **DWORD** -Wert zurück, für den bis zu drei Bits festgelegt werden können:</span><span class="sxs-lookup"><span data-stu-id="53e71-107">This constructed attribute returns a single **DWORD** value that can have up to three bits set:</span></span>

-   <span data-ttu-id="53e71-108">\_Sicherheits \_ Informationen für den Besitzer</span><span class="sxs-lookup"><span data-stu-id="53e71-108">OWNER\_SECURITY\_INFORMATION</span></span>
-   <span data-ttu-id="53e71-109">DACL- \_ Sicherheits \_ Informationen</span><span class="sxs-lookup"><span data-stu-id="53e71-109">DACL\_SECURITY\_INFORMATION</span></span>
-   <span data-ttu-id="53e71-110">SACL- \_ Sicherheits \_ Informationen</span><span class="sxs-lookup"><span data-stu-id="53e71-110">SACL\_SECURITY\_INFORMATION</span></span>

<span data-ttu-id="53e71-111">Wenn ein Bit festgelegt ist, hat der Benutzer Schreibzugriff auf den entsprechenden Teil der Sicherheits Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="53e71-111">If a bit is set, then the user has write access to the corresponding part of the security descriptor.</span></span> <span data-ttu-id="53e71-112">Owner bedeutet Besitzer und Gruppe.</span><span class="sxs-lookup"><span data-stu-id="53e71-112">Owner means both owner and group.</span></span>



| <span data-ttu-id="53e71-113">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53e71-113">Entry</span></span> | <span data-ttu-id="53e71-114">Wert</span><span class="sxs-lookup"><span data-stu-id="53e71-114">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="53e71-115">CN</span><span class="sxs-lookup"><span data-stu-id="53e71-115">CN</span></span>                | <span data-ttu-id="53e71-116">SD-Rechte</span><span class="sxs-lookup"><span data-stu-id="53e71-116">SD-Rights-Effective</span></span>                  |
| <span data-ttu-id="53e71-117">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="53e71-117">Ldap-Display-Name</span></span> | <span data-ttu-id="53e71-118">sdrightabffective</span><span class="sxs-lookup"><span data-stu-id="53e71-118">sDRightsEffective</span></span>                    |
| <span data-ttu-id="53e71-119">Size</span><span class="sxs-lookup"><span data-stu-id="53e71-119">Size</span></span>              | \-                                   |
| <span data-ttu-id="53e71-120">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="53e71-120">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="53e71-121">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="53e71-121">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="53e71-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="53e71-122">Attribute-Id</span></span>      | <span data-ttu-id="53e71-123">1.2.840.113556.1.4.1304</span><span class="sxs-lookup"><span data-stu-id="53e71-123">1.2.840.113556.1.4.1304</span></span>              |
| <span data-ttu-id="53e71-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="53e71-124">System-Id-Guid</span></span>    | <span data-ttu-id="53e71-125">c3dbafa6-33df-11d2-98b2-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="53e71-125">c3dbafa6-33df-11d2-98b2-0000f87a57d4</span></span> |
| <span data-ttu-id="53e71-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="53e71-126">Syntax</span></span>            | [<span data-ttu-id="53e71-127">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="53e71-127">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="53e71-128">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="53e71-128">Implementations</span></span>

-   [<span data-ttu-id="53e71-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="53e71-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="53e71-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="53e71-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="53e71-131">**Adam**</span><span class="sxs-lookup"><span data-stu-id="53e71-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="53e71-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="53e71-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="53e71-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="53e71-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="53e71-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="53e71-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="53e71-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="53e71-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="53e71-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="53e71-136">Windows 2000 Server</span></span>



| <span data-ttu-id="53e71-137">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53e71-137">Entry</span></span> | <span data-ttu-id="53e71-138">Wert</span><span class="sxs-lookup"><span data-stu-id="53e71-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="53e71-139">Link-ID</span><span class="sxs-lookup"><span data-stu-id="53e71-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="53e71-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53e71-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="53e71-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="53e71-141">System-Only</span></span>            | <span data-ttu-id="53e71-142">False</span><span class="sxs-lookup"><span data-stu-id="53e71-142">False</span></span>                           |
| <span data-ttu-id="53e71-143">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="53e71-143">Is-Single-Valued</span></span>       | <span data-ttu-id="53e71-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="53e71-144">True</span></span>                            |
| <span data-ttu-id="53e71-145">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="53e71-145">Is Indexed</span></span>             | <span data-ttu-id="53e71-146">False</span><span class="sxs-lookup"><span data-stu-id="53e71-146">False</span></span>                           |
| <span data-ttu-id="53e71-147">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="53e71-147">In Global Catalog</span></span>      | <span data-ttu-id="53e71-148">False</span><span class="sxs-lookup"><span data-stu-id="53e71-148">False</span></span>                           |
| <span data-ttu-id="53e71-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="53e71-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="53e71-150">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="53e71-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="53e71-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53e71-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="53e71-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53e71-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="53e71-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53e71-153">Search-Flags</span></span>           | <span data-ttu-id="53e71-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53e71-154">0x00000000</span></span>                      |
| <span data-ttu-id="53e71-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53e71-155">System-Flags</span></span>           | <span data-ttu-id="53e71-156">0x08000014</span><span class="sxs-lookup"><span data-stu-id="53e71-156">0x08000014</span></span>                      |
| <span data-ttu-id="53e71-157">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="53e71-157">Classes used in</span></span>        | [<span data-ttu-id="53e71-158">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="53e71-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="53e71-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="53e71-159">Windows Server 2003</span></span>



| <span data-ttu-id="53e71-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53e71-160">Entry</span></span> | <span data-ttu-id="53e71-161">Wert</span><span class="sxs-lookup"><span data-stu-id="53e71-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="53e71-162">Link-ID</span><span class="sxs-lookup"><span data-stu-id="53e71-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="53e71-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53e71-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="53e71-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="53e71-164">System-Only</span></span>            | <span data-ttu-id="53e71-165">False</span><span class="sxs-lookup"><span data-stu-id="53e71-165">False</span></span>                           |
| <span data-ttu-id="53e71-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="53e71-166">Is-Single-Valued</span></span>       | <span data-ttu-id="53e71-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="53e71-167">True</span></span>                            |
| <span data-ttu-id="53e71-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="53e71-168">Is Indexed</span></span>             | <span data-ttu-id="53e71-169">False</span><span class="sxs-lookup"><span data-stu-id="53e71-169">False</span></span>                           |
| <span data-ttu-id="53e71-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="53e71-170">In Global Catalog</span></span>      | <span data-ttu-id="53e71-171">False</span><span class="sxs-lookup"><span data-stu-id="53e71-171">False</span></span>                           |
| <span data-ttu-id="53e71-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="53e71-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="53e71-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="53e71-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="53e71-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53e71-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="53e71-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53e71-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="53e71-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53e71-176">Search-Flags</span></span>           | <span data-ttu-id="53e71-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53e71-177">0x00000000</span></span>                      |
| <span data-ttu-id="53e71-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53e71-178">System-Flags</span></span>           | <span data-ttu-id="53e71-179">0x08000014</span><span class="sxs-lookup"><span data-stu-id="53e71-179">0x08000014</span></span>                      |
| <span data-ttu-id="53e71-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="53e71-180">Classes used in</span></span>        | [<span data-ttu-id="53e71-181">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="53e71-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="53e71-182">Adam</span><span class="sxs-lookup"><span data-stu-id="53e71-182">ADAM</span></span>



| <span data-ttu-id="53e71-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53e71-183">Entry</span></span> | <span data-ttu-id="53e71-184">Wert</span><span class="sxs-lookup"><span data-stu-id="53e71-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="53e71-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="53e71-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="53e71-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53e71-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="53e71-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="53e71-187">System-Only</span></span>            | <span data-ttu-id="53e71-188">False</span><span class="sxs-lookup"><span data-stu-id="53e71-188">False</span></span>                           |
| <span data-ttu-id="53e71-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="53e71-189">Is-Single-Valued</span></span>       | <span data-ttu-id="53e71-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="53e71-190">True</span></span>                            |
| <span data-ttu-id="53e71-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="53e71-191">Is Indexed</span></span>             | <span data-ttu-id="53e71-192">False</span><span class="sxs-lookup"><span data-stu-id="53e71-192">False</span></span>                           |
| <span data-ttu-id="53e71-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="53e71-193">In Global Catalog</span></span>      | <span data-ttu-id="53e71-194">False</span><span class="sxs-lookup"><span data-stu-id="53e71-194">False</span></span>                           |
| <span data-ttu-id="53e71-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="53e71-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="53e71-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="53e71-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="53e71-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53e71-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="53e71-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53e71-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="53e71-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53e71-199">Search-Flags</span></span>           | <span data-ttu-id="53e71-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53e71-200">0x00000000</span></span>                      |
| <span data-ttu-id="53e71-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53e71-201">System-Flags</span></span>           | <span data-ttu-id="53e71-202">0x08000014</span><span class="sxs-lookup"><span data-stu-id="53e71-202">0x08000014</span></span>                      |
| <span data-ttu-id="53e71-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="53e71-203">Classes used in</span></span>        | [<span data-ttu-id="53e71-204">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="53e71-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="53e71-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="53e71-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="53e71-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53e71-206">Entry</span></span> | <span data-ttu-id="53e71-207">Wert</span><span class="sxs-lookup"><span data-stu-id="53e71-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="53e71-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="53e71-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="53e71-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53e71-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="53e71-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="53e71-210">System-Only</span></span>            | <span data-ttu-id="53e71-211">False</span><span class="sxs-lookup"><span data-stu-id="53e71-211">False</span></span>                           |
| <span data-ttu-id="53e71-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="53e71-212">Is-Single-Valued</span></span>       | <span data-ttu-id="53e71-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="53e71-213">True</span></span>                            |
| <span data-ttu-id="53e71-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="53e71-214">Is Indexed</span></span>             | <span data-ttu-id="53e71-215">False</span><span class="sxs-lookup"><span data-stu-id="53e71-215">False</span></span>                           |
| <span data-ttu-id="53e71-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="53e71-216">In Global Catalog</span></span>      | <span data-ttu-id="53e71-217">False</span><span class="sxs-lookup"><span data-stu-id="53e71-217">False</span></span>                           |
| <span data-ttu-id="53e71-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="53e71-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="53e71-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="53e71-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="53e71-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53e71-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="53e71-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53e71-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="53e71-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53e71-222">Search-Flags</span></span>           | <span data-ttu-id="53e71-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53e71-223">0x00000000</span></span>                      |
| <span data-ttu-id="53e71-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53e71-224">System-Flags</span></span>           | <span data-ttu-id="53e71-225">0x08000014</span><span class="sxs-lookup"><span data-stu-id="53e71-225">0x08000014</span></span>                      |
| <span data-ttu-id="53e71-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="53e71-226">Classes used in</span></span>        | [<span data-ttu-id="53e71-227">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="53e71-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="53e71-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53e71-228">Windows Server 2008</span></span>



| <span data-ttu-id="53e71-229">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53e71-229">Entry</span></span> | <span data-ttu-id="53e71-230">Wert</span><span class="sxs-lookup"><span data-stu-id="53e71-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="53e71-231">Link-ID</span><span class="sxs-lookup"><span data-stu-id="53e71-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="53e71-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53e71-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="53e71-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="53e71-233">System-Only</span></span>            | <span data-ttu-id="53e71-234">False</span><span class="sxs-lookup"><span data-stu-id="53e71-234">False</span></span>                           |
| <span data-ttu-id="53e71-235">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="53e71-235">Is-Single-Valued</span></span>       | <span data-ttu-id="53e71-236">Richtig</span><span class="sxs-lookup"><span data-stu-id="53e71-236">True</span></span>                            |
| <span data-ttu-id="53e71-237">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="53e71-237">Is Indexed</span></span>             | <span data-ttu-id="53e71-238">False</span><span class="sxs-lookup"><span data-stu-id="53e71-238">False</span></span>                           |
| <span data-ttu-id="53e71-239">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="53e71-239">In Global Catalog</span></span>      | <span data-ttu-id="53e71-240">False</span><span class="sxs-lookup"><span data-stu-id="53e71-240">False</span></span>                           |
| <span data-ttu-id="53e71-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="53e71-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="53e71-242">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="53e71-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="53e71-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53e71-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="53e71-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53e71-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="53e71-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53e71-245">Search-Flags</span></span>           | <span data-ttu-id="53e71-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53e71-246">0x00000000</span></span>                      |
| <span data-ttu-id="53e71-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53e71-247">System-Flags</span></span>           | <span data-ttu-id="53e71-248">0x08000014</span><span class="sxs-lookup"><span data-stu-id="53e71-248">0x08000014</span></span>                      |
| <span data-ttu-id="53e71-249">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="53e71-249">Classes used in</span></span>        | [<span data-ttu-id="53e71-250">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="53e71-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="53e71-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="53e71-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="53e71-252">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53e71-252">Entry</span></span> | <span data-ttu-id="53e71-253">Wert</span><span class="sxs-lookup"><span data-stu-id="53e71-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="53e71-254">Link-ID</span><span class="sxs-lookup"><span data-stu-id="53e71-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="53e71-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53e71-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="53e71-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="53e71-256">System-Only</span></span>            | <span data-ttu-id="53e71-257">False</span><span class="sxs-lookup"><span data-stu-id="53e71-257">False</span></span>                           |
| <span data-ttu-id="53e71-258">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="53e71-258">Is-Single-Valued</span></span>       | <span data-ttu-id="53e71-259">Richtig</span><span class="sxs-lookup"><span data-stu-id="53e71-259">True</span></span>                            |
| <span data-ttu-id="53e71-260">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="53e71-260">Is Indexed</span></span>             | <span data-ttu-id="53e71-261">False</span><span class="sxs-lookup"><span data-stu-id="53e71-261">False</span></span>                           |
| <span data-ttu-id="53e71-262">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="53e71-262">In Global Catalog</span></span>      | <span data-ttu-id="53e71-263">False</span><span class="sxs-lookup"><span data-stu-id="53e71-263">False</span></span>                           |
| <span data-ttu-id="53e71-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="53e71-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="53e71-265">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="53e71-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="53e71-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53e71-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="53e71-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53e71-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="53e71-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53e71-268">Search-Flags</span></span>           | <span data-ttu-id="53e71-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53e71-269">0x00000000</span></span>                      |
| <span data-ttu-id="53e71-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53e71-270">System-Flags</span></span>           | <span data-ttu-id="53e71-271">0x08000014</span><span class="sxs-lookup"><span data-stu-id="53e71-271">0x08000014</span></span>                      |
| <span data-ttu-id="53e71-272">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="53e71-272">Classes used in</span></span>        | [<span data-ttu-id="53e71-273">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="53e71-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="53e71-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="53e71-274">Windows Server 2012</span></span>



| <span data-ttu-id="53e71-275">Eingabe</span><span class="sxs-lookup"><span data-stu-id="53e71-275">Entry</span></span> | <span data-ttu-id="53e71-276">Wert</span><span class="sxs-lookup"><span data-stu-id="53e71-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="53e71-277">Link-ID</span><span class="sxs-lookup"><span data-stu-id="53e71-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="53e71-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53e71-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="53e71-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="53e71-279">System-Only</span></span>            | <span data-ttu-id="53e71-280">False</span><span class="sxs-lookup"><span data-stu-id="53e71-280">False</span></span>                           |
| <span data-ttu-id="53e71-281">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="53e71-281">Is-Single-Valued</span></span>       | <span data-ttu-id="53e71-282">Richtig</span><span class="sxs-lookup"><span data-stu-id="53e71-282">True</span></span>                            |
| <span data-ttu-id="53e71-283">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="53e71-283">Is Indexed</span></span>             | <span data-ttu-id="53e71-284">False</span><span class="sxs-lookup"><span data-stu-id="53e71-284">False</span></span>                           |
| <span data-ttu-id="53e71-285">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="53e71-285">In Global Catalog</span></span>      | <span data-ttu-id="53e71-286">False</span><span class="sxs-lookup"><span data-stu-id="53e71-286">False</span></span>                           |
| <span data-ttu-id="53e71-287">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="53e71-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="53e71-288">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="53e71-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="53e71-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53e71-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="53e71-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53e71-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="53e71-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53e71-291">Search-Flags</span></span>           | <span data-ttu-id="53e71-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53e71-292">0x00000000</span></span>                      |
| <span data-ttu-id="53e71-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53e71-293">System-Flags</span></span>           | <span data-ttu-id="53e71-294">0x08000014</span><span class="sxs-lookup"><span data-stu-id="53e71-294">0x08000014</span></span>                      |
| <span data-ttu-id="53e71-295">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="53e71-295">Classes used in</span></span>        | [<span data-ttu-id="53e71-296">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="53e71-296">**Top**</span></span>](c-top.md)<br/> |



 

 





