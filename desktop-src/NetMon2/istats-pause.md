---
description: Mit der Pause-Methode wird die aktuelle Erfassung vorübergehend beendet.
ms.assetid: 43176e9e-1502-484c-a8af-4e7bbf5f6474
title: IStats::P ause-Methode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d9e9f04ce3d25399866c711dad7a853f2c43c2ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106361087"
---
# <a name="istatspause-method"></a><span data-ttu-id="572c3-103">IStats::P ause-Methode</span><span class="sxs-lookup"><span data-stu-id="572c3-103">IStats::Pause method</span></span>

<span data-ttu-id="572c3-104">Mit der **Pause** -Methode wird die aktuelle Erfassung vorübergehend beendet.</span><span class="sxs-lookup"><span data-stu-id="572c3-104">The **Pause** method temporarily stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="572c3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="572c3-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="572c3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="572c3-106">Parameters</span></span>

<span data-ttu-id="572c3-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="572c3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="572c3-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="572c3-108">Return value</span></span>

<span data-ttu-id="572c3-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="572c3-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="572c3-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="572c3-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="572c3-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="572c3-111">Return code</span></span>                                                                                            | <span data-ttu-id="572c3-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="572c3-112">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="572c3-113"><dt>**nmerr- \_ Erfassung \_ angehalten**</dt></span><span class="sxs-lookup"><span data-stu-id="572c3-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl>  | <span data-ttu-id="572c3-114">Die Erfassung wurde bereits angehalten.</span><span class="sxs-lookup"><span data-stu-id="572c3-114">The capture is already paused.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="572c3-115"><dt>**nmerr wird \_ nicht \_ erfasst**</dt></span><span class="sxs-lookup"><span data-stu-id="572c3-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="572c3-116">Der NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="572c3-116">The NPP is not capturing data.</span></span> <span data-ttu-id="572c3-117">Ruft die [iStats:: Start](istats-start.md) -Methode auf, um die Erfassung zu starten.</span><span class="sxs-lookup"><span data-stu-id="572c3-117">Call the [IStats::Start](istats-start.md) method to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="572c3-118"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="572c3-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="572c3-119">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="572c3-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="572c3-120">Wenden Sie die [iStats:: Connect](istats-connect.md) -Methode an, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="572c3-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="572c3-121"><dt>**nmerr \_ nicht \_ \_ nur Statistiken**</dt></span><span class="sxs-lookup"><span data-stu-id="572c3-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="572c3-122">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iStats:: Connect](istats-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="572c3-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="572c3-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="572c3-123">Remarks</span></span>

<span data-ttu-id="572c3-124">Während die Erfassung angehalten wird, werden neue Frames erst aufgezeichnet, wenn ein Aufrufe der [iStats:: Resume](istats-resume.md) -Methode die Erfassung neu startet.</span><span class="sxs-lookup"><span data-stu-id="572c3-124">While the capture is paused, new frames are not captured until a call to the [IStats::Resume](istats-resume.md) method restarts the capture.</span></span>

<span data-ttu-id="572c3-125">Wenn Sie die **iStats::P ause** -Methode und die **iStats:: Resume** -Methode verwenden, um die Erfassung zu steuern, werden Netzwerkmonitor weiterhin [*Konversations Statistiken*](c.md) hinzufügen, sobald die Erfassung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="572c3-125">When you use the **IStats::Pause** and **IStats::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="572c3-126">Zum Neustarten des Aufzeichnungs Aufrufes [iStats:: Resume](istats-resume.md).</span><span class="sxs-lookup"><span data-stu-id="572c3-126">To restart the capture call [IStats::Resume](istats-resume.md).</span></span> <span data-ttu-id="572c3-127">Um die Erfassung anzuhalten, nennen Sie [iStats:: Beendigung](istats-stop.md).</span><span class="sxs-lookup"><span data-stu-id="572c3-127">To stop the capture, call [IStats::Stop](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="572c3-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="572c3-128">Requirements</span></span>



| <span data-ttu-id="572c3-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="572c3-129">Requirement</span></span> | <span data-ttu-id="572c3-130">Wert</span><span class="sxs-lookup"><span data-stu-id="572c3-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="572c3-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="572c3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="572c3-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="572c3-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="572c3-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="572c3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="572c3-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="572c3-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="572c3-135">Header</span><span class="sxs-lookup"><span data-stu-id="572c3-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="572c3-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="572c3-136"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="572c3-137">DLL</span><span class="sxs-lookup"><span data-stu-id="572c3-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="572c3-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="572c3-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="572c3-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="572c3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="572c3-140">IStats</span><span class="sxs-lookup"><span data-stu-id="572c3-140">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="572c3-141">IStats:: Connect</span><span class="sxs-lookup"><span data-stu-id="572c3-141">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="572c3-142">IStats:: Resume</span><span class="sxs-lookup"><span data-stu-id="572c3-142">IStats::Resume</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="572c3-143">IStats:: Start</span><span class="sxs-lookup"><span data-stu-id="572c3-143">IStats::Start</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="572c3-144">IStats:: Beendigung</span><span class="sxs-lookup"><span data-stu-id="572c3-144">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




