---
description: 'IDelaydC::Stop-Methode: Die Stop-Methode beendet die aktuelle Erfassung.'
ms.assetid: 1b627137-e72d-4425-98d9-e296fb07e509
title: IDelaydC::Stop-Methode (Netmon.h)
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
ms.openlocfilehash: 38be5b6ba4c3f6edcd716f4d0235150e96dd692a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110778"
---
# <a name="idelaydcstop-method"></a><span data-ttu-id="9d4bb-103">IDelaydC::Stop-Methode</span><span class="sxs-lookup"><span data-stu-id="9d4bb-103">IDelaydC::Stop method</span></span>

<span data-ttu-id="9d4bb-104">Die **Stop-Methode** beendet die aktuelle Erfassung.</span><span class="sxs-lookup"><span data-stu-id="9d4bb-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d4bb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d4bb-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="9d4bb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d4bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d4bb-107">*lpStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9d4bb-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d4bb-108">Zeiger auf eine [STATISTICS-Struktur,](statistics.md) die Netzwerkstatistiken enthält, z. B. gesamt erfasste Frames und gesamt erfasste Bytes.</span><span class="sxs-lookup"><span data-stu-id="9d4bb-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d4bb-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d4bb-109">Return value</span></span>

<span data-ttu-id="9d4bb-110">Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="9d4bb-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="9d4bb-111">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="9d4bb-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="9d4bb-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9d4bb-112">Return code</span></span>                                                                                          | <span data-ttu-id="9d4bb-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d4bb-113">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9d4bb-114"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="9d4bb-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="9d4bb-115">Das NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="9d4bb-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="9d4bb-116">Rufen Sie [IDelaydC::Connect](idelaydc-connect.md) auf, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="9d4bb-116">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="9d4bb-117"><dt>**NMERR \_ NICHT \_ ERFASSEN**</dt></span><span class="sxs-lookup"><span data-stu-id="9d4bb-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="9d4bb-118">Das NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="9d4bb-118">The NPP is not capturing data.</span></span> <span data-ttu-id="9d4bb-119">Rufen Sie [IDelaydC::Start](idelaydc-start.md) auf, um die Erfassung zu starten.</span><span class="sxs-lookup"><span data-stu-id="9d4bb-119">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="9d4bb-120"><dt>**NMERR \_ NICHT \_ VERZÖGERT**</dt></span><span class="sxs-lookup"><span data-stu-id="9d4bb-120"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="9d4bb-121">Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IDelaydC::Connect-Methode.](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="9d4bb-121">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="9d4bb-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d4bb-122">Remarks</span></span>

<span data-ttu-id="9d4bb-123">Wenn **IDelaydC::Stop** aufgerufen wird, beendet Netzwerkmonitor die Erfassung von Daten und schließt die [*Erfassungsdatei*](c.md).</span><span class="sxs-lookup"><span data-stu-id="9d4bb-123">When **IDelaydC::Stop** is called, Network Monitor stops capturing data and closes the [*capture file*](c.md).</span></span> <span data-ttu-id="9d4bb-124">(Der Name der Erfassungsdatei wurde zurückgegeben, als [IDelaydC::Start](idelaydc-start.md) aufgerufen wurde.)</span><span class="sxs-lookup"><span data-stu-id="9d4bb-124">(The name of the capture file was returned when [IDelaydC::Start](idelaydc-start.md) was called).</span></span> <span data-ttu-id="9d4bb-125">Sie können sich nun den Inhalt der Aufzeichnungsdatei ansehen.</span><span class="sxs-lookup"><span data-stu-id="9d4bb-125">You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="9d4bb-126">Wenn Sie die Erfassung beenden und starten, stellen Sie sicher, dass Sie jedes Mal die [IDelaydC::Configure-Methode](idelaydc-configure.md) aufrufen, wenn Sie [IDelaydC::Start](idelaydc-start.md) aufrufen, um die Erfassung neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="9d4bb-126">When you stop and start the capture, make sure you call the [IDelaydC::Configure](idelaydc-configure.md) method each time you call [IDelaydC::Start](idelaydc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d4bb-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d4bb-127">Requirements</span></span>



| <span data-ttu-id="9d4bb-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d4bb-128">Requirement</span></span> | <span data-ttu-id="9d4bb-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9d4bb-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4bb-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d4bb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9d4bb-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d4bb-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="9d4bb-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d4bb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9d4bb-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d4bb-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="9d4bb-134">Header</span><span class="sxs-lookup"><span data-stu-id="9d4bb-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d4bb-135"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="9d4bb-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="9d4bb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9d4bb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d4bb-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d4bb-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d4bb-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9d4bb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d4bb-139">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="9d4bb-139">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="9d4bb-140">IDelaydC::Connect</span><span class="sxs-lookup"><span data-stu-id="9d4bb-140">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="9d4bb-141">IDelaydC::Configure</span><span class="sxs-lookup"><span data-stu-id="9d4bb-141">IDelaydC::Configure</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="9d4bb-142">IDelaydC::Start</span><span class="sxs-lookup"><span data-stu-id="9d4bb-142">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="9d4bb-143">Statistiken</span><span class="sxs-lookup"><span data-stu-id="9d4bb-143">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




