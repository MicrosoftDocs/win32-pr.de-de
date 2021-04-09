---
description: Mit der Resume-Methode wird eine angehaltene Erfassung neu gestartet.
ms.assetid: 4fa47220-d323-407b-9dae-704969f66bdd
title: 'Idelta aydc:: Resume-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ba0deef666c2e9829cb5a71d91e73da9c1b7d780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750057"
---
# <a name="idelaydcresume-method"></a><span data-ttu-id="1f01f-103">Idelta aydc:: Resume-Methode</span><span class="sxs-lookup"><span data-stu-id="1f01f-103">IDelaydC::Resume method</span></span>

<span data-ttu-id="1f01f-104">Mit der **Resume** -Methode wird eine angehaltene Erfassung neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="1f01f-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f01f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f01f-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="1f01f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f01f-106">Parameters</span></span>

<span data-ttu-id="1f01f-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1f01f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1f01f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f01f-108">Return value</span></span>

<span data-ttu-id="1f01f-109">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1f01f-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1f01f-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="1f01f-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="1f01f-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1f01f-111">Return code</span></span>                                                                                                | <span data-ttu-id="1f01f-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f01f-112">Description</span></span>                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1f01f-113"><dt>**nmerr- \_ Erfassung wurde \_ nicht \_ angehalten.**</dt></span><span class="sxs-lookup"><span data-stu-id="1f01f-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="1f01f-114">Die Erfassung wird nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="1f01f-114">The capture is not paused.</span></span> <span data-ttu-id="1f01f-115">Wenden Sie [**idelta DC::P ause**](idelaydc-pause.md) an, um die Erfassung anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="1f01f-115">Call [**IDelaydC::Pause**](idelaydc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="1f01f-116"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="1f01f-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="1f01f-117">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="1f01f-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="1f01f-118">Wenden Sie [**idelta-DC:: Connect**](idelaydc-connect.md) an, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="1f01f-118">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="1f01f-119"><dt>**nmerr \_ nicht \_ verzögert**</dt></span><span class="sxs-lookup"><span data-stu-id="1f01f-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>         | <span data-ttu-id="1f01f-120">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [**idelta aydc:: Connect**](idelaydc-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1f01f-120">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="1f01f-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f01f-121">Remarks</span></span>

<span data-ttu-id="1f01f-122">Während die Erfassung angehalten wird, werden neue Daten erst zur aktuellen [*Erfassungs Datei*](c.md) hinzugefügt, wenn die **idelta-DC:: Resume** -Methode aufgerufen wird, um die Erfassung neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="1f01f-122">While the capture is paused, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="1f01f-123">Wenn anhalten und **fortsetzen verwendet** werden, um die Erfassung zu [**beenden und neu**](idelaydc-pause.md) zu starten, werden alle erfassten Informationen in derselben Erfassungs Datei abgelegt.</span><span class="sxs-lookup"><span data-stu-id="1f01f-123">When [**Pause**](idelaydc-pause.md) and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="1f01f-124">Bei der [**Verwendung**](idelaydc-pause.md) von **Anhalten und fort** setzen zur Steuerung der Erfassung werden Netzwerkmonitor weiterhin [*Konversations Statistiken*](c.md) zu den vorhandenen Statistiken für die aktuelle Erfassung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1f01f-124">When using [**Pause**](idelaydc-pause.md) and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="1f01f-125">Um die Erfassung anzuhalten, nennen Sie [**idelta aydc:: Stop.**](idelaydc-stop.md)</span><span class="sxs-lookup"><span data-stu-id="1f01f-125">To stop the capture, call [**IDelaydC::Stop**](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f01f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f01f-126">Requirements</span></span>



| <span data-ttu-id="1f01f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f01f-127">Requirement</span></span> | <span data-ttu-id="1f01f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="1f01f-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f01f-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f01f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1f01f-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f01f-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="1f01f-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f01f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1f01f-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f01f-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="1f01f-133">Header</span><span class="sxs-lookup"><span data-stu-id="1f01f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f01f-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f01f-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="1f01f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1f01f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f01f-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f01f-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f01f-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f01f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f01f-138">Idelta-DC</span><span class="sxs-lookup"><span data-stu-id="1f01f-138">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="1f01f-139">**Idelta aydc:: Connect**</span><span class="sxs-lookup"><span data-stu-id="1f01f-139">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="1f01f-140">**Idelta aydc::P ause**</span><span class="sxs-lookup"><span data-stu-id="1f01f-140">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="1f01f-141">**Idelta aydc:: Beendigung**</span><span class="sxs-lookup"><span data-stu-id="1f01f-141">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




