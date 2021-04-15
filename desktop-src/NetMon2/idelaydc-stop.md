---
description: Die Methode "beenden" beendet die aktuelle Erfassung.
ms.assetid: 1b627137-e72d-4425-98d9-e296fb07e509
title: 'Idelta aydc:: stopmethode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 42c9cc1c4b6da7b5f934dd96f26aa9348c43ac0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484307"
---
# <a name="idelaydcstop-method"></a><span data-ttu-id="e80fb-103">Idelta aydc:: stopmethode</span><span class="sxs-lookup"><span data-stu-id="e80fb-103">IDelaydC::Stop method</span></span>

<span data-ttu-id="e80fb-104">Die Methode " **Beenden** " beendet die aktuelle Erfassung.</span><span class="sxs-lookup"><span data-stu-id="e80fb-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="e80fb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e80fb-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="e80fb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e80fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e80fb-107">*lpstats* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e80fb-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e80fb-108">Zeiger auf eine [Statistik](statistics.md) Struktur, die Netzwerk Statistiken enthält, z. b. Gesamtrahmen und erfasste Bytes insgesamt.</span><span class="sxs-lookup"><span data-stu-id="e80fb-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e80fb-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e80fb-109">Return value</span></span>

<span data-ttu-id="e80fb-110">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e80fb-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e80fb-111">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="e80fb-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="e80fb-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e80fb-112">Return code</span></span>                                                                                          | <span data-ttu-id="e80fb-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e80fb-113">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e80fb-114"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="e80fb-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="e80fb-115">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="e80fb-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="e80fb-116">Wenden Sie [idelta-DC:: Connect](idelaydc-connect.md) an, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="e80fb-116">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="e80fb-117"><dt>**nmerr wird \_ nicht \_ erfasst**</dt></span><span class="sxs-lookup"><span data-stu-id="e80fb-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="e80fb-118">Der NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="e80fb-118">The NPP is not capturing data.</span></span> <span data-ttu-id="e80fb-119">Wenden Sie [idelta-DC:: Start](idelaydc-start.md) an, um die Erfassung zu starten.</span><span class="sxs-lookup"><span data-stu-id="e80fb-119">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="e80fb-120"><dt>**nmerr \_ nicht \_ verzögert**</dt></span><span class="sxs-lookup"><span data-stu-id="e80fb-120"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="e80fb-121">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [idelta aydc:: Connect](idelaydc-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e80fb-121">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="e80fb-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e80fb-122">Remarks</span></span>

<span data-ttu-id="e80fb-123">Wenn **idelta aydc:: Stopp** aufgerufen wird, beendet Netzwerkmonitor die Erfassung von Daten und schließt die [*Erfassungs Datei*](c.md).</span><span class="sxs-lookup"><span data-stu-id="e80fb-123">When **IDelaydC::Stop** is called, Network Monitor stops capturing data and closes the [*capture file*](c.md).</span></span> <span data-ttu-id="e80fb-124">(Der Name der Erfassungs Datei wurde zurückgegeben, als " [idelta aydc:: Start](idelaydc-start.md) " aufgerufen wurde).</span><span class="sxs-lookup"><span data-stu-id="e80fb-124">(The name of the capture file was returned when [IDelaydC::Start](idelaydc-start.md) was called).</span></span> <span data-ttu-id="e80fb-125">Nun können Sie sich den Inhalt der Erfassungs Datei ansehen.</span><span class="sxs-lookup"><span data-stu-id="e80fb-125">You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="e80fb-126">Wenn Sie die Erfassung beenden und starten, stellen Sie sicher, dass Sie jedes Mal, wenn Sie [idelta aydc:: Start](idelaydc-start.md) aufgerufen haben, die [idelta-DC:: Configure](idelaydc-configure.md) -Methode aufruft, um die Erfassung neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="e80fb-126">When you stop and start the capture, make sure you call the [IDelaydC::Configure](idelaydc-configure.md) method each time you call [IDelaydC::Start](idelaydc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="e80fb-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e80fb-127">Requirements</span></span>



| <span data-ttu-id="e80fb-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e80fb-128">Requirement</span></span> | <span data-ttu-id="e80fb-129">Wert</span><span class="sxs-lookup"><span data-stu-id="e80fb-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e80fb-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e80fb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e80fb-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e80fb-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="e80fb-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e80fb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e80fb-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e80fb-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="e80fb-134">Header</span><span class="sxs-lookup"><span data-stu-id="e80fb-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e80fb-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e80fb-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="e80fb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e80fb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e80fb-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e80fb-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e80fb-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e80fb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e80fb-139">Idelta-DC</span><span class="sxs-lookup"><span data-stu-id="e80fb-139">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="e80fb-140">Idelta aydc:: Connect</span><span class="sxs-lookup"><span data-stu-id="e80fb-140">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="e80fb-141">Idelta aydc:: Configure</span><span class="sxs-lookup"><span data-stu-id="e80fb-141">IDelaydC::Configure</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="e80fb-142">Idelta aydc:: Start</span><span class="sxs-lookup"><span data-stu-id="e80fb-142">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="e80fb-143">Kam</span><span class="sxs-lookup"><span data-stu-id="e80fb-143">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




