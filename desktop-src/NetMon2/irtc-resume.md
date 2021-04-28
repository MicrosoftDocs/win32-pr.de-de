---
description: 'IRTC::Resume-Methode: Die Resume-Methode startet eine angehaltene Erfassung neu.'
ms.assetid: 685dfdee-3bd0-44b3-ac4f-c9960cf77c5c
title: IRTC::Resume-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 55e5cb66eecbee96df9573e9347d1f32e3508d2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110562"
---
# <a name="irtcresume-method"></a><span data-ttu-id="3e652-103">IRTC::Resume-Methode</span><span class="sxs-lookup"><span data-stu-id="3e652-103">IRTC::Resume method</span></span>

<span data-ttu-id="3e652-104">Die **Resume-Methode** startet eine angehaltene Erfassung neu.</span><span class="sxs-lookup"><span data-stu-id="3e652-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e652-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e652-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="3e652-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e652-106">Parameters</span></span>

<span data-ttu-id="3e652-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3e652-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3e652-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e652-108">Return value</span></span>

<span data-ttu-id="3e652-109">Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="3e652-109">If the method is successful the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3e652-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="3e652-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="3e652-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3e652-111">Return code</span></span>                                                                                                | <span data-ttu-id="3e652-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e652-112">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e652-113"><dt>**NMERR \_ CAPTURE \_ NOT \_ PAUSED**</dt></span><span class="sxs-lookup"><span data-stu-id="3e652-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="3e652-114">Die Erfassung wird nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="3e652-114">The capture is not paused.</span></span> <span data-ttu-id="3e652-115">Rufen Sie [IRTC::P ause](irtc-pause.md) auf, um die Erfassung anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="3e652-115">Call [IRTC::Pause](irtc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="3e652-116"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="3e652-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="3e652-117">Das NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="3e652-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="3e652-118">Rufen Sie [IRTC::Connect](irtc-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="3e652-118">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="3e652-119"><dt>**NMERR \_ NOT \_ REALTIME**</dt></span><span class="sxs-lookup"><span data-stu-id="3e652-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>        | <span data-ttu-id="3e652-120">Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IRTC::Connect-Methode.](irtc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="3e652-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="3e652-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e652-121">Remarks</span></span>

<span data-ttu-id="3e652-122">Während sich die Erfassung in einem angehaltenen Zustand befindet, werden neue Daten erst erfasst, wenn die Erfassung durch einen Aufruf der [IRTC::Resume-Methode](idelaydc-resume.md) neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="3e652-122">While the capture is in a paused state, new data is not captured until a call to the [IRTC::Resume](idelaydc-resume.md) method restarts the capture.</span></span>

<span data-ttu-id="3e652-123">Wenn Sie die Methoden **Anhalten** und **Fortsetzen** verwenden, um die Erfassung zu steuern, fügt Netzwerkmonitor den vorhandenen Statistiken für die aktuelle Erfassung weiterhin [*Konversationsstatistiken*](c.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="3e652-123">When using the **Pause** and **Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="3e652-124">Um die Erfassung zu beenden, rufen Sie die [IRTC::Stop-Methode](irtc-stop.md) auf.</span><span class="sxs-lookup"><span data-stu-id="3e652-124">To stop the capture, call the [IRTC::Stop](irtc-stop.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e652-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e652-125">Requirements</span></span>



| <span data-ttu-id="3e652-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e652-126">Requirement</span></span> | <span data-ttu-id="3e652-127">Wert</span><span class="sxs-lookup"><span data-stu-id="3e652-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e652-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e652-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3e652-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e652-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="3e652-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e652-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3e652-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e652-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="3e652-132">Header</span><span class="sxs-lookup"><span data-stu-id="3e652-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e652-133"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="3e652-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="3e652-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3e652-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e652-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e652-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e652-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3e652-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e652-137">IRTC</span><span class="sxs-lookup"><span data-stu-id="3e652-137">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="3e652-138">IRTC::Connect</span><span class="sxs-lookup"><span data-stu-id="3e652-138">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="3e652-139">IRTC::P ause</span><span class="sxs-lookup"><span data-stu-id="3e652-139">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="3e652-140">IRTC::Stop</span><span class="sxs-lookup"><span data-stu-id="3e652-140">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




