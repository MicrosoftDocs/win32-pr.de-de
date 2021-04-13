---
title: Zulässige Berechtigung zum Authentifizieren von erweiterten Rechten
description: Das Steuerelement Zugriffsrecht steuert, wer sich bei einem bestimmten Computer oder Dienst authentifizieren kann.
ms.assetid: 265e6240-0fb5-4037-8c66-05fadc646100
ms.tgt_platform: multiple
keywords:
- Das AD-Schema für erweiterte Rechte kann nicht authentifiziert werden.
topic_type:
- apiref
api_name:
- Allowed-To-Authenticate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2fca1b6f4670fd340170ed5cfd1f0160d61945
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480447"
---
# <a name="allowed-to-authenticate-extended-right"></a><span data-ttu-id="5ad6b-104">Zulässige Berechtigung zum Authentifizieren von erweiterten Rechten</span><span class="sxs-lookup"><span data-stu-id="5ad6b-104">Allowed-To-Authenticate extended right</span></span>

<span data-ttu-id="5ad6b-105">Das Steuerelement Zugriffsrecht steuert, wer sich bei einem bestimmten Computer oder Dienst authentifizieren kann.</span><span class="sxs-lookup"><span data-stu-id="5ad6b-105">The control access right controls who can authenticate to a particular computer or service.</span></span> <span data-ttu-id="5ad6b-106">Sie befindet sich im Grunde auf Computern, Benutzern und inetOrgPerson-Objekten.</span><span class="sxs-lookup"><span data-stu-id="5ad6b-106">It basically lives on computer, user, and InetOrgPerson objects.</span></span> <span data-ttu-id="5ad6b-107">Dies gilt auch für das Domänen Objekt, wenn der Zugriff für die gesamte Domäne zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="5ad6b-107">It is also applicable on the domain object if access is allowed for the entire domain.</span></span> <span data-ttu-id="5ad6b-108">Sie kann auf Organisationseinheiten angewendet werden, um Benutzern die Möglichkeit zu geben, vererbbare ACEs auf Organisationseinheiten festzulegen, die eine Gruppe von Benutzer-oder Computer Objekten enthalten.</span><span class="sxs-lookup"><span data-stu-id="5ad6b-108">It can be applied to OUs to permit users to be able to set inheritable ACEs on OUs that contain a set of user or computer objects.</span></span>



| <span data-ttu-id="5ad6b-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5ad6b-109">Entry</span></span> | <span data-ttu-id="5ad6b-110">Wert</span><span class="sxs-lookup"><span data-stu-id="5ad6b-110">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="5ad6b-111">CN</span><span class="sxs-lookup"><span data-stu-id="5ad6b-111">CN</span></span>           | <span data-ttu-id="5ad6b-112">Zulässig zu authentifizieren</span><span class="sxs-lookup"><span data-stu-id="5ad6b-112">Allowed-To-Authenticate</span></span>              |
| <span data-ttu-id="5ad6b-113">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="5ad6b-113">Display-Name</span></span> | <span data-ttu-id="5ad6b-114">Authentifizieren zulässig</span><span class="sxs-lookup"><span data-stu-id="5ad6b-114">Allowed to Authenticate</span></span>              |
| <span data-ttu-id="5ad6b-115">Rights-GUID</span><span class="sxs-lookup"><span data-stu-id="5ad6b-115">Rights-GUID</span></span>  | <span data-ttu-id="5ad6b-116">68b1d179-0d15-4d4f-ab71-46152e79a7bc</span><span class="sxs-lookup"><span data-stu-id="5ad6b-116">68b1d179-0d15-4d4f-ab71-46152e79a7bc</span></span> |



## <a name="implementations"></a><span data-ttu-id="5ad6b-117">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="5ad6b-117">Implementations</span></span>

-   [<span data-ttu-id="5ad6b-118">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-118">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5ad6b-119">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-119">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5ad6b-120">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-120">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5ad6b-121">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-121">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5ad6b-122">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-122">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="5ad6b-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5ad6b-123">Windows Server 2003</span></span>



| <span data-ttu-id="5ad6b-124">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5ad6b-124">Entry</span></span> | <span data-ttu-id="5ad6b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="5ad6b-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad6b-126">Applies-To</span><span class="sxs-lookup"><span data-stu-id="5ad6b-126">Applies-To</span></span>              | [<span data-ttu-id="5ad6b-127">**Computer**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-127">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="5ad6b-128">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-128">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="5ad6b-129">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-129">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="5ad6b-130">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="5ad6b-130">Localization-Display-ID</span></span> | <span data-ttu-id="5ad6b-131">65</span><span class="sxs-lookup"><span data-stu-id="5ad6b-131">65</span></span>                                                                                                                              |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5ad6b-132">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5ad6b-132">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5ad6b-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5ad6b-133">Entry</span></span> | <span data-ttu-id="5ad6b-134">Wert</span><span class="sxs-lookup"><span data-stu-id="5ad6b-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad6b-135">Applies-To</span><span class="sxs-lookup"><span data-stu-id="5ad6b-135">Applies-To</span></span>              | [<span data-ttu-id="5ad6b-136">**Computer**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-136">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="5ad6b-137">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-137">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="5ad6b-138">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-138">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="5ad6b-139">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="5ad6b-139">Localization-Display-ID</span></span> | <span data-ttu-id="5ad6b-140">65</span><span class="sxs-lookup"><span data-stu-id="5ad6b-140">65</span></span>                                                                                                                              |



## <a name="windows-server-2008"></a><span data-ttu-id="5ad6b-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ad6b-141">Windows Server 2008</span></span>



| <span data-ttu-id="5ad6b-142">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5ad6b-142">Entry</span></span> | <span data-ttu-id="5ad6b-143">Wert</span><span class="sxs-lookup"><span data-stu-id="5ad6b-143">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad6b-144">Applies-To</span><span class="sxs-lookup"><span data-stu-id="5ad6b-144">Applies-To</span></span>              | [<span data-ttu-id="5ad6b-145">**Computer**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-145">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="5ad6b-146">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-146">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="5ad6b-147">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-147">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="5ad6b-148">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="5ad6b-148">Localization-Display-ID</span></span> | <span data-ttu-id="5ad6b-149">65</span><span class="sxs-lookup"><span data-stu-id="5ad6b-149">65</span></span>                                                                                                                              |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5ad6b-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5ad6b-150">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5ad6b-151">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5ad6b-151">Entry</span></span> | <span data-ttu-id="5ad6b-152">Wert</span><span class="sxs-lookup"><span data-stu-id="5ad6b-152">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad6b-153">Applies-To</span><span class="sxs-lookup"><span data-stu-id="5ad6b-153">Applies-To</span></span>              | [<span data-ttu-id="5ad6b-154">**Computer**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-154">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="5ad6b-155">**ms-DS-Managed-Service-Konto**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-155">**ms-DS-Managed-Service-Account**</span></span>](c-msds-managedserviceaccount.md)<br/> [<span data-ttu-id="5ad6b-156">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-156">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="5ad6b-157">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-157">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="5ad6b-158">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="5ad6b-158">Localization-Display-ID</span></span> | <span data-ttu-id="5ad6b-159">65</span><span class="sxs-lookup"><span data-stu-id="5ad6b-159">65</span></span>                                                                                                                                                                                                               |



## <a name="windows-server-2012"></a><span data-ttu-id="5ad6b-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ad6b-160">Windows Server 2012</span></span>



| <span data-ttu-id="5ad6b-161">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5ad6b-161">Entry</span></span> | <span data-ttu-id="5ad6b-162">Wert</span><span class="sxs-lookup"><span data-stu-id="5ad6b-162">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad6b-163">Applies-To</span><span class="sxs-lookup"><span data-stu-id="5ad6b-163">Applies-To</span></span>              | [<span data-ttu-id="5ad6b-164">**Computer**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-164">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="5ad6b-165">**ms-DS-Managed-Service-Konto**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-165">**ms-DS-Managed-Service-Account**</span></span>](c-msds-managedserviceaccount.md)<br/> [<span data-ttu-id="5ad6b-166">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-166">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="5ad6b-167">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="5ad6b-167">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="5ad6b-168">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="5ad6b-168">Localization-Display-ID</span></span> | <span data-ttu-id="5ad6b-169">65</span><span class="sxs-lookup"><span data-stu-id="5ad6b-169">65</span></span>                                                                                                                                                                                                               |



 

 





