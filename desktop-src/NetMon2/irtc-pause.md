---
description: 'IRTC::P ause-Methode: Die Pause-Methode hält die aktuelle Erfassung an.'
ms.assetid: 8c7b310e-de04-4bd8-9c96-3c5948e610be
title: IRTC::P ause-Methode (Netmon.h)
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
ms.openlocfilehash: d42af1912365a4237889e4e46d0fb3343377c772
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110678"
---
# <a name="irtcpause-method"></a><span data-ttu-id="c7606-103">IRTC::P ause-Methode</span><span class="sxs-lookup"><span data-stu-id="c7606-103">IRTC::Pause method</span></span>

<span data-ttu-id="c7606-104">Die **Pause-Methode** hält die aktuelle Erfassung an.</span><span class="sxs-lookup"><span data-stu-id="c7606-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7606-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7606-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="c7606-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7606-106">Parameters</span></span>

<span data-ttu-id="c7606-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c7606-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c7606-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7606-108">Return value</span></span>

<span data-ttu-id="c7606-109">Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="c7606-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c7606-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="c7606-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="c7606-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c7606-111">Return code</span></span>                                                                                           | <span data-ttu-id="c7606-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7606-112">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c7606-113"><dt>**NMERR \_ CAPTURE \_ PAUSED**</dt></span><span class="sxs-lookup"><span data-stu-id="c7606-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="c7606-114">Die Erfassung ist bereits angehalten.</span><span class="sxs-lookup"><span data-stu-id="c7606-114">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="c7606-115"><dt>**NMERR \_ NICHT \_ ERFASSEN**</dt></span><span class="sxs-lookup"><span data-stu-id="c7606-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="c7606-116">Das NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="c7606-116">The NPP is not capturing data.</span></span> <span data-ttu-id="c7606-117">Rufen Sie [IRTC::Start](irtc-start.md) auf, um die Erfassung zu starten.</span><span class="sxs-lookup"><span data-stu-id="c7606-117">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="c7606-118"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="c7606-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="c7606-119">Das NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="c7606-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="c7606-120">Rufen Sie [IRTC::Connect](irtc-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="c7606-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="c7606-121"><dt>**NMERR \_ NOT \_ REALTIME**</dt></span><span class="sxs-lookup"><span data-stu-id="c7606-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>   | <span data-ttu-id="c7606-122">Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IRTC::Connect-Methode.](irtc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="c7606-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="c7606-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7606-123">Remarks</span></span>

<span data-ttu-id="c7606-124">Während sich die Erfassung in einem angehaltenen Zustand befindet, werden neue Frames erst erfasst, wenn die [IRTC::Resume-Methode](irtc-resume.md) aufgerufen wird, um die Erfassung neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="c7606-124">While the capture is in a paused state, new frames are not captured until the [IRTC::Resume](irtc-resume.md) method is called to restart the capture.</span></span>

<span data-ttu-id="c7606-125">Wenn Sie die **Methoden IRTC::P ause** und **IRTC::Resume** verwenden, um die Erfassung zu steuern, fügt Netzwerkmonitor bei jeder Ausführung der Erfassung [*weiterhin Konversationsstatistiken*](c.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="c7606-125">When you use the **IRTC::Pause** and **IRTC::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="c7606-126">Um den Aufzeichnungsaufruf neu zu starten, rufen [Sie IRTC::Resume auf.](irtc-resume.md)</span><span class="sxs-lookup"><span data-stu-id="c7606-126">To restart the capture call [IRTC::Resume](irtc-resume.md).</span></span> <span data-ttu-id="c7606-127">Um die Erfassung zu beenden, rufen Sie [IRTC::Stop](irtc-stop.md)auf.</span><span class="sxs-lookup"><span data-stu-id="c7606-127">To stop the capture, call [IRTC::Stop](irtc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7606-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7606-128">Requirements</span></span>



| <span data-ttu-id="c7606-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7606-129">Requirement</span></span> | <span data-ttu-id="c7606-130">Wert</span><span class="sxs-lookup"><span data-stu-id="c7606-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7606-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7606-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c7606-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7606-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c7606-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7606-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c7606-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7606-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c7606-135">Header</span><span class="sxs-lookup"><span data-stu-id="c7606-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7606-136"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="c7606-136"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c7606-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c7606-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7606-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7606-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7606-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c7606-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7606-140">IRTC</span><span class="sxs-lookup"><span data-stu-id="c7606-140">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="c7606-141">IRTC::Connect</span><span class="sxs-lookup"><span data-stu-id="c7606-141">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="c7606-142">IRTC::Resume</span><span class="sxs-lookup"><span data-stu-id="c7606-142">IRTC::Resume</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="c7606-143">IRTC::Start</span><span class="sxs-lookup"><span data-stu-id="c7606-143">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="c7606-144">IRTC::Stop</span><span class="sxs-lookup"><span data-stu-id="c7606-144">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




