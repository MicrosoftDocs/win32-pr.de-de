---
title: Wzlistenername (WtsApi32. h)
description: Stellt den Namen einer Remotedesktopdienste Listener auf einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server dar.
ms.assetid: 3C41F507-6A67-4244-860F-E89B0F9E33B0
ms.tgt_platform: multiple
keywords:
- Wout-listenernamew
- Wout-listenernamea
- Wzlistenername
- Pwzlistenername
- Wzlistenername
- Pwzlistenername
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a82576fc9f4490b133916852441c50dcf77e849d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392059"
---
# <a name="wtslistenername"></a><span data-ttu-id="99abb-109">Wzlistenername</span><span class="sxs-lookup"><span data-stu-id="99abb-109">WTSLISTENERNAME</span></span>

<span data-ttu-id="99abb-110">Stellt den Namen einer Remotedesktopdienste Listener auf einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server dar.</span><span class="sxs-lookup"><span data-stu-id="99abb-110">Represents the name of a Remote Desktop Services listeners on a Remote Desktop Session Host (RD Session Host) server.</span></span>


```C++
typedef WCHAR WTSLISTENERNAMEW[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEW;
typedef CHAR WTSLISTENERNAMEA[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEA;
#if UNICODE
typedef WTSLISTENERNAMEW WTSLISTENERNAME;
typedef PWTSLISTENERNAMEW PWTSLISTENERNAME;
#else 
typedef WTSLISTENERNAMEA WTSLISTENERNAME;
typedef PWTSLISTENERNAMEA PWTSLISTENERNAME;
#endif 
```



<dl> <dt>

<span data-ttu-id="99abb-111">**Wout-listenernamew**</span><span class="sxs-lookup"><span data-stu-id="99abb-111">**WTSLISTENERNAMEW**</span></span>
</dt> <dd>

<span data-ttu-id="99abb-112">Der Unicode-Name des Listener.</span><span class="sxs-lookup"><span data-stu-id="99abb-112">The Unicode name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="99abb-113">**Wout-listenernamea**</span><span class="sxs-lookup"><span data-stu-id="99abb-113">**WTSLISTENERNAMEA**</span></span>
</dt> <dd>

<span data-ttu-id="99abb-114">Ein Zeiger auf den ANSI-Namen des Listener.</span><span class="sxs-lookup"><span data-stu-id="99abb-114">A pointer to the ANSI name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="99abb-115">**Wzlistenername**</span><span class="sxs-lookup"><span data-stu-id="99abb-115">**WTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="99abb-116">Der Name des Listeners.</span><span class="sxs-lookup"><span data-stu-id="99abb-116">The name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="99abb-117">**Pwzlistenername**</span><span class="sxs-lookup"><span data-stu-id="99abb-117">**PWTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="99abb-118">Ein Zeiger auf den Namen des Listener.</span><span class="sxs-lookup"><span data-stu-id="99abb-118">A pointer to the name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="99abb-119">**Wzlistenername**</span><span class="sxs-lookup"><span data-stu-id="99abb-119">**WTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="99abb-120">Der Name des Listeners.</span><span class="sxs-lookup"><span data-stu-id="99abb-120">The name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="99abb-121">**Pwzlistenername**</span><span class="sxs-lookup"><span data-stu-id="99abb-121">**PWTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="99abb-122">Ein Zeiger auf den Namen des Listener.</span><span class="sxs-lookup"><span data-stu-id="99abb-122">A pointer to the name of the listener.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99abb-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99abb-123">Requirements</span></span>



| <span data-ttu-id="99abb-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99abb-124">Requirement</span></span> | <span data-ttu-id="99abb-125">Wert</span><span class="sxs-lookup"><span data-stu-id="99abb-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99abb-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99abb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="99abb-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99abb-127">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="99abb-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99abb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="99abb-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99abb-129">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="99abb-130">Header</span><span class="sxs-lookup"><span data-stu-id="99abb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="99abb-131"><dt>WtsApi32. h</dt></span><span class="sxs-lookup"><span data-stu-id="99abb-131"><dt>WtsApi32.h</dt></span></span> </dl> |



 

 





