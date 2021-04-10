---
description: Leert den Shim-Daten Bank Cache. Diese Funktion sollte nach der Installation einer neuen Shimdatenbank aufgerufen werden.
ms.assetid: 7e5bbdca-7b58-4c51-9cd1-105b05ee7fbe
title: Shimflushcache-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShimFlushCache
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 35e279c5036142ec87c5bad6d7c512388033bc94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041322"
---
# <a name="shimflushcache-function"></a><span data-ttu-id="391af-104">Shimflushcache-Funktion</span><span class="sxs-lookup"><span data-stu-id="391af-104">ShimFlushCache function</span></span>

<span data-ttu-id="391af-105">Leert den Shim-Daten Bank Cache.</span><span class="sxs-lookup"><span data-stu-id="391af-105">Flushes the shim database cache.</span></span> <span data-ttu-id="391af-106">Diese Funktion sollte nach der Installation einer neuen Shimdatenbank aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="391af-106">This function should be called after installing a new shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="391af-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="391af-107">Syntax</span></span>


```C++
BOOL WINAPI ShimFlushCache(
  _In_opt_ HWND      hwnd,
  _In_opt_ HINSTANCE hInstance,
  _In_opt_ LPCSTR    lpszCmdLine,
  _In_     int       nCmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="391af-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="391af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="391af-109">*HWND* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="391af-109">*hwnd* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="391af-110">Genutzt muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="391af-110">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="391af-111">*HINSTANCE* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="391af-111">*hInstance* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="391af-112">Genutzt muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="391af-112">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="391af-113">*lpszCmdLine* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="391af-113">*lpszCmdLine* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="391af-114">Genutzt muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="391af-114">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="391af-115">*nCmdShow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="391af-115">*nCmdShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="391af-116">Genutzt muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="391af-116">Unused; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="391af-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="391af-117">Return value</span></span>

<span data-ttu-id="391af-118">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="391af-118">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="391af-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="391af-119">Remarks</span></span>

<span data-ttu-id="391af-120">Der Aufrufer muss ein Administrator sein.</span><span class="sxs-lookup"><span data-stu-id="391af-120">The caller must be an administrator.</span></span>

## <a name="requirements"></a><span data-ttu-id="391af-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="391af-121">Requirements</span></span>



| <span data-ttu-id="391af-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="391af-122">Requirement</span></span> | <span data-ttu-id="391af-123">Wert</span><span class="sxs-lookup"><span data-stu-id="391af-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="391af-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="391af-124">Minimum supported client</span></span><br/> | <span data-ttu-id="391af-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="391af-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="391af-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="391af-126">Minimum supported server</span></span><br/> | <span data-ttu-id="391af-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="391af-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="391af-128">DLL</span><span class="sxs-lookup"><span data-stu-id="391af-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="391af-129"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="391af-129"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="391af-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="391af-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="391af-131">**Baseflushappcompatcache**</span><span class="sxs-lookup"><span data-stu-id="391af-131">**BaseFlushAppcompatCache**</span></span>](baseflushappcompatcache.md)
</dt> </dl>

 

 




