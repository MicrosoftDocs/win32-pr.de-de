---
description: Die Methode "beenden" beendet die aktuelle Erfassung.
ms.assetid: d2d4e51a-c6a4-4aec-a805-929af621ffb3
title: 'IESP:: stopmethode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 50dfb274e1355af93c473609f95607e6b3faf1fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345477"
---
# <a name="iespstop-method"></a><span data-ttu-id="8ba90-103">IESP:: Station-Methode</span><span class="sxs-lookup"><span data-stu-id="8ba90-103">IESP::Stop method</span></span>

<span data-ttu-id="8ba90-104">Die Methode " **Beenden** " beendet die aktuelle Erfassung.</span><span class="sxs-lookup"><span data-stu-id="8ba90-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ba90-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ba90-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="8ba90-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ba90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ba90-107">*lpstats* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8ba90-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba90-108">Zeiger auf eine [Statistik](statistics.md) Struktur, die Netzwerk Statistiken enthält, z. b. Gesamtrahmen und erfasste Bytes insgesamt.</span><span class="sxs-lookup"><span data-stu-id="8ba90-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ba90-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ba90-109">Return value</span></span>

<span data-ttu-id="8ba90-110">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="8ba90-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="8ba90-111">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="8ba90-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="8ba90-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8ba90-112">Return code</span></span>                                                                                          | <span data-ttu-id="8ba90-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ba90-113">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8ba90-114"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="8ba90-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="8ba90-115">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="8ba90-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="8ba90-116">Wenden Sie [iESP:: Connect](iesp-connect.md) an, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="8ba90-116">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="8ba90-117"><dt>**nmerr wird \_ nicht \_ erfasst**</dt></span><span class="sxs-lookup"><span data-stu-id="8ba90-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="8ba90-118">Der NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="8ba90-118">The NPP is not capturing data.</span></span> <span data-ttu-id="8ba90-119">Wenden Sie [iESP:: Start](iesp-start.md) an, um die Erfassung zu starten.</span><span class="sxs-lookup"><span data-stu-id="8ba90-119">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="8ba90-120"><dt>**nmerr \_ nicht \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="8ba90-120"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="8ba90-121">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iESP:: Connect](iesp-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8ba90-121">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="8ba90-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ba90-122">Remarks</span></span>

<span data-ttu-id="8ba90-123">Wenn die **iESP:: Stopp** -Methode aufgerufen wird, beendet Netzwerkmonitor die Erfassung von Daten und schließt die [*Erfassungs Datei.*](c.md)</span><span class="sxs-lookup"><span data-stu-id="8ba90-123">When the **IESP::Stop** method is called, Network Monitor stops capturing data and closes the [*capture file.*](c.md)</span></span> <span data-ttu-id="8ba90-124">(Der Name der Erfassungs Datei wurde zurückgegeben, als " [iESP:: Start](iesp-start.md) " aufgerufen wurde.) Nun können Sie sich den Inhalt der Erfassungs Datei ansehen.</span><span class="sxs-lookup"><span data-stu-id="8ba90-124">(The name of the capture file was returned when [IESP::Start](iesp-start.md) was called.) You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="8ba90-125">Wenn Sie die Erfassung beenden und neu starten, stellen Sie sicher, dass Sie bei jedem Aufruf von [iESP:: Start](iesp-start.md) die Methode [iESP:: Configure](iesp-configure.md) aufruft, um die Erfassung neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="8ba90-125">When you stop and restart the capture, make sure to call the [IESP::Configure](iesp-configure.md) method each time you call [IESP::Start](iesp-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ba90-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ba90-126">Requirements</span></span>



| <span data-ttu-id="8ba90-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ba90-127">Requirement</span></span> | <span data-ttu-id="8ba90-128">Wert</span><span class="sxs-lookup"><span data-stu-id="8ba90-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba90-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8ba90-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8ba90-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ba90-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="8ba90-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8ba90-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8ba90-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ba90-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="8ba90-133">Header</span><span class="sxs-lookup"><span data-stu-id="8ba90-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ba90-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ba90-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="8ba90-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8ba90-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ba90-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ba90-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ba90-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ba90-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ba90-138">IESP</span><span class="sxs-lookup"><span data-stu-id="8ba90-138">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="8ba90-139">IESP:: Connect</span><span class="sxs-lookup"><span data-stu-id="8ba90-139">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="8ba90-140">IESP:: Start</span><span class="sxs-lookup"><span data-stu-id="8ba90-140">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="8ba90-141">Kam</span><span class="sxs-lookup"><span data-stu-id="8ba90-141">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




