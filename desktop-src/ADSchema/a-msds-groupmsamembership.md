---
title: ms-DS-groupmsamembership-Attribut
description: Dieses Attribut wird für Zugriffs Überprüfungen verwendet, um zu bestimmen, ob ein Anforderer über die Berechtigung zum Abrufen des Kennworts für eine Gruppen-MSA verfügt.
ms.assetid: 1512826d-fb7e-4039-ad93-f9334fd1d485
ms.tgt_platform: multiple
keywords:
- AD-Schema des ms-DS-groupmsamembership-Attributs
- AD-Schema des msDS-groupmsamembership-Attributs
topic_type:
- apiref
api_name:
- ms-DS-GroupMSAMembership
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184f7f682d5360a0524f58e07c3f468b96e15b14
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957514"
---
# <a name="ms-ds-groupmsamembership-attribute"></a><span data-ttu-id="09be9-105">ms-DS-groupmsamembership-Attribut</span><span class="sxs-lookup"><span data-stu-id="09be9-105">ms-DS-GroupMSAMembership attribute</span></span>

<span data-ttu-id="09be9-106">Dieses Attribut wird für Zugriffs Überprüfungen verwendet, um zu bestimmen, ob ein Anforderer über die Berechtigung zum Abrufen des Kennworts für eine Gruppen-MSA verfügt.</span><span class="sxs-lookup"><span data-stu-id="09be9-106">This attribute is used for access checks to determine if a requestor has permission to retrieve the password for a group MSA.</span></span>



| <span data-ttu-id="09be9-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="09be9-107">Entry</span></span> | <span data-ttu-id="09be9-108">Wert</span><span class="sxs-lookup"><span data-stu-id="09be9-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="09be9-109">CN</span><span class="sxs-lookup"><span data-stu-id="09be9-109">CN</span></span>                | <span data-ttu-id="09be9-110">ms-DS-groupmsamembership</span><span class="sxs-lookup"><span data-stu-id="09be9-110">ms-DS-GroupMSAMembership</span></span>                            |
| <span data-ttu-id="09be9-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="09be9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="09be9-112">MSDS-groupmsamembership</span><span class="sxs-lookup"><span data-stu-id="09be9-112">msDS-GroupMSAMembership</span></span>                             |
| <span data-ttu-id="09be9-113">Size</span><span class="sxs-lookup"><span data-stu-id="09be9-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="09be9-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="09be9-114">Update Privilege</span></span>  | \-                                                  |
| <span data-ttu-id="09be9-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="09be9-115">Update Frequency</span></span>  | \-                                                  |
| <span data-ttu-id="09be9-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="09be9-116">Attribute-Id</span></span>      | <span data-ttu-id="09be9-117">1.2.840.113556.1.4.2200</span><span class="sxs-lookup"><span data-stu-id="09be9-117">1.2.840.113556.1.4.2200</span></span>                             |
| <span data-ttu-id="09be9-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="09be9-118">System-Id-Guid</span></span>    | <span data-ttu-id="09be9-119">888eedd6-ce04-df40-b462-b8a50e41ba38</span><span class="sxs-lookup"><span data-stu-id="09be9-119">888eedd6-ce04-df40-b462-b8a50e41ba38</span></span>                |
| <span data-ttu-id="09be9-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="09be9-120">Syntax</span></span>            | [<span data-ttu-id="09be9-121">**String(NT-Sec-Desc)**</span><span class="sxs-lookup"><span data-stu-id="09be9-121">**String(NT-Sec-Desc)**</span></span>](s-string-nt-sec-desc.md) |



## <a name="implementations"></a><span data-ttu-id="09be9-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="09be9-122">Implementations</span></span>

-   [<span data-ttu-id="09be9-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="09be9-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="09be9-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="09be9-124">Windows Server 2012</span></span>



| <span data-ttu-id="09be9-125">Eingabe</span><span class="sxs-lookup"><span data-stu-id="09be9-125">Entry</span></span> | <span data-ttu-id="09be9-126">Wert</span><span class="sxs-lookup"><span data-stu-id="09be9-126">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="09be9-127">Link-ID</span><span class="sxs-lookup"><span data-stu-id="09be9-127">Link-Id</span></span>                | \-                                                                                          |
| <span data-ttu-id="09be9-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09be9-128">MAPI-Id</span></span>                | \-                                                                                          |
| <span data-ttu-id="09be9-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="09be9-129">System-Only</span></span>            | <span data-ttu-id="09be9-130">False</span><span class="sxs-lookup"><span data-stu-id="09be9-130">False</span></span>                                                                                       |
| <span data-ttu-id="09be9-131">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="09be9-131">Is-Single-Valued</span></span>       | <span data-ttu-id="09be9-132">Richtig</span><span class="sxs-lookup"><span data-stu-id="09be9-132">True</span></span>                                                                                        |
| <span data-ttu-id="09be9-133">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="09be9-133">Is Indexed</span></span>             | <span data-ttu-id="09be9-134">False</span><span class="sxs-lookup"><span data-stu-id="09be9-134">False</span></span>                                                                                       |
| <span data-ttu-id="09be9-135">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="09be9-135">In Global Catalog</span></span>      | <span data-ttu-id="09be9-136">False</span><span class="sxs-lookup"><span data-stu-id="09be9-136">False</span></span>                                                                                       |
| <span data-ttu-id="09be9-137">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="09be9-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="09be9-138">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="09be9-138">O:BAG:BAD:S:</span></span>                                                                                |
| <span data-ttu-id="09be9-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09be9-139">Range-Lower</span></span>            | \-                                                                                          |
| <span data-ttu-id="09be9-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09be9-140">Range-Upper</span></span>            | \-                                                                                          |
| <span data-ttu-id="09be9-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09be9-141">Search-Flags</span></span>           | <span data-ttu-id="09be9-142">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09be9-142">0x00000000</span></span>                                                                                  |
| <span data-ttu-id="09be9-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09be9-143">System-Flags</span></span>           | <span data-ttu-id="09be9-144">0x00000010</span><span class="sxs-lookup"><span data-stu-id="09be9-144">0x00000010</span></span>                                                                                  |
| <span data-ttu-id="09be9-145">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="09be9-145">Classes used in</span></span>        | [<span data-ttu-id="09be9-146">**ms-DS-Group-Managed-Service-Konto**</span><span class="sxs-lookup"><span data-stu-id="09be9-146">**ms-DS-Group-Managed-Service-Account**</span></span>](c-msds-groupmanagedserviceaccount.md)<br/> |



 

 





