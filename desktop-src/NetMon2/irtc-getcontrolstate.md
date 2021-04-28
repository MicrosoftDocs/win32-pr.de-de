---
description: 'IRTC::GetControlState-Methode: Die GetControlState-Methode ruft den Zustand der Erfassung ab, der angibt, ob die Erfassung ausgeführt oder angehalten wird.'
ms.assetid: ae0cf869-bf5b-4c23-a924-014554053c92
title: IRTC::GetControlState-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d2e41ad3e4119fffbada26fe3ebebdfe3bf82043
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110708"
---
# <a name="irtcgetcontrolstate-method"></a><span data-ttu-id="7c382-103">IRTC::GetControlState-Methode</span><span class="sxs-lookup"><span data-stu-id="7c382-103">IRTC::GetControlState method</span></span>

<span data-ttu-id="7c382-104">Die **GetControlState-Methode** ruft den Zustand der [*Erfassung*](c.md)ab, der angibt, ob die Erfassung ausgeführt oder angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="7c382-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c382-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c382-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="7c382-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c382-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c382-107">*IsRunnning* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7c382-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c382-108">Indikator, dass die aktuelle Erfassung ausgeführt wird, einschließlich, wenn die Erfassung angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="7c382-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="7c382-109">*IsPaused* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7c382-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c382-110">Indikator, dass die aktuelle Erfassung angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="7c382-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c382-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c382-111">Return value</span></span>

<span data-ttu-id="7c382-112">Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="7c382-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="7c382-113">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="7c382-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="7c382-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7c382-114">Return code</span></span>                                                                                          | <span data-ttu-id="7c382-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c382-115">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7c382-116"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="7c382-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="7c382-117">Das NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="7c382-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="7c382-118">Rufen Sie [IRTC::Connect](irtc-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="7c382-118">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="7c382-119"><dt>**NMERR \_ NOT \_ REALTIME**</dt></span><span class="sxs-lookup"><span data-stu-id="7c382-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="7c382-120">Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IRTC::Connect-Methode.](irtc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="7c382-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="7c382-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c382-121">Remarks</span></span>

<span data-ttu-id="7c382-122">Diese Methode kann jedes Mal aufgerufen werden, wenn das NPP mit dem Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="7c382-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="7c382-123">Sie können diese Methode verwenden, um herauszufinden, ob eine Erfassung ausgeführt wird, ob die Erfassung angehalten wurde oder ob die Erfassung beendet wurde, aber das NPP noch verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="7c382-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c382-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c382-124">Requirements</span></span>



| <span data-ttu-id="7c382-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c382-125">Requirement</span></span> | <span data-ttu-id="7c382-126">Wert</span><span class="sxs-lookup"><span data-stu-id="7c382-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c382-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c382-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7c382-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c382-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="7c382-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c382-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7c382-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c382-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="7c382-131">Header</span><span class="sxs-lookup"><span data-stu-id="7c382-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c382-132"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="7c382-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="7c382-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7c382-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c382-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c382-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c382-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7c382-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c382-136">IRTC</span><span class="sxs-lookup"><span data-stu-id="7c382-136">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="7c382-137">IRTC::Connect</span><span class="sxs-lookup"><span data-stu-id="7c382-137">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="7c382-138">IRTC::P ause</span><span class="sxs-lookup"><span data-stu-id="7c382-138">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="7c382-139">IRTC::Start</span><span class="sxs-lookup"><span data-stu-id="7c382-139">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="7c382-140">IRTC::Stop</span><span class="sxs-lookup"><span data-stu-id="7c382-140">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




