---
description: Blockiert, bis der Thread beendet wird.
ms.assetid: 1ee547b5-cd73-4ce8-8e66-c2062714d0f0
title: Cmsgthread. waitforthreadexit-Methode (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.WaitForThreadExit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b48573c4297a2d5d5d008eba88fd8ea437333c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361586"
---
# <a name="cmsgthreadwaitforthreadexit-method"></a><span data-ttu-id="d1b9e-103">Cmsgthread. waitforthreadexit-Methode</span><span class="sxs-lookup"><span data-stu-id="d1b9e-103">CMsgThread.WaitForThreadExit method</span></span>

<span data-ttu-id="d1b9e-104">Blockiert, bis der Thread beendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1b9e-104">Blocks until the thread exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1b9e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1b9e-105">Syntax</span></span>


```C++
BOOL WaitForThreadExit(
   LPDWORD lpdwExitCode
);
```



## <a name="parameters"></a><span data-ttu-id="d1b9e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1b9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1b9e-107">*lpdwexitcode*</span><span class="sxs-lookup"><span data-stu-id="d1b9e-107">*lpdwExitCode*</span></span> 
</dt> <dd>

<span data-ttu-id="d1b9e-108">Zeiger auf den Exitcode, der vom Thread zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="d1b9e-108">Pointer to the exit code returned by the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1b9e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1b9e-109">Return value</span></span>

<span data-ttu-id="d1b9e-110">Gibt entweder " **true** " oder " **false**" zurück. die Bedeutung von wird von der Klasse bestimmt, die die überschriebene [**cmsgthread:: threadmessageproc**](cmsgthread-threadmessageproc.md) -Member-Funktion und die aufrufende Member-Funktion bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="d1b9e-110">Returns either **TRUE** or **FALSE**, the meaning of which is determined by the class supplying the overridden [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function and the calling member function.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1b9e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1b9e-111">Remarks</span></span>

<span data-ttu-id="d1b9e-112">Stellen Sie sicher, dass der Arbeitsthread vollständig beendet wurde, bevor Sie die Zerstörung ihrer abgeleiteten Klasse abschließen. Andernfalls kann der Thread nach dem Entladen der Dynamic Link Library (dll) aus dem Adressraum des Prozesses weiter ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d1b9e-112">Ensure that the worker thread has exited completely before completing the destruction of your derived class; otherwise, the thread might still execute after your dynamic-link library (DLL) has been unloaded from the address space of the process.</span></span> <span data-ttu-id="d1b9e-113">Auch wenn die einzige Anweisung, die zum Beenden übrig ist, eine-Anweisung ist, würde dies zu einer Ausnahme führen.</span><span class="sxs-lookup"><span data-stu-id="d1b9e-113">Even if the only instruction left to exit is a single-return instruction, this would cause an exception.</span></span> <span data-ttu-id="d1b9e-114">Die einzige zuverlässige Möglichkeit, um sicherzustellen, dass der Thread beendet wurde, besteht darin, den Thread zu beenden (mithilfe eines privat ausgehandelten [**CMSG**](cmsg.md) -Objekts, das an die Member-Funktion [**cmsgthread::P utthreadmsg**](cmsgthread-putthreadmsg.md) gesendet wurde), und dann diese Member-Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d1b9e-114">The only reliable way to ensure that the thread has exited is to signal the thread to exit (using a privately negotiated [**CMsg**](cmsg.md) object sent to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function) and then call this member function.</span></span> <span data-ttu-id="d1b9e-115">Dies sollte im Dekonstruktor für Ihre abgeleitete Klasse durchzuführen sein.</span><span class="sxs-lookup"><span data-stu-id="d1b9e-115">You should do this in the destructor for your derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1b9e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1b9e-116">Requirements</span></span>



| <span data-ttu-id="d1b9e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1b9e-117">Requirement</span></span> | <span data-ttu-id="d1b9e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d1b9e-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1b9e-119">Header</span><span class="sxs-lookup"><span data-stu-id="d1b9e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d1b9e-120"><dt>Msgthrd. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1b9e-120"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d1b9e-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d1b9e-121">Library</span></span><br/> | <dl> <span data-ttu-id="d1b9e-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d1b9e-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1b9e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1b9e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1b9e-124">**Cmsgthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d1b9e-124">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




