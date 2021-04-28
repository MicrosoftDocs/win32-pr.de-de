---
description: 'IDelaydC::Start-Methode: Die Start-Methode startet eine Erfassung.'
ms.assetid: 92b25afc-d5d8-47e4-a155-4ed2a3571038
title: IDelaydC::Start-Methode (Netmon.h)
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
ms.openlocfilehash: 25bf778d9cccce20c736c5f8b83e6af9754ac933
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118438"
---
# <a name="idelaydcstart-method"></a><span data-ttu-id="531d1-103">IDelaydC::Start-Methode</span><span class="sxs-lookup"><span data-stu-id="531d1-103">IDelaydC::Start method</span></span>

<span data-ttu-id="531d1-104">Die **Start-Methode** startet eine Erfassung.</span><span class="sxs-lookup"><span data-stu-id="531d1-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="531d1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="531d1-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="531d1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="531d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="531d1-107">*pFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="531d1-107">*pFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="531d1-108">Zeiger auf den Namen der [*Erfassungsdatei,*](c.md) die zum Speichern der Netzwerkdaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="531d1-108">Pointer to the name of the [*capture file*](c.md) used to store the network data.</span></span> <span data-ttu-id="531d1-109">Stellen Sie sicher, dass Sie diesen Dateinamen zwischenspeichern, wenn er für zukünftige Verweise benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="531d1-109">Be sure to cache this file name if it is needed for future reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="531d1-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="531d1-110">Return value</span></span>

<span data-ttu-id="531d1-111">Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="531d1-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="531d1-112">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="531d1-112">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="531d1-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="531d1-113">Return code</span></span>                                                                                           | <span data-ttu-id="531d1-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="531d1-114">Description</span></span>                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="531d1-115"><dt>**NMERR \_ CAPTURE \_ PAUSED**</dt></span><span class="sxs-lookup"><span data-stu-id="531d1-115"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="531d1-116">Die Erfassung befindet sich in einem angehaltenen Zustand und muss beendet werden, bevor sie neu gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="531d1-116">The capture is in a paused state and must be stopped before it can be restarted.</span></span> <span data-ttu-id="531d1-117">Rufen [**Sie IDelaydC::Stop auf,**](idelaydc-stop.md) um die Erfassung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="531d1-117">Call [**IDelaydC::Stop**](idelaydc-stop.md) to stop the capture.</span></span> <span data-ttu-id="531d1-118">Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="531d1-118">For more information, see the Remarks section in this topic.</span></span><br/> |
| <dl> <span data-ttu-id="531d1-119"><dt>**NMERR-ERFASSUNG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="531d1-119"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="531d1-120">Die Erfassung wurde bereits gestartet.</span><span class="sxs-lookup"><span data-stu-id="531d1-120">The capture is already started.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="531d1-121"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="531d1-121"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="531d1-122">Der NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="531d1-122">The NPP is not connected to the network.</span></span> <span data-ttu-id="531d1-123">Rufen [**Sie IDelaydC::Connect auf, um**](idelaydc-connect.md) eine Verbindung mit dem Netzwerk herzustellen.</span><span class="sxs-lookup"><span data-stu-id="531d1-123">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect to the network.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="531d1-124"><dt>**NMERR \_ NICHT \_ VERZÖGERT**</dt></span><span class="sxs-lookup"><span data-stu-id="531d1-124"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>    | <span data-ttu-id="531d1-125">Das NPP ist mit dem Netzwerk verbunden, aber nicht mit der [**IDelaydC::Connect-Methode.**](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="531d1-125">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="531d1-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="531d1-126">Remarks</span></span>

<span data-ttu-id="531d1-127">Der Speicherort der [*Erfassungsdatei*](c.md) wird in Ihrer Windows-Registrierung angegeben, aber Sie können Netzwerkmonitor verwenden, um den Speicherort der Datei zu ändern.</span><span class="sxs-lookup"><span data-stu-id="531d1-127">The location of the [*capture file*](c.md) is specified in your Windows registry, but you can use Network Monitor to change the file's location.</span></span>

<span data-ttu-id="531d1-128">Um die Erfassung **mithilfe von IDelaydC::Start** und [**IDelaydC::Stop**](idelaydc-stop.md)neu zu starten, müssen Sie die [**IDelaydC::Configure-Methode**](idelaydc-configure.md) aufrufen, um die Verbindung jedes Mal neu zu konfigurieren, wenn Sie die **IDelaydC::Start-Methode** aufrufen, um die Erfassung von Daten neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="531d1-128">To restart the capture by using **IDelaydC::Start** and [**IDelaydC::Stop**](idelaydc-stop.md), you must call the [**IDelaydC::Configure**](idelaydc-configure.md) method to reconfigure the connection each time you call the **IDelaydC::Start** method to restart capturing data.</span></span> <span data-ttu-id="531d1-129">Wenn Sie die Erfassung mit diesen drei Methoden starten und beenden, wird bei jedem Start der Erfassung eine neue Erfassungsdatei erstellt.</span><span class="sxs-lookup"><span data-stu-id="531d1-129">When you start and stop the capture with these three methods, a new capture file is created each time the capture is started.</span></span>

> [!Note]  
> <span data-ttu-id="531d1-130">Sie können die Erfassung auch mithilfe der [**Methoden IDelaydC::P ause und**](idelaydc-pause.md) [**IDelaydC::Resume**](idelaydc-resume.md) starten und beenden.</span><span class="sxs-lookup"><span data-stu-id="531d1-130">You can also start and stop the capture by using the [**IDelaydC::Pause**](idelaydc-pause.md) and [**IDelaydC::Resume**](idelaydc-resume.md) methods.</span></span> <span data-ttu-id="531d1-131">Wenn Sie diese beiden Methoden verwenden, werden die erfassten Daten in derselben Erfassungsdatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="531d1-131">When you use these two methods, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="531d1-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="531d1-132">Requirements</span></span>



| <span data-ttu-id="531d1-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="531d1-133">Requirement</span></span> | <span data-ttu-id="531d1-134">Wert</span><span class="sxs-lookup"><span data-stu-id="531d1-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="531d1-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="531d1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="531d1-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="531d1-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="531d1-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="531d1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="531d1-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="531d1-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="531d1-139">Header</span><span class="sxs-lookup"><span data-stu-id="531d1-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="531d1-140"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="531d1-140"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="531d1-141">DLL</span><span class="sxs-lookup"><span data-stu-id="531d1-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="531d1-142"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="531d1-142"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="531d1-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="531d1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="531d1-144">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="531d1-144">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="531d1-145">**IDelaydC::Configure**</span><span class="sxs-lookup"><span data-stu-id="531d1-145">**IDelaydC::Configure**</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="531d1-146">**IDelaydC::Connect**</span><span class="sxs-lookup"><span data-stu-id="531d1-146">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="531d1-147">**IDelaydC::P ause**</span><span class="sxs-lookup"><span data-stu-id="531d1-147">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="531d1-148">**IDelaydC::Resume**</span><span class="sxs-lookup"><span data-stu-id="531d1-148">**IDelaydC::Resume**</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="531d1-149">**IDelaydC::Stop**</span><span class="sxs-lookup"><span data-stu-id="531d1-149">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




