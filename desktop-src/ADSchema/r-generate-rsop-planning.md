---
title: Generieren von RSoP-Planen von erweiterten Rechten
description: Der Benutzer, der über die Rechte für eine Organisationseinheit oder Domäne verfügt, kann die RSoP-Daten des Planungsmodus für die Benutzer oder Computer in der Organisationseinheit generieren.
ms.assetid: 4a874e47-c88b-4945-912b-7d4a2dd799df
ms.tgt_platform: multiple
keywords:
- Generieren von RSoP-Planen des AD-Schemas für erweiterte Rechte
topic_type:
- apiref
api_name:
- Generate-RSoP-Planning
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f20b7d3a6431dcc19e83f95c594fd0332e35eb2b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106345568"
---
# <a name="generate-rsop-planning-extended-right"></a><span data-ttu-id="b983a-104">Generieren von RSoP-Planen von erweiterten Rechten</span><span class="sxs-lookup"><span data-stu-id="b983a-104">Generate-RSoP-Planning extended right</span></span>

<span data-ttu-id="b983a-105">Der Benutzer, der über die Rechte für eine Organisationseinheit oder Domäne verfügt, kann die RSoP-Daten des Planungsmodus für die Benutzer oder Computer in der Organisationseinheit generieren.</span><span class="sxs-lookup"><span data-stu-id="b983a-105">The user who has the rights on an OU or Domain will be able to generate planning mode RSoP data for the users or computers within the OU.</span></span>



| <span data-ttu-id="b983a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b983a-106">Entry</span></span> | <span data-ttu-id="b983a-107">Wert</span><span class="sxs-lookup"><span data-stu-id="b983a-107">Value</span></span> |
|--------------|---------------------------------------------|
| <span data-ttu-id="b983a-108">CN</span><span class="sxs-lookup"><span data-stu-id="b983a-108">CN</span></span>           | <span data-ttu-id="b983a-109">Generieren von RSoP-Planning</span><span class="sxs-lookup"><span data-stu-id="b983a-109">Generate-RSoP-Planning</span></span>                      |
| <span data-ttu-id="b983a-110">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="b983a-110">Display-Name</span></span> | <span data-ttu-id="b983a-111">Richtlinienergebnissatz erstellen (Planung)</span><span class="sxs-lookup"><span data-stu-id="b983a-111">Generate Resultant Set of Policy (Planning)</span></span> |
| <span data-ttu-id="b983a-112">Rights-GUID</span><span class="sxs-lookup"><span data-stu-id="b983a-112">Rights-GUID</span></span>  | <span data-ttu-id="b983a-113">b7b1b3dd-ab09-4242-9e30-9980e5d322f7</span><span class="sxs-lookup"><span data-stu-id="b983a-113">b7b1b3dd-ab09-4242-9e30-9980e5d322f7</span></span>        |



## <a name="implementations"></a><span data-ttu-id="b983a-114">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="b983a-114">Implementations</span></span>

-   [<span data-ttu-id="b983a-115">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b983a-115">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b983a-116">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b983a-116">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b983a-117">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b983a-117">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b983a-118">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b983a-118">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b983a-119">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b983a-119">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b983a-120">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b983a-120">Windows Server 2003</span></span>



| <span data-ttu-id="b983a-121">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b983a-121">Entry</span></span> | <span data-ttu-id="b983a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b983a-122">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b983a-123">Applies-To</span><span class="sxs-lookup"><span data-stu-id="b983a-123">Applies-To</span></span>              | [<span data-ttu-id="b983a-124">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="b983a-124">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="b983a-125">**Domäne: DNS**</span><span class="sxs-lookup"><span data-stu-id="b983a-125">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="b983a-126">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="b983a-126">Localization-Display-ID</span></span> | <span data-ttu-id="b983a-127">55</span><span class="sxs-lookup"><span data-stu-id="b983a-127">55</span></span>                                                                                                          |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b983a-128">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b983a-128">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b983a-129">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b983a-129">Entry</span></span> | <span data-ttu-id="b983a-130">Wert</span><span class="sxs-lookup"><span data-stu-id="b983a-130">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b983a-131">Applies-To</span><span class="sxs-lookup"><span data-stu-id="b983a-131">Applies-To</span></span>              | [<span data-ttu-id="b983a-132">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="b983a-132">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="b983a-133">**Domäne: DNS**</span><span class="sxs-lookup"><span data-stu-id="b983a-133">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="b983a-134">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="b983a-134">Localization-Display-ID</span></span> | <span data-ttu-id="b983a-135">55</span><span class="sxs-lookup"><span data-stu-id="b983a-135">55</span></span>                                                                                                          |



## <a name="windows-server-2008"></a><span data-ttu-id="b983a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b983a-136">Windows Server 2008</span></span>



| <span data-ttu-id="b983a-137">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b983a-137">Entry</span></span> | <span data-ttu-id="b983a-138">Wert</span><span class="sxs-lookup"><span data-stu-id="b983a-138">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b983a-139">Applies-To</span><span class="sxs-lookup"><span data-stu-id="b983a-139">Applies-To</span></span>              | [<span data-ttu-id="b983a-140">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="b983a-140">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="b983a-141">**Domäne: DNS**</span><span class="sxs-lookup"><span data-stu-id="b983a-141">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="b983a-142">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="b983a-142">Localization-Display-ID</span></span> | <span data-ttu-id="b983a-143">55</span><span class="sxs-lookup"><span data-stu-id="b983a-143">55</span></span>                                                                                                          |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b983a-144">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b983a-144">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b983a-145">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b983a-145">Entry</span></span> | <span data-ttu-id="b983a-146">Wert</span><span class="sxs-lookup"><span data-stu-id="b983a-146">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b983a-147">Applies-To</span><span class="sxs-lookup"><span data-stu-id="b983a-147">Applies-To</span></span>              | [<span data-ttu-id="b983a-148">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="b983a-148">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="b983a-149">**Domäne: DNS**</span><span class="sxs-lookup"><span data-stu-id="b983a-149">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="b983a-150">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="b983a-150">Localization-Display-ID</span></span> | <span data-ttu-id="b983a-151">55</span><span class="sxs-lookup"><span data-stu-id="b983a-151">55</span></span>                                                                                                          |



## <a name="windows-server-2012"></a><span data-ttu-id="b983a-152">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b983a-152">Windows Server 2012</span></span>



| <span data-ttu-id="b983a-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b983a-153">Entry</span></span> | <span data-ttu-id="b983a-154">Wert</span><span class="sxs-lookup"><span data-stu-id="b983a-154">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b983a-155">Applies-To</span><span class="sxs-lookup"><span data-stu-id="b983a-155">Applies-To</span></span>              | [<span data-ttu-id="b983a-156">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="b983a-156">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="b983a-157">**Domäne: DNS**</span><span class="sxs-lookup"><span data-stu-id="b983a-157">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="b983a-158">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="b983a-158">Localization-Display-ID</span></span> | <span data-ttu-id="b983a-159">55</span><span class="sxs-lookup"><span data-stu-id="b983a-159">55</span></span>                                                                                                          |



 

 





