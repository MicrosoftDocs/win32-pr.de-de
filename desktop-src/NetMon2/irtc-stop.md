---
description: Die Methode "beenden" beendet die aktuelle Erfassung.
ms.assetid: 64a80ff1-5a48-4be8-835d-a3d304ebb324
title: 'Untc:: stopmethode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: f25bf9d56a6f41acefad9a552dd2f591158bc74e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345280"
---
# <a name="irtcstop-method"></a><span data-ttu-id="ea0f6-103">Untc:: stopmethode</span><span class="sxs-lookup"><span data-stu-id="ea0f6-103">IRTC::Stop method</span></span>

<span data-ttu-id="ea0f6-104">Die Methode " **Beenden** " beendet die aktuelle Erfassung.</span><span class="sxs-lookup"><span data-stu-id="ea0f6-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea0f6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea0f6-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a><span data-ttu-id="ea0f6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea0f6-106">Parameters</span></span>

<span data-ttu-id="ea0f6-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ea0f6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ea0f6-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea0f6-108">Return value</span></span>

<span data-ttu-id="ea0f6-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="ea0f6-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ea0f6-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="ea0f6-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="ea0f6-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ea0f6-111">Return code</span></span>                                                                                          | <span data-ttu-id="ea0f6-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea0f6-112">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ea0f6-113"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="ea0f6-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="ea0f6-114">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="ea0f6-114">The NPP is not connected to the network.</span></span> <span data-ttu-id="ea0f6-115">Wenden [Sie](irtc-connect.md) sich an, um den NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="ea0f6-115">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="ea0f6-116"><dt>**nmerr wird \_ nicht \_ erfasst**</dt></span><span class="sxs-lookup"><span data-stu-id="ea0f6-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="ea0f6-117">Der NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="ea0f6-117">The NPP is not capturing data.</span></span> <span data-ttu-id="ea0f6-118">Wenden Sie zum Starten der Erfassung den Befehl " [irren:: Start](irtc-start.md) " an.</span><span class="sxs-lookup"><span data-stu-id="ea0f6-118">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="ea0f6-119"><dt>**nmerr \_ nicht in \_ Echtzeit**</dt></span><span class="sxs-lookup"><span data-stu-id="ea0f6-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="ea0f6-120">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der Methode " [iritc:: Connect](irtc-connect.md) ".</span><span class="sxs-lookup"><span data-stu-id="ea0f6-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="ea0f6-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea0f6-121">Remarks</span></span>

<span data-ttu-id="ea0f6-122">Wenn Sie die Erfassung nach dem Aufrufen der Methode " **untc:: beenden** " neu starten, müssen Sie bei jedem Aufrufen von " [untc:: Start](irtc-start.md) " den Befehl " [iritc:: Configure](irtc-configure.md) " aufrufen, um die Erfassung neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="ea0f6-122">When you restart the capture after calling the **IRTC::Stop** method, make sure to call [IRTC::Configure](irtc-configure.md) each time you call [IRTC::Start](irtc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea0f6-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea0f6-123">Requirements</span></span>



| <span data-ttu-id="ea0f6-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea0f6-124">Requirement</span></span> | <span data-ttu-id="ea0f6-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ea0f6-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea0f6-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea0f6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ea0f6-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea0f6-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="ea0f6-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea0f6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ea0f6-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea0f6-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="ea0f6-130">Header</span><span class="sxs-lookup"><span data-stu-id="ea0f6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea0f6-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea0f6-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="ea0f6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ea0f6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea0f6-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea0f6-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea0f6-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea0f6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea0f6-135">"Iran"</span><span class="sxs-lookup"><span data-stu-id="ea0f6-135">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="ea0f6-136">Iran:: Connect</span><span class="sxs-lookup"><span data-stu-id="ea0f6-136">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="ea0f6-137">"Iran:: Configure"</span><span class="sxs-lookup"><span data-stu-id="ea0f6-137">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="ea0f6-138">"Iran:: Start"</span><span class="sxs-lookup"><span data-stu-id="ea0f6-138">IRTC::Start</span></span>](irtc-start.md)
</dt> </dl>

 

 




