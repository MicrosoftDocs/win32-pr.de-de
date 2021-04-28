---
description: 'IESP::P ause-Methode: Die Pause-Methode hält die aktuelle Erfassung an.'
ms.assetid: efbc8947-b9fe-4dbd-8097-375b5f99845e
title: IESP::P ause-Methode (Netmon.h)
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
ms.openlocfilehash: 486c7aedc7092e0dd0f9f68cc1ea2ccad08d9438
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084238"
---
# <a name="iesppause-method"></a><span data-ttu-id="f8b77-103">IESP::P ause-Methode</span><span class="sxs-lookup"><span data-stu-id="f8b77-103">IESP::Pause method</span></span>

<span data-ttu-id="f8b77-104">Die **Pause-Methode** hält die aktuelle Erfassung an.</span><span class="sxs-lookup"><span data-stu-id="f8b77-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8b77-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8b77-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause(
   LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="f8b77-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8b77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8b77-107">*lpStats*</span><span class="sxs-lookup"><span data-stu-id="f8b77-107">*lpStats*</span></span> 
</dt> <dd>

<span data-ttu-id="f8b77-108">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="f8b77-108">Obsolete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8b77-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8b77-109">Return value</span></span>

<span data-ttu-id="f8b77-110">Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="f8b77-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="f8b77-111">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="f8b77-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="f8b77-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f8b77-112">Return code</span></span>                                                                                           | <span data-ttu-id="f8b77-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8b77-113">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f8b77-114"><dt>**NMERR \_ CAPTURE \_ PAUSED**</dt></span><span class="sxs-lookup"><span data-stu-id="f8b77-114"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="f8b77-115">Die Erfassung wurde bereits angehalten.</span><span class="sxs-lookup"><span data-stu-id="f8b77-115">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="f8b77-116"><dt>**NMERR NOT CAPTURING (NMERR \_ WIRD NICHT \_ ERFASST)**</dt></span><span class="sxs-lookup"><span data-stu-id="f8b77-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="f8b77-117">Der NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="f8b77-117">The NPP is not capturing data.</span></span> <span data-ttu-id="f8b77-118">Rufen [Sie IESP::Start auf,](iesp-start.md) um die Erfassung zu starten.</span><span class="sxs-lookup"><span data-stu-id="f8b77-118">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="f8b77-119"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="f8b77-119"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="f8b77-120">Der NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="f8b77-120">The NPP is not connected to the network.</span></span> <span data-ttu-id="f8b77-121">Rufen [Sie IESP::Connect auf,](iesp-connect.md) um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="f8b77-121">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="f8b77-122"><dt>**NMERR \_ NICHT \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="f8b77-122"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="f8b77-123">Das NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IESP::Connect-Methode.](iesp-connect.md)</span><span class="sxs-lookup"><span data-stu-id="f8b77-123">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="f8b77-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8b77-124">Remarks</span></span>

<span data-ttu-id="f8b77-125">Während sich die Erfassung in einem angehaltenen Zustand befindet, werden der aktuellen Erfassungsdatei erst dann neue Daten hinzugefügt, wenn Sie die [IESP::Resume-Methode](iesp-resume.md) aufrufen, um die Erfassung neu zu starten. [](c.md)</span><span class="sxs-lookup"><span data-stu-id="f8b77-125">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until you call the [IESP::Resume](iesp-resume.md) method to restart the capture.</span></span> <span data-ttu-id="f8b77-126">Wenn **Anhalten** und **Fortsetzen** zum Beenden und Neustarten der Erfassung verwendet werden, werden alle erfassten Informationen in derselben Erfassungsdatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f8b77-126">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="f8b77-127">Wenn Sie die **Methoden IESP::P ause** und **IESP::Resume** verwenden, um die Erfassung [](c.md) zu steuern, fügt Netzwerkmonitor weiterhin Konversationsstatistiken hinzu, wenn die Erfassung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8b77-127">When you use the **IESP::Pause** and **IESP::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="f8b77-128">Rufen Sie [IESP::Resume](iesp-resume.md)auf, um die Erfassung neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="f8b77-128">To restart the capture, call [IESP::Resume](iesp-resume.md).</span></span> <span data-ttu-id="f8b77-129">Um die Erfassung zu beenden, rufen Sie [IESP::Stop](iesp-stop.md)auf.</span><span class="sxs-lookup"><span data-stu-id="f8b77-129">To stop the capture, call [IESP::Stop](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8b77-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8b77-130">Requirements</span></span>



| <span data-ttu-id="f8b77-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8b77-131">Requirement</span></span> | <span data-ttu-id="f8b77-132">Wert</span><span class="sxs-lookup"><span data-stu-id="f8b77-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b77-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8b77-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f8b77-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8b77-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="f8b77-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8b77-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f8b77-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8b77-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="f8b77-137">Header</span><span class="sxs-lookup"><span data-stu-id="f8b77-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8b77-138"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="f8b77-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="f8b77-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f8b77-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8b77-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8b77-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8b77-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f8b77-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8b77-142">IESP</span><span class="sxs-lookup"><span data-stu-id="f8b77-142">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="f8b77-143">IESP::Connect</span><span class="sxs-lookup"><span data-stu-id="f8b77-143">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="f8b77-144">IESP::Resume</span><span class="sxs-lookup"><span data-stu-id="f8b77-144">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="f8b77-145">IESP::Start</span><span class="sxs-lookup"><span data-stu-id="f8b77-145">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="f8b77-146">IESP::Stop</span><span class="sxs-lookup"><span data-stu-id="f8b77-146">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




