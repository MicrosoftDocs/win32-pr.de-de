---
description: 'IStats::GetControlState-Methode: Die GetControlState-Methode ruft den Zustand der Erfassung ab, der angibt, ob die Erfassung ausgeführt oder angehalten wird.'
ms.assetid: 0faf2300-d9ff-4fe0-9d50-18beafd1daea
title: IStats::GetControlState-Methode (Netmon.h)
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
ms.openlocfilehash: 25532293335756a872ef5104d5eef66027fe2ae4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098468"
---
# <a name="istatsgetcontrolstate-method"></a><span data-ttu-id="6c1d6-103">IStats::GetControlState-Methode</span><span class="sxs-lookup"><span data-stu-id="6c1d6-103">IStats::GetControlState method</span></span>

<span data-ttu-id="6c1d6-104">Die **GetControlState-Methode** ruft den Zustand der [*Erfassung*](c.md)ab, der angibt, ob die Erfassung ausgeführt oder angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="6c1d6-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c1d6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c1d6-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="6c1d6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c1d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c1d6-107">*IsRunnning* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6c1d6-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1d6-108">Indikator, dass die aktuelle Erfassung ausgeführt wird, einschließlich, wenn die Erfassung angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="6c1d6-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="6c1d6-109">*IsPaused* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6c1d6-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1d6-110">Indikator, dass die aktuelle Erfassung angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="6c1d6-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c1d6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c1d6-111">Return value</span></span>

<span data-ttu-id="6c1d6-112">Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="6c1d6-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6c1d6-113">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="6c1d6-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="6c1d6-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6c1d6-114">Return code</span></span>                                                                                            | <span data-ttu-id="6c1d6-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c1d6-115">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c1d6-116"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="6c1d6-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="6c1d6-117">Das NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="6c1d6-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="6c1d6-118">Rufen Sie [IStats::Connect](istats-connect.md) auf, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="6c1d6-118">Call [IStats::Connect](istats-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="6c1d6-119"><dt>**NMERR \_ NOT \_ STATS \_ ONLY**</dt></span><span class="sxs-lookup"><span data-stu-id="6c1d6-119"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="6c1d6-120">Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IStats::Connect-Methode.](istats-connect.md)</span><span class="sxs-lookup"><span data-stu-id="6c1d6-120">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="6c1d6-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c1d6-121">Remarks</span></span>

<span data-ttu-id="6c1d6-122">Diese Methode kann jedes Mal aufgerufen werden, wenn das NPP mit dem Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="6c1d6-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="6c1d6-123">Sie können diese Methode verwenden, um herauszufinden, ob eine Erfassung ausgeführt wird, ob die Erfassung angehalten wurde oder ob die Erfassung beendet wurde, das NPP jedoch nicht getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="6c1d6-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is not disconnected.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c1d6-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c1d6-124">Requirements</span></span>



| <span data-ttu-id="6c1d6-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c1d6-125">Requirement</span></span> | <span data-ttu-id="6c1d6-126">Wert</span><span class="sxs-lookup"><span data-stu-id="6c1d6-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c1d6-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c1d6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6c1d6-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c1d6-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="6c1d6-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c1d6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6c1d6-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c1d6-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="6c1d6-131">Header</span><span class="sxs-lookup"><span data-stu-id="6c1d6-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c1d6-132"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="6c1d6-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="6c1d6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6c1d6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c1d6-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c1d6-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c1d6-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6c1d6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c1d6-136">IStats</span><span class="sxs-lookup"><span data-stu-id="6c1d6-136">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="6c1d6-137">IStats::Connect</span><span class="sxs-lookup"><span data-stu-id="6c1d6-137">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="6c1d6-138">IStats::P ause</span><span class="sxs-lookup"><span data-stu-id="6c1d6-138">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="6c1d6-139">IStatsC::Start</span><span class="sxs-lookup"><span data-stu-id="6c1d6-139">IStatsC::Start</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="6c1d6-140">IStatsC::Stop</span><span class="sxs-lookup"><span data-stu-id="6c1d6-140">IStatsC::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




