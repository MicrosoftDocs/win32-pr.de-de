---
title: MS-IIS-FTP-Root-Attribut
description: Dieses Attribut bestimmt die Dateiserver Freigabe. Sie wird in Verbindung mit MS-IIS-FTP-dir verwendet, um das Start Verzeichnis des FTP-Benutzers zu bestimmen.
ms.assetid: b86dcafb-0b0d-4225-924c-690f739092a8
ms.tgt_platform: multiple
keywords:
- AD-Schema für MS-IIS-FTP-Root-Attribut
- AD-Schema des msIIS-FTPRoot-Attributs
topic_type:
- apiref
api_name:
- ms-IIS-FTP-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e7c55980b8b08865889f7567fa6bdb4dcf7bde1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480330"
---
# <a name="ms-iis-ftp-root-attribute"></a><span data-ttu-id="e7772-106">MS-IIS-FTP-Root-Attribut</span><span class="sxs-lookup"><span data-stu-id="e7772-106">ms-IIS-FTP-Root attribute</span></span>

<span data-ttu-id="e7772-107">Dieses Attribut bestimmt die Dateiserver Freigabe.</span><span class="sxs-lookup"><span data-stu-id="e7772-107">This attribute determines the file server share.</span></span> <span data-ttu-id="e7772-108">Sie wird in Verbindung mit MS-IIS-FTP-dir verwendet, um das Start Verzeichnis des FTP-Benutzers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="e7772-108">It is used in conjunction with ms-IIS-FTP-Dir to determine the FTP user home directory.</span></span>



| <span data-ttu-id="e7772-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e7772-109">Entry</span></span> | <span data-ttu-id="e7772-110">Wert</span><span class="sxs-lookup"><span data-stu-id="e7772-110">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7772-111">CN</span><span class="sxs-lookup"><span data-stu-id="e7772-111">CN</span></span>                | <span data-ttu-id="e7772-112">MS-IIS-FTP-Root</span><span class="sxs-lookup"><span data-stu-id="e7772-112">ms-IIS-FTP-Root</span></span>                                                                                                                 |
| <span data-ttu-id="e7772-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e7772-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e7772-114">msIIS-FTPRoot</span><span class="sxs-lookup"><span data-stu-id="e7772-114">msIIS-FTPRoot</span></span>                                                                                                                   |
| <span data-ttu-id="e7772-115">Size</span><span class="sxs-lookup"><span data-stu-id="e7772-115">Size</span></span>              | <span data-ttu-id="e7772-116">30-50 Zeichen (15-25 Unicode-Zeichen für jede Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e7772-116">30-50 characters (15-25 Unicode characters for each property)</span></span>                                                                   |
| <span data-ttu-id="e7772-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e7772-117">Update Privilege</span></span>  | <span data-ttu-id="e7772-118">Domänen Administrator & lokales System</span><span class="sxs-lookup"><span data-stu-id="e7772-118">Domain administrator & local system</span></span>                                                                                             |
| <span data-ttu-id="e7772-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="e7772-119">Update Frequency</span></span>  | <span data-ttu-id="e7772-120">Diese Eigenschaft wird festgelegt, wenn der Administrator die Website erstellt und die FTP-Isolation festlegt.</span><span class="sxs-lookup"><span data-stu-id="e7772-120">This property is set when the administrator creates the website and sets FTP isolation.</span></span> <span data-ttu-id="e7772-121">Es wird nur selten geändert.</span><span class="sxs-lookup"><span data-stu-id="e7772-121">It's rarely going to change after that.</span></span> |
| <span data-ttu-id="e7772-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e7772-122">Attribute-Id</span></span>      | <span data-ttu-id="e7772-123">1.2.840.113556.1.4.1785</span><span class="sxs-lookup"><span data-stu-id="e7772-123">1.2.840.113556.1.4.1785</span></span>                                                                                                         |
| <span data-ttu-id="e7772-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e7772-124">System-Id-Guid</span></span>    | <span data-ttu-id="e7772-125">2a7827a4-1483-49a5-9d84-52e3812156b4</span><span class="sxs-lookup"><span data-stu-id="e7772-125">2a7827a4-1483-49a5-9d84-52e3812156b4</span></span>                                                                                            |
| <span data-ttu-id="e7772-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7772-126">Syntax</span></span>            | [<span data-ttu-id="e7772-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e7772-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                     |



## <a name="implementations"></a><span data-ttu-id="e7772-128">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="e7772-128">Implementations</span></span>

-   [<span data-ttu-id="e7772-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e7772-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e7772-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e7772-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e7772-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e7772-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e7772-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e7772-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e7772-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e7772-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e7772-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e7772-134">Windows Server 2003</span></span>



| <span data-ttu-id="e7772-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e7772-135">Entry</span></span> | <span data-ttu-id="e7772-136">Wert</span><span class="sxs-lookup"><span data-stu-id="e7772-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e7772-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e7772-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e7772-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7772-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e7772-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7772-139">System-Only</span></span>            | <span data-ttu-id="e7772-140">False</span><span class="sxs-lookup"><span data-stu-id="e7772-140">False</span></span>                             |
| <span data-ttu-id="e7772-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e7772-141">Is-Single-Valued</span></span>       | <span data-ttu-id="e7772-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="e7772-142">True</span></span>                              |
| <span data-ttu-id="e7772-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e7772-143">Is Indexed</span></span>             | <span data-ttu-id="e7772-144">False</span><span class="sxs-lookup"><span data-stu-id="e7772-144">False</span></span>                             |
| <span data-ttu-id="e7772-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e7772-145">In Global Catalog</span></span>      | <span data-ttu-id="e7772-146">False</span><span class="sxs-lookup"><span data-stu-id="e7772-146">False</span></span>                             |
| <span data-ttu-id="e7772-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e7772-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7772-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e7772-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e7772-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7772-149">Range-Lower</span></span>            | <span data-ttu-id="e7772-150">1</span><span class="sxs-lookup"><span data-stu-id="e7772-150">1</span></span>                                 |
| <span data-ttu-id="e7772-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7772-151">Range-Upper</span></span>            | <span data-ttu-id="e7772-152">256</span><span class="sxs-lookup"><span data-stu-id="e7772-152">256</span></span>                               |
| <span data-ttu-id="e7772-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7772-153">Search-Flags</span></span>           | <span data-ttu-id="e7772-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7772-154">0x00000000</span></span>                        |
| <span data-ttu-id="e7772-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7772-155">System-Flags</span></span>           | <span data-ttu-id="e7772-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7772-156">0x00000010</span></span>                        |
| <span data-ttu-id="e7772-157">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e7772-157">Classes used in</span></span>        | [<span data-ttu-id="e7772-158">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="e7772-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e7772-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e7772-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e7772-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e7772-160">Entry</span></span> | <span data-ttu-id="e7772-161">Wert</span><span class="sxs-lookup"><span data-stu-id="e7772-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e7772-162">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e7772-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e7772-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7772-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e7772-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7772-164">System-Only</span></span>            | <span data-ttu-id="e7772-165">False</span><span class="sxs-lookup"><span data-stu-id="e7772-165">False</span></span>                             |
| <span data-ttu-id="e7772-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e7772-166">Is-Single-Valued</span></span>       | <span data-ttu-id="e7772-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="e7772-167">True</span></span>                              |
| <span data-ttu-id="e7772-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e7772-168">Is Indexed</span></span>             | <span data-ttu-id="e7772-169">False</span><span class="sxs-lookup"><span data-stu-id="e7772-169">False</span></span>                             |
| <span data-ttu-id="e7772-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e7772-170">In Global Catalog</span></span>      | <span data-ttu-id="e7772-171">False</span><span class="sxs-lookup"><span data-stu-id="e7772-171">False</span></span>                             |
| <span data-ttu-id="e7772-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e7772-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7772-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e7772-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e7772-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7772-174">Range-Lower</span></span>            | <span data-ttu-id="e7772-175">1</span><span class="sxs-lookup"><span data-stu-id="e7772-175">1</span></span>                                 |
| <span data-ttu-id="e7772-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7772-176">Range-Upper</span></span>            | <span data-ttu-id="e7772-177">256</span><span class="sxs-lookup"><span data-stu-id="e7772-177">256</span></span>                               |
| <span data-ttu-id="e7772-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7772-178">Search-Flags</span></span>           | <span data-ttu-id="e7772-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7772-179">0x00000000</span></span>                        |
| <span data-ttu-id="e7772-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7772-180">System-Flags</span></span>           | <span data-ttu-id="e7772-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7772-181">0x00000010</span></span>                        |
| <span data-ttu-id="e7772-182">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e7772-182">Classes used in</span></span>        | [<span data-ttu-id="e7772-183">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="e7772-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e7772-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7772-184">Windows Server 2008</span></span>



| <span data-ttu-id="e7772-185">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e7772-185">Entry</span></span> | <span data-ttu-id="e7772-186">Wert</span><span class="sxs-lookup"><span data-stu-id="e7772-186">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e7772-187">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e7772-187">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e7772-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7772-188">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e7772-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7772-189">System-Only</span></span>            | <span data-ttu-id="e7772-190">False</span><span class="sxs-lookup"><span data-stu-id="e7772-190">False</span></span>                             |
| <span data-ttu-id="e7772-191">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e7772-191">Is-Single-Valued</span></span>       | <span data-ttu-id="e7772-192">Richtig</span><span class="sxs-lookup"><span data-stu-id="e7772-192">True</span></span>                              |
| <span data-ttu-id="e7772-193">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e7772-193">Is Indexed</span></span>             | <span data-ttu-id="e7772-194">False</span><span class="sxs-lookup"><span data-stu-id="e7772-194">False</span></span>                             |
| <span data-ttu-id="e7772-195">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e7772-195">In Global Catalog</span></span>      | <span data-ttu-id="e7772-196">False</span><span class="sxs-lookup"><span data-stu-id="e7772-196">False</span></span>                             |
| <span data-ttu-id="e7772-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e7772-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7772-198">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e7772-198">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e7772-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7772-199">Range-Lower</span></span>            | <span data-ttu-id="e7772-200">1</span><span class="sxs-lookup"><span data-stu-id="e7772-200">1</span></span>                                 |
| <span data-ttu-id="e7772-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7772-201">Range-Upper</span></span>            | <span data-ttu-id="e7772-202">256</span><span class="sxs-lookup"><span data-stu-id="e7772-202">256</span></span>                               |
| <span data-ttu-id="e7772-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7772-203">Search-Flags</span></span>           | <span data-ttu-id="e7772-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7772-204">0x00000000</span></span>                        |
| <span data-ttu-id="e7772-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7772-205">System-Flags</span></span>           | <span data-ttu-id="e7772-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7772-206">0x00000010</span></span>                        |
| <span data-ttu-id="e7772-207">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e7772-207">Classes used in</span></span>        | [<span data-ttu-id="e7772-208">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="e7772-208">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e7772-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e7772-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e7772-210">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e7772-210">Entry</span></span> | <span data-ttu-id="e7772-211">Wert</span><span class="sxs-lookup"><span data-stu-id="e7772-211">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e7772-212">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e7772-212">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e7772-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7772-213">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e7772-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7772-214">System-Only</span></span>            | <span data-ttu-id="e7772-215">False</span><span class="sxs-lookup"><span data-stu-id="e7772-215">False</span></span>                             |
| <span data-ttu-id="e7772-216">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e7772-216">Is-Single-Valued</span></span>       | <span data-ttu-id="e7772-217">Richtig</span><span class="sxs-lookup"><span data-stu-id="e7772-217">True</span></span>                              |
| <span data-ttu-id="e7772-218">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e7772-218">Is Indexed</span></span>             | <span data-ttu-id="e7772-219">False</span><span class="sxs-lookup"><span data-stu-id="e7772-219">False</span></span>                             |
| <span data-ttu-id="e7772-220">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e7772-220">In Global Catalog</span></span>      | <span data-ttu-id="e7772-221">False</span><span class="sxs-lookup"><span data-stu-id="e7772-221">False</span></span>                             |
| <span data-ttu-id="e7772-222">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e7772-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7772-223">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e7772-223">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e7772-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7772-224">Range-Lower</span></span>            | <span data-ttu-id="e7772-225">1</span><span class="sxs-lookup"><span data-stu-id="e7772-225">1</span></span>                                 |
| <span data-ttu-id="e7772-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7772-226">Range-Upper</span></span>            | <span data-ttu-id="e7772-227">256</span><span class="sxs-lookup"><span data-stu-id="e7772-227">256</span></span>                               |
| <span data-ttu-id="e7772-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7772-228">Search-Flags</span></span>           | <span data-ttu-id="e7772-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7772-229">0x00000000</span></span>                        |
| <span data-ttu-id="e7772-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7772-230">System-Flags</span></span>           | <span data-ttu-id="e7772-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7772-231">0x00000010</span></span>                        |
| <span data-ttu-id="e7772-232">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e7772-232">Classes used in</span></span>        | [<span data-ttu-id="e7772-233">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="e7772-233">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e7772-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e7772-234">Windows Server 2012</span></span>



| <span data-ttu-id="e7772-235">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e7772-235">Entry</span></span> | <span data-ttu-id="e7772-236">Wert</span><span class="sxs-lookup"><span data-stu-id="e7772-236">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e7772-237">Link-ID</span><span class="sxs-lookup"><span data-stu-id="e7772-237">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e7772-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7772-238">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e7772-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7772-239">System-Only</span></span>            | <span data-ttu-id="e7772-240">False</span><span class="sxs-lookup"><span data-stu-id="e7772-240">False</span></span>                             |
| <span data-ttu-id="e7772-241">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="e7772-241">Is-Single-Valued</span></span>       | <span data-ttu-id="e7772-242">Richtig</span><span class="sxs-lookup"><span data-stu-id="e7772-242">True</span></span>                              |
| <span data-ttu-id="e7772-243">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="e7772-243">Is Indexed</span></span>             | <span data-ttu-id="e7772-244">False</span><span class="sxs-lookup"><span data-stu-id="e7772-244">False</span></span>                             |
| <span data-ttu-id="e7772-245">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="e7772-245">In Global Catalog</span></span>      | <span data-ttu-id="e7772-246">False</span><span class="sxs-lookup"><span data-stu-id="e7772-246">False</span></span>                             |
| <span data-ttu-id="e7772-247">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e7772-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7772-248">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="e7772-248">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e7772-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7772-249">Range-Lower</span></span>            | <span data-ttu-id="e7772-250">1</span><span class="sxs-lookup"><span data-stu-id="e7772-250">1</span></span>                                 |
| <span data-ttu-id="e7772-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7772-251">Range-Upper</span></span>            | <span data-ttu-id="e7772-252">256</span><span class="sxs-lookup"><span data-stu-id="e7772-252">256</span></span>                               |
| <span data-ttu-id="e7772-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7772-253">Search-Flags</span></span>           | <span data-ttu-id="e7772-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7772-254">0x00000000</span></span>                        |
| <span data-ttu-id="e7772-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7772-255">System-Flags</span></span>           | <span data-ttu-id="e7772-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7772-256">0x00000010</span></span>                        |
| <span data-ttu-id="e7772-257">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="e7772-257">Classes used in</span></span>        | [<span data-ttu-id="e7772-258">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="e7772-258">**User**</span></span>](c-user.md)<br/> |



 

 





