---
title: Dlldebugobjectrpchook-Funktion
description: Exportiert durch COM-DLLs zum Aktivieren des Remote Debuggens.
ms.assetid: a0f8bf12-0889-452d-84d0-255c5c143bc1
keywords:
- Dlldebugobjectrpchook-Funktion com
topic_type:
- apiref
api_name:
- DllDebugObjectRPCHook
api_location:
- ole32.dll
- API-MS-Win-Core-Com-private-l1-1-0.dll
- ComBase.dll
- API-MS-Win-Core-COM-Private-l1-1-1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62fffe6cc2d9ca650442d0a1c3fea2048fc6c84b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345932"
---
# <a name="dlldebugobjectrpchook-function"></a><span data-ttu-id="cc6c4-104">Dlldebugobjectrpchook-Funktion</span><span class="sxs-lookup"><span data-stu-id="cc6c4-104">DllDebugObjectRPCHook function</span></span>

<span data-ttu-id="cc6c4-105">Exportiert durch COM-DLLs zum Aktivieren des Remote Debuggens.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-105">Exported by COM DLLs to enable remote debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc6c4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc6c4-106">Syntax</span></span>


```C++
BOOL WINAPI DllDebugObjectRPCHook(
   BOOL             fTrace,
   LPORPC_INIT_ARGS lpOrpcInitArgs
);
```



## <a name="parameters"></a><span data-ttu-id="cc6c4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc6c4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc6c4-108">*Ablaufverfolgungs-*</span><span class="sxs-lookup"><span data-stu-id="cc6c4-108">*fTrace*</span></span> 
</dt> <dd>

<span data-ttu-id="cc6c4-109">**True** gibt an, dass Remote Debugging aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-109">If **TRUE**, remote debugging is enabled.</span></span> <span data-ttu-id="cc6c4-110">**False** gibt an, dass Remote Debugging nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-110">If **FALSE**, remote debugging is not enabled.</span></span>

</dd> <dt>

<span data-ttu-id="cc6c4-111">*lporpcinitargs*</span><span class="sxs-lookup"><span data-stu-id="cc6c4-111">*lpOrpcInitArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="cc6c4-112">Ein Zeiger auf eine [**ORPC \_ Init \_ args**](orpc-init-args.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="cc6c4-112">A pointer to an [**ORPC\_INIT\_ARGS**](orpc-init-args.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc6c4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc6c4-113">Return value</span></span>

<span data-ttu-id="cc6c4-114">**True** , wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="cc6c4-114">**TRUE** if successful, **FALSE** otherwise</span></span>

## <a name="requirements"></a><span data-ttu-id="cc6c4-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc6c4-115">Requirements</span></span>



| <span data-ttu-id="cc6c4-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc6c4-116">Requirement</span></span> | <span data-ttu-id="cc6c4-117">Wert</span><span class="sxs-lookup"><span data-stu-id="cc6c4-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cc6c4-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc6c4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cc6c4-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc6c4-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cc6c4-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc6c4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cc6c4-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc6c4-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cc6c4-122">Header</span><span class="sxs-lookup"><span data-stu-id="cc6c4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc6c4-123"><dt>N/V</dt></span><span class="sxs-lookup"><span data-stu-id="cc6c4-123"><dt>N/A</dt></span></span> </dl>       |
| <span data-ttu-id="cc6c4-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cc6c4-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="cc6c4-125"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc6c4-125"><dt>Ole32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cc6c4-126">DLL</span><span class="sxs-lookup"><span data-stu-id="cc6c4-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc6c4-127"><dt>Ole32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc6c4-127"><dt>Ole32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc6c4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc6c4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc6c4-129">**ORPC \_ dbg \_ alle**</span><span class="sxs-lookup"><span data-stu-id="cc6c4-129">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="cc6c4-130">**ORPC \_ dbg- \_ Puffer**</span><span class="sxs-lookup"><span data-stu-id="cc6c4-130">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="cc6c4-131">**ORPC-init-Argumente \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cc6c4-131">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="cc6c4-132">**Iorpcdebug-Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="cc6c4-132">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





