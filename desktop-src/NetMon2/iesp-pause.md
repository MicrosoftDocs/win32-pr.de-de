---
description: Die Pause-Methode hält die aktuelle Erfassung an.
ms.assetid: efbc8947-b9fe-4dbd-8097-375b5f99845e
title: IESP::P ause-Methode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0558c5dfe36f26e3aad9f31101364d2e8e5c4967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525118"
---
# <a name="iesppause-method"></a><span data-ttu-id="2a23f-103">IESP::P ause-Methode</span><span class="sxs-lookup"><span data-stu-id="2a23f-103">IESP::Pause method</span></span>

<span data-ttu-id="2a23f-104">Die **Pause** -Methode hält die aktuelle Erfassung an.</span><span class="sxs-lookup"><span data-stu-id="2a23f-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a23f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a23f-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause(
   LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="2a23f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a23f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a23f-107">*lpstats*</span><span class="sxs-lookup"><span data-stu-id="2a23f-107">*lpStats*</span></span> 
</dt> <dd>

<span data-ttu-id="2a23f-108">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="2a23f-108">Obsolete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a23f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a23f-109">Return value</span></span>

<span data-ttu-id="2a23f-110">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="2a23f-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2a23f-111">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="2a23f-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="2a23f-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2a23f-112">Return code</span></span>                                                                                           | <span data-ttu-id="2a23f-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a23f-113">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2a23f-114"><dt>**nmerr- \_ Erfassung \_ angehalten**</dt></span><span class="sxs-lookup"><span data-stu-id="2a23f-114"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="2a23f-115">Die Erfassung wurde bereits angehalten.</span><span class="sxs-lookup"><span data-stu-id="2a23f-115">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="2a23f-116"><dt>**nmerr wird \_ nicht \_ erfasst**</dt></span><span class="sxs-lookup"><span data-stu-id="2a23f-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="2a23f-117">Der NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="2a23f-117">The NPP is not capturing data.</span></span> <span data-ttu-id="2a23f-118">Wenden Sie [iESP:: Start](iesp-start.md) an, um die Erfassung zu starten.</span><span class="sxs-lookup"><span data-stu-id="2a23f-118">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="2a23f-119"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="2a23f-119"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="2a23f-120">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="2a23f-120">The NPP is not connected to the network.</span></span> <span data-ttu-id="2a23f-121">Wenden Sie [iESP:: Connect](iesp-connect.md) an, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="2a23f-121">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="2a23f-122"><dt>**nmerr \_ nicht \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="2a23f-122"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="2a23f-123">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iESP:: Connect](iesp-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="2a23f-123">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="2a23f-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a23f-124">Remarks</span></span>

<span data-ttu-id="2a23f-125">Während sich die Erfassung in einem angehaltenen Zustand befindet, werden der aktuellen [*Erfassungs Datei*](c.md) keine neuen Daten hinzugefügt, bis Sie die [iESP:: Resume](iesp-resume.md) -Methode zum Neustarten der Erfassung aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="2a23f-125">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until you call the [IESP::Resume](iesp-resume.md) method to restart the capture.</span></span> <span data-ttu-id="2a23f-126">Wenn anhalten und **fortsetzen verwendet** werden, um die Erfassung zu **beenden und neu** zu starten, werden alle erfassten Informationen in derselben Erfassungs Datei abgelegt.</span><span class="sxs-lookup"><span data-stu-id="2a23f-126">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="2a23f-127">Wenn Sie die **iESP::P ause** -Methode und die **iESP:: Resume** -Methode verwenden, um die Erfassung zu steuern, werden Netzwerkmonitor weiterhin [*Konversations Statistiken*](c.md) hinzufügen, sobald die Erfassung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a23f-127">When you use the **IESP::Pause** and **IESP::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="2a23f-128">Um die Erfassung neu zu starten, nennen Sie [iESP:: Resume](iesp-resume.md).</span><span class="sxs-lookup"><span data-stu-id="2a23f-128">To restart the capture, call [IESP::Resume](iesp-resume.md).</span></span> <span data-ttu-id="2a23f-129">Um die Erfassung anzuhalten, nennen Sie [iESP:: Beendigung](iesp-stop.md).</span><span class="sxs-lookup"><span data-stu-id="2a23f-129">To stop the capture, call [IESP::Stop](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a23f-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a23f-130">Requirements</span></span>



| <span data-ttu-id="2a23f-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a23f-131">Requirement</span></span> | <span data-ttu-id="2a23f-132">Wert</span><span class="sxs-lookup"><span data-stu-id="2a23f-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a23f-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a23f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2a23f-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a23f-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="2a23f-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a23f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2a23f-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a23f-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="2a23f-137">Header</span><span class="sxs-lookup"><span data-stu-id="2a23f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a23f-138"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a23f-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="2a23f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2a23f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a23f-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a23f-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a23f-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a23f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a23f-142">IESP</span><span class="sxs-lookup"><span data-stu-id="2a23f-142">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="2a23f-143">IESP:: Connect</span><span class="sxs-lookup"><span data-stu-id="2a23f-143">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="2a23f-144">IESP:: Resume</span><span class="sxs-lookup"><span data-stu-id="2a23f-144">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="2a23f-145">IESP:: Start</span><span class="sxs-lookup"><span data-stu-id="2a23f-145">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="2a23f-146">IESP:: Beendigung</span><span class="sxs-lookup"><span data-stu-id="2a23f-146">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




