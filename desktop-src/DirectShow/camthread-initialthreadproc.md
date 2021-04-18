---
description: Die initialthread proc-Methode ruft die Hauptthread Prozedur auf.
ms.assetid: 1546c214-7ea9-4484-974b-dbd4b2b3e296
title: CAMThread.Initialthread proc-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd7fd0aa12d0659776db7e39fb223095762fc209
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360936"
---
# <a name="camthreadinitialthreadproc-method"></a><span data-ttu-id="207b4-103">CAMThread.Initialthread proc-Methode</span><span class="sxs-lookup"><span data-stu-id="207b4-103">CAMThread.InitialThreadProc method</span></span>

<span data-ttu-id="207b4-104">Die- `InitialThreadProc` Methode ruft die Hauptthread Prozedur auf.</span><span class="sxs-lookup"><span data-stu-id="207b4-104">The `InitialThreadProc` method calls the main thread procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="207b4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="207b4-105">Syntax</span></span>


```C++
DWORD InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a><span data-ttu-id="207b4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="207b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="207b4-107">*teuren*</span><span class="sxs-lookup"><span data-stu-id="207b4-107">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="207b4-108">`this` Zeichner.</span><span class="sxs-lookup"><span data-stu-id="207b4-108">`this` pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="207b4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="207b4-109">Return value</span></span>

<span data-ttu-id="207b4-110">Gibt das von " [**camthread:: ThreadProc**](camthread-threadproc.md)" zurückgegebene **DWORD** zurück.</span><span class="sxs-lookup"><span data-stu-id="207b4-110">Returns the **DWORD** returned by [**CAMThread::ThreadProc**](camthread-threadproc.md).</span></span> <span data-ttu-id="207b4-111">Diese Werte werden von der abgeleiteten Klasse definiert.</span><span class="sxs-lookup"><span data-stu-id="207b4-111">The derived class defines this value.</span></span>

## <a name="remarks"></a><span data-ttu-id="207b4-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="207b4-112">Remarks</span></span>

<span data-ttu-id="207b4-113">Die Methode " [**camthread:: Create**](camthread-create.md) " verwendet diese Methode für die Thread Prozedur, wenn der Thread erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="207b4-113">The [**CAMThread::Create**](camthread-create.md) method uses this method for the thread procedure when it creates the thread.</span></span> <span data-ttu-id="207b4-114">Der Zeiger wird `this` als Thread Argument verwendet.</span><span class="sxs-lookup"><span data-stu-id="207b4-114">It uses the `this` pointer as the thread argument.</span></span>

<span data-ttu-id="207b4-115">Diese Methode ruft die Methode [**camthread:: coinitializehelper**](camthread-coinitializehelper.md) und dann ThreadProc auf.</span><span class="sxs-lookup"><span data-stu-id="207b4-115">This method calls the [**CAMThread::CoInitializeHelper**](camthread-coinitializehelper.md) method and then ThreadProc.</span></span>

## <a name="requirements"></a><span data-ttu-id="207b4-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="207b4-116">Requirements</span></span>



| <span data-ttu-id="207b4-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="207b4-117">Requirement</span></span> | <span data-ttu-id="207b4-118">Wert</span><span class="sxs-lookup"><span data-stu-id="207b4-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="207b4-119">Header</span><span class="sxs-lookup"><span data-stu-id="207b4-119">Header</span></span><br/>  | <dl> <span data-ttu-id="207b4-120"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="207b4-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="207b4-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="207b4-121">Library</span></span><br/> | <dl> <span data-ttu-id="207b4-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="207b4-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="207b4-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="207b4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="207b4-124">**Camthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="207b4-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




