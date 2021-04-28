---
description: 'IDelaydC::GetControlState-Methode: Die GetControlState-Methode ruft den Zustand der Erfassung ab, der angibt, ob die Erfassung ausgeführt oder angehalten wird.'
ms.assetid: 21b7faaa-591f-4e15-b4e9-453ea690ab4a
title: IDelaydC::GetControlState-Methode (Netmon.h)
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
ms.openlocfilehash: 825112ec9a33ef176d5a69765837214249e33102
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110768"
---
# <a name="idelaydcgetcontrolstate-method"></a><span data-ttu-id="74bc0-103">IDelaydC::GetControlState-Methode</span><span class="sxs-lookup"><span data-stu-id="74bc0-103">IDelaydC::GetControlState method</span></span>

<span data-ttu-id="74bc0-104">Die **GetControlState-Methode** ruft den Zustand der [*Erfassung*](c.md)ab, der angibt, ob die Erfassung ausgeführt oder angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="74bc0-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="74bc0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="74bc0-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="74bc0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="74bc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74bc0-107">*IsRunnning* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="74bc0-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74bc0-108">Indikator, dass die aktuelle Erfassung ausgeführt wird, einschließlich, wenn die Erfassung angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="74bc0-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="74bc0-109">*IsPaused* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="74bc0-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74bc0-110">Indikator, dass die aktuelle Erfassung angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="74bc0-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74bc0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74bc0-111">Return value</span></span>

<span data-ttu-id="74bc0-112">Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="74bc0-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="74bc0-113">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="74bc0-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="74bc0-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="74bc0-114">Return code</span></span>                                                                                          | <span data-ttu-id="74bc0-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74bc0-115">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="74bc0-116"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="74bc0-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="74bc0-117">Das NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="74bc0-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="74bc0-118">Rufen Sie [IDelaydC::Connect](idelaydc-connect.md) auf, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="74bc0-118">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="74bc0-119"><dt>**NMERR \_ NICHT \_ VERZÖGERT**</dt></span><span class="sxs-lookup"><span data-stu-id="74bc0-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="74bc0-120">Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IDelaydC::Connect-Methode.](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="74bc0-120">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="74bc0-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74bc0-121">Remarks</span></span>

<span data-ttu-id="74bc0-122">Diese Methode kann jedes Mal aufgerufen werden, wenn das NPP mit dem Netzwerk verbunden ist, indem die [IDelaydC-Schnittstelle](idelaydc.md) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="74bc0-122">This method can be called any time the NPP is connected to the network by using the [IDelaydC](idelaydc.md) interface.</span></span> <span data-ttu-id="74bc0-123">Sie können diese Methode verwenden, um herauszufinden, ob eine Erfassung ausgeführt wird, ob die Erfassung angehalten wurde oder ob die Erfassung beendet wurde, das NPP jedoch nicht getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="74bc0-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is not disconnected.</span></span>

<span data-ttu-id="74bc0-124">Die Methoden zum Starten, Anhalten und Beenden der Erfassung sind unten in der Liste Siehe auch aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="74bc0-124">The methods used to start, pause, and, stop the capture are listed in the See Also list below.</span></span>

## <a name="requirements"></a><span data-ttu-id="74bc0-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74bc0-125">Requirements</span></span>



| <span data-ttu-id="74bc0-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74bc0-126">Requirement</span></span> | <span data-ttu-id="74bc0-127">Wert</span><span class="sxs-lookup"><span data-stu-id="74bc0-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74bc0-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74bc0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="74bc0-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74bc0-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="74bc0-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74bc0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="74bc0-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74bc0-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="74bc0-132">Header</span><span class="sxs-lookup"><span data-stu-id="74bc0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="74bc0-133"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="74bc0-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="74bc0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="74bc0-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74bc0-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74bc0-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74bc0-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="74bc0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74bc0-137">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="74bc0-137">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="74bc0-138">IDelaydC::Connect</span><span class="sxs-lookup"><span data-stu-id="74bc0-138">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="74bc0-139">IDelaydC::P ause</span><span class="sxs-lookup"><span data-stu-id="74bc0-139">IDelaydC::Pause</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="74bc0-140">IDelaydC::Start</span><span class="sxs-lookup"><span data-stu-id="74bc0-140">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="74bc0-141">IDelaydC::Stop</span><span class="sxs-lookup"><span data-stu-id="74bc0-141">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




