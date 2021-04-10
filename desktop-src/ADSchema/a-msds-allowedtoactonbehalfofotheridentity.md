---
title: ms-DS-allowed-to-act-on-Auftrag-of-Identity-Attribut
description: Dieses Attribut wird für Zugriffs Überprüfungen verwendet, um zu bestimmen, ob ein Anforderer über die Berechtigung verfügt, im Namen anderer Identitäten für Dienste, die als dieses Konto ausgeführt werden, zu agieren.
ms.assetid: 38203665-4505-461b-b6ab-b634725ac2fa
ms.tgt_platform: multiple
keywords:
- AD-Schema "ms-DS-allowed-to-act-on-Do-of-Identity-Attribute"
- AD-Schema für das msDS-Zustellungs Attribut
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45dacd532b1d8a55b3656dc1d65fc1ebd940476c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859861"
---
# <a name="ms-ds-allowed-to-act-on-behalf-of-other-identity-attribute"></a><span data-ttu-id="bfa47-105">ms-DS-allowed-to-act-on-Auftrag-of-Identity-Attribut</span><span class="sxs-lookup"><span data-stu-id="bfa47-105">ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity attribute</span></span>

<span data-ttu-id="bfa47-106">Dieses Attribut wird für Zugriffs Überprüfungen verwendet, um zu bestimmen, ob ein Anforderer über die Berechtigung verfügt, im Namen anderer Identitäten für Dienste, die als dieses Konto ausgeführt werden, zu agieren.</span><span class="sxs-lookup"><span data-stu-id="bfa47-106">This attribute is used for access checks to determine if a requestor has permission to act on the behalf of other identities to services running as this account.</span></span>



| <span data-ttu-id="bfa47-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bfa47-107">Entry</span></span> | <span data-ttu-id="bfa47-108">Wert</span><span class="sxs-lookup"><span data-stu-id="bfa47-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="bfa47-109">CN</span><span class="sxs-lookup"><span data-stu-id="bfa47-109">CN</span></span>                | <span data-ttu-id="bfa47-110">ms-DS-allowed-to-act-on-Do-of-other-Identity</span><span class="sxs-lookup"><span data-stu-id="bfa47-110">ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity</span></span>    |
| <span data-ttu-id="bfa47-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bfa47-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bfa47-112">MSDS-Zuweisung von "msDS--ID"</span><span class="sxs-lookup"><span data-stu-id="bfa47-112">msDS-AllowedToActOnBehalfOfOtherIdentity</span></span>            |
| <span data-ttu-id="bfa47-113">Size</span><span class="sxs-lookup"><span data-stu-id="bfa47-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="bfa47-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="bfa47-114">Update Privilege</span></span>  | \-                                                  |
| <span data-ttu-id="bfa47-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="bfa47-115">Update Frequency</span></span>  | \-                                                  |
| <span data-ttu-id="bfa47-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bfa47-116">Attribute-Id</span></span>      | <span data-ttu-id="bfa47-117">1.2.840.113556.1.4.2182</span><span class="sxs-lookup"><span data-stu-id="bfa47-117">1.2.840.113556.1.4.2182</span></span>                             |
| <span data-ttu-id="bfa47-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bfa47-118">System-Id-Guid</span></span>    | <span data-ttu-id="bfa47-119">3b78c3e5-b-46bd-a0b8-9d18116ddc79</span><span class="sxs-lookup"><span data-stu-id="bfa47-119">3f78c3e5-f79a-46bd-a0b8-9d18116ddc79</span></span>                |
| <span data-ttu-id="bfa47-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfa47-120">Syntax</span></span>            | [<span data-ttu-id="bfa47-121">**String(NT-Sec-Desc)**</span><span class="sxs-lookup"><span data-stu-id="bfa47-121">**String(NT-Sec-Desc)**</span></span>](s-string-nt-sec-desc.md) |



## <a name="implementations"></a><span data-ttu-id="bfa47-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="bfa47-122">Implementations</span></span>

-   [<span data-ttu-id="bfa47-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bfa47-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="bfa47-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bfa47-124">Windows Server 2012</span></span>



| <span data-ttu-id="bfa47-125">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bfa47-125">Entry</span></span> | <span data-ttu-id="bfa47-126">Wert</span><span class="sxs-lookup"><span data-stu-id="bfa47-126">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="bfa47-127">Link-ID</span><span class="sxs-lookup"><span data-stu-id="bfa47-127">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bfa47-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfa47-128">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bfa47-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfa47-129">System-Only</span></span>            | <span data-ttu-id="bfa47-130">Richtig</span><span class="sxs-lookup"><span data-stu-id="bfa47-130">True</span></span>                                                               |
| <span data-ttu-id="bfa47-131">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="bfa47-131">Is-Single-Valued</span></span>       | <span data-ttu-id="bfa47-132">Richtig</span><span class="sxs-lookup"><span data-stu-id="bfa47-132">True</span></span>                                                               |
| <span data-ttu-id="bfa47-133">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="bfa47-133">Is Indexed</span></span>             | <span data-ttu-id="bfa47-134">False</span><span class="sxs-lookup"><span data-stu-id="bfa47-134">False</span></span>                                                              |
| <span data-ttu-id="bfa47-135">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="bfa47-135">In Global Catalog</span></span>      | <span data-ttu-id="bfa47-136">False</span><span class="sxs-lookup"><span data-stu-id="bfa47-136">False</span></span>                                                              |
| <span data-ttu-id="bfa47-137">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bfa47-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfa47-138">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="bfa47-138">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="bfa47-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfa47-139">Range-Lower</span></span>            | <span data-ttu-id="bfa47-140">0</span><span class="sxs-lookup"><span data-stu-id="bfa47-140">0</span></span>                                                                  |
| <span data-ttu-id="bfa47-141">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfa47-141">Range-Upper</span></span>            | <span data-ttu-id="bfa47-142">132096</span><span class="sxs-lookup"><span data-stu-id="bfa47-142">132096</span></span>                                                             |
| <span data-ttu-id="bfa47-143">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfa47-143">Search-Flags</span></span>           | <span data-ttu-id="bfa47-144">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfa47-144">0x00000000</span></span>                                                         |
| <span data-ttu-id="bfa47-145">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfa47-145">System-Flags</span></span>           | <span data-ttu-id="bfa47-146">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bfa47-146">0x00000010</span></span>                                                         |
| <span data-ttu-id="bfa47-147">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="bfa47-147">Classes used in</span></span>        | [<span data-ttu-id="bfa47-148">**Unternehmensperson**</span><span class="sxs-lookup"><span data-stu-id="bfa47-148">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





