---
description: Mit der Resume-Methode wird eine angehaltene Erfassung neu gestartet.
ms.assetid: 047ea5f8-de3d-40db-ada3-fc0ef4deccef
title: 'IESP:: Resume-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 01bbb748fc91bcc5a78b281ec9ebdd2a6d479888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343227"
---
# <a name="iespresume-method"></a><span data-ttu-id="c516d-103">IESP:: Resume-Methode</span><span class="sxs-lookup"><span data-stu-id="c516d-103">IESP::Resume method</span></span>

<span data-ttu-id="c516d-104">Mit der **Resume** -Methode wird eine angehaltene Erfassung neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="c516d-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c516d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c516d-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="c516d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c516d-106">Parameters</span></span>

<span data-ttu-id="c516d-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c516d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c516d-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c516d-108">Return value</span></span>

<span data-ttu-id="c516d-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c516d-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c516d-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="c516d-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="c516d-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c516d-111">Return code</span></span>                                                                                                | <span data-ttu-id="c516d-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c516d-112">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c516d-113"><dt>**nmerr- \_ Erfassung wurde \_ nicht \_ angehalten.**</dt></span><span class="sxs-lookup"><span data-stu-id="c516d-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="c516d-114">Die Erfassung wird nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="c516d-114">The capture is not paused.</span></span> <span data-ttu-id="c516d-115">Wenden Sie [**iESP an::P ause**](iesp-pause.md) , um die Erfassung anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="c516d-115">Call [**IESP::Pause**](iesp-pause.md) to pause the capture.</span></span><br/>                        |
| <dl> <span data-ttu-id="c516d-116"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="c516d-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="c516d-117">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="c516d-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="c516d-118">Wenden Sie [**iESP:: Connect**](iesp-connect.md) an, um eine Verbindung mit dem Netzwerk herzustellen.</span><span class="sxs-lookup"><span data-stu-id="c516d-118">Call [**IESP::Connect**](iesp-connect.md) to connect to the network.</span></span><br/> |
| <dl> <span data-ttu-id="c516d-119"><dt>**nmerr \_ nicht \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="c516d-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>             | <span data-ttu-id="c516d-120">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [**iESP:: Connect**](iesp-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c516d-120">The NPP is connected to the network, but not with the [**IESP::Connect**](iesp-connect.md) method.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="c516d-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c516d-121">Remarks</span></span>

<span data-ttu-id="c516d-122">Während sich die Erfassung im angehaltenen Zustand befindet, werden der aktuellen [*Erfassungs Datei*](c.md) keine neuen Daten hinzugefügt, bis **iESP:: Resume** aufgerufen wird, um die Erfassung neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="c516d-122">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until **IESP::Resume** is called to restart the capture.</span></span> <span data-ttu-id="c516d-123">Wenn anhalten und **fortsetzen verwendet** werden, um die Erfassung zu **beenden und neu** zu starten, werden alle erfassten Informationen in derselben Erfassungs Datei abgelegt.</span><span class="sxs-lookup"><span data-stu-id="c516d-123">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="c516d-124">Bei der **Verwendung** von **Anhalten und fort** setzen zur Steuerung der Erfassung werden Netzwerkmonitor weiterhin [*Konversations Statistiken*](c.md) zu den vorhandenen Statistiken für die aktuelle Erfassung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c516d-124">When using **Pause** and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="c516d-125">Um die Erfassung anzuhalten, nennen Sie [**iESP:: Beendigung**](iesp-stop.md).</span><span class="sxs-lookup"><span data-stu-id="c516d-125">To stop the capture, call [**IESP::Stop**](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c516d-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c516d-126">Requirements</span></span>



| <span data-ttu-id="c516d-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c516d-127">Requirement</span></span> | <span data-ttu-id="c516d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c516d-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c516d-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c516d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c516d-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c516d-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c516d-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c516d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c516d-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c516d-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c516d-133">Header</span><span class="sxs-lookup"><span data-stu-id="c516d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c516d-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c516d-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c516d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c516d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c516d-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c516d-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c516d-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c516d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c516d-138">IESP</span><span class="sxs-lookup"><span data-stu-id="c516d-138">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="c516d-139">**IESP:: Connect**</span><span class="sxs-lookup"><span data-stu-id="c516d-139">**IESP::Connect**</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="c516d-140">**IESP::P ause**</span><span class="sxs-lookup"><span data-stu-id="c516d-140">**IESP::Pause**</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="c516d-141">**IESP:: Beendigung**</span><span class="sxs-lookup"><span data-stu-id="c516d-141">**IESP::Stop**</span></span>](iesp-stop.md)
</dt> </dl>

 

 




