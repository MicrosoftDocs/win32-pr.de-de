---
description: Mit der Resume-Methode wird eine angehaltene Erfassung neu gestartet.
ms.assetid: 685dfdee-3bd0-44b3-ac4f-c9960cf77c5c
title: 'Untc:: Resume-Methode (Netmon. h)'
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
ms.openlocfilehash: 991f70944b44ce13641318219788d9d6122b15c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343825"
---
# <a name="irtcresume-method"></a><span data-ttu-id="421f6-103">Untc:: Resume-Methode</span><span class="sxs-lookup"><span data-stu-id="421f6-103">IRTC::Resume method</span></span>

<span data-ttu-id="421f6-104">Mit der **Resume** -Methode wird eine angehaltene Erfassung neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="421f6-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="421f6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="421f6-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="421f6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="421f6-106">Parameters</span></span>

<span data-ttu-id="421f6-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="421f6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="421f6-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="421f6-108">Return value</span></span>

<span data-ttu-id="421f6-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="421f6-109">If the method is successful the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="421f6-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="421f6-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="421f6-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="421f6-111">Return code</span></span>                                                                                                | <span data-ttu-id="421f6-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="421f6-112">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="421f6-113"><dt>**nmerr- \_ Erfassung wurde \_ nicht \_ angehalten.**</dt></span><span class="sxs-lookup"><span data-stu-id="421f6-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="421f6-114">Die Erfassung wird nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="421f6-114">The capture is not paused.</span></span> <span data-ttu-id="421f6-115">Wenden Sie die [:P ause](irtc-pause.md) an, um die Erfassung anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="421f6-115">Call [IRTC::Pause](irtc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="421f6-116"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="421f6-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="421f6-117">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="421f6-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="421f6-118">Wenden [Sie](irtc-connect.md) sich an, um den NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="421f6-118">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="421f6-119"><dt>**nmerr \_ nicht in \_ Echtzeit**</dt></span><span class="sxs-lookup"><span data-stu-id="421f6-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>        | <span data-ttu-id="421f6-120">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der Methode " [iritc:: Connect](irtc-connect.md) ".</span><span class="sxs-lookup"><span data-stu-id="421f6-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="421f6-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="421f6-121">Remarks</span></span>

<span data-ttu-id="421f6-122">Während sich die Erfassung in einem angehaltenen Zustand befindet, werden neue Daten erst aufgezeichnet, wenn ein Aufrufe der Methode " [untc:: Resume](idelaydc-resume.md) " die Erfassung neu startet.</span><span class="sxs-lookup"><span data-stu-id="421f6-122">While the capture is in a paused state, new data is not captured until a call to the [IRTC::Resume](idelaydc-resume.md) method restarts the capture.</span></span>

<span data-ttu-id="421f6-123">Bei der Verwendung der Methoden  **zum Anhalten und fort** setzen zum Steuern der Erfassung werden von Netzwerkmonitor weiterhin [*Konversations Statistiken*](c.md) zu den vorhandenen Statistiken für die aktuelle Erfassung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="421f6-123">When using the **Pause** and **Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="421f6-124">Um die Erfassung zu verhindern, wenden Sie die Methode " [untc:: stopand](irtc-stop.md) " an.</span><span class="sxs-lookup"><span data-stu-id="421f6-124">To stop the capture, call the [IRTC::Stop](irtc-stop.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="421f6-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="421f6-125">Requirements</span></span>



| <span data-ttu-id="421f6-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="421f6-126">Requirement</span></span> | <span data-ttu-id="421f6-127">Wert</span><span class="sxs-lookup"><span data-stu-id="421f6-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="421f6-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="421f6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="421f6-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="421f6-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="421f6-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="421f6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="421f6-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="421f6-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="421f6-132">Header</span><span class="sxs-lookup"><span data-stu-id="421f6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="421f6-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="421f6-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="421f6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="421f6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="421f6-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="421f6-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="421f6-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="421f6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="421f6-137">"Iran"</span><span class="sxs-lookup"><span data-stu-id="421f6-137">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="421f6-138">Iran:: Connect</span><span class="sxs-lookup"><span data-stu-id="421f6-138">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="421f6-139">Iran::P ause</span><span class="sxs-lookup"><span data-stu-id="421f6-139">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="421f6-140">Iran:: Beendigung</span><span class="sxs-lookup"><span data-stu-id="421f6-140">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




