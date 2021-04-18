---
description: Die Start-Methode startet eine Aufzeichnung.
ms.assetid: 8bf8c0c7-20be-4404-8ea5-b28b4c658523
title: 'IESP:: Start-Methode (Netmon. h)'
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
ms.openlocfilehash: 2d9fc3a75fc82964f6fc5a5660ef77414ae065d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347922"
---
# <a name="iespstart-method"></a><span data-ttu-id="c21bb-103">IESP:: Start-Methode</span><span class="sxs-lookup"><span data-stu-id="c21bb-103">IESP::Start method</span></span>

<span data-ttu-id="c21bb-104">Die **Start** -Methode startet eine Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="c21bb-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c21bb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c21bb-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="c21bb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c21bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c21bb-107">*pfilename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c21bb-107">*pFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c21bb-108">Zeiger auf den Namen der [*Erfassungs Datei*](c.md) , in der die Netzwerkdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c21bb-108">Pointer to the name of the [*capture file*](c.md) used to store the network data.</span></span> <span data-ttu-id="c21bb-109">Stellen Sie sicher, dass der Dateiname zwischengespeichert wird, wenn er für den zukünftigen Verweis benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="c21bb-109">Be sure to cache this file name if it is needed for future reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c21bb-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c21bb-110">Return value</span></span>

<span data-ttu-id="c21bb-111">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c21bb-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c21bb-112">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="c21bb-112">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="c21bb-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c21bb-113">Return code</span></span>                                                                                           | <span data-ttu-id="c21bb-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c21bb-114">Description</span></span>                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c21bb-115"><dt>**nmerr- \_ Erfassung \_ angehalten**</dt></span><span class="sxs-lookup"><span data-stu-id="c21bb-115"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="c21bb-116">Die Erfassung wird angehalten und muss beendet werden, bevor Sie neu gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c21bb-116">The capture is paused and must be stopped before it can be restarted.</span></span> <span data-ttu-id="c21bb-117">Wenden Sie [iESP:: Beendigung](iesp-stop.md) an, um die Erfassung anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="c21bb-117">Call [IESP::Stop](iesp-stop.md) to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="c21bb-118"><dt>**nmerr- \_ Erfassung**</dt></span><span class="sxs-lookup"><span data-stu-id="c21bb-118"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="c21bb-119">Die Erfassung wurde bereits gestartet.</span><span class="sxs-lookup"><span data-stu-id="c21bb-119">The capture is already started.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="c21bb-120"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="c21bb-120"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="c21bb-121">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="c21bb-121">The NPP is not connected to the network.</span></span> <span data-ttu-id="c21bb-122">Wenden Sie [iESP:: Connect](iesp-connect.md) an, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="c21bb-122">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/>          |
| <dl> <span data-ttu-id="c21bb-123"><dt>**nmerr \_ nicht \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="c21bb-123"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="c21bb-124">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iESP:: Connect](iesp-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c21bb-124">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="c21bb-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c21bb-125">Remarks</span></span>

<span data-ttu-id="c21bb-126">Der Speicherort der [*Erfassungs Datei*](c.md) wird in der Windows-Registrierung angegeben, aber Sie können Netzwerkmonitor verwenden, um den Speicherort des Verzeichnisses zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c21bb-126">The location of the [*capture file*](c.md) is specified in the Windows registry, but you can use Network Monitor to change the directory location.</span></span>

<span data-ttu-id="c21bb-127">Wenn Sie die Erfassung mit den Methoden iESP:: Start und [iESP:: beenden](iesp-stop.md) neu starten, müssen Sie die Methode [iESP:: Configure](iesp-configure.md) zum erneuten Konfigurieren der Verbindung mit jedem Aufruf von iESP:: Start zum Neustarten der Datenerfassung verwenden.</span><span class="sxs-lookup"><span data-stu-id="c21bb-127">When you restart the capture by using the IESP::Start and [IESP::Stop](iesp-stop.md) methods, you must call the [IESP::Configure](iesp-configure.md) method to reconfigure the connection each time you call IESP::Start to restart capturing data.</span></span> <span data-ttu-id="c21bb-128">Wenn Sie die Erfassung mit diesen drei Methoden starten und beenden, wird jedes Mal eine neue Erfassungs Datei erstellt, wenn die Erfassung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c21bb-128">When you start and stop the capture with these three methods, a new capture file is created each time the capture is started.</span></span>

> [!Note]  
> <span data-ttu-id="c21bb-129">Sie können die Erfassung auch starten und Abbrechen, indem Sie die [iESP::P ause](iesp-pause.md) -Methode und die [iESP:: Resume](iesp-resume.md) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="c21bb-129">You can also start and stop the capture by using the [IESP::Pause](iesp-pause.md) and [IESP::Resume](iesp-resume.md) methods.</span></span> <span data-ttu-id="c21bb-130">Wenn diese beiden Methoden verwendet werden, werden die erfassten Daten in derselben Erfassungs Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c21bb-130">When these two methods are used, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c21bb-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c21bb-131">Requirements</span></span>



| <span data-ttu-id="c21bb-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c21bb-132">Requirement</span></span> | <span data-ttu-id="c21bb-133">Wert</span><span class="sxs-lookup"><span data-stu-id="c21bb-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c21bb-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c21bb-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c21bb-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c21bb-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c21bb-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c21bb-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c21bb-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c21bb-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c21bb-138">Header</span><span class="sxs-lookup"><span data-stu-id="c21bb-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c21bb-139"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c21bb-139"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c21bb-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c21bb-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c21bb-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c21bb-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c21bb-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c21bb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c21bb-143">IESP</span><span class="sxs-lookup"><span data-stu-id="c21bb-143">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="c21bb-144">IESP:: Configure</span><span class="sxs-lookup"><span data-stu-id="c21bb-144">IESP::Configure</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="c21bb-145">IESP:: Connect</span><span class="sxs-lookup"><span data-stu-id="c21bb-145">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="c21bb-146">IESP::P ause</span><span class="sxs-lookup"><span data-stu-id="c21bb-146">IESP::Pause</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="c21bb-147">IESP:: Resume</span><span class="sxs-lookup"><span data-stu-id="c21bb-147">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="c21bb-148">IESP:: Beendigung</span><span class="sxs-lookup"><span data-stu-id="c21bb-148">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




