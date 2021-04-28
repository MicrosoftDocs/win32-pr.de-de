---
description: 'IESP::Resume-Methode: Die Resume-Methode startet eine angehaltene Erfassung neu.'
ms.assetid: 047ea5f8-de3d-40db-ada3-fc0ef4deccef
title: IESP::Resume-Methode (Netmon.h)
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
ms.openlocfilehash: 498beda4f2f6c61af918d542542c4ed7b789ba1a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084248"
---
# <a name="iespresume-method"></a><span data-ttu-id="e9aef-103">IESP::Resume-Methode</span><span class="sxs-lookup"><span data-stu-id="e9aef-103">IESP::Resume method</span></span>

<span data-ttu-id="e9aef-104">Die **Resume-Methode** startet eine angehaltene Erfassung neu.</span><span class="sxs-lookup"><span data-stu-id="e9aef-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9aef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9aef-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="e9aef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9aef-106">Parameters</span></span>

<span data-ttu-id="e9aef-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e9aef-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e9aef-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9aef-108">Return value</span></span>

<span data-ttu-id="e9aef-109">Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="e9aef-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e9aef-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="e9aef-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="e9aef-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e9aef-111">Return code</span></span>                                                                                                | <span data-ttu-id="e9aef-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9aef-112">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e9aef-113"><dt>**NMERR \_ CAPTURE \_ NOT \_ PAUSED**</dt></span><span class="sxs-lookup"><span data-stu-id="e9aef-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="e9aef-114">Die Erfassung wird nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="e9aef-114">The capture is not paused.</span></span> <span data-ttu-id="e9aef-115">Rufen Sie [**IESP::P ause**](iesp-pause.md) auf, um die Erfassung anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="e9aef-115">Call [**IESP::Pause**](iesp-pause.md) to pause the capture.</span></span><br/>                        |
| <dl> <span data-ttu-id="e9aef-116"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="e9aef-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="e9aef-117">Das NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="e9aef-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="e9aef-118">Rufen Sie [**IESP::Connect**](iesp-connect.md) auf, um eine Verbindung mit dem Netzwerk herzustellen.</span><span class="sxs-lookup"><span data-stu-id="e9aef-118">Call [**IESP::Connect**](iesp-connect.md) to connect to the network.</span></span><br/> |
| <dl> <span data-ttu-id="e9aef-119"><dt>**NMERR \_ NOT \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="e9aef-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>             | <span data-ttu-id="e9aef-120">Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [**IESP::Connect-Methode.**](iesp-connect.md)</span><span class="sxs-lookup"><span data-stu-id="e9aef-120">The NPP is connected to the network, but not with the [**IESP::Connect**](iesp-connect.md) method.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="e9aef-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9aef-121">Remarks</span></span>

<span data-ttu-id="e9aef-122">Während sich die Erfassung in einem angehaltenen Zustand befindet, werden der aktuellen [*Erfassungsdatei*](c.md) erst neue Daten hinzugefügt, wenn **IESP::Resume** aufgerufen wird, um die Erfassung neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="e9aef-122">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until **IESP::Resume** is called to restart the capture.</span></span> <span data-ttu-id="e9aef-123">Wenn **Anhalten** und **Fortsetzen** zum Beenden und Neustarten der Erfassung verwendet werden, werden alle erfassten Informationen in derselben Erfassungsdatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e9aef-123">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="e9aef-124">Wenn **Sie anhalten** und **fortsetzen** verwenden, um die Erfassung zu steuern, fügt Netzwerkmonitor den vorhandenen Statistiken für die aktuelle Erfassung weiterhin [*Konversationsstatistiken*](c.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="e9aef-124">When using **Pause** and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="e9aef-125">Um die Erfassung zu beenden, rufen Sie [**IESP::Stop**](iesp-stop.md)auf.</span><span class="sxs-lookup"><span data-stu-id="e9aef-125">To stop the capture, call [**IESP::Stop**](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9aef-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9aef-126">Requirements</span></span>



| <span data-ttu-id="e9aef-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9aef-127">Requirement</span></span> | <span data-ttu-id="e9aef-128">Wert</span><span class="sxs-lookup"><span data-stu-id="e9aef-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9aef-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9aef-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e9aef-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9aef-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="e9aef-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9aef-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e9aef-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9aef-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="e9aef-133">Header</span><span class="sxs-lookup"><span data-stu-id="e9aef-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9aef-134"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="e9aef-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="e9aef-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e9aef-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9aef-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9aef-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9aef-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e9aef-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9aef-138">IESP</span><span class="sxs-lookup"><span data-stu-id="e9aef-138">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="e9aef-139">**IESP::Connect**</span><span class="sxs-lookup"><span data-stu-id="e9aef-139">**IESP::Connect**</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="e9aef-140">**IESP::P ause**</span><span class="sxs-lookup"><span data-stu-id="e9aef-140">**IESP::Pause**</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="e9aef-141">**IESP::Stop**</span><span class="sxs-lookup"><span data-stu-id="e9aef-141">**IESP::Stop**</span></span>](iesp-stop.md)
</dt> </dl>

 

 




