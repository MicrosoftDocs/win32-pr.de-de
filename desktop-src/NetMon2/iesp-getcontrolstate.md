---
description: 'IESP::GetControlState-Methode: Die GetControlState-Methode ruft den Zustand der Erfassung ab, der angibt, ob die Erfassung ausgeführt wird oder angehalten wurde.'
ms.assetid: 19cc3095-3aa3-4482-95f5-959b19f76cea
title: IESP::GetControlState-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b007eb6824ee3e65cdf8195914bbff3a50c39b2c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114678"
---
# <a name="iespgetcontrolstate-method"></a><span data-ttu-id="2fe2d-103">IESP::GetControlState-Methode</span><span class="sxs-lookup"><span data-stu-id="2fe2d-103">IESP::GetControlState method</span></span>

<span data-ttu-id="2fe2d-104">Die **GetControlState-Methode** ruft den Zustand der Erfassung [*ab,*](c.md)die angibt, ob die Erfassung ausgeführt wird oder angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="2fe2d-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fe2d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fe2d-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="2fe2d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fe2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fe2d-107">*IsRunnning* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2fe2d-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fe2d-108">Gibt an, dass die aktuelle Erfassung ausgeführt wird, einschließlich, ob die Erfassung angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="2fe2d-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="2fe2d-109">*IsPaused* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2fe2d-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fe2d-110">Gibt an, dass die aktuelle Erfassung angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="2fe2d-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fe2d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2fe2d-111">Return value</span></span>

<span data-ttu-id="2fe2d-112">Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="2fe2d-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2fe2d-113">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="2fe2d-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="2fe2d-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2fe2d-114">Return code</span></span>                                                                                          | <span data-ttu-id="2fe2d-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2fe2d-115">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2fe2d-116"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="2fe2d-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="2fe2d-117">Der NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="2fe2d-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="2fe2d-118">Rufen [Sie IESP::Connect auf,](iesp-connect.md) um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="2fe2d-118">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="2fe2d-119"><dt>**NMERR \_ NICHT \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="2fe2d-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="2fe2d-120">Das NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IESP::Connect-Methode.](iesp-connect.md)</span><span class="sxs-lookup"><span data-stu-id="2fe2d-120">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="2fe2d-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fe2d-121">Remarks</span></span>

<span data-ttu-id="2fe2d-122">Diese Methode kann jedes Mal aufgerufen werden, wenn die NPP mit dem Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="2fe2d-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="2fe2d-123">Mit dieser Methode können Sie herausfinden, ob eine Erfassung ausgeführt wird, ob die Erfassung angehalten wurde oder ob die Erfassung beendet wurde, die NPP aber weiterhin verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="2fe2d-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fe2d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2fe2d-124">Requirements</span></span>



| <span data-ttu-id="2fe2d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2fe2d-125">Requirement</span></span> | <span data-ttu-id="2fe2d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2fe2d-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fe2d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2fe2d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2fe2d-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2fe2d-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="2fe2d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2fe2d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2fe2d-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2fe2d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="2fe2d-131">Header</span><span class="sxs-lookup"><span data-stu-id="2fe2d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fe2d-132"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="2fe2d-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="2fe2d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2fe2d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fe2d-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fe2d-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fe2d-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2fe2d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fe2d-136">IESP</span><span class="sxs-lookup"><span data-stu-id="2fe2d-136">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="2fe2d-137">IESP::Connect</span><span class="sxs-lookup"><span data-stu-id="2fe2d-137">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="2fe2d-138">IESP::P ause</span><span class="sxs-lookup"><span data-stu-id="2fe2d-138">IESP::Pause</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="2fe2d-139">IESP::Start</span><span class="sxs-lookup"><span data-stu-id="2fe2d-139">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="2fe2d-140">IESP::Stop</span><span class="sxs-lookup"><span data-stu-id="2fe2d-140">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




