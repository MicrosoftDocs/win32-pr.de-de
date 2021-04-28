---
description: 'IESP::Start-Methode: Die Start-Methode startet eine Erfassung.'
ms.assetid: 8bf8c0c7-20be-4404-8ea5-b28b4c658523
title: IESP::Start-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 6dd0d1159132e594b6d48ea6799da5846eeb626e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103798"
---
# <a name="iespstart-method"></a><span data-ttu-id="42c46-103">IESP::Start-Methode</span><span class="sxs-lookup"><span data-stu-id="42c46-103">IESP::Start method</span></span>

<span data-ttu-id="42c46-104">Die **Start-Methode** startet eine Erfassung.</span><span class="sxs-lookup"><span data-stu-id="42c46-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="42c46-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="42c46-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="42c46-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="42c46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42c46-107">*pFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="42c46-107">*pFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42c46-108">Zeiger auf den Namen der [*Erfassungsdatei,*](c.md) die zum Speichern der Netzwerkdaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="42c46-108">Pointer to the name of the [*capture file*](c.md) used to store the network data.</span></span> <span data-ttu-id="42c46-109">Stellen Sie sicher, dass Sie diesen Dateinamen zwischenspeichern, wenn er für zukünftige Verweise benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="42c46-109">Be sure to cache this file name if it is needed for future reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42c46-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42c46-110">Return value</span></span>

<span data-ttu-id="42c46-111">Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="42c46-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="42c46-112">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="42c46-112">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="42c46-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="42c46-113">Return code</span></span>                                                                                           | <span data-ttu-id="42c46-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42c46-114">Description</span></span>                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="42c46-115"><dt>**NMERR \_ CAPTURE \_ PAUSED**</dt></span><span class="sxs-lookup"><span data-stu-id="42c46-115"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="42c46-116">Die Erfassung wird angehalten und muss beendet werden, bevor sie neu gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="42c46-116">The capture is paused and must be stopped before it can be restarted.</span></span> <span data-ttu-id="42c46-117">Rufen [Sie IESP::Stop auf,](iesp-stop.md) um die Erfassung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="42c46-117">Call [IESP::Stop](iesp-stop.md) to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="42c46-118"><dt>**NMERR-ERFASSUNG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="42c46-118"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="42c46-119">Die Erfassung wurde bereits gestartet.</span><span class="sxs-lookup"><span data-stu-id="42c46-119">The capture is already started.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="42c46-120"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="42c46-120"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="42c46-121">Der NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="42c46-121">The NPP is not connected to the network.</span></span> <span data-ttu-id="42c46-122">Rufen [Sie IESP::Connect auf,](iesp-connect.md) um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="42c46-122">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/>          |
| <dl> <span data-ttu-id="42c46-123"><dt>**NMERR \_ NICHT \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="42c46-123"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="42c46-124">Das NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IESP::Connect-Methode.](iesp-connect.md)</span><span class="sxs-lookup"><span data-stu-id="42c46-124">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="42c46-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42c46-125">Remarks</span></span>

<span data-ttu-id="42c46-126">Der Speicherort der [*Erfassungsdatei wird*](c.md) in der Windows-Registrierung angegeben. Sie können jedoch Netzwerkmonitor verzeichnisspeicherort ändern.</span><span class="sxs-lookup"><span data-stu-id="42c46-126">The location of the [*capture file*](c.md) is specified in the Windows registry, but you can use Network Monitor to change the directory location.</span></span>

<span data-ttu-id="42c46-127">Wenn Sie die Erfassung mithilfe der Methoden IESP::Start und [IESP::Stop](iesp-stop.md) neu starten, müssen Sie die [IESP::Configure-Methode](iesp-configure.md) aufrufen, um die Verbindung jedes Mal neu zu konfigurieren, wenn Sie IESP::Start aufrufen, um die Erfassungsdaten neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="42c46-127">When you restart the capture by using the IESP::Start and [IESP::Stop](iesp-stop.md) methods, you must call the [IESP::Configure](iesp-configure.md) method to reconfigure the connection each time you call IESP::Start to restart capturing data.</span></span> <span data-ttu-id="42c46-128">Wenn Sie die Erfassung mit diesen drei Methoden starten und beenden, wird bei jedem Start der Erfassung eine neue Erfassungsdatei erstellt.</span><span class="sxs-lookup"><span data-stu-id="42c46-128">When you start and stop the capture with these three methods, a new capture file is created each time the capture is started.</span></span>

> [!Note]  
> <span data-ttu-id="42c46-129">Sie können die Erfassung auch mithilfe der [Methoden IESP::P ause](iesp-pause.md) und [IESP::Resume](iesp-resume.md) starten und beenden.</span><span class="sxs-lookup"><span data-stu-id="42c46-129">You can also start and stop the capture by using the [IESP::Pause](iesp-pause.md) and [IESP::Resume](iesp-resume.md) methods.</span></span> <span data-ttu-id="42c46-130">Wenn diese beiden Methoden verwendet werden, werden die erfassten Daten in derselben Erfassungsdatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="42c46-130">When these two methods are used, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="42c46-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42c46-131">Requirements</span></span>



| <span data-ttu-id="42c46-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42c46-132">Requirement</span></span> | <span data-ttu-id="42c46-133">Wert</span><span class="sxs-lookup"><span data-stu-id="42c46-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42c46-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42c46-134">Minimum supported client</span></span><br/> | <span data-ttu-id="42c46-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42c46-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="42c46-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42c46-136">Minimum supported server</span></span><br/> | <span data-ttu-id="42c46-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42c46-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="42c46-138">Header</span><span class="sxs-lookup"><span data-stu-id="42c46-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="42c46-139"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="42c46-139"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="42c46-140">DLL</span><span class="sxs-lookup"><span data-stu-id="42c46-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42c46-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42c46-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42c46-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="42c46-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42c46-143">IESP</span><span class="sxs-lookup"><span data-stu-id="42c46-143">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="42c46-144">IESP::Configure</span><span class="sxs-lookup"><span data-stu-id="42c46-144">IESP::Configure</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="42c46-145">IESP::Connect</span><span class="sxs-lookup"><span data-stu-id="42c46-145">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="42c46-146">IESP::P ause</span><span class="sxs-lookup"><span data-stu-id="42c46-146">IESP::Pause</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="42c46-147">IESP::Resume</span><span class="sxs-lookup"><span data-stu-id="42c46-147">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="42c46-148">IESP::Stop</span><span class="sxs-lookup"><span data-stu-id="42c46-148">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




