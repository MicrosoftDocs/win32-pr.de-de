---
description: Mit der Resume-Methode wird eine angehaltene Erfassung neu gestartet.
ms.assetid: 128e38c4-7459-4376-a3d7-2c6944fcf535
title: 'IStats:: Resume-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: db84f51d2a2a2c2d15e3b4164fe1fac09e72bf20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867020"
---
# <a name="istatsresume-method"></a><span data-ttu-id="69e39-103">IStats:: Resume-Methode</span><span class="sxs-lookup"><span data-stu-id="69e39-103">IStats::Resume method</span></span>

<span data-ttu-id="69e39-104">Mit der **Resume** -Methode wird eine angehaltene Erfassung neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="69e39-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="69e39-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="69e39-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="69e39-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="69e39-106">Parameters</span></span>

<span data-ttu-id="69e39-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="69e39-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="69e39-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69e39-108">Return value</span></span>

<span data-ttu-id="69e39-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="69e39-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="69e39-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="69e39-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="69e39-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="69e39-111">Return code</span></span>                                                                                                | <span data-ttu-id="69e39-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69e39-112">Description</span></span>                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="69e39-113"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="69e39-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="69e39-114">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="69e39-114">The NPP is not connected to the network.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="69e39-115"><dt>**nmerr- \_ Erfassung wurde \_ nicht \_ angehalten.**</dt></span><span class="sxs-lookup"><span data-stu-id="69e39-115"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="69e39-116">Die Erfassung wird nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="69e39-116">The capture is not paused.</span></span> <span data-ttu-id="69e39-117">Nennen Sie die [iStats::P ause](istats-pause.md) -Methode, um die Erfassung vorübergehend anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="69e39-117">Call the [IStats::Pause](istats-pause.md) method to temporarily stop the capture.</span></span><br/>                     |
| <dl> <span data-ttu-id="69e39-118"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="69e39-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="69e39-119">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="69e39-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="69e39-120">Wenden Sie die [iStats:: Connect](istats-connect.md) -Methode an, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="69e39-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="69e39-121"><dt>**nmerr \_ nicht \_ \_ nur Statistiken**</dt></span><span class="sxs-lookup"><span data-stu-id="69e39-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl>     | <span data-ttu-id="69e39-122">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iStats:: Connect](istats-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="69e39-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="69e39-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69e39-123">Remarks</span></span>

<span data-ttu-id="69e39-124">Während sich die Erfassung im angehaltenen Zustand befindet, werden neue Daten erst aufgezeichnet, wenn die iStats:: Resume-Methode aufgerufen wird, um die Erfassung neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="69e39-124">While the capture is in a paused state, new data is not captured until the IStats::Resume method is called to restart the capture.</span></span>

<span data-ttu-id="69e39-125">Bei der Verwendung der Methoden  **zum Anhalten und fort** setzen zum Steuern der Erfassung werden von Netzwerkmonitor weiterhin [*Konversations Statistiken*](c.md) zu den vorhandenen Statistiken für die aktuelle Erfassung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="69e39-125">When using the **Pause** and **Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="69e39-126">Um die Erfassung anzuhalten, nennen Sie [iStats:: Beendigung](istats-stop.md).</span><span class="sxs-lookup"><span data-stu-id="69e39-126">To stop the capture, call [IStats::Stop](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69e39-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69e39-127">Requirements</span></span>



| <span data-ttu-id="69e39-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69e39-128">Requirement</span></span> | <span data-ttu-id="69e39-129">Wert</span><span class="sxs-lookup"><span data-stu-id="69e39-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69e39-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69e39-130">Minimum supported client</span></span><br/> | <span data-ttu-id="69e39-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69e39-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="69e39-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69e39-132">Minimum supported server</span></span><br/> | <span data-ttu-id="69e39-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69e39-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="69e39-134">Header</span><span class="sxs-lookup"><span data-stu-id="69e39-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="69e39-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="69e39-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="69e39-136">DLL</span><span class="sxs-lookup"><span data-stu-id="69e39-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69e39-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69e39-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69e39-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69e39-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69e39-139">IStats</span><span class="sxs-lookup"><span data-stu-id="69e39-139">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="69e39-140">IStats:: Connect</span><span class="sxs-lookup"><span data-stu-id="69e39-140">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="69e39-141">IStats::P ause</span><span class="sxs-lookup"><span data-stu-id="69e39-141">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="69e39-142">IStats:: Beendigung</span><span class="sxs-lookup"><span data-stu-id="69e39-142">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




