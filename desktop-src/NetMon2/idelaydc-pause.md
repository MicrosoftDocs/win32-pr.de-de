---
description: 'IDelaydC::P ause-Methode: Die Pause-Methode hält die aktuelle Erfassung an.'
ms.assetid: 9d5e11d1-8c45-4cf5-9fea-10c9e7a6fe86
title: IDelaydC::P ause-Methode (Netmon.h)
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
ms.openlocfilehash: 21b4cd7b6cb921f7bd71b8670a37da12b2239b92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098498"
---
# <a name="idelaydcpause-method"></a><span data-ttu-id="ef7cb-103">IDelaydC::P ause-Methode</span><span class="sxs-lookup"><span data-stu-id="ef7cb-103">IDelaydC::Pause method</span></span>

<span data-ttu-id="ef7cb-104">Die **Pause-Methode** hält die aktuelle Erfassung an.</span><span class="sxs-lookup"><span data-stu-id="ef7cb-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef7cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef7cb-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="ef7cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef7cb-106">Parameters</span></span>

<span data-ttu-id="ef7cb-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ef7cb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ef7cb-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef7cb-108">Return value</span></span>

<span data-ttu-id="ef7cb-109">Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="ef7cb-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ef7cb-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="ef7cb-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="ef7cb-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ef7cb-111">Return code</span></span>                                                                                           | <span data-ttu-id="ef7cb-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef7cb-112">Description</span></span>                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef7cb-113"><dt>**NMERR \_ CAPTURE \_ PAUSED**</dt></span><span class="sxs-lookup"><span data-stu-id="ef7cb-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="ef7cb-114">Die Erfassung befindet sich bereits in einem angehaltenen Zustand.</span><span class="sxs-lookup"><span data-stu-id="ef7cb-114">The capture is already in a paused state.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="ef7cb-115"><dt>**NMERR \_ NICHT \_ ERFASSEN**</dt></span><span class="sxs-lookup"><span data-stu-id="ef7cb-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="ef7cb-116">Das NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="ef7cb-116">The NPP is not capturing data.</span></span> <span data-ttu-id="ef7cb-117">Rufen Sie [IDelaydC::Start](idelaydc-start.md) auf, um die Erfassung zu starten.</span><span class="sxs-lookup"><span data-stu-id="ef7cb-117">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="ef7cb-118"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="ef7cb-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="ef7cb-119">Das NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="ef7cb-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="ef7cb-120">Rufen Sie [IDelaydC::Connect](idelaydc-connect.md) auf, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="ef7cb-120">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="ef7cb-121"><dt>**NMERR \_ NICHT \_ VERZÖGERT**</dt></span><span class="sxs-lookup"><span data-stu-id="ef7cb-121"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>    | <span data-ttu-id="ef7cb-122">Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IDelaydC::Connect-Methode.](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="ef7cb-122">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="ef7cb-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef7cb-123">Remarks</span></span>

<span data-ttu-id="ef7cb-124">Während sich die Erfassung in einem angehaltenen Zustand befindet, werden der aktuellen [*Erfassungsdatei*](c.md) erst neue Daten hinzugefügt, wenn die **IDelaydC::Resume-Methode** aufgerufen wird, um die Erfassung neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="ef7cb-124">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="ef7cb-125">Wenn **Anhalten** und **Fortsetzen** zum Beenden und Neustarten der Erfassung verwendet werden, werden alle erfassten Informationen in derselben Erfassungsdatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ef7cb-125">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="ef7cb-126">Wenn **Sie IDelaydC::P ause** und **IDelaydC::Resume** verwenden, um die Erfassung zu steuern, fügt Netzwerkmonitor bei jeder Ausführung der Erfassung [*weiterhin Konversationsstatistiken*](c.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="ef7cb-126">When using **IDelaydC::Pause** and **IDelaydC::Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="ef7cb-127">Um die Erfassung neu zu starten, rufen [Sie IDelaydC::Resume auf.](idelaydc-resume.md)</span><span class="sxs-lookup"><span data-stu-id="ef7cb-127">To restart the capture, call [IDelaydC::Resume](idelaydc-resume.md).</span></span>

<span data-ttu-id="ef7cb-128">Um die Erfassung zu beenden, rufen [Sie IDelaydC::Stop](idelaydc-stop.md)auf.</span><span class="sxs-lookup"><span data-stu-id="ef7cb-128">To stop the capture, call [IDelaydC::Stop](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef7cb-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef7cb-129">Requirements</span></span>



| <span data-ttu-id="ef7cb-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef7cb-130">Requirement</span></span> | <span data-ttu-id="ef7cb-131">Wert</span><span class="sxs-lookup"><span data-stu-id="ef7cb-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef7cb-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef7cb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ef7cb-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef7cb-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="ef7cb-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef7cb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ef7cb-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef7cb-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="ef7cb-136">Header</span><span class="sxs-lookup"><span data-stu-id="ef7cb-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef7cb-137"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="ef7cb-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="ef7cb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ef7cb-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef7cb-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef7cb-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef7cb-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ef7cb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef7cb-141">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="ef7cb-141">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="ef7cb-142">IDelaydC::Connect</span><span class="sxs-lookup"><span data-stu-id="ef7cb-142">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="ef7cb-143">IDelaydC::Resume</span><span class="sxs-lookup"><span data-stu-id="ef7cb-143">IDelaydC::Resume</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="ef7cb-144">IDelaydC::Start</span><span class="sxs-lookup"><span data-stu-id="ef7cb-144">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="ef7cb-145">IDelaydC::Stop</span><span class="sxs-lookup"><span data-stu-id="ef7cb-145">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




