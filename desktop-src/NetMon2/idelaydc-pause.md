---
description: Die Pause-Methode hält die aktuelle Erfassung an.
ms.assetid: 9d5e11d1-8c45-4cf5-9fea-10c9e7a6fe86
title: Idelta-DC::P ause-Methode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d44ae7792388d9ca637232b45e63d618a37acb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861995"
---
# <a name="idelaydcpause-method"></a><span data-ttu-id="c9489-103">Idelta aydc::P ause-Methode</span><span class="sxs-lookup"><span data-stu-id="c9489-103">IDelaydC::Pause method</span></span>

<span data-ttu-id="c9489-104">Die **Pause** -Methode hält die aktuelle Erfassung an.</span><span class="sxs-lookup"><span data-stu-id="c9489-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9489-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9489-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="c9489-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9489-106">Parameters</span></span>

<span data-ttu-id="c9489-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c9489-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9489-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9489-108">Return value</span></span>

<span data-ttu-id="c9489-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c9489-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c9489-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="c9489-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="c9489-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c9489-111">Return code</span></span>                                                                                           | <span data-ttu-id="c9489-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9489-112">Description</span></span>                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9489-113"><dt>**nmerr- \_ Erfassung \_ angehalten**</dt></span><span class="sxs-lookup"><span data-stu-id="c9489-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="c9489-114">Die Erfassung befindet sich bereits im angehaltenen Zustand.</span><span class="sxs-lookup"><span data-stu-id="c9489-114">The capture is already in a paused state.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="c9489-115"><dt>**nmerr wird \_ nicht \_ erfasst**</dt></span><span class="sxs-lookup"><span data-stu-id="c9489-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="c9489-116">Der NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="c9489-116">The NPP is not capturing data.</span></span> <span data-ttu-id="c9489-117">Wenden Sie [idelta-DC:: Start](idelaydc-start.md) an, um die Erfassung zu starten.</span><span class="sxs-lookup"><span data-stu-id="c9489-117">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="c9489-118"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="c9489-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="c9489-119">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="c9489-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="c9489-120">Wenden Sie [idelta-DC:: Connect](idelaydc-connect.md) an, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="c9489-120">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="c9489-121"><dt>**nmerr \_ nicht \_ verzögert**</dt></span><span class="sxs-lookup"><span data-stu-id="c9489-121"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>    | <span data-ttu-id="c9489-122">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [idelta aydc:: Connect](idelaydc-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c9489-122">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="c9489-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9489-123">Remarks</span></span>

<span data-ttu-id="c9489-124">Während sich die Erfassung im angehaltenen Zustand befindet, werden der aktuellen [*Erfassungs Datei*](c.md) keine neuen Daten hinzugefügt, bis die **idelta-DC:: Resume** -Methode aufgerufen wird, um die Erfassung neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="c9489-124">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="c9489-125">Wenn anhalten und **fortsetzen verwendet** werden, um die Erfassung zu **beenden und neu** zu starten, werden alle erfassten Informationen in derselben Erfassungs Datei abgelegt.</span><span class="sxs-lookup"><span data-stu-id="c9489-125">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="c9489-126">Bei der Verwendung von **idelta aydc::P ause** und **idelta aydc:: Resume** zum Steuern der Erfassung werden von Netzwerkmonitor weiterhin [*Konversations Statistiken*](c.md) hinzugefügt, wenn die Erfassung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9489-126">When using **IDelaydC::Pause** and **IDelaydC::Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="c9489-127">Um die Erfassung neu zu starten, nennen Sie [idelta aydc:: Resume](idelaydc-resume.md).</span><span class="sxs-lookup"><span data-stu-id="c9489-127">To restart the capture, call [IDelaydC::Resume](idelaydc-resume.md).</span></span>

<span data-ttu-id="c9489-128">Um die Erfassung anzuhalten, nennen Sie [idelta aydc:: Stop.](idelaydc-stop.md)</span><span class="sxs-lookup"><span data-stu-id="c9489-128">To stop the capture, call [IDelaydC::Stop](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9489-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9489-129">Requirements</span></span>



| <span data-ttu-id="c9489-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9489-130">Requirement</span></span> | <span data-ttu-id="c9489-131">Wert</span><span class="sxs-lookup"><span data-stu-id="c9489-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9489-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9489-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c9489-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9489-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c9489-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9489-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c9489-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9489-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c9489-136">Header</span><span class="sxs-lookup"><span data-stu-id="c9489-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9489-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9489-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c9489-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c9489-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9489-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9489-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9489-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9489-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9489-141">Idelta-DC</span><span class="sxs-lookup"><span data-stu-id="c9489-141">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="c9489-142">Idelta aydc:: Connect</span><span class="sxs-lookup"><span data-stu-id="c9489-142">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="c9489-143">Idelta aydc:: Resume</span><span class="sxs-lookup"><span data-stu-id="c9489-143">IDelaydC::Resume</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="c9489-144">Idelta aydc:: Start</span><span class="sxs-lookup"><span data-stu-id="c9489-144">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="c9489-145">Idelta aydc:: Beendigung</span><span class="sxs-lookup"><span data-stu-id="c9489-145">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




