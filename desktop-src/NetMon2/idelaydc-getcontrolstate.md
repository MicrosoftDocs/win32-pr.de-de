---
description: Die getcontrolstate-Methode ruft den Status der Erfassung ab, der angibt, ob die Erfassung ausgeführt wird oder angehalten wird.
ms.assetid: 21b7faaa-591f-4e15-b4e9-453ea690ab4a
title: 'Idelta-DC:: getcontrolstate-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8f5c3f084db788844f061ba2005d9c3ca38acef0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958705"
---
# <a name="idelaydcgetcontrolstate-method"></a><span data-ttu-id="56665-103">Idelta aydc:: getcontrolstate-Methode</span><span class="sxs-lookup"><span data-stu-id="56665-103">IDelaydC::GetControlState method</span></span>

<span data-ttu-id="56665-104">Die **getcontrolstate** -Methode ruft den Status der [*Erfassung*](c.md)ab, der angibt, ob die Erfassung ausgeführt wird oder angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="56665-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="56665-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="56665-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="56665-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56665-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56665-107">*Isrunnning* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="56665-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56665-108">Indikator, dass die aktuelle Erfassung ausgeführt wird, einschließlich, wenn die Erfassung angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="56665-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="56665-109">*IsPaused* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="56665-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56665-110">Indikator, dass die aktuelle Erfassung angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="56665-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56665-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56665-111">Return value</span></span>

<span data-ttu-id="56665-112">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="56665-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="56665-113">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="56665-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="56665-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="56665-114">Return code</span></span>                                                                                          | <span data-ttu-id="56665-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56665-115">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="56665-116"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="56665-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="56665-117">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="56665-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="56665-118">Wenden Sie [idelta-DC:: Connect](idelaydc-connect.md) an, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="56665-118">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="56665-119"><dt>**nmerr \_ nicht \_ verzögert**</dt></span><span class="sxs-lookup"><span data-stu-id="56665-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="56665-120">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [idelta aydc:: Connect](idelaydc-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="56665-120">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="56665-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56665-121">Remarks</span></span>

<span data-ttu-id="56665-122">Diese Methode kann jedes Mal aufgerufen werden, wenn die NPP über die [idelta-DC](idelaydc.md) -Schnittstelle mit dem Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="56665-122">This method can be called any time the NPP is connected to the network by using the [IDelaydC](idelaydc.md) interface.</span></span> <span data-ttu-id="56665-123">Mit dieser Methode können Sie herausfinden, ob eine Erfassung ausgeführt wird, ob die Erfassung angehalten wurde oder ob die Erfassung angehalten wurde, aber der npp ist nicht getrennt.</span><span class="sxs-lookup"><span data-stu-id="56665-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is not disconnected.</span></span>

<span data-ttu-id="56665-124">Die Methoden, die zum Starten, anhalten und Abbrechen der Erfassung verwendet werden, werden in der Liste siehe auch unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="56665-124">The methods used to start, pause, and, stop the capture are listed in the See Also list below.</span></span>

## <a name="requirements"></a><span data-ttu-id="56665-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56665-125">Requirements</span></span>



| <span data-ttu-id="56665-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56665-126">Requirement</span></span> | <span data-ttu-id="56665-127">Wert</span><span class="sxs-lookup"><span data-stu-id="56665-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56665-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56665-128">Minimum supported client</span></span><br/> | <span data-ttu-id="56665-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56665-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="56665-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56665-130">Minimum supported server</span></span><br/> | <span data-ttu-id="56665-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56665-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="56665-132">Header</span><span class="sxs-lookup"><span data-stu-id="56665-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="56665-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="56665-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="56665-134">DLL</span><span class="sxs-lookup"><span data-stu-id="56665-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56665-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56665-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56665-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56665-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56665-137">Idelta-DC</span><span class="sxs-lookup"><span data-stu-id="56665-137">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="56665-138">Idelta aydc:: Connect</span><span class="sxs-lookup"><span data-stu-id="56665-138">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="56665-139">Idelta aydc::P ause</span><span class="sxs-lookup"><span data-stu-id="56665-139">IDelaydC::Pause</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="56665-140">Idelta aydc:: Start</span><span class="sxs-lookup"><span data-stu-id="56665-140">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="56665-141">Idelta aydc:: Beendigung</span><span class="sxs-lookup"><span data-stu-id="56665-141">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




