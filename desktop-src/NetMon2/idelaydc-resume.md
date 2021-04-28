---
description: 'IDelaydC::Resume-Methode: Die Resume-Methode startet eine angehaltene Erfassung neu.'
ms.assetid: 4fa47220-d323-407b-9dae-704969f66bdd
title: IDelaydC::Resume-Methode (Netmon.h)
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
ms.openlocfilehash: 9c8c3b505e0e9fb306a444111cce22c8c580d015
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109188"
---
# <a name="idelaydcresume-method"></a><span data-ttu-id="2a01a-103">IDelaydC::Resume-Methode</span><span class="sxs-lookup"><span data-stu-id="2a01a-103">IDelaydC::Resume method</span></span>

<span data-ttu-id="2a01a-104">Die **Resume-Methode** startet eine angehaltene Erfassung neu.</span><span class="sxs-lookup"><span data-stu-id="2a01a-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a01a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a01a-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="2a01a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a01a-106">Parameters</span></span>

<span data-ttu-id="2a01a-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2a01a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2a01a-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a01a-108">Return value</span></span>

<span data-ttu-id="2a01a-109">Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="2a01a-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2a01a-110">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="2a01a-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="2a01a-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2a01a-111">Return code</span></span>                                                                                                | <span data-ttu-id="2a01a-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a01a-112">Description</span></span>                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2a01a-113"><dt>**NMERR \_ CAPTURE \_ NOT \_ PAUSED**</dt></span><span class="sxs-lookup"><span data-stu-id="2a01a-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="2a01a-114">Die Erfassung wird nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="2a01a-114">The capture is not paused.</span></span> <span data-ttu-id="2a01a-115">Rufen Sie [**IDelaydC::P ause**](idelaydc-pause.md) auf, um die Erfassung anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="2a01a-115">Call [**IDelaydC::Pause**](idelaydc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="2a01a-116"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="2a01a-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="2a01a-117">Das NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="2a01a-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="2a01a-118">Rufen Sie [**IDelaydC::Connect**](idelaydc-connect.md) auf, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="2a01a-118">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="2a01a-119"><dt>**NMERR \_ NICHT \_ VERZÖGERT**</dt></span><span class="sxs-lookup"><span data-stu-id="2a01a-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>         | <span data-ttu-id="2a01a-120">Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [**IDelaydC::Connect-Methode.**](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="2a01a-120">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="2a01a-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a01a-121">Remarks</span></span>

<span data-ttu-id="2a01a-122">Während die Erfassung angehalten wird, werden der aktuellen [*Erfassungsdatei*](c.md) erst neue Daten hinzugefügt, wenn die **IDelaydC::Resume-Methode** aufgerufen wird, um die Erfassung neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="2a01a-122">While the capture is paused, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="2a01a-123">Wenn [**Anhalten**](idelaydc-pause.md) und **Fortsetzen** zum Beenden und Neustarten der Erfassung verwendet werden, werden alle erfassten Informationen in derselben Erfassungsdatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2a01a-123">When [**Pause**](idelaydc-pause.md) and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="2a01a-124">Wenn [**Sie anhalten**](idelaydc-pause.md) und **fortsetzen** verwenden, um die Erfassung zu steuern, fügt Netzwerkmonitor den vorhandenen Statistiken für die aktuelle Erfassung weiterhin [*Konversationsstatistiken*](c.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="2a01a-124">When using [**Pause**](idelaydc-pause.md) and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="2a01a-125">Um die Erfassung zu beenden, rufen [**Sie IDelaydC::Stop**](idelaydc-stop.md)auf.</span><span class="sxs-lookup"><span data-stu-id="2a01a-125">To stop the capture, call [**IDelaydC::Stop**](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a01a-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a01a-126">Requirements</span></span>



| <span data-ttu-id="2a01a-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a01a-127">Requirement</span></span> | <span data-ttu-id="2a01a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="2a01a-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a01a-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a01a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2a01a-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a01a-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="2a01a-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a01a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2a01a-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a01a-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="2a01a-133">Header</span><span class="sxs-lookup"><span data-stu-id="2a01a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a01a-134"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="2a01a-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="2a01a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2a01a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a01a-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a01a-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a01a-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2a01a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a01a-138">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="2a01a-138">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="2a01a-139">**IDelaydC::Connect**</span><span class="sxs-lookup"><span data-stu-id="2a01a-139">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="2a01a-140">**IDelaydC::P ause**</span><span class="sxs-lookup"><span data-stu-id="2a01a-140">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="2a01a-141">**IDelaydC::Stop**</span><span class="sxs-lookup"><span data-stu-id="2a01a-141">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




