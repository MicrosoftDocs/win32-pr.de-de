---
title: Generieren von RSoP-Protokollierung erweitert rechts
description: Der Benutzer, der über die Rechte für eine Organisationseinheit oder Domäne verfügt, kann die Protokollierungs Modus-RSOP-Daten für die Benutzer oder Computer in der Organisationseinheit generieren.
ms.assetid: 557be624-a58d-417c-bb20-43a9baa751b5
ms.tgt_platform: multiple
keywords:
- Generieren von RSoP-AD-Schema für erweiterte Rechte Protokollierung
topic_type:
- apiref
api_name:
- Generate-RSoP-Logging
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd2798cdba03cd5ad362acb8720f75153437c28
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123109"
---
# <a name="generate-rsop-logging-extended-right"></a><span data-ttu-id="d4a77-104">Generieren von RSoP-Protokollierung erweitert rechts</span><span class="sxs-lookup"><span data-stu-id="d4a77-104">Generate-RSoP-Logging extended right</span></span>

<span data-ttu-id="d4a77-105">Der Benutzer, der über die Rechte für eine Organisationseinheit oder Domäne verfügt, kann die Protokollierungs Modus-RSOP-Daten für die Benutzer oder Computer in der Organisationseinheit generieren.</span><span class="sxs-lookup"><span data-stu-id="d4a77-105">The user who has the rights on an OU or Domain will be able to generate logging mode RSoP data for the users or computers within the OU.</span></span>



| <span data-ttu-id="d4a77-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d4a77-106">Entry</span></span> | <span data-ttu-id="d4a77-107">Wert</span><span class="sxs-lookup"><span data-stu-id="d4a77-107">Value</span></span> |
|--------------|--------------------------------------------|
| <span data-ttu-id="d4a77-108">CN</span><span class="sxs-lookup"><span data-stu-id="d4a77-108">CN</span></span>           | <span data-ttu-id="d4a77-109">Generieren von RSoP-Protokollierung</span><span class="sxs-lookup"><span data-stu-id="d4a77-109">Generate-RSoP-Logging</span></span>                      |
| <span data-ttu-id="d4a77-110">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="d4a77-110">Display-Name</span></span> | <span data-ttu-id="d4a77-111">Richtlinienergebnissatz erstellen (Protokollierung)</span><span class="sxs-lookup"><span data-stu-id="d4a77-111">Generate Resultant Set of Policy (Logging)</span></span> |
| <span data-ttu-id="d4a77-112">Rights-GUID</span><span class="sxs-lookup"><span data-stu-id="d4a77-112">Rights-GUID</span></span>  | <span data-ttu-id="d4a77-113">b7b1b3de-ab09-4242-9e30-9980e5d322f7</span><span class="sxs-lookup"><span data-stu-id="d4a77-113">b7b1b3de-ab09-4242-9e30-9980e5d322f7</span></span>       |



## <a name="implementations"></a><span data-ttu-id="d4a77-114">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="d4a77-114">Implementations</span></span>

-   [<span data-ttu-id="d4a77-115">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d4a77-115">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d4a77-116">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d4a77-116">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d4a77-117">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d4a77-117">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d4a77-118">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d4a77-118">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d4a77-119">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d4a77-119">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="d4a77-120">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d4a77-120">Windows Server 2003</span></span>



| <span data-ttu-id="d4a77-121">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d4a77-121">Entry</span></span> | <span data-ttu-id="d4a77-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d4a77-122">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a77-123">Applies-To</span><span class="sxs-lookup"><span data-stu-id="d4a77-123">Applies-To</span></span>              | [<span data-ttu-id="d4a77-124">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="d4a77-124">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="d4a77-125">**Domäne: DNS**</span><span class="sxs-lookup"><span data-stu-id="d4a77-125">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="d4a77-126">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="d4a77-126">Localization-Display-ID</span></span> | <span data-ttu-id="d4a77-127">58</span><span class="sxs-lookup"><span data-stu-id="d4a77-127">58</span></span>                                                                                                          |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d4a77-128">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d4a77-128">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d4a77-129">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d4a77-129">Entry</span></span> | <span data-ttu-id="d4a77-130">Wert</span><span class="sxs-lookup"><span data-stu-id="d4a77-130">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a77-131">Applies-To</span><span class="sxs-lookup"><span data-stu-id="d4a77-131">Applies-To</span></span>              | [<span data-ttu-id="d4a77-132">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="d4a77-132">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="d4a77-133">**Domäne: DNS**</span><span class="sxs-lookup"><span data-stu-id="d4a77-133">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="d4a77-134">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="d4a77-134">Localization-Display-ID</span></span> | <span data-ttu-id="d4a77-135">58</span><span class="sxs-lookup"><span data-stu-id="d4a77-135">58</span></span>                                                                                                          |



## <a name="windows-server-2008"></a><span data-ttu-id="d4a77-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4a77-136">Windows Server 2008</span></span>



| <span data-ttu-id="d4a77-137">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d4a77-137">Entry</span></span> | <span data-ttu-id="d4a77-138">Wert</span><span class="sxs-lookup"><span data-stu-id="d4a77-138">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a77-139">Applies-To</span><span class="sxs-lookup"><span data-stu-id="d4a77-139">Applies-To</span></span>              | [<span data-ttu-id="d4a77-140">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="d4a77-140">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="d4a77-141">**Domäne: DNS**</span><span class="sxs-lookup"><span data-stu-id="d4a77-141">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="d4a77-142">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="d4a77-142">Localization-Display-ID</span></span> | <span data-ttu-id="d4a77-143">58</span><span class="sxs-lookup"><span data-stu-id="d4a77-143">58</span></span>                                                                                                          |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d4a77-144">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d4a77-144">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d4a77-145">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d4a77-145">Entry</span></span> | <span data-ttu-id="d4a77-146">Wert</span><span class="sxs-lookup"><span data-stu-id="d4a77-146">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a77-147">Applies-To</span><span class="sxs-lookup"><span data-stu-id="d4a77-147">Applies-To</span></span>              | [<span data-ttu-id="d4a77-148">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="d4a77-148">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="d4a77-149">**Domäne: DNS**</span><span class="sxs-lookup"><span data-stu-id="d4a77-149">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="d4a77-150">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="d4a77-150">Localization-Display-ID</span></span> | <span data-ttu-id="d4a77-151">58</span><span class="sxs-lookup"><span data-stu-id="d4a77-151">58</span></span>                                                                                                          |



## <a name="windows-server-2012"></a><span data-ttu-id="d4a77-152">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d4a77-152">Windows Server 2012</span></span>



| <span data-ttu-id="d4a77-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d4a77-153">Entry</span></span> | <span data-ttu-id="d4a77-154">Wert</span><span class="sxs-lookup"><span data-stu-id="d4a77-154">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a77-155">Applies-To</span><span class="sxs-lookup"><span data-stu-id="d4a77-155">Applies-To</span></span>              | [<span data-ttu-id="d4a77-156">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="d4a77-156">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="d4a77-157">**Domäne: DNS**</span><span class="sxs-lookup"><span data-stu-id="d4a77-157">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="d4a77-158">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="d4a77-158">Localization-Display-ID</span></span> | <span data-ttu-id="d4a77-159">58</span><span class="sxs-lookup"><span data-stu-id="d4a77-159">58</span></span>                                                                                                          |



 

 





