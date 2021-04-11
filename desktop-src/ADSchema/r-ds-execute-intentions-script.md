---
title: DS-Execute-Absichten-Skript erweitert rechts
description: Steuern des Zugriffsrechts, das dem Partitions Container erteilt werden soll, sodass der Rendom.exe-oder Vorbereitungs Vorgang in einer Domänen Umbenennung verwendet werden kann.
ms.assetid: 39e9e76c-55c5-4514-ad4d-102844bcbc5a
ms.tgt_platform: multiple
keywords:
- AD-Schema "DS-Execute-Absichten-Script Extended right"
topic_type:
- apiref
api_name:
- DS-Execute-Intentions-Script
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b34765db2063688ccc8fced0a1e25cac23b98ded
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123122"
---
# <a name="ds-execute-intentions-script-extended-right"></a><span data-ttu-id="2832d-104">DS-Execute-Absichten-Skript erweitert rechts</span><span class="sxs-lookup"><span data-stu-id="2832d-104">DS-Execute-Intentions-Script extended right</span></span>

<span data-ttu-id="2832d-105">Steuern des Zugriffsrechts, das dem Partitions Container erteilt werden soll, sodass der Rendom.exe-oder Vorbereitungs Vorgang in einer Domänen Umbenennung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2832d-105">Control access right, which should be granted to the partitions container, that allows the Rendom.exe or prepare operation to be used in a domain rename.</span></span> <span data-ttu-id="2832d-106">Dieses Zugriffsrecht für das Steuerelement wird auch als nur Überwachungs Recht angezeigt, wenn der Vorgang Rendom.exe oder Schritt ausführen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2832d-106">This control access right also appears as an audit-only right when the Rendom.exe or execute step operation is performed.</span></span>



| <span data-ttu-id="2832d-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2832d-107">Entry</span></span> | <span data-ttu-id="2832d-108">Wert</span><span class="sxs-lookup"><span data-stu-id="2832d-108">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="2832d-109">CN</span><span class="sxs-lookup"><span data-stu-id="2832d-109">CN</span></span>           | <span data-ttu-id="2832d-110">DS-Execute-Absichten-Skript</span><span class="sxs-lookup"><span data-stu-id="2832d-110">DS-Execute-Intentions-Script</span></span>         |
| <span data-ttu-id="2832d-111">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="2832d-111">Display-Name</span></span> | <span data-ttu-id="2832d-112">Skript für Gesamtstruktur Update ausführen</span><span class="sxs-lookup"><span data-stu-id="2832d-112">Execute Forest Update Script</span></span>         |
| <span data-ttu-id="2832d-113">Rights-GUID</span><span class="sxs-lookup"><span data-stu-id="2832d-113">Rights-GUID</span></span>  | <span data-ttu-id="2832d-114">2b16c4a5-b98e-432c-952a-cb388ba33f 2E</span><span class="sxs-lookup"><span data-stu-id="2832d-114">2f16c4a5-b98e-432c-952a-cb388ba33f2e</span></span> |



## <a name="implementations"></a><span data-ttu-id="2832d-115">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="2832d-115">Implementations</span></span>

-   [<span data-ttu-id="2832d-116">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2832d-116">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2832d-117">**Adam**</span><span class="sxs-lookup"><span data-stu-id="2832d-117">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2832d-118">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2832d-118">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2832d-119">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2832d-119">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2832d-120">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2832d-120">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2832d-121">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2832d-121">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="2832d-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2832d-122">Windows Server 2003</span></span>



| <span data-ttu-id="2832d-123">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2832d-123">Entry</span></span> | <span data-ttu-id="2832d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2832d-124">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="2832d-125">Applies-To</span><span class="sxs-lookup"><span data-stu-id="2832d-125">Applies-To</span></span>              | [<span data-ttu-id="2832d-126">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="2832d-126">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="2832d-127">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="2832d-127">Localization-Display-ID</span></span> | <span data-ttu-id="2832d-128">66</span><span class="sxs-lookup"><span data-stu-id="2832d-128">66</span></span>                                                            |



## <a name="adam"></a><span data-ttu-id="2832d-129">Adam</span><span class="sxs-lookup"><span data-stu-id="2832d-129">ADAM</span></span>



| <span data-ttu-id="2832d-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2832d-130">Entry</span></span> | <span data-ttu-id="2832d-131">Wert</span><span class="sxs-lookup"><span data-stu-id="2832d-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="2832d-132">Applies-To</span><span class="sxs-lookup"><span data-stu-id="2832d-132">Applies-To</span></span>              | [<span data-ttu-id="2832d-133">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="2832d-133">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="2832d-134">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="2832d-134">Localization-Display-ID</span></span> | <span data-ttu-id="2832d-135">66</span><span class="sxs-lookup"><span data-stu-id="2832d-135">66</span></span>                                                            |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2832d-136">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2832d-136">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2832d-137">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2832d-137">Entry</span></span> | <span data-ttu-id="2832d-138">Wert</span><span class="sxs-lookup"><span data-stu-id="2832d-138">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="2832d-139">Applies-To</span><span class="sxs-lookup"><span data-stu-id="2832d-139">Applies-To</span></span>              | [<span data-ttu-id="2832d-140">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="2832d-140">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="2832d-141">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="2832d-141">Localization-Display-ID</span></span> | <span data-ttu-id="2832d-142">66</span><span class="sxs-lookup"><span data-stu-id="2832d-142">66</span></span>                                                            |



## <a name="windows-server-2008"></a><span data-ttu-id="2832d-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2832d-143">Windows Server 2008</span></span>



| <span data-ttu-id="2832d-144">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2832d-144">Entry</span></span> | <span data-ttu-id="2832d-145">Wert</span><span class="sxs-lookup"><span data-stu-id="2832d-145">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="2832d-146">Applies-To</span><span class="sxs-lookup"><span data-stu-id="2832d-146">Applies-To</span></span>              | [<span data-ttu-id="2832d-147">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="2832d-147">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="2832d-148">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="2832d-148">Localization-Display-ID</span></span> | <span data-ttu-id="2832d-149">66</span><span class="sxs-lookup"><span data-stu-id="2832d-149">66</span></span>                                                            |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2832d-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2832d-150">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2832d-151">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2832d-151">Entry</span></span> | <span data-ttu-id="2832d-152">Wert</span><span class="sxs-lookup"><span data-stu-id="2832d-152">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="2832d-153">Applies-To</span><span class="sxs-lookup"><span data-stu-id="2832d-153">Applies-To</span></span>              | [<span data-ttu-id="2832d-154">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="2832d-154">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="2832d-155">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="2832d-155">Localization-Display-ID</span></span> | <span data-ttu-id="2832d-156">66</span><span class="sxs-lookup"><span data-stu-id="2832d-156">66</span></span>                                                            |



## <a name="windows-server-2012"></a><span data-ttu-id="2832d-157">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2832d-157">Windows Server 2012</span></span>



| <span data-ttu-id="2832d-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2832d-158">Entry</span></span> | <span data-ttu-id="2832d-159">Wert</span><span class="sxs-lookup"><span data-stu-id="2832d-159">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="2832d-160">Applies-To</span><span class="sxs-lookup"><span data-stu-id="2832d-160">Applies-To</span></span>              | [<span data-ttu-id="2832d-161">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="2832d-161">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="2832d-162">Lokalisierung-Display-ID</span><span class="sxs-lookup"><span data-stu-id="2832d-162">Localization-Display-ID</span></span> | <span data-ttu-id="2832d-163">66</span><span class="sxs-lookup"><span data-stu-id="2832d-163">66</span></span>                                                            |



 

 





