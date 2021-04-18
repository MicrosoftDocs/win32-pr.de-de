---
description: Die Methode "beenden" beendet die aktuelle Erfassung.
ms.assetid: 3aeeb29e-e174-46a2-82bb-44c466b8db98
title: 'IStats:: stopmethode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 7b7b58527e7bde0c3bbdec4fc162b705dd178c10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345772"
---
# <a name="istatsstop-method"></a><span data-ttu-id="81312-103">IStats:: stopmethode</span><span class="sxs-lookup"><span data-stu-id="81312-103">IStats::Stop method</span></span>

<span data-ttu-id="81312-104">Die Methode " **Beenden** " beendet die aktuelle Erfassung.</span><span class="sxs-lookup"><span data-stu-id="81312-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="81312-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="81312-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a><span data-ttu-id="81312-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="81312-106">Parameters</span></span>

<span data-ttu-id="81312-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="81312-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81312-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81312-108">Return value</span></span>

<span data-ttu-id="81312-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="81312-109">If the method is successful the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="81312-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="81312-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="81312-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="81312-111">Return code</span></span>                                                                                            | <span data-ttu-id="81312-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81312-112">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="81312-113"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="81312-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="81312-114">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="81312-114">The NPP is not connected to the network.</span></span> <span data-ttu-id="81312-115">Wenden Sie die [iStats:: Connect](istats-connect.md) -Methode an, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="81312-115">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="81312-116"><dt>**nmerr wird \_ nicht \_ erfasst**</dt></span><span class="sxs-lookup"><span data-stu-id="81312-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="81312-117">Der NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="81312-117">The NPP is not capturing data.</span></span> <span data-ttu-id="81312-118">Ruft die [iStats:: Start](istats-start.md) -Methode auf, um die Erfassung zu starten.</span><span class="sxs-lookup"><span data-stu-id="81312-118">Call the [IStats::Start](istats-start.md) method to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="81312-119"><dt>**nmerr \_ nicht \_ \_ nur Statistiken**</dt></span><span class="sxs-lookup"><span data-stu-id="81312-119"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="81312-120">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iStats:: Connect](istats-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="81312-120">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="81312-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81312-121">Remarks</span></span>

<span data-ttu-id="81312-122">Wenn Sie die Erfassung nach dem Aufrufen von **iStats:: beenden** neu starten, stellen Sie sicher, dass Sie jedes Mal, wenn Sie [iStats:: Start](istats-start.md) aufrufen, die [iStats:: Configure](istats-configure.md) -Methode aufrufen, um die Erfassung neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="81312-122">When restarting the capture after **IStats::Stop** has been called, make sure you call the [IStats::Configure](istats-configure.md) method each time you call [IStats::Start](istats-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="81312-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81312-123">Requirements</span></span>



| <span data-ttu-id="81312-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81312-124">Requirement</span></span> | <span data-ttu-id="81312-125">Wert</span><span class="sxs-lookup"><span data-stu-id="81312-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81312-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81312-126">Minimum supported client</span></span><br/> | <span data-ttu-id="81312-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81312-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="81312-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81312-128">Minimum supported server</span></span><br/> | <span data-ttu-id="81312-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81312-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="81312-130">Header</span><span class="sxs-lookup"><span data-stu-id="81312-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="81312-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="81312-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="81312-132">DLL</span><span class="sxs-lookup"><span data-stu-id="81312-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81312-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81312-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81312-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81312-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81312-135">IStats</span><span class="sxs-lookup"><span data-stu-id="81312-135">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="81312-136">IStats:: Connect</span><span class="sxs-lookup"><span data-stu-id="81312-136">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="81312-137">IStats:: Configure</span><span class="sxs-lookup"><span data-stu-id="81312-137">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="81312-138">IStats:: Start</span><span class="sxs-lookup"><span data-stu-id="81312-138">IStats::Start</span></span>](istats-start.md)
</dt> </dl>

 

 




