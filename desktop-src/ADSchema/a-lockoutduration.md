---
title: Lockout-Duration-Attribut
description: Die Zeitspanne, für die ein Konto aufgrund der Überschreitung des Lockout-Threshold gesperrt ist.
ms.assetid: 6a26ef80-86ed-433f-9032-cdd1aaf00388
ms.tgt_platform: multiple
keywords:
- AD-Schema für Lockout-Duration-Attribut
- AD-Schema für LockoutDuration-Attribut
topic_type:
- apiref
api_name:
- Lockout-Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526fedef47bea20148a591259dbc7ec1702b5a15
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106338818"
---
# <a name="lockout-duration-attribute"></a><span data-ttu-id="5a4e2-105">Lockout-Duration-Attribut</span><span class="sxs-lookup"><span data-stu-id="5a4e2-105">Lockout-Duration attribute</span></span>

<span data-ttu-id="5a4e2-106">Die Zeitspanne, für die ein Konto gesperrt ist, weil der [**Sperr Schwellenwert**](a-lockoutthreshold.md) überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="5a4e2-106">The amount of time that an account is locked due to the [**Lockout-Threshold**](a-lockoutthreshold.md) being exceeded.</span></span> <span data-ttu-id="5a4e2-107">Dieser Wert wird als große ganze Zahl gespeichert, die den negativen Wert der Anzahl der 100-Nanosekunden-Intervalle ab dem Zeitpunkt darstellt, zu dem der Sperrungs [**Schwellen**](a-lockoutthreshold.md) Wert überschritten wird, der vergehen muss, bevor das Konto entsperrt wird.</span><span class="sxs-lookup"><span data-stu-id="5a4e2-107">This value is stored as a large integer that represents the negative of the number of 100-nanosecond intervals from the time the [**Lockout-Threshold**](a-lockoutthreshold.md) is exceeded that must elapse before the account is unlocked.</span></span>



| <span data-ttu-id="5a4e2-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a4e2-108">Entry</span></span> | <span data-ttu-id="5a4e2-109">Wert</span><span class="sxs-lookup"><span data-stu-id="5a4e2-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5a4e2-110">CN</span><span class="sxs-lookup"><span data-stu-id="5a4e2-110">CN</span></span>                | <span data-ttu-id="5a4e2-111">Lockout-Duration</span><span class="sxs-lookup"><span data-stu-id="5a4e2-111">Lockout-Duration</span></span>                     |
| <span data-ttu-id="5a4e2-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5a4e2-112">Ldap-Display-Name</span></span> | <span data-ttu-id="5a4e2-113">LockoutDuration</span><span class="sxs-lookup"><span data-stu-id="5a4e2-113">lockoutDuration</span></span>                      |
| <span data-ttu-id="5a4e2-114">Size</span><span class="sxs-lookup"><span data-stu-id="5a4e2-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="5a4e2-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5a4e2-115">Update Privilege</span></span>  | <span data-ttu-id="5a4e2-116">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="5a4e2-116">Domain administrator</span></span>                 |
| <span data-ttu-id="5a4e2-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="5a4e2-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="5a4e2-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5a4e2-118">Attribute-Id</span></span>      | <span data-ttu-id="5a4e2-119">1.2.840.113556.1.4.60</span><span class="sxs-lookup"><span data-stu-id="5a4e2-119">1.2.840.113556.1.4.60</span></span>                |
| <span data-ttu-id="5a4e2-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5a4e2-120">System-Id-Guid</span></span>    | <span data-ttu-id="5a4e2-121">bf9679a5-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="5a4e2-121">bf9679a5-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="5a4e2-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a4e2-122">Syntax</span></span>            | [<span data-ttu-id="5a4e2-123">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="5a4e2-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="5a4e2-124">Implementations</span></span>

-   [<span data-ttu-id="5a4e2-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5a4e2-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5a4e2-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5a4e2-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5a4e2-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5a4e2-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5a4e2-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5a4e2-131">Windows 2000 Server</span></span>



| <span data-ttu-id="5a4e2-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a4e2-132">Entry</span></span> | <span data-ttu-id="5a4e2-133">Wert</span><span class="sxs-lookup"><span data-stu-id="5a4e2-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a4e2-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5a4e2-134">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a4e2-135">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a4e2-136">System-Only</span></span>            | <span data-ttu-id="5a4e2-137">False</span><span class="sxs-lookup"><span data-stu-id="5a4e2-137">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="5a4e2-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5a4e2-138">Is-Single-Valued</span></span>       | <span data-ttu-id="5a4e2-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a4e2-139">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="5a4e2-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5a4e2-140">Is Indexed</span></span>             | <span data-ttu-id="5a4e2-141">False</span><span class="sxs-lookup"><span data-stu-id="5a4e2-141">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="5a4e2-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5a4e2-142">In Global Catalog</span></span>      | <span data-ttu-id="5a4e2-143">False</span><span class="sxs-lookup"><span data-stu-id="5a4e2-143">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="5a4e2-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5a4e2-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a4e2-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5a4e2-145">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="5a4e2-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a4e2-146">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a4e2-147">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a4e2-148">Search-Flags</span></span>           | <span data-ttu-id="5a4e2-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a4e2-149">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="5a4e2-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a4e2-150">System-Flags</span></span>           | <span data-ttu-id="5a4e2-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a4e2-151">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="5a4e2-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5a4e2-152">Classes used in</span></span>        | [<span data-ttu-id="5a4e2-153">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="5a4e2-154">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-154">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="5a4e2-155">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-155">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5a4e2-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5a4e2-156">Windows Server 2003</span></span>



| <span data-ttu-id="5a4e2-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a4e2-157">Entry</span></span> | <span data-ttu-id="5a4e2-158">Wert</span><span class="sxs-lookup"><span data-stu-id="5a4e2-158">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a4e2-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5a4e2-159">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a4e2-160">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a4e2-161">System-Only</span></span>            | <span data-ttu-id="5a4e2-162">False</span><span class="sxs-lookup"><span data-stu-id="5a4e2-162">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="5a4e2-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5a4e2-163">Is-Single-Valued</span></span>       | <span data-ttu-id="5a4e2-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a4e2-164">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="5a4e2-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5a4e2-165">Is Indexed</span></span>             | <span data-ttu-id="5a4e2-166">False</span><span class="sxs-lookup"><span data-stu-id="5a4e2-166">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="5a4e2-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5a4e2-167">In Global Catalog</span></span>      | <span data-ttu-id="5a4e2-168">False</span><span class="sxs-lookup"><span data-stu-id="5a4e2-168">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="5a4e2-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5a4e2-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a4e2-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5a4e2-170">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="5a4e2-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a4e2-171">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a4e2-172">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a4e2-173">Search-Flags</span></span>           | <span data-ttu-id="5a4e2-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a4e2-174">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="5a4e2-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a4e2-175">System-Flags</span></span>           | <span data-ttu-id="5a4e2-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a4e2-176">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="5a4e2-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5a4e2-177">Classes used in</span></span>        | [<span data-ttu-id="5a4e2-178">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-178">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="5a4e2-179">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-179">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="5a4e2-180">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-180">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5a4e2-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5a4e2-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5a4e2-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a4e2-182">Entry</span></span> | <span data-ttu-id="5a4e2-183">Wert</span><span class="sxs-lookup"><span data-stu-id="5a4e2-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a4e2-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5a4e2-184">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a4e2-185">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a4e2-186">System-Only</span></span>            | <span data-ttu-id="5a4e2-187">False</span><span class="sxs-lookup"><span data-stu-id="5a4e2-187">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="5a4e2-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5a4e2-188">Is-Single-Valued</span></span>       | <span data-ttu-id="5a4e2-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a4e2-189">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="5a4e2-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5a4e2-190">Is Indexed</span></span>             | <span data-ttu-id="5a4e2-191">False</span><span class="sxs-lookup"><span data-stu-id="5a4e2-191">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="5a4e2-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5a4e2-192">In Global Catalog</span></span>      | <span data-ttu-id="5a4e2-193">False</span><span class="sxs-lookup"><span data-stu-id="5a4e2-193">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="5a4e2-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5a4e2-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a4e2-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5a4e2-195">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="5a4e2-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a4e2-196">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a4e2-197">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a4e2-198">Search-Flags</span></span>           | <span data-ttu-id="5a4e2-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a4e2-199">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="5a4e2-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a4e2-200">System-Flags</span></span>           | <span data-ttu-id="5a4e2-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a4e2-201">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="5a4e2-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5a4e2-202">Classes used in</span></span>        | [<span data-ttu-id="5a4e2-203">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-203">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="5a4e2-204">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-204">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="5a4e2-205">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-205">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5a4e2-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a4e2-206">Windows Server 2008</span></span>



| <span data-ttu-id="5a4e2-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a4e2-207">Entry</span></span> | <span data-ttu-id="5a4e2-208">Wert</span><span class="sxs-lookup"><span data-stu-id="5a4e2-208">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a4e2-209">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5a4e2-209">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a4e2-210">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a4e2-211">System-Only</span></span>            | <span data-ttu-id="5a4e2-212">False</span><span class="sxs-lookup"><span data-stu-id="5a4e2-212">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="5a4e2-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5a4e2-213">Is-Single-Valued</span></span>       | <span data-ttu-id="5a4e2-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a4e2-214">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="5a4e2-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5a4e2-215">Is Indexed</span></span>             | <span data-ttu-id="5a4e2-216">False</span><span class="sxs-lookup"><span data-stu-id="5a4e2-216">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="5a4e2-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5a4e2-217">In Global Catalog</span></span>      | <span data-ttu-id="5a4e2-218">False</span><span class="sxs-lookup"><span data-stu-id="5a4e2-218">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="5a4e2-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5a4e2-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a4e2-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5a4e2-220">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="5a4e2-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a4e2-221">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a4e2-222">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a4e2-223">Search-Flags</span></span>           | <span data-ttu-id="5a4e2-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a4e2-224">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="5a4e2-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a4e2-225">System-Flags</span></span>           | <span data-ttu-id="5a4e2-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a4e2-226">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="5a4e2-227">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5a4e2-227">Classes used in</span></span>        | [<span data-ttu-id="5a4e2-228">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-228">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="5a4e2-229">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-229">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="5a4e2-230">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-230">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5a4e2-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5a4e2-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5a4e2-232">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a4e2-232">Entry</span></span> | <span data-ttu-id="5a4e2-233">Wert</span><span class="sxs-lookup"><span data-stu-id="5a4e2-233">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a4e2-234">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5a4e2-234">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a4e2-235">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a4e2-236">System-Only</span></span>            | <span data-ttu-id="5a4e2-237">False</span><span class="sxs-lookup"><span data-stu-id="5a4e2-237">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="5a4e2-238">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5a4e2-238">Is-Single-Valued</span></span>       | <span data-ttu-id="5a4e2-239">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a4e2-239">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="5a4e2-240">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5a4e2-240">Is Indexed</span></span>             | <span data-ttu-id="5a4e2-241">False</span><span class="sxs-lookup"><span data-stu-id="5a4e2-241">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="5a4e2-242">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5a4e2-242">In Global Catalog</span></span>      | <span data-ttu-id="5a4e2-243">False</span><span class="sxs-lookup"><span data-stu-id="5a4e2-243">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="5a4e2-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5a4e2-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a4e2-245">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5a4e2-245">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="5a4e2-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a4e2-246">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a4e2-247">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a4e2-248">Search-Flags</span></span>           | <span data-ttu-id="5a4e2-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a4e2-249">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="5a4e2-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a4e2-250">System-Flags</span></span>           | <span data-ttu-id="5a4e2-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a4e2-251">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="5a4e2-252">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5a4e2-252">Classes used in</span></span>        | [<span data-ttu-id="5a4e2-253">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-253">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="5a4e2-254">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-254">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="5a4e2-255">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-255">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5a4e2-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5a4e2-256">Windows Server 2012</span></span>



| <span data-ttu-id="5a4e2-257">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a4e2-257">Entry</span></span> | <span data-ttu-id="5a4e2-258">Wert</span><span class="sxs-lookup"><span data-stu-id="5a4e2-258">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a4e2-259">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5a4e2-259">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a4e2-260">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a4e2-261">System-Only</span></span>            | <span data-ttu-id="5a4e2-262">False</span><span class="sxs-lookup"><span data-stu-id="5a4e2-262">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="5a4e2-263">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5a4e2-263">Is-Single-Valued</span></span>       | <span data-ttu-id="5a4e2-264">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a4e2-264">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="5a4e2-265">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5a4e2-265">Is Indexed</span></span>             | <span data-ttu-id="5a4e2-266">False</span><span class="sxs-lookup"><span data-stu-id="5a4e2-266">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="5a4e2-267">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5a4e2-267">In Global Catalog</span></span>      | <span data-ttu-id="5a4e2-268">False</span><span class="sxs-lookup"><span data-stu-id="5a4e2-268">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="5a4e2-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5a4e2-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a4e2-270">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5a4e2-270">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="5a4e2-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a4e2-271">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a4e2-272">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="5a4e2-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a4e2-273">Search-Flags</span></span>           | <span data-ttu-id="5a4e2-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a4e2-274">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="5a4e2-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a4e2-275">System-Flags</span></span>           | <span data-ttu-id="5a4e2-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a4e2-276">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="5a4e2-277">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5a4e2-277">Classes used in</span></span>        | [<span data-ttu-id="5a4e2-278">**Domänen Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-278">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="5a4e2-279">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-279">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="5a4e2-280">**SAM-Domain-Base**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-280">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="5a4e2-281">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a4e2-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a4e2-282">**Sperrungs Schwellenwert**</span><span class="sxs-lookup"><span data-stu-id="5a4e2-282">**Lockout-Threshold**</span></span>](a-lockoutthreshold.md)
</dt> </dl>

 

 





