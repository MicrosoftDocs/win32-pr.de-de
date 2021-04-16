---
title: Ibackgroundcopyjob-Methoden (Bits)
description: Die ibackgroundcopyjob-Schnittstelle stellt die folgenden Methoden zur Verfügung. | Ibackgroundcopyjob-Methoden (Bits)
ms.assetid: CB1C6D64-416A-4F31-AC9D-B3C1A6818034
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a7ebeeefa90c90435f1294d78c4816cf77be3c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530626"
---
# <a name="ibackgroundcopyjob-methods-bits"></a><span data-ttu-id="03207-104">Ibackgroundcopyjob-Methoden (Bits)</span><span class="sxs-lookup"><span data-stu-id="03207-104">IBackgroundCopyJob Methods (BITS)</span></span>

<span data-ttu-id="03207-105">Die [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstelle stellt die folgenden Methoden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="03207-105">The [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="03207-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="03207-106">In this section</span></span>

-   [<span data-ttu-id="03207-107">**AddFile-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-107">**AddFile Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)
-   [<span data-ttu-id="03207-108">**ADDFILESET-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-108">**AddFileSet Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)
-   [<span data-ttu-id="03207-109">**Cancel-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-109">**Cancel Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel)
-   [<span data-ttu-id="03207-110">**Complete-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-110">**Complete Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)
-   [<span data-ttu-id="03207-111">**EnumFiles-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-111">**EnumFiles Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles)
-   [<span data-ttu-id="03207-112">**GetDescription-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-112">**GetDescription Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getdescription)
-   [<span data-ttu-id="03207-113">**GetDisplayName-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-113">**GetDisplayName Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getdisplayname)
-   [<span data-ttu-id="03207-114">**GetError-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-114">**GetError Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror)
-   [<span data-ttu-id="03207-115">**GetErrorCount-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-115">**GetErrorCount Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterrorcount)
-   [<span data-ttu-id="03207-116">**GetId-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-116">**GetId Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getid)
-   [<span data-ttu-id="03207-117">**Getminimumretrydelay-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-117">**GetMinimumRetryDelay Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getminimumretrydelay)
-   [<span data-ttu-id="03207-118">**Getnoprogresstimeout-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-118">**GetNoProgressTimeout Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnoprogresstimeout)
-   [<span data-ttu-id="03207-119">**Getnotifyflags-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-119">**GetNotifyFlags Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnotifyflags)
-   [<span data-ttu-id="03207-120">**Getnotifyinterface-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-120">**GetNotifyInterface Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnotifyinterface)
-   [<span data-ttu-id="03207-121">**GetOwner-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-121">**GetOwner Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getowner)
-   [<span data-ttu-id="03207-122">**GetPriority-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-122">**GetPriority Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getpriority)
-   [<span data-ttu-id="03207-123">**GetProgress-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-123">**GetProgress Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress)
-   [<span data-ttu-id="03207-124">**Getproxysettings-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-124">**GetProxySettings Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getproxysettings)
-   [<span data-ttu-id="03207-125">**GetState-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-125">**GetState Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate)
-   [<span data-ttu-id="03207-126">**Gettimes-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-126">**GetTimes Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-gettimes)
-   [<span data-ttu-id="03207-127">**GetType-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-127">**GetType Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-gettype)
-   [<span data-ttu-id="03207-128">**Resume-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-128">**Resume Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
-   [<span data-ttu-id="03207-129">**SetDescription-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-129">**SetDescription Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setdescription)
-   [<span data-ttu-id="03207-130">**Setdisplayname-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-130">**SetDisplayName Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setdisplayname)
-   [<span data-ttu-id="03207-131">**Setminimumretrydelay-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-131">**SetMinimumRetryDelay Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay)
-   [<span data-ttu-id="03207-132">**Setnoprogresstimeout-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-132">**SetNoProgressTimeout Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout)
-   [<span data-ttu-id="03207-133">**Setnotifyflags-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-133">**SetNotifyFlags Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)
-   [<span data-ttu-id="03207-134">**Setnotifyinterface-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-134">**SetNotifyInterface Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface)
-   [<span data-ttu-id="03207-135">**SetPriority-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-135">**SetPriority Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setpriority)
-   [<span data-ttu-id="03207-136">**Setproxysettings-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-136">**SetProxySettings Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings)
-   [<span data-ttu-id="03207-137">**Suspend-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-137">**Suspend Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-suspend)
-   [<span data-ttu-id="03207-138">**TakeOwnership-Methode**</span><span class="sxs-lookup"><span data-stu-id="03207-138">**TakeOwnership Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership)

 

 




