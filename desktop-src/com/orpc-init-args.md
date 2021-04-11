---
title: ORPC_INIT_ARGS Struktur
description: Die ORPC \_ Init \_ args-Struktur enthält Informationen, die zum Initialisieren des Remote Debuggens mithilfe der iorpcdebugnotify-Schnittstelle verwendet werden.
ms.assetid: be7646c7-3394-45ae-ae8f-9cee68bbc789
keywords:
- COM für ORPC_INIT_ARGS Struktur
- LPORPC_INIT_ARGS Struktur Zeiger com
topic_type:
- apiref
api_name:
- ORPC_INIT_ARGS
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e7dca0209f745d5034bde2da852829b99d7dcb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103255"
---
# <a name="orpc_init_args-structure"></a><span data-ttu-id="c3714-105">ORPC \_ Init \_ args-Struktur</span><span class="sxs-lookup"><span data-stu-id="c3714-105">ORPC\_INIT\_ARGS structure</span></span>

<span data-ttu-id="c3714-106">Die **ORPC \_ Init \_ args** -Struktur enthält Informationen, die zum Initialisieren des Remote Debuggens mithilfe der [**iorpcdebugnotify**](iorpcdebugnotify.md) -Schnittstelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3714-106">The **ORPC\_INIT\_ARGS** structure contains information used to initialize remote debugging using the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3714-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3714-107">Syntax</span></span>


```C++
typedef struct ORPC_INIT_ARGS {
  IOrpcDebugNotify *lpIntfOrpcDebug;
  void             *pvPSN;
  DWORD            *dwReserved1;
  DWORD            *dwReserved2;
} ORPC_INIT_ARGS, *LPORPC_INIT_ARGS;
```



## <a name="members"></a><span data-ttu-id="c3714-108">Member</span><span class="sxs-lookup"><span data-stu-id="c3714-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c3714-109">**lpintforpcdebug**</span><span class="sxs-lookup"><span data-stu-id="c3714-109">**lpIntfOrpcDebug**</span></span>
</dt> <dd>

<span data-ttu-id="c3714-110">Ein Zeiger auf die [**iorpcdebugnotify**](iorpcdebugnotify.md) -Schnittstelle, die von in-Process-Debuggern verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3714-110">A pointer to the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface for use by in-process debuggers.</span></span> <span data-ttu-id="c3714-111">Wenn der Debugger nicht in-Process oder ein Macintosh-System ist, muss dieses Feld **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c3714-111">If the debugger is not in-process or is a Macintosh system, this field must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c3714-112">**pvpsn**</span><span class="sxs-lookup"><span data-stu-id="c3714-112">**pvPSN**</span></span>
</dt> <dd>

<span data-ttu-id="c3714-113">Ein Zeiger auf die Macintosh-Prozess Seriennummer des zu debuggenden Prozesses.</span><span class="sxs-lookup"><span data-stu-id="c3714-113">A pointer to the Macintosh process serial number of the debuggee's process.</span></span> <span data-ttu-id="c3714-114">Wenn die zu debuggende Komponente kein Macintosh-System ist, muss dieses Feld **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c3714-114">If the debuggee is not a Macintosh system, this field must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c3714-115">**dwReserved1**</span><span class="sxs-lookup"><span data-stu-id="c3714-115">**dwReserved1**</span></span>
</dt> <dd>

<span data-ttu-id="c3714-116">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="c3714-116">Reserved.</span></span> <span data-ttu-id="c3714-117">Muss den Wert 0 (null) haben.</span><span class="sxs-lookup"><span data-stu-id="c3714-117">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="c3714-118">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="c3714-118">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="c3714-119">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="c3714-119">Reserved.</span></span> <span data-ttu-id="c3714-120">Muss den Wert 0 (null) haben.</span><span class="sxs-lookup"><span data-stu-id="c3714-120">Must be 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3714-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3714-121">Requirements</span></span>



| <span data-ttu-id="c3714-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3714-122">Requirement</span></span> | <span data-ttu-id="c3714-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c3714-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="c3714-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3714-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c3714-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3714-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="c3714-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3714-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c3714-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3714-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c3714-128">Header</span><span class="sxs-lookup"><span data-stu-id="c3714-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3714-129"><dt>N/V</dt></span><span class="sxs-lookup"><span data-stu-id="c3714-129"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3714-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3714-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3714-131">**ORPC \_ dbg \_ alle**</span><span class="sxs-lookup"><span data-stu-id="c3714-131">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="c3714-132">**ORPC \_ dbg- \_ Puffer**</span><span class="sxs-lookup"><span data-stu-id="c3714-132">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="c3714-133">**Dlldebugobjectrpchook**</span><span class="sxs-lookup"><span data-stu-id="c3714-133">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="c3714-134">**Iorpcdebug-Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="c3714-134">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





