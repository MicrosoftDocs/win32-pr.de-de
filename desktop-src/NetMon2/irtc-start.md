---
description: Die Start-Methode startet die Erfassung.
ms.assetid: 1f676e19-18ff-4c34-a83f-2723ff356be2
title: 'Untc:: Start-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 3ee30112baf7813c983230fb90cd15ea7f52e2bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864064"
---
# <a name="irtcstart-method"></a><span data-ttu-id="9f631-103">Untc:: Start-Methode</span><span class="sxs-lookup"><span data-stu-id="9f631-103">IRTC::Start method</span></span>

<span data-ttu-id="9f631-104">Die **Start** -Methode startet die Erfassung.</span><span class="sxs-lookup"><span data-stu-id="9f631-104">The **Start** method starts the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f631-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f631-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a><span data-ttu-id="9f631-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f631-106">Parameters</span></span>

<span data-ttu-id="9f631-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9f631-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f631-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f631-108">Return value</span></span>

<span data-ttu-id="9f631-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="9f631-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="9f631-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="9f631-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="9f631-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9f631-111">Return code</span></span>                                                                                           | <span data-ttu-id="9f631-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f631-112">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9f631-113"><dt>**nmerr- \_ Erfassung \_ angehalten**</dt></span><span class="sxs-lookup"><span data-stu-id="9f631-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="9f631-114">Die Erfassung befindet sich im angehaltenen Zustand und muss beendet werden, bevor Sie neu gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9f631-114">The capture is in a paused state and must be stopped before it can be restarted.</span></span> <span data-ttu-id="9f631-115">Zum Abbrechen der Erfassung wird der Befehl " [untc:: Beendigung](idelaydc-stop.md) " aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9f631-115">Call [IRTC::Stop](idelaydc-stop.md) to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="9f631-116"><dt>**nmerr- \_ Erfassung**</dt></span><span class="sxs-lookup"><span data-stu-id="9f631-116"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="9f631-117">Die Erfassung wurde bereits gestartet.</span><span class="sxs-lookup"><span data-stu-id="9f631-117">The capture is already started.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="9f631-118"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="9f631-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="9f631-119">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="9f631-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="9f631-120">Wenden [Sie](irtc-connect.md) sich an, um den NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="9f631-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/>                         |
| <dl> <span data-ttu-id="9f631-121"><dt>**nmerr \_ nicht in \_ Echtzeit**</dt></span><span class="sxs-lookup"><span data-stu-id="9f631-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>   | <span data-ttu-id="9f631-122">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der Methode " [iritc:: Connect](irtc-connect.md) ".</span><span class="sxs-lookup"><span data-stu-id="9f631-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="9f631-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f631-123">Remarks</span></span>

<span data-ttu-id="9f631-124">Wenn Sie die Erfassung mit den Methoden "untc:: Start" und " [untc:: beenden](irtc-stop.md) " neu starten, müssen Sie die Methode " [iritc:: Configure](irtc-configure.md) " zum erneuten Konfigurieren der Verbindung bei jedem Aufruf von "untc:: Start" zum Neustarten der Datenerfassung verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f631-124">When you restart the capture by using the IRTC::Start and [IRTC::Stop](irtc-stop.md) methods, you must call the [IRTC::Configure](irtc-configure.md) method to reconfigure the connection each time you call IRTC::Start to restart the data capture.</span></span>

> [!Note]  
> <span data-ttu-id="9f631-125">Sie können die Erfassung auch starten und Abbrechen, indem Sie die Methoden " [untc::P ause](irtc-pause.md) " und " [untc:: Resume](irtc-resume.md) " verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f631-125">You can also start and stop the capture by using the [IRTC::Pause](irtc-pause.md) and [IRTC::Resume](irtc-resume.md) methods.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9f631-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f631-126">Requirements</span></span>



| <span data-ttu-id="9f631-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f631-127">Requirement</span></span> | <span data-ttu-id="9f631-128">Wert</span><span class="sxs-lookup"><span data-stu-id="9f631-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f631-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f631-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9f631-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f631-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="9f631-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f631-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9f631-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f631-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="9f631-133">Header</span><span class="sxs-lookup"><span data-stu-id="9f631-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f631-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f631-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="9f631-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9f631-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f631-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f631-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f631-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f631-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f631-138">"Iran"</span><span class="sxs-lookup"><span data-stu-id="9f631-138">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="9f631-139">"Iran:: Configure"</span><span class="sxs-lookup"><span data-stu-id="9f631-139">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="9f631-140">Iran:: Connect</span><span class="sxs-lookup"><span data-stu-id="9f631-140">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="9f631-141">Iran::P ause</span><span class="sxs-lookup"><span data-stu-id="9f631-141">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="9f631-142">Iran:: Resume</span><span class="sxs-lookup"><span data-stu-id="9f631-142">IRTC::Resume</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="9f631-143">Iran:: Beendigung</span><span class="sxs-lookup"><span data-stu-id="9f631-143">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




