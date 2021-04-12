---
title: ms-DS-managedpassword-Attribut
description: Dieses konstruierte Attribut gibt ein BLOB zurück, das das Clear-Text Previous und das aktuelle Kennwort, timeuntilepochexpire und timeuntilnextscheduledupdate für eine Gruppen-MSA enthält.
ms.assetid: bcabb20f-46f3-4c15-b71b-a8dfc43678bc
ms.tgt_platform: multiple
keywords:
- AD-Schema des ms-DS-managedpassword-Attributs
- AD-Schema des msDS-managedpassword-Attributs
topic_type:
- apiref
api_name:
- ms-DS-ManagedPassword
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a440f1849e01ae4930b72441f75b17ce51a0566b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107811"
---
# <a name="ms-ds-managedpassword-attribute"></a><span data-ttu-id="fcfe9-105">ms-DS-managedpassword-Attribut</span><span class="sxs-lookup"><span data-stu-id="fcfe9-105">ms-DS-ManagedPassword attribute</span></span>

<span data-ttu-id="fcfe9-106">Dieses konstruierte Attribut gibt ein BLOB zurück, das das Clear-Text Previous und das aktuelle Kennwort, timeuntilepochexpire und timeuntilnextscheduledupdate für eine Gruppen-MSA enthält.</span><span class="sxs-lookup"><span data-stu-id="fcfe9-106">This constructed attribute returns a blob that contains the clear-text previous and current password, TimeUntilEpochExpires, and TimeUntilNextScheduledUpdate for a group MSA.</span></span>



| <span data-ttu-id="fcfe9-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fcfe9-107">Entry</span></span> | <span data-ttu-id="fcfe9-108">Wert</span><span class="sxs-lookup"><span data-stu-id="fcfe9-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="fcfe9-109">CN</span><span class="sxs-lookup"><span data-stu-id="fcfe9-109">CN</span></span>                | <span data-ttu-id="fcfe9-110">ms-DS-managedpassword</span><span class="sxs-lookup"><span data-stu-id="fcfe9-110">ms-DS-ManagedPassword</span></span>                                 |
| <span data-ttu-id="fcfe9-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="fcfe9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fcfe9-112">MSDS-managedpassword</span><span class="sxs-lookup"><span data-stu-id="fcfe9-112">msDS-ManagedPassword</span></span>                                  |
| <span data-ttu-id="fcfe9-113">Size</span><span class="sxs-lookup"><span data-stu-id="fcfe9-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="fcfe9-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="fcfe9-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="fcfe9-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="fcfe9-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="fcfe9-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fcfe9-116">Attribute-Id</span></span>      | <span data-ttu-id="fcfe9-117">1.2.840.113556.1.4.2196</span><span class="sxs-lookup"><span data-stu-id="fcfe9-117">1.2.840.113556.1.4.2196</span></span>                               |
| <span data-ttu-id="fcfe9-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fcfe9-118">System-Id-Guid</span></span>    | <span data-ttu-id="fcfe9-119">e362ed86-b728-0842-b27d-2dea7a9df218</span><span class="sxs-lookup"><span data-stu-id="fcfe9-119">e362ed86-b728-0842-b27d-2dea7a9df218</span></span>                  |
| <span data-ttu-id="fcfe9-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcfe9-120">Syntax</span></span>            | [<span data-ttu-id="fcfe9-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="fcfe9-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="fcfe9-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="fcfe9-122">Implementations</span></span>

-   [<span data-ttu-id="fcfe9-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fcfe9-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="fcfe9-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fcfe9-124">Windows Server 2012</span></span>



| <span data-ttu-id="fcfe9-125">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fcfe9-125">Entry</span></span> | <span data-ttu-id="fcfe9-126">Wert</span><span class="sxs-lookup"><span data-stu-id="fcfe9-126">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcfe9-127">Link-ID</span><span class="sxs-lookup"><span data-stu-id="fcfe9-127">Link-Id</span></span>                | \-                                                                                          |
| <span data-ttu-id="fcfe9-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fcfe9-128">MAPI-Id</span></span>                | \-                                                                                          |
| <span data-ttu-id="fcfe9-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="fcfe9-129">System-Only</span></span>            | <span data-ttu-id="fcfe9-130">False</span><span class="sxs-lookup"><span data-stu-id="fcfe9-130">False</span></span>                                                                                       |
| <span data-ttu-id="fcfe9-131">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="fcfe9-131">Is-Single-Valued</span></span>       | <span data-ttu-id="fcfe9-132">Richtig</span><span class="sxs-lookup"><span data-stu-id="fcfe9-132">True</span></span>                                                                                        |
| <span data-ttu-id="fcfe9-133">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="fcfe9-133">Is Indexed</span></span>             | <span data-ttu-id="fcfe9-134">False</span><span class="sxs-lookup"><span data-stu-id="fcfe9-134">False</span></span>                                                                                       |
| <span data-ttu-id="fcfe9-135">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="fcfe9-135">In Global Catalog</span></span>      | <span data-ttu-id="fcfe9-136">False</span><span class="sxs-lookup"><span data-stu-id="fcfe9-136">False</span></span>                                                                                       |
| <span data-ttu-id="fcfe9-137">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fcfe9-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="fcfe9-138">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="fcfe9-138">O:BAG:BAD:S:</span></span>                                                                                |
| <span data-ttu-id="fcfe9-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fcfe9-139">Range-Lower</span></span>            | \-                                                                                          |
| <span data-ttu-id="fcfe9-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fcfe9-140">Range-Upper</span></span>            | \-                                                                                          |
| <span data-ttu-id="fcfe9-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fcfe9-141">Search-Flags</span></span>           | <span data-ttu-id="fcfe9-142">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fcfe9-142">0x00000000</span></span>                                                                                  |
| <span data-ttu-id="fcfe9-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fcfe9-143">System-Flags</span></span>           | <span data-ttu-id="fcfe9-144">0x00000014</span><span class="sxs-lookup"><span data-stu-id="fcfe9-144">0x00000014</span></span>                                                                                  |
| <span data-ttu-id="fcfe9-145">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="fcfe9-145">Classes used in</span></span>        | [<span data-ttu-id="fcfe9-146">**ms-DS-Group-Managed-Service-Konto**</span><span class="sxs-lookup"><span data-stu-id="fcfe9-146">**ms-DS-Group-Managed-Service-Account**</span></span>](c-msds-groupmanagedserviceaccount.md)<br/> |



 

 





