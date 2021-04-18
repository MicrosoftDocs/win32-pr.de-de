---
description: Die getcontrolstate-Methode ruft den Status der Erfassung ab, der angibt, ob die Erfassung ausgeführt wird oder angehalten wird.
ms.assetid: 0faf2300-d9ff-4fe0-9d50-18beafd1daea
title: 'IStats:: getcontrolstate-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a83b5d20461b28b7022bfdc3ddbf3d5d92149c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366270"
---
# <a name="istatsgetcontrolstate-method"></a><span data-ttu-id="b6017-103">IStats:: getcontrolstate-Methode</span><span class="sxs-lookup"><span data-stu-id="b6017-103">IStats::GetControlState method</span></span>

<span data-ttu-id="b6017-104">Die **getcontrolstate** -Methode ruft den Status der [*Erfassung*](c.md)ab, der angibt, ob die Erfassung ausgeführt wird oder angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="b6017-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6017-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6017-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="b6017-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6017-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6017-107">*Isrunnning* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b6017-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6017-108">Indikator, dass die aktuelle Erfassung ausgeführt wird, einschließlich, wenn die Erfassung angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="b6017-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="b6017-109">*IsPaused* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b6017-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6017-110">Indikator, dass die aktuelle Erfassung angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="b6017-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6017-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6017-111">Return value</span></span>

<span data-ttu-id="b6017-112">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b6017-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b6017-113">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="b6017-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="b6017-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b6017-114">Return code</span></span>                                                                                            | <span data-ttu-id="b6017-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6017-115">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b6017-116"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="b6017-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="b6017-117">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="b6017-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="b6017-118">Wenden Sie [iStats:: Connect](istats-connect.md) an, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="b6017-118">Call [IStats::Connect](istats-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="b6017-119"><dt>**nmerr \_ nicht \_ \_ nur Statistiken**</dt></span><span class="sxs-lookup"><span data-stu-id="b6017-119"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="b6017-120">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iStats:: Connect](istats-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b6017-120">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="b6017-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6017-121">Remarks</span></span>

<span data-ttu-id="b6017-122">Diese Methode kann jedes Mal aufgerufen werden, wenn der NPP mit dem Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="b6017-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="b6017-123">Mit dieser Methode können Sie herausfinden, ob eine Erfassung ausgeführt wird, ob die Erfassung angehalten wurde oder ob die Erfassung angehalten wurde, aber der npp ist nicht getrennt.</span><span class="sxs-lookup"><span data-stu-id="b6017-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is not disconnected.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6017-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6017-124">Requirements</span></span>



| <span data-ttu-id="b6017-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6017-125">Requirement</span></span> | <span data-ttu-id="b6017-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b6017-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6017-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6017-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b6017-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6017-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="b6017-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6017-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b6017-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6017-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="b6017-131">Header</span><span class="sxs-lookup"><span data-stu-id="b6017-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6017-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6017-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="b6017-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b6017-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6017-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6017-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6017-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6017-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6017-136">IStats</span><span class="sxs-lookup"><span data-stu-id="b6017-136">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="b6017-137">IStats:: Connect</span><span class="sxs-lookup"><span data-stu-id="b6017-137">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="b6017-138">IStats::P ause</span><span class="sxs-lookup"><span data-stu-id="b6017-138">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="b6017-139">Istatus SC:: Start</span><span class="sxs-lookup"><span data-stu-id="b6017-139">IStatsC::Start</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="b6017-140">Istatusc:: Beendigung</span><span class="sxs-lookup"><span data-stu-id="b6017-140">IStatsC::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




