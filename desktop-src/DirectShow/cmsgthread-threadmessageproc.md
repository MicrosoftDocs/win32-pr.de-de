---
description: Verarbeitet Anforderungen. Dies ist eine reine virtuelle Member-Funktion.
ms.assetid: ffdbc287-ca17-44e4-b00a-d72a2367f510
title: Cmsgthread. threadmessageproc-Methode (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ThreadMessageProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf47eb63a6f9d8fe4921985bb64567de6678b44c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368640"
---
# <a name="cmsgthreadthreadmessageproc-method"></a><span data-ttu-id="a3f4e-104">Cmsgthread. threadmessageproc-Methode</span><span class="sxs-lookup"><span data-stu-id="a3f4e-104">CMsgThread.ThreadMessageProc method</span></span>

<span data-ttu-id="a3f4e-105">Verarbeitet Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="a3f4e-105">Processes requests.</span></span> <span data-ttu-id="a3f4e-106">Dies ist eine reine virtuelle Member-Funktion.</span><span class="sxs-lookup"><span data-stu-id="a3f4e-106">This is a pure virtual member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3f4e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3f4e-107">Syntax</span></span>


```C++
virtual LRESULT ThreadMessageProc(
   UINT     uMsg,
   DWORD    dwFlags,
   LPVOID   lpParam,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a><span data-ttu-id="a3f4e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3f4e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3f4e-109">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="a3f4e-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="a3f4e-110">Anforderungs Code.</span><span class="sxs-lookup"><span data-stu-id="a3f4e-110">Request code.</span></span>

</dd> <dt>

<span data-ttu-id="a3f4e-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="a3f4e-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="a3f4e-112">Optionaler Flag-Parameter für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a3f4e-112">Optional flag parameter to request.</span></span>

</dd> <dt>

<span data-ttu-id="a3f4e-113">*lpparam*</span><span class="sxs-lookup"><span data-stu-id="a3f4e-113">*lpParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3f4e-114">Optionaler Zeiger auf zusätzliche Daten oder einen Rückgabe Datenblock.</span><span class="sxs-lookup"><span data-stu-id="a3f4e-114">Optional pointer to extra data or a return data block.</span></span>

</dd> <dt>

<span data-ttu-id="a3f4e-115">*Peer Event*</span><span class="sxs-lookup"><span data-stu-id="a3f4e-115">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="a3f4e-116">Optionaler Zeiger auf ein Ereignis Objekt.</span><span class="sxs-lookup"><span data-stu-id="a3f4e-116">Optional pointer to an event object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3f4e-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3f4e-117">Return value</span></span>

<span data-ttu-id="a3f4e-118">Eine Rückgabe ungleich NULL bewirkt, dass der Thread beendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3f4e-118">Any nonzero return causes the thread to exit.</span></span> <span data-ttu-id="a3f4e-119">Gibt NULL zurück, es sei denn, eine Beendigungs Anforderung wurde kürzlich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a3f4e-119">Returns zero unless an exit request has been processed recently.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3f4e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3f4e-120">Remarks</span></span>

<span data-ttu-id="a3f4e-121">Diese reine virtuelle Funktion muss in der abgeleiteten Klasse überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a3f4e-121">This pure virtual function must be overridden in your derived class.</span></span> <span data-ttu-id="a3f4e-122">Sie wird einmal für jede Anforderung aufgerufen, die durch einen Aufruf der [**cmsgthread::P utthreadmsg**](cmsgthread-putthreadmsg.md) -Member-Funktion in der Warteschlange eingereiht wird.</span><span class="sxs-lookup"><span data-stu-id="a3f4e-122">It will be called once for each request queued by a call to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function.</span></span>

<span data-ttu-id="a3f4e-123">Die Member-Funktion definiert die vier Parameter.</span><span class="sxs-lookup"><span data-stu-id="a3f4e-123">The member function defines the four parameters.</span></span> <span data-ttu-id="a3f4e-124">Verwenden Sie in der Regel den Parameter " *übersg* ", um die Anforderung anzugeben, und die anderen drei Parameter sind optionale zusätzliche Parameter.</span><span class="sxs-lookup"><span data-stu-id="a3f4e-124">Typically, use the *uMsg* parameter to indicate the request, and the other three parameters will be optional additional parameters.</span></span> <span data-ttu-id="a3f4e-125">Die aufrufenden Anwendung kann einen Zeiger auf ein [**camevent**](camevent.md) -Objekt im Parameter " *GVENT* " bereitstellen, wenn dies für Ihre Anwendung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a3f4e-125">The calling application can supply a pointer to a [**CAMEvent**](camevent.md) object in the *pEvent* parameter if your application requires it.</span></span> <span data-ttu-id="a3f4e-126">Sie müssen dieses Ereignis festlegen, nachdem Sie das Ereignis mithilfe eines Ausdrucks wie z. b. verarbeitet haben:</span><span class="sxs-lookup"><span data-stu-id="a3f4e-126">You must set this event after processing the event by using an expression such as:</span></span>


```C++
pEvent->SetEvent
```



<span data-ttu-id="a3f4e-127">Ein Anforderungs Code muss reserviert werden, um dem Arbeits Thread mitzuteilen, dass er beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3f4e-127">One request code must be set aside to tell the worker thread to exit.</span></span> <span data-ttu-id="a3f4e-128">Wenn diese Anforderung empfangen wird, wird 1 von dieser Member-Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a3f4e-128">Upon receiving this request, return 1 from this member function.</span></span> <span data-ttu-id="a3f4e-129">Gibt 0 zurück, wenn der Arbeits Thread nicht beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3f4e-129">Return 0 if you do not want the worker thread to exit.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3f4e-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3f4e-130">Requirements</span></span>



| <span data-ttu-id="a3f4e-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3f4e-131">Requirement</span></span> | <span data-ttu-id="a3f4e-132">Wert</span><span class="sxs-lookup"><span data-stu-id="a3f4e-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3f4e-133">Header</span><span class="sxs-lookup"><span data-stu-id="a3f4e-133">Header</span></span><br/>  | <dl> <span data-ttu-id="a3f4e-134"><dt>Msgthrd. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3f4e-134"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a3f4e-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a3f4e-135">Library</span></span><br/> | <dl> <span data-ttu-id="a3f4e-136">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a3f4e-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3f4e-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3f4e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3f4e-138">**Cmsgthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a3f4e-138">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




