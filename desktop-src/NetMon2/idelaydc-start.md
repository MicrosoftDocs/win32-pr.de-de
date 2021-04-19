---
description: Die Start-Methode startet eine Aufzeichnung.
ms.assetid: 92b25afc-d5d8-47e4-a155-4ed2a3571038
title: 'Idelta-DC:: Start-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a912af44dddb8a25d3279a5cdd7f021646c26e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346684"
---
# <a name="idelaydcstart-method"></a><span data-ttu-id="df8a5-103">Idelta aydc:: Start-Methode</span><span class="sxs-lookup"><span data-stu-id="df8a5-103">IDelaydC::Start method</span></span>

<span data-ttu-id="df8a5-104">Die **Start** -Methode startet eine Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="df8a5-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="df8a5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="df8a5-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="df8a5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="df8a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df8a5-107">*pfilename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="df8a5-107">*pFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df8a5-108">Zeiger auf den Namen der [*Erfassungs Datei*](c.md) , in der die Netzwerkdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="df8a5-108">Pointer to the name of the [*capture file*](c.md) used to store the network data.</span></span> <span data-ttu-id="df8a5-109">Stellen Sie sicher, dass der Dateiname zwischengespeichert wird, wenn er für den zukünftigen Verweis benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="df8a5-109">Be sure to cache this file name if it is needed for future reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df8a5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df8a5-110">Return value</span></span>

<span data-ttu-id="df8a5-111">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="df8a5-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="df8a5-112">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="df8a5-112">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="df8a5-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="df8a5-113">Return code</span></span>                                                                                           | <span data-ttu-id="df8a5-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df8a5-114">Description</span></span>                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="df8a5-115"><dt>**nmerr- \_ Erfassung \_ angehalten**</dt></span><span class="sxs-lookup"><span data-stu-id="df8a5-115"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="df8a5-116">Die Erfassung befindet sich im angehaltenen Zustand und muss beendet werden, bevor Sie neu gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="df8a5-116">The capture is in a paused state and must be stopped before it can be restarted.</span></span> <span data-ttu-id="df8a5-117">Nennen Sie [**idelta aydc:: Beendigung**](idelaydc-stop.md) , um die Erfassung anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="df8a5-117">Call [**IDelaydC::Stop**](idelaydc-stop.md) to stop the capture.</span></span> <span data-ttu-id="df8a5-118">Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="df8a5-118">For more information, see the Remarks section in this topic.</span></span><br/> |
| <dl> <span data-ttu-id="df8a5-119"><dt>**nmerr- \_ Erfassung**</dt></span><span class="sxs-lookup"><span data-stu-id="df8a5-119"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="df8a5-120">Die Erfassung wurde bereits gestartet.</span><span class="sxs-lookup"><span data-stu-id="df8a5-120">The capture is already started.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="df8a5-121"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="df8a5-121"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="df8a5-122">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="df8a5-122">The NPP is not connected to the network.</span></span> <span data-ttu-id="df8a5-123">Wenden Sie [**idelta-DC:: Connect**](idelaydc-connect.md) an, um eine Verbindung mit dem Netzwerk herzustellen.</span><span class="sxs-lookup"><span data-stu-id="df8a5-123">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect to the network.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="df8a5-124"><dt>**nmerr \_ nicht \_ verzögert**</dt></span><span class="sxs-lookup"><span data-stu-id="df8a5-124"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>    | <span data-ttu-id="df8a5-125">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [**idelta aydc:: Connect**](idelaydc-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="df8a5-125">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="df8a5-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df8a5-126">Remarks</span></span>

<span data-ttu-id="df8a5-127">Der Speicherort der [*Erfassungs Datei*](c.md) wird in der Windows-Registrierung angegeben, aber Sie können Netzwerkmonitor verwenden, um den Speicherort der Datei zu ändern.</span><span class="sxs-lookup"><span data-stu-id="df8a5-127">The location of the [*capture file*](c.md) is specified in your Windows registry, but you can use Network Monitor to change the file's location.</span></span>

<span data-ttu-id="df8a5-128">Zum Neustarten der Erfassung mithilfe von **idelta aydc:: Start** und [**idelta aydc:: stoppmüssen**](idelaydc-stop.md)Sie die [**idelta-DC:: Configure**](idelaydc-configure.md) -Methode zum Neukonfigurieren der Verbindung bei jedem Aufruf der **idelta aydc:: Start** -Methode zum Neustarten der Datenerfassung verwenden.</span><span class="sxs-lookup"><span data-stu-id="df8a5-128">To restart the capture by using **IDelaydC::Start** and [**IDelaydC::Stop**](idelaydc-stop.md), you must call the [**IDelaydC::Configure**](idelaydc-configure.md) method to reconfigure the connection each time you call the **IDelaydC::Start** method to restart capturing data.</span></span> <span data-ttu-id="df8a5-129">Wenn Sie die Erfassung mit diesen drei Methoden starten und beenden, wird jedes Mal eine neue Erfassungs Datei erstellt, wenn die Erfassung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="df8a5-129">When you start and stop the capture with these three methods, a new capture file is created each time the capture is started.</span></span>

> [!Note]  
> <span data-ttu-id="df8a5-130">Sie können die Erfassung auch starten und Abbrechen, indem Sie die Methoden [**idelta aydc::P ause**](idelaydc-pause.md) und [**idelta aydc:: Resume**](idelaydc-resume.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="df8a5-130">You can also start and stop the capture by using the [**IDelaydC::Pause**](idelaydc-pause.md) and [**IDelaydC::Resume**](idelaydc-resume.md) methods.</span></span> <span data-ttu-id="df8a5-131">Wenn Sie diese beiden Methoden verwenden, werden die erfassten Daten in derselben Erfassungs Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="df8a5-131">When you use these two methods, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="df8a5-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df8a5-132">Requirements</span></span>



| <span data-ttu-id="df8a5-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df8a5-133">Requirement</span></span> | <span data-ttu-id="df8a5-134">Wert</span><span class="sxs-lookup"><span data-stu-id="df8a5-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df8a5-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df8a5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="df8a5-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df8a5-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="df8a5-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df8a5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="df8a5-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df8a5-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="df8a5-139">Header</span><span class="sxs-lookup"><span data-stu-id="df8a5-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="df8a5-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="df8a5-140"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="df8a5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="df8a5-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df8a5-142"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df8a5-142"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df8a5-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df8a5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df8a5-144">Idelta-DC</span><span class="sxs-lookup"><span data-stu-id="df8a5-144">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="df8a5-145">**Idelta aydc:: Configure**</span><span class="sxs-lookup"><span data-stu-id="df8a5-145">**IDelaydC::Configure**</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="df8a5-146">**Idelta aydc:: Connect**</span><span class="sxs-lookup"><span data-stu-id="df8a5-146">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="df8a5-147">**Idelta aydc::P ause**</span><span class="sxs-lookup"><span data-stu-id="df8a5-147">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="df8a5-148">**Idelta aydc:: Resume**</span><span class="sxs-lookup"><span data-stu-id="df8a5-148">**IDelaydC::Resume**</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="df8a5-149">**Idelta aydc:: Beendigung**</span><span class="sxs-lookup"><span data-stu-id="df8a5-149">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




