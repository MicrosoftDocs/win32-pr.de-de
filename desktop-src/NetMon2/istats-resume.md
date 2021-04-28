---
description: 'IStats::Resume-Methode: Die Resume-Methode startet eine angehaltene Erfassung neu.'
ms.assetid: 128e38c4-7459-4376-a3d7-2c6944fcf535
title: IStats::Resume-Methode (Netmon.h)
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
ms.openlocfilehash: ee7818da3d8a02e41488d473d3cf26607d3b84ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114618"
---
# <a name="istatsresume-method"></a><span data-ttu-id="e9245-103">IStats::Resume-Methode</span><span class="sxs-lookup"><span data-stu-id="e9245-103">IStats::Resume method</span></span>

<span data-ttu-id="e9245-104">Die **Resume-Methode** startet eine angehaltene Erfassung neu.</span><span class="sxs-lookup"><span data-stu-id="e9245-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9245-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9245-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="e9245-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9245-106">Parameters</span></span>

<span data-ttu-id="e9245-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e9245-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e9245-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9245-108">Return value</span></span>

<span data-ttu-id="e9245-109">Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="e9245-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e9245-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="e9245-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="e9245-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e9245-111">Return code</span></span>                                                                                                | <span data-ttu-id="e9245-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9245-112">Description</span></span>                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e9245-113"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="e9245-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="e9245-114">Das NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="e9245-114">The NPP is not connected to the network.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="e9245-115"><dt>**NMERR \_ CAPTURE \_ NOT \_ PAUSED**</dt></span><span class="sxs-lookup"><span data-stu-id="e9245-115"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="e9245-116">Die Erfassung wird nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="e9245-116">The capture is not paused.</span></span> <span data-ttu-id="e9245-117">Rufen Sie die [IStats::P ause-Methode](istats-pause.md) auf, um die Erfassung vorübergehend zu beenden.</span><span class="sxs-lookup"><span data-stu-id="e9245-117">Call the [IStats::Pause](istats-pause.md) method to temporarily stop the capture.</span></span><br/>                     |
| <dl> <span data-ttu-id="e9245-118"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="e9245-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="e9245-119">Das NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="e9245-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="e9245-120">Rufen Sie die [IStats::Connect-Methode](istats-connect.md) auf, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="e9245-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="e9245-121"><dt>**NMERR \_ NOT \_ STATS \_ ONLY**</dt></span><span class="sxs-lookup"><span data-stu-id="e9245-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl>     | <span data-ttu-id="e9245-122">Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IStats::Connect-Methode.](istats-connect.md)</span><span class="sxs-lookup"><span data-stu-id="e9245-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="e9245-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9245-123">Remarks</span></span>

<span data-ttu-id="e9245-124">Während sich die Erfassung in einem angehaltenen Zustand befindet, werden neue Daten erst erfasst, wenn die IStats::Resume-Methode aufgerufen wird, um die Erfassung neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="e9245-124">While the capture is in a paused state, new data is not captured until the IStats::Resume method is called to restart the capture.</span></span>

<span data-ttu-id="e9245-125">Wenn Sie die Methoden **Anhalten** und **Fortsetzen** verwenden, um die Erfassung zu steuern, fügt Netzwerkmonitor den vorhandenen Statistiken für die aktuelle Erfassung weiterhin [*Konversationsstatistiken*](c.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="e9245-125">When using the **Pause** and **Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="e9245-126">Rufen Sie [IStats::Stop](istats-stop.md)auf, um die Erfassung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="e9245-126">To stop the capture, call [IStats::Stop](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9245-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9245-127">Requirements</span></span>



| <span data-ttu-id="e9245-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9245-128">Requirement</span></span> | <span data-ttu-id="e9245-129">Wert</span><span class="sxs-lookup"><span data-stu-id="e9245-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9245-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9245-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e9245-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9245-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="e9245-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9245-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e9245-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9245-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="e9245-134">Header</span><span class="sxs-lookup"><span data-stu-id="e9245-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9245-135"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="e9245-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="e9245-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e9245-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9245-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9245-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9245-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e9245-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9245-139">IStats</span><span class="sxs-lookup"><span data-stu-id="e9245-139">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="e9245-140">IStats::Connect</span><span class="sxs-lookup"><span data-stu-id="e9245-140">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="e9245-141">IStats::P ause</span><span class="sxs-lookup"><span data-stu-id="e9245-141">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="e9245-142">IStats::Stop</span><span class="sxs-lookup"><span data-stu-id="e9245-142">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




