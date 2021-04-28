---
description: 'IStats::Start-Methode: Die Start-Methode startet eine Erfassung.'
ms.assetid: d4086e30-e5ed-4f29-90f0-d65125d9af6d
title: IStats::Start-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 64f02529ba10d98092eb30a1bcc350d5c72049fc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094548"
---
# <a name="istatsstart-method"></a><span data-ttu-id="97264-103">IStats::Start-Methode</span><span class="sxs-lookup"><span data-stu-id="97264-103">IStats::Start method</span></span>

<span data-ttu-id="97264-104">Die **Start-Methode** startet eine Erfassung.</span><span class="sxs-lookup"><span data-stu-id="97264-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="97264-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="97264-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a><span data-ttu-id="97264-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="97264-106">Parameters</span></span>

<span data-ttu-id="97264-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="97264-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="97264-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97264-108">Return value</span></span>

<span data-ttu-id="97264-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="97264-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="97264-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="97264-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="97264-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="97264-111">Return code</span></span>                                                                                            | <span data-ttu-id="97264-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97264-112">Description</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="97264-113"><dt>**NMERR \_ CAPTURE \_ PAUSED**</dt></span><span class="sxs-lookup"><span data-stu-id="97264-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl>  | <span data-ttu-id="97264-114">Die Erfassung wurde angehalten und muss beendet werden, bevor sie neu gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="97264-114">The capture has paused and must be stopped before it can be restarted.</span></span> <span data-ttu-id="97264-115">Rufen Sie die [IStats::Stop-Methode auf,](istats-stop.md) um die Erfassung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="97264-115">Call the [IStats::Stop](istats-stop.md) method to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="97264-116"><dt>**NMERR-ERFASSUNG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="97264-116"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>        | <span data-ttu-id="97264-117">Die Erfassung wurde bereits gestartet.</span><span class="sxs-lookup"><span data-stu-id="97264-117">The capture has already started.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="97264-118"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="97264-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="97264-119">Der NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="97264-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="97264-120">Rufen Sie [die IStats::Connect-Methode auf,](istats-connect.md) um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="97264-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/>           |
| <dl> <span data-ttu-id="97264-121"><dt>**NMERR \_ NICHT \_ NUR STATISTIKEN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="97264-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="97264-122">Der NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IStats::Connect-Methode.](istats-connect.md)</span><span class="sxs-lookup"><span data-stu-id="97264-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="97264-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97264-123">Remarks</span></span>

<span data-ttu-id="97264-124">Wenn Sie die Erfassung mithilfe der Methoden IStats::Start und [IStats::Stop](istats-stop.md) neu starten, müssen Sie die [IStats::Configure-Methode](istats-configure.md) aufrufen, um die Verbindung jedes Mal neu zu konfigurieren, wenn Sie IStats::Start aufrufen, um die Datenerfassung neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="97264-124">When restarting the capture by using the IStats::Start and [IStats::Stop](istats-stop.md) methods, you must call the [IStats::Configure](istats-configure.md) method to reconfigure the connection each time you call IStats::Start to restart the data capture.</span></span>

> [!Note]  
> <span data-ttu-id="97264-125">Sie können die Erfassung auch mithilfe der [Methoden IStats::P ause und](istats-pause.md) [IStats::Resume](istats-resume.md) starten und beenden.</span><span class="sxs-lookup"><span data-stu-id="97264-125">You can also start and stop the capture by using the [IStats::Pause](istats-pause.md) and [IStats::Resume](istats-resume.md) methods.</span></span> <span data-ttu-id="97264-126">Wenn Sie diese Methoden verwenden, werden die erfassten Daten in derselben Erfassungsdatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="97264-126">When you use these methods, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="97264-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97264-127">Requirements</span></span>



| <span data-ttu-id="97264-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97264-128">Requirement</span></span> | <span data-ttu-id="97264-129">Wert</span><span class="sxs-lookup"><span data-stu-id="97264-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97264-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97264-130">Minimum supported client</span></span><br/> | <span data-ttu-id="97264-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97264-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="97264-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97264-132">Minimum supported server</span></span><br/> | <span data-ttu-id="97264-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97264-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="97264-134">Header</span><span class="sxs-lookup"><span data-stu-id="97264-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="97264-135"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="97264-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="97264-136">DLL</span><span class="sxs-lookup"><span data-stu-id="97264-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97264-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97264-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97264-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="97264-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97264-139">IStats</span><span class="sxs-lookup"><span data-stu-id="97264-139">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="97264-140">IStats::Configure</span><span class="sxs-lookup"><span data-stu-id="97264-140">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="97264-141">IStats::Connect</span><span class="sxs-lookup"><span data-stu-id="97264-141">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="97264-142">IStats::P ause</span><span class="sxs-lookup"><span data-stu-id="97264-142">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="97264-143">IStats::Resume</span><span class="sxs-lookup"><span data-stu-id="97264-143">IStats::Resume</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="97264-144">IStats::Stop</span><span class="sxs-lookup"><span data-stu-id="97264-144">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




