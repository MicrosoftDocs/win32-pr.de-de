---
title: Bindungs handle-Funktionen
description: Die folgende Tabelle enthält die Liste der RPC-Lauf Zeit Routinen, die für Bindungs Handles verwendet werden, und gibt den Typ des zulässigen Bindungs Handles an.
ms.assetid: 16effe59-ebe2-48c3-b97a-90656b6d3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e00b3cbb2d5fc5637b9414d6f009cfb2e4ade4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339188"
---
# <a name="binding-handle-functions"></a><span data-ttu-id="2baa3-103">Bindungs handle-Funktionen</span><span class="sxs-lookup"><span data-stu-id="2baa3-103">Binding Handle Functions</span></span>

<span data-ttu-id="2baa3-104">Die folgende Tabelle enthält die Liste der RPC-Lauf Zeit Routinen, die für Bindungs Handles verwendet werden, und gibt den Typ des zulässigen Bindungs Handles an.</span><span class="sxs-lookup"><span data-stu-id="2baa3-104">The following table contains the list of RPC run-time routines that operate on binding handles and specifies the type of binding handle allowed.</span></span>



| <span data-ttu-id="2baa3-105">-Routine zurückgegebener Wert</span><span class="sxs-lookup"><span data-stu-id="2baa3-105">Routine</span></span>                                                            | <span data-ttu-id="2baa3-106">Eingabe Argument</span><span class="sxs-lookup"><span data-stu-id="2baa3-106">Input argument</span></span>   | <span data-ttu-id="2baa3-107">Ausgabe Argument</span><span class="sxs-lookup"><span data-stu-id="2baa3-107">Output argument</span></span> |
|--------------------------------------------------------------------|------------------|-----------------|
| [<span data-ttu-id="2baa3-108">**Rpcbindingcopy**</span><span class="sxs-lookup"><span data-stu-id="2baa3-108">**RpcBindingCopy**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy)                           | <span data-ttu-id="2baa3-109">Server</span><span class="sxs-lookup"><span data-stu-id="2baa3-109">Server</span></span>           | <span data-ttu-id="2baa3-110">Server</span><span class="sxs-lookup"><span data-stu-id="2baa3-110">Server</span></span>          |
| [<span data-ttu-id="2baa3-111">**Rpcbindingfree**</span><span class="sxs-lookup"><span data-stu-id="2baa3-111">**RpcBindingFree**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)                           | <span data-ttu-id="2baa3-112">Server</span><span class="sxs-lookup"><span data-stu-id="2baa3-112">Server</span></span>           | <span data-ttu-id="2baa3-113">Keine</span><span class="sxs-lookup"><span data-stu-id="2baa3-113">None</span></span>            |
| [<span data-ttu-id="2baa3-114">**RpcBindingFromStringBinding**</span><span class="sxs-lookup"><span data-stu-id="2baa3-114">**RpcBindingFromStringBinding**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) | <span data-ttu-id="2baa3-115">Keine</span><span class="sxs-lookup"><span data-stu-id="2baa3-115">None</span></span>             | <span data-ttu-id="2baa3-116">Server</span><span class="sxs-lookup"><span data-stu-id="2baa3-116">Server</span></span>          |
| [<span data-ttu-id="2baa3-117">**Rpcbindinginqauthclient**</span><span class="sxs-lookup"><span data-stu-id="2baa3-117">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)         | <span data-ttu-id="2baa3-118">Client</span><span class="sxs-lookup"><span data-stu-id="2baa3-118">Client</span></span>           | <span data-ttu-id="2baa3-119">Keine</span><span class="sxs-lookup"><span data-stu-id="2baa3-119">None</span></span>            |
| [<span data-ttu-id="2baa3-120">**Rpcbindinginqauthinfo**</span><span class="sxs-lookup"><span data-stu-id="2baa3-120">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)             | <span data-ttu-id="2baa3-121">Server</span><span class="sxs-lookup"><span data-stu-id="2baa3-121">Server</span></span>           | <span data-ttu-id="2baa3-122">Keine</span><span class="sxs-lookup"><span data-stu-id="2baa3-122">None</span></span>            |
| [<span data-ttu-id="2baa3-123">**Rpcbindinginqobject**</span><span class="sxs-lookup"><span data-stu-id="2baa3-123">**RpcBindingInqObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqobject)                 | <span data-ttu-id="2baa3-124">Server oder Client</span><span class="sxs-lookup"><span data-stu-id="2baa3-124">Server or client</span></span> | <span data-ttu-id="2baa3-125">Keine</span><span class="sxs-lookup"><span data-stu-id="2baa3-125">None</span></span>            |
| [<span data-ttu-id="2baa3-126">**Rpcbindingreset**</span><span class="sxs-lookup"><span data-stu-id="2baa3-126">**RpcBindingReset**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)                         | <span data-ttu-id="2baa3-127">Server</span><span class="sxs-lookup"><span data-stu-id="2baa3-127">Server</span></span>           | <span data-ttu-id="2baa3-128">Keine</span><span class="sxs-lookup"><span data-stu-id="2baa3-128">None</span></span>            |
| [<span data-ttu-id="2baa3-129">**Rpcbindingsetauthinfo**</span><span class="sxs-lookup"><span data-stu-id="2baa3-129">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)             | <span data-ttu-id="2baa3-130">Server</span><span class="sxs-lookup"><span data-stu-id="2baa3-130">Server</span></span>           | <span data-ttu-id="2baa3-131">Keine</span><span class="sxs-lookup"><span data-stu-id="2baa3-131">None</span></span>            |
| [<span data-ttu-id="2baa3-132">**Rpcbindingsetobject**</span><span class="sxs-lookup"><span data-stu-id="2baa3-132">**RpcBindingSetObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)                 | <span data-ttu-id="2baa3-133">Server</span><span class="sxs-lookup"><span data-stu-id="2baa3-133">Server</span></span>           | <span data-ttu-id="2baa3-134">Keine</span><span class="sxs-lookup"><span data-stu-id="2baa3-134">None</span></span>            |
| [<span data-ttu-id="2baa3-135">**Rpcbindingtostringbinding**</span><span class="sxs-lookup"><span data-stu-id="2baa3-135">**RpcBindingToStringBinding**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)     | <span data-ttu-id="2baa3-136">Server oder Client</span><span class="sxs-lookup"><span data-stu-id="2baa3-136">Server or client</span></span> | <span data-ttu-id="2baa3-137">Keine</span><span class="sxs-lookup"><span data-stu-id="2baa3-137">None</span></span>            |
| [<span data-ttu-id="2baa3-138">**Rpcbindingvector Free**</span><span class="sxs-lookup"><span data-stu-id="2baa3-138">**RpcBindingVectorFree**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)               | <span data-ttu-id="2baa3-139">Server</span><span class="sxs-lookup"><span data-stu-id="2baa3-139">Server</span></span>           | <span data-ttu-id="2baa3-140">Keine</span><span class="sxs-lookup"><span data-stu-id="2baa3-140">None</span></span>            |
| [<span data-ttu-id="2baa3-141">**Rpcnsbindingexport**</span><span class="sxs-lookup"><span data-stu-id="2baa3-141">**RpcNsBindingExport**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)                   | <span data-ttu-id="2baa3-142">Server</span><span class="sxs-lookup"><span data-stu-id="2baa3-142">Server</span></span>           | <span data-ttu-id="2baa3-143">Keine</span><span class="sxs-lookup"><span data-stu-id="2baa3-143">None</span></span>            |
| [<span data-ttu-id="2baa3-144">**Rpcnsbindingimportnext**</span><span class="sxs-lookup"><span data-stu-id="2baa3-144">**RpcNsBindingImportNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)           | <span data-ttu-id="2baa3-145">Keine</span><span class="sxs-lookup"><span data-stu-id="2baa3-145">None</span></span>             | <span data-ttu-id="2baa3-146">Server</span><span class="sxs-lookup"><span data-stu-id="2baa3-146">Server</span></span>          |
| [<span data-ttu-id="2baa3-147">**Rpcnsbindinglookupnext**</span><span class="sxs-lookup"><span data-stu-id="2baa3-147">**RpcNsBindingLookupNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)           | <span data-ttu-id="2baa3-148">Keine</span><span class="sxs-lookup"><span data-stu-id="2baa3-148">None</span></span>             | <span data-ttu-id="2baa3-149">Server</span><span class="sxs-lookup"><span data-stu-id="2baa3-149">Server</span></span>          |
| [<span data-ttu-id="2baa3-150">**Rpcnsbindingselect**</span><span class="sxs-lookup"><span data-stu-id="2baa3-150">**RpcNsBindingSelect**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingselect)                   | <span data-ttu-id="2baa3-151">Server</span><span class="sxs-lookup"><span data-stu-id="2baa3-151">Server</span></span>           | <span data-ttu-id="2baa3-152">Server</span><span class="sxs-lookup"><span data-stu-id="2baa3-152">Server</span></span>          |
| [<span data-ttu-id="2baa3-153">**Rpcserverinqbindungen**</span><span class="sxs-lookup"><span data-stu-id="2baa3-153">**RpcServerInqBindings**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings)               | <span data-ttu-id="2baa3-154">Keine</span><span class="sxs-lookup"><span data-stu-id="2baa3-154">None</span></span>             | <span data-ttu-id="2baa3-155">Server</span><span class="sxs-lookup"><span data-stu-id="2baa3-155">Server</span></span>          |



 

 

 




