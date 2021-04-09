---
description: Die getcontrolstate-Methode ruft den Status der Erfassung ab, der angibt, ob die Erfassung ausgeführt wird oder angehalten wird.
ms.assetid: ae0cf869-bf5b-4c23-a924-014554053c92
title: 'Untc:: getcontrolstate-Methode (Netmon. h)'
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
ms.openlocfilehash: d437d9463ed3225cd3a474e78220acf1f07af4bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864072"
---
# <a name="irtcgetcontrolstate-method"></a><span data-ttu-id="84e22-103">Untc:: getcontrolstate-Methode</span><span class="sxs-lookup"><span data-stu-id="84e22-103">IRTC::GetControlState method</span></span>

<span data-ttu-id="84e22-104">Die **getcontrolstate** -Methode ruft den Status der [*Erfassung*](c.md)ab, der angibt, ob die Erfassung ausgeführt wird oder angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="84e22-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="84e22-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="84e22-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="84e22-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="84e22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84e22-107">*Isrunnning* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="84e22-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84e22-108">Indikator, dass die aktuelle Erfassung ausgeführt wird, einschließlich, wenn die Erfassung angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="84e22-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="84e22-109">*IsPaused* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="84e22-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84e22-110">Indikator, dass die aktuelle Erfassung angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="84e22-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84e22-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84e22-111">Return value</span></span>

<span data-ttu-id="84e22-112">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="84e22-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="84e22-113">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="84e22-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="84e22-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="84e22-114">Return code</span></span>                                                                                          | <span data-ttu-id="84e22-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84e22-115">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="84e22-116"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="84e22-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="84e22-117">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="84e22-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="84e22-118">Wenden [Sie](irtc-connect.md) sich an, um den NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="84e22-118">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="84e22-119"><dt>**nmerr \_ nicht in \_ Echtzeit**</dt></span><span class="sxs-lookup"><span data-stu-id="84e22-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="84e22-120">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der Methode " [iritc:: Connect](irtc-connect.md) ".</span><span class="sxs-lookup"><span data-stu-id="84e22-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="84e22-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84e22-121">Remarks</span></span>

<span data-ttu-id="84e22-122">Diese Methode kann jedes Mal aufgerufen werden, wenn der NPP mit dem Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="84e22-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="84e22-123">Mit dieser Methode können Sie herausfinden, ob eine Erfassung ausgeführt wird, ob die Erfassung angehalten wurde oder ob die Erfassung angehalten wurde, aber der npp ist weiterhin verbunden.</span><span class="sxs-lookup"><span data-stu-id="84e22-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="84e22-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84e22-124">Requirements</span></span>



| <span data-ttu-id="84e22-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84e22-125">Requirement</span></span> | <span data-ttu-id="84e22-126">Wert</span><span class="sxs-lookup"><span data-stu-id="84e22-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84e22-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84e22-127">Minimum supported client</span></span><br/> | <span data-ttu-id="84e22-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84e22-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="84e22-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84e22-129">Minimum supported server</span></span><br/> | <span data-ttu-id="84e22-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84e22-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="84e22-131">Header</span><span class="sxs-lookup"><span data-stu-id="84e22-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="84e22-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="84e22-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="84e22-133">DLL</span><span class="sxs-lookup"><span data-stu-id="84e22-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84e22-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84e22-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84e22-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84e22-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84e22-136">"Iran"</span><span class="sxs-lookup"><span data-stu-id="84e22-136">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="84e22-137">Iran:: Connect</span><span class="sxs-lookup"><span data-stu-id="84e22-137">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="84e22-138">Iran::P ause</span><span class="sxs-lookup"><span data-stu-id="84e22-138">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="84e22-139">"Iran:: Start"</span><span class="sxs-lookup"><span data-stu-id="84e22-139">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="84e22-140">Iran:: Beendigung</span><span class="sxs-lookup"><span data-stu-id="84e22-140">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




