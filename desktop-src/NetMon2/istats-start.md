---
description: Die Start-Methode startet eine Aufzeichnung.
ms.assetid: d4086e30-e5ed-4f29-90f0-d65125d9af6d
title: 'IStats:: Start-Methode (Netmon. h)'
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
ms.openlocfilehash: d58821ecc06e0a25d6a260bb2ba9393162dcdca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863035"
---
# <a name="istatsstart-method"></a><span data-ttu-id="6b511-103">IStats:: Start-Methode</span><span class="sxs-lookup"><span data-stu-id="6b511-103">IStats::Start method</span></span>

<span data-ttu-id="6b511-104">Die **Start** -Methode startet eine Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="6b511-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b511-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b511-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a><span data-ttu-id="6b511-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b511-106">Parameters</span></span>

<span data-ttu-id="6b511-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6b511-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6b511-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b511-108">Return value</span></span>

<span data-ttu-id="6b511-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6b511-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6b511-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="6b511-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="6b511-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6b511-111">Return code</span></span>                                                                                            | <span data-ttu-id="6b511-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b511-112">Description</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b511-113"><dt>**nmerr- \_ Erfassung \_ angehalten**</dt></span><span class="sxs-lookup"><span data-stu-id="6b511-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl>  | <span data-ttu-id="6b511-114">Die Erfassung wurde angehalten und muss beendet werden, bevor Sie neu gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6b511-114">The capture has paused and must be stopped before it can be restarted.</span></span> <span data-ttu-id="6b511-115">Zum Abbrechen der Erfassung wird die [iStats:: stopmethode](istats-stop.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6b511-115">Call the [IStats::Stop](istats-stop.md) method to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="6b511-116"><dt>**nmerr- \_ Erfassung**</dt></span><span class="sxs-lookup"><span data-stu-id="6b511-116"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>        | <span data-ttu-id="6b511-117">Die Erfassung wurde bereits gestartet.</span><span class="sxs-lookup"><span data-stu-id="6b511-117">The capture has already started.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="6b511-118"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="6b511-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="6b511-119">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="6b511-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="6b511-120">Wenden Sie die [iStats:: Connect](istats-connect.md) -Methode an, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="6b511-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/>           |
| <dl> <span data-ttu-id="6b511-121"><dt>**nmerr \_ nicht \_ \_ nur Statistiken**</dt></span><span class="sxs-lookup"><span data-stu-id="6b511-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="6b511-122">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iStats:: Connect](istats-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6b511-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="6b511-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b511-123">Remarks</span></span>

<span data-ttu-id="6b511-124">Wenn Sie die Erfassung mit der iStats:: Start-Methode und der [iStats:: beenden](istats-stop.md) -Methode neu starten, müssen Sie die [iStats:: Configure](istats-configure.md) -Methode zum Neukonfigurieren der Verbindung bei jedem Aufruf von iStats:: Start zum Neustarten der Datenerfassung verwenden.</span><span class="sxs-lookup"><span data-stu-id="6b511-124">When restarting the capture by using the IStats::Start and [IStats::Stop](istats-stop.md) methods, you must call the [IStats::Configure](istats-configure.md) method to reconfigure the connection each time you call IStats::Start to restart the data capture.</span></span>

> [!Note]  
> <span data-ttu-id="6b511-125">Sie können die Erfassung auch starten und Abbrechen, indem Sie die [iStats::P ause](istats-pause.md) -Methode und die [iStats:: Resume](istats-resume.md) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="6b511-125">You can also start and stop the capture by using the [IStats::Pause](istats-pause.md) and [IStats::Resume](istats-resume.md) methods.</span></span> <span data-ttu-id="6b511-126">Wenn Sie diese Methoden verwenden, werden die erfassten Daten in derselben Erfassungs Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6b511-126">When you use these methods, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6b511-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b511-127">Requirements</span></span>



| <span data-ttu-id="6b511-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b511-128">Requirement</span></span> | <span data-ttu-id="6b511-129">Wert</span><span class="sxs-lookup"><span data-stu-id="6b511-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b511-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b511-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6b511-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b511-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="6b511-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b511-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6b511-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b511-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="6b511-134">Header</span><span class="sxs-lookup"><span data-stu-id="6b511-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b511-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b511-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="6b511-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6b511-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b511-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b511-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b511-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b511-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b511-139">IStats</span><span class="sxs-lookup"><span data-stu-id="6b511-139">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="6b511-140">IStats:: Configure</span><span class="sxs-lookup"><span data-stu-id="6b511-140">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="6b511-141">IStats:: Connect</span><span class="sxs-lookup"><span data-stu-id="6b511-141">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="6b511-142">IStats::P ause</span><span class="sxs-lookup"><span data-stu-id="6b511-142">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="6b511-143">IStats:: Resume</span><span class="sxs-lookup"><span data-stu-id="6b511-143">IStats::Resume</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="6b511-144">IStats:: Beendigung</span><span class="sxs-lookup"><span data-stu-id="6b511-144">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




