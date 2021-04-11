---
title: MS-Authz-Resource-Condition-Attribut
description: Für eine zentrale Zugriffs Regel ist dieses Attribut ein Ausdruck, der den Bereich der Ziel Ressource identifiziert, auf die die Richtlinie angewendet wird.
ms.assetid: d3c1815e-3fa1-4106-82a1-74403f07fcde
ms.tgt_platform: multiple
keywords:
- "\"MS-Authz-Resource-Condition\"-Attribut, AD-Schema"
- AD-Schema des msauthz-resourcecondition-Attributs
topic_type:
- apiref
api_name:
- ms-Authz-Resource-Condition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3891e75763fd52d14d4ceaac560b33c824d06449
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123026"
---
# <a name="ms-authz-resource-condition-attribute"></a><span data-ttu-id="16207-105">MS-Authz-Resource-Condition-Attribut</span><span class="sxs-lookup"><span data-stu-id="16207-105">ms-Authz-Resource-Condition attribute</span></span>

<span data-ttu-id="16207-106">Für eine zentrale Zugriffs Regel ist dieses Attribut ein Ausdruck, der den Bereich der Ziel Ressource identifiziert, auf die die Richtlinie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="16207-106">For a central access rule, this attribute is an expression that identifies the scope of the target resource to which the policy applies.</span></span>



| <span data-ttu-id="16207-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="16207-107">Entry</span></span> | <span data-ttu-id="16207-108">Wert</span><span class="sxs-lookup"><span data-stu-id="16207-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="16207-109">CN</span><span class="sxs-lookup"><span data-stu-id="16207-109">CN</span></span>                | <span data-ttu-id="16207-110">MS-Authz-Resource-Condition</span><span class="sxs-lookup"><span data-stu-id="16207-110">ms-Authz-Resource-Condition</span></span>                 |
| <span data-ttu-id="16207-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="16207-111">Ldap-Display-Name</span></span> | <span data-ttu-id="16207-112">msauthz-resourcecondition</span><span class="sxs-lookup"><span data-stu-id="16207-112">msAuthz-ResourceCondition</span></span>                   |
| <span data-ttu-id="16207-113">Size</span><span class="sxs-lookup"><span data-stu-id="16207-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="16207-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="16207-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="16207-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="16207-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="16207-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="16207-116">Attribute-Id</span></span>      | <span data-ttu-id="16207-117">1.2.840.113556.1.4.2153</span><span class="sxs-lookup"><span data-stu-id="16207-117">1.2.840.113556.1.4.2153</span></span>                     |
| <span data-ttu-id="16207-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="16207-118">System-Id-Guid</span></span>    | <span data-ttu-id="16207-119">80997877-F874-4c68-864d-6e508a83bdbd</span><span class="sxs-lookup"><span data-stu-id="16207-119">80997877-f874-4c68-864d-6e508a83bdbd</span></span>        |
| <span data-ttu-id="16207-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="16207-120">Syntax</span></span>            | [<span data-ttu-id="16207-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="16207-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="16207-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="16207-122">Implementations</span></span>

-   [<span data-ttu-id="16207-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="16207-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="16207-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="16207-124">Windows Server 2012</span></span>



| <span data-ttu-id="16207-125">Eingabe</span><span class="sxs-lookup"><span data-stu-id="16207-125">Entry</span></span> | <span data-ttu-id="16207-126">Wert</span><span class="sxs-lookup"><span data-stu-id="16207-126">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="16207-127">Link-ID</span><span class="sxs-lookup"><span data-stu-id="16207-127">Link-Id</span></span>                | \-                                                                             |
| <span data-ttu-id="16207-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16207-128">MAPI-Id</span></span>                | \-                                                                             |
| <span data-ttu-id="16207-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="16207-129">System-Only</span></span>            | <span data-ttu-id="16207-130">False</span><span class="sxs-lookup"><span data-stu-id="16207-130">False</span></span>                                                                          |
| <span data-ttu-id="16207-131">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="16207-131">Is-Single-Valued</span></span>       | <span data-ttu-id="16207-132">Richtig</span><span class="sxs-lookup"><span data-stu-id="16207-132">True</span></span>                                                                           |
| <span data-ttu-id="16207-133">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="16207-133">Is Indexed</span></span>             | <span data-ttu-id="16207-134">False</span><span class="sxs-lookup"><span data-stu-id="16207-134">False</span></span>                                                                          |
| <span data-ttu-id="16207-135">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="16207-135">In Global Catalog</span></span>      | <span data-ttu-id="16207-136">False</span><span class="sxs-lookup"><span data-stu-id="16207-136">False</span></span>                                                                          |
| <span data-ttu-id="16207-137">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="16207-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="16207-138">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="16207-138">O:BAG:BAD:S:</span></span>                                                                   |
| <span data-ttu-id="16207-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16207-139">Range-Lower</span></span>            | \-                                                                             |
| <span data-ttu-id="16207-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16207-140">Range-Upper</span></span>            | \-                                                                             |
| <span data-ttu-id="16207-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16207-141">Search-Flags</span></span>           | <span data-ttu-id="16207-142">0x00000000</span><span class="sxs-lookup"><span data-stu-id="16207-142">0x00000000</span></span>                                                                     |
| <span data-ttu-id="16207-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16207-143">System-Flags</span></span>           | <span data-ttu-id="16207-144">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16207-144">0x00000010</span></span>                                                                     |
| <span data-ttu-id="16207-145">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="16207-145">Classes used in</span></span>        | [<span data-ttu-id="16207-146">**MS-Authz-Central-Access-Rule**</span><span class="sxs-lookup"><span data-stu-id="16207-146">**ms-Authz-Central-Access-Rule**</span></span>](c-msauthz-centralaccessrule.md)<br/> |



 

 





