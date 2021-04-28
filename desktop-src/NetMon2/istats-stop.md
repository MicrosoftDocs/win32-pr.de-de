---
description: 'IStats::Stop-Methode: Die Stop-Methode beendet die aktuelle Erfassung.'
ms.assetid: 3aeeb29e-e174-46a2-82bb-44c466b8db98
title: IStats::Stop-Methode (Netmon.h)
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
ms.openlocfilehash: ef51aff870a3193963b3802332112c51f1024826
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114608"
---
# <a name="istatsstop-method"></a><span data-ttu-id="03c08-103">IStats::Stop-Methode</span><span class="sxs-lookup"><span data-stu-id="03c08-103">IStats::Stop method</span></span>

<span data-ttu-id="03c08-104">Die **Stop-Methode** beendet die aktuelle Erfassung.</span><span class="sxs-lookup"><span data-stu-id="03c08-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="03c08-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="03c08-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a><span data-ttu-id="03c08-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="03c08-106">Parameters</span></span>

<span data-ttu-id="03c08-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="03c08-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03c08-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03c08-108">Return value</span></span>

<span data-ttu-id="03c08-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="03c08-109">If the method is successful the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="03c08-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="03c08-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="03c08-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="03c08-111">Return code</span></span>                                                                                            | <span data-ttu-id="03c08-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03c08-112">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="03c08-113"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="03c08-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="03c08-114">Der NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="03c08-114">The NPP is not connected to the network.</span></span> <span data-ttu-id="03c08-115">Rufen Sie [die IStats::Connect-Methode auf,](istats-connect.md) um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="03c08-115">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="03c08-116"><dt>**NMERR NOT CAPTURING (NMERR \_ WIRD NICHT \_ ERFASST)**</dt></span><span class="sxs-lookup"><span data-stu-id="03c08-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="03c08-117">Der NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="03c08-117">The NPP is not capturing data.</span></span> <span data-ttu-id="03c08-118">Rufen Sie die [IStats::Start-Methode auf,](istats-start.md) um die Erfassung zu starten.</span><span class="sxs-lookup"><span data-stu-id="03c08-118">Call the [IStats::Start](istats-start.md) method to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="03c08-119"><dt>**NMERR \_ NICHT \_ NUR STATISTIKEN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="03c08-119"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="03c08-120">Der NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IStats::Connect-Methode.](istats-connect.md)</span><span class="sxs-lookup"><span data-stu-id="03c08-120">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="03c08-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03c08-121">Remarks</span></span>

<span data-ttu-id="03c08-122">Stellen Sie beim Neustarten der Erfassung nach dem Aufruf von **IStats::Stop** sicher, dass Sie jedes Mal die [IStats::Configure-Methode](istats-configure.md) aufrufen, wenn Sie [IStats::Start](istats-start.md) aufrufen, um die Erfassung neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="03c08-122">When restarting the capture after **IStats::Stop** has been called, make sure you call the [IStats::Configure](istats-configure.md) method each time you call [IStats::Start](istats-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="03c08-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03c08-123">Requirements</span></span>



| <span data-ttu-id="03c08-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03c08-124">Requirement</span></span> | <span data-ttu-id="03c08-125">Wert</span><span class="sxs-lookup"><span data-stu-id="03c08-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03c08-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03c08-126">Minimum supported client</span></span><br/> | <span data-ttu-id="03c08-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03c08-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="03c08-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03c08-128">Minimum supported server</span></span><br/> | <span data-ttu-id="03c08-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03c08-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="03c08-130">Header</span><span class="sxs-lookup"><span data-stu-id="03c08-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="03c08-131"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="03c08-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="03c08-132">DLL</span><span class="sxs-lookup"><span data-stu-id="03c08-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03c08-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03c08-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03c08-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="03c08-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03c08-135">IStats</span><span class="sxs-lookup"><span data-stu-id="03c08-135">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="03c08-136">IStats::Connect</span><span class="sxs-lookup"><span data-stu-id="03c08-136">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="03c08-137">IStats::Configure</span><span class="sxs-lookup"><span data-stu-id="03c08-137">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="03c08-138">IStats::Start</span><span class="sxs-lookup"><span data-stu-id="03c08-138">IStats::Start</span></span>](istats-start.md)
</dt> </dl>

 

 




