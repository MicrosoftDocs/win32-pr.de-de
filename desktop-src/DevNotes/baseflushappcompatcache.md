---
description: Leert den Anwendungskompatibilitäts-Cache.
ms.assetid: 03f47813-87f6-4b71-b453-77a2facab019
title: Baseflushappcompatcache-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BaseFlushAppcompatCache
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-appcompat-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-appcompat-l1-1-1.dll
ms.openlocfilehash: 6118c78784bb96b9f25e008cd2221112eeb646f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126212"
---
# <a name="baseflushappcompatcache-function"></a><span data-ttu-id="d8469-103">Baseflushappcompatcache-Funktion</span><span class="sxs-lookup"><span data-stu-id="d8469-103">BaseFlushAppcompatCache function</span></span>

<span data-ttu-id="d8469-104">Leert den Anwendungskompatibilitäts-Cache.</span><span class="sxs-lookup"><span data-stu-id="d8469-104">Flushes the application compatibility cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8469-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8469-105">Syntax</span></span>


```C++
BOOL WINAPI BaseFlushAppcompatCache(void);
```



## <a name="parameters"></a><span data-ttu-id="d8469-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8469-106">Parameters</span></span>

<span data-ttu-id="d8469-107">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d8469-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d8469-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d8469-108">Return value</span></span>

<span data-ttu-id="d8469-109">Die Funktion gibt **true** zurück, wenn Sie erfolgreich ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="d8469-109">The function returns **TRUE** if it succeeds and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8469-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8469-110">Remarks</span></span>

<span data-ttu-id="d8469-111">Der Aufrufer muss ein Administrator sein.</span><span class="sxs-lookup"><span data-stu-id="d8469-111">The caller must be an administrator.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8469-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8469-112">Requirements</span></span>



| <span data-ttu-id="d8469-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8469-113">Requirement</span></span> | <span data-ttu-id="d8469-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d8469-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8469-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8469-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d8469-116">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8469-116">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d8469-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8469-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d8469-118">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8469-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d8469-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d8469-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8469-120"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8469-120"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8469-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8469-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8469-122">**Shimflushcache**</span><span class="sxs-lookup"><span data-stu-id="d8469-122">**ShimFlushCache**</span></span>](shimflushcache.md)
</dt> </dl>

 

 




