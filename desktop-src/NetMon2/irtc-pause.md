---
description: Die Pause-Methode hält die aktuelle Erfassung an.
ms.assetid: 8c7b310e-de04-4bd8-9c96-3c5948e610be
title: Untc::P ause-Methode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d2593c380d0fea52d030586da2f473a3f3fa9446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215471"
---
# <a name="irtcpause-method"></a><span data-ttu-id="c558e-103">Untc::P ause-Methode</span><span class="sxs-lookup"><span data-stu-id="c558e-103">IRTC::Pause method</span></span>

<span data-ttu-id="c558e-104">Die **Pause** -Methode hält die aktuelle Erfassung an.</span><span class="sxs-lookup"><span data-stu-id="c558e-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c558e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c558e-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="c558e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c558e-106">Parameters</span></span>

<span data-ttu-id="c558e-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c558e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c558e-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c558e-108">Return value</span></span>

<span data-ttu-id="c558e-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c558e-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c558e-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="c558e-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="c558e-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c558e-111">Return code</span></span>                                                                                           | <span data-ttu-id="c558e-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c558e-112">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c558e-113"><dt>**nmerr- \_ Erfassung \_ angehalten**</dt></span><span class="sxs-lookup"><span data-stu-id="c558e-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="c558e-114">Die Erfassung wurde bereits angehalten.</span><span class="sxs-lookup"><span data-stu-id="c558e-114">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="c558e-115"><dt>**nmerr wird \_ nicht \_ erfasst**</dt></span><span class="sxs-lookup"><span data-stu-id="c558e-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="c558e-116">Der NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="c558e-116">The NPP is not capturing data.</span></span> <span data-ttu-id="c558e-117">Wenden Sie zum Starten der Erfassung den Befehl " [irren:: Start](irtc-start.md) " an.</span><span class="sxs-lookup"><span data-stu-id="c558e-117">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="c558e-118"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="c558e-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="c558e-119">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="c558e-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="c558e-120">Wenden [Sie](irtc-connect.md) sich an, um den NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="c558e-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="c558e-121"><dt>**nmerr \_ nicht in \_ Echtzeit**</dt></span><span class="sxs-lookup"><span data-stu-id="c558e-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>   | <span data-ttu-id="c558e-122">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der Methode " [iritc:: Connect](irtc-connect.md) ".</span><span class="sxs-lookup"><span data-stu-id="c558e-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="c558e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c558e-123">Remarks</span></span>

<span data-ttu-id="c558e-124">Während sich die Erfassung in einem angehaltenen Zustand befindet, werden neue Frames erst aufgezeichnet, wenn die Methode " [iritc:: Resume](irtc-resume.md) " aufgerufen wird, um die Erfassung neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="c558e-124">While the capture is in a paused state, new frames are not captured until the [IRTC::Resume](irtc-resume.md) method is called to restart the capture.</span></span>

<span data-ttu-id="c558e-125">Wenn Sie die Methode **IRTC::P ause** und **IRTC:: Resume** zum Steuern der Erfassung verwenden, werden Netzwerkmonitor weiterhin [*Konversations Statistiken*](c.md) hinzufügen, sobald die Erfassung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c558e-125">When you use the **IRTC::Pause** and **IRTC::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="c558e-126">Zum Neustarten des Aufzeichnungs Aufrufes " [untc:: Resume](irtc-resume.md)".</span><span class="sxs-lookup"><span data-stu-id="c558e-126">To restart the capture call [IRTC::Resume](irtc-resume.md).</span></span> <span data-ttu-id="c558e-127">Um die Erfassung zu verhindern, nennen Sie " [irren:: Ende](irtc-stop.md)".</span><span class="sxs-lookup"><span data-stu-id="c558e-127">To stop the capture, call [IRTC::Stop](irtc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c558e-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c558e-128">Requirements</span></span>



| <span data-ttu-id="c558e-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c558e-129">Requirement</span></span> | <span data-ttu-id="c558e-130">Wert</span><span class="sxs-lookup"><span data-stu-id="c558e-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c558e-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c558e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c558e-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c558e-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c558e-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c558e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c558e-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c558e-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c558e-135">Header</span><span class="sxs-lookup"><span data-stu-id="c558e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c558e-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c558e-136"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c558e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c558e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c558e-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c558e-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c558e-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c558e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c558e-140">"Iran"</span><span class="sxs-lookup"><span data-stu-id="c558e-140">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="c558e-141">Iran:: Connect</span><span class="sxs-lookup"><span data-stu-id="c558e-141">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="c558e-142">Iran:: Resume</span><span class="sxs-lookup"><span data-stu-id="c558e-142">IRTC::Resume</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="c558e-143">"Iran:: Start"</span><span class="sxs-lookup"><span data-stu-id="c558e-143">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="c558e-144">Iran:: Beendigung</span><span class="sxs-lookup"><span data-stu-id="c558e-144">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




