---
title: Refresh-Group-Cache erweitert rechts
description: Dies gilt für keine GC-Anmeldung. Keine GC-Anmeldung stützt sich auf das Zwischenspeichern von Gruppenmitgliedschaften, und dieses Zugriffsrecht wird verwendet, um Administratoren und Operatoren Berechtigungen zu erteilen, um eine sofortige Aktualisierung des Caches zu ermöglichen und eine Verbindung mit einem verfügbaren GC aufzunehmen.
ms.assetid: 1db49a92-ccf8-4087-ac79-f4c1bcea6aa4
ms.tgt_platform: multiple
keywords:
- AD-Schema für Aktualisierungs-und Gruppen Cache Erweiterung
topic_type:
- apiref
api_name:
- Refresh-Group-Cache
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb576b5ef2310bceedb632a3b1ab8453b4d435e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859418"
---
# <a name="refresh-group-cache-extended-right"></a><span data-ttu-id="8e731-105">Refresh-Group-Cache erweitert rechts</span><span class="sxs-lookup"><span data-stu-id="8e731-105">Refresh-Group-Cache extended right</span></span>

<span data-ttu-id="8e731-106">Dies gilt für keine GC-Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="8e731-106">This is for no GC logon.</span></span> <span data-ttu-id="8e731-107">Keine GC-Anmeldung stützt sich auf das Zwischenspeichern von Gruppenmitgliedschaften, und dieses Zugriffsrecht wird verwendet, um Administratoren und Operatoren Berechtigungen zu erteilen, um eine sofortige Aktualisierung des Caches zu ermöglichen und eine Verbindung mit einem verfügbaren GC aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="8e731-107">No GC logon relies on caching group memberships, and this control access right is used to grant administrators and operators permission rights to cause an immediate refresh of the cache, contacting an available GC.</span></span>



| <span data-ttu-id="8e731-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e731-108">Entry</span></span> | <span data-ttu-id="8e731-109">Wert</span><span class="sxs-lookup"><span data-stu-id="8e731-109">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="8e731-110">CN</span><span class="sxs-lookup"><span data-stu-id="8e731-110">CN</span></span>           | <span data-ttu-id="8e731-111">Refresh-Group-Cache</span><span class="sxs-lookup"><span data-stu-id="8e731-111">Refresh-Group-Cache</span></span>                  |
| <span data-ttu-id="8e731-112">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="8e731-112">Display-Name</span></span> | <span data-ttu-id="8e731-113">Gruppen Cache für Anmeldungen aktualisieren</span><span class="sxs-lookup"><span data-stu-id="8e731-113">Refresh Group Cache for Logons</span></span>       |
| <span data-ttu-id="8e731-114">Rights-GUID</span><span class="sxs-lookup"><span data-stu-id="8e731-114">Rights-GUID</span></span>  | <span data-ttu-id="8e731-115">9432c620-033c-4db7-8b58-14ef6d0bf 477</span><span class="sxs-lookup"><span data-stu-id="8e731-115">9432c620-033c-4db7-8b58-14ef6d0bf477</span></span> |



## <a name="implementations"></a><span data-ttu-id="8e731-116">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="8e731-116">Implementations</span></span>

-   [<span data-ttu-id="8e731-117">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8e731-117">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8e731-118">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8e731-118">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8e731-119">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8e731-119">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8e731-120">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8e731-120">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8e731-121">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8e731-121">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="8e731-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8e731-122">Windows Server 2003</span></span>



| <span data-ttu-id="8e731-123">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e731-123">Entry</span></span> | <span data-ttu-id="8e731-124">Wert</span><span class="sxs-lookup"><span data-stu-id="8e731-124">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="8e731-125">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8e731-125">Applies-To</span></span>              | [<span data-ttu-id="8e731-126">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8e731-126">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="8e731-127">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="8e731-127">Localization-Display-ID</span></span> | <span data-ttu-id="8e731-128">56</span><span class="sxs-lookup"><span data-stu-id="8e731-128">56</span></span>                                       |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8e731-129">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8e731-129">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8e731-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e731-130">Entry</span></span> | <span data-ttu-id="8e731-131">Wert</span><span class="sxs-lookup"><span data-stu-id="8e731-131">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="8e731-132">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8e731-132">Applies-To</span></span>              | [<span data-ttu-id="8e731-133">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8e731-133">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="8e731-134">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="8e731-134">Localization-Display-ID</span></span> | <span data-ttu-id="8e731-135">56</span><span class="sxs-lookup"><span data-stu-id="8e731-135">56</span></span>                                       |



## <a name="windows-server-2008"></a><span data-ttu-id="8e731-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e731-136">Windows Server 2008</span></span>



| <span data-ttu-id="8e731-137">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e731-137">Entry</span></span> | <span data-ttu-id="8e731-138">Wert</span><span class="sxs-lookup"><span data-stu-id="8e731-138">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="8e731-139">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8e731-139">Applies-To</span></span>              | [<span data-ttu-id="8e731-140">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8e731-140">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="8e731-141">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="8e731-141">Localization-Display-ID</span></span> | <span data-ttu-id="8e731-142">56</span><span class="sxs-lookup"><span data-stu-id="8e731-142">56</span></span>                                       |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8e731-143">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8e731-143">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8e731-144">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e731-144">Entry</span></span> | <span data-ttu-id="8e731-145">Wert</span><span class="sxs-lookup"><span data-stu-id="8e731-145">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="8e731-146">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8e731-146">Applies-To</span></span>              | [<span data-ttu-id="8e731-147">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8e731-147">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="8e731-148">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="8e731-148">Localization-Display-ID</span></span> | <span data-ttu-id="8e731-149">56</span><span class="sxs-lookup"><span data-stu-id="8e731-149">56</span></span>                                       |



## <a name="windows-server-2012"></a><span data-ttu-id="8e731-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8e731-150">Windows Server 2012</span></span>



| <span data-ttu-id="8e731-151">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e731-151">Entry</span></span> | <span data-ttu-id="8e731-152">Wert</span><span class="sxs-lookup"><span data-stu-id="8e731-152">Value</span></span> |
|-------------------------|------------------------------------------|
| <span data-ttu-id="8e731-153">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8e731-153">Applies-To</span></span>              | [<span data-ttu-id="8e731-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8e731-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |
| <span data-ttu-id="8e731-155">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="8e731-155">Localization-Display-ID</span></span> | <span data-ttu-id="8e731-156">56</span><span class="sxs-lookup"><span data-stu-id="8e731-156">56</span></span>                                       |



 

 





