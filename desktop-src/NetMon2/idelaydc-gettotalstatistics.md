---
description: Die gettotalstatistics-Methode ruft die Gesamtstatistik für die aktuelle Erfassung ab.
ms.assetid: 904c7496-5603-41b9-8481-06fa31f6f112
title: 'Idelta-DC:: gettotalstatistics-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0d194426933532fcf7a1965ed59b099489eefcb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393410"
---
# <a name="idelaydcgettotalstatistics-method"></a><span data-ttu-id="9bcb3-103">Idelta aydc:: gettotalstatistics-Methode</span><span class="sxs-lookup"><span data-stu-id="9bcb3-103">IDelaydC::GetTotalStatistics method</span></span>

<span data-ttu-id="9bcb3-104">Die **gettotalstatistics** -Methode ruft die [*Gesamtstatistik*](t.md) für die aktuelle [*Erfassung*](c.md)ab.</span><span class="sxs-lookup"><span data-stu-id="9bcb3-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9bcb3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bcb3-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="9bcb3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bcb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bcb3-107">*lpstats* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9bcb3-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bcb3-108">Zeiger auf eine [Statistik](statistics.md)Struktur, die die Gesamtstatistik für die Erfassung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9bcb3-108">Pointer to a [STATISTICS](statistics.md)structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="9bcb3-109">Es liegt in der Verantwortung des Aufrufers, den von der **Statistik** Struktur genutzten Arbeitsspeicher zuzuordnen und freizugeben.</span><span class="sxs-lookup"><span data-stu-id="9bcb3-109">It is the caller's responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="9bcb3-110">*f/oder Lese* \[ Vorgänge in\]</span><span class="sxs-lookup"><span data-stu-id="9bcb3-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bcb3-111">Flag, mit dem Netzwerkmonitor wird, wie der interne Speicher der gesamten Statistik behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9bcb3-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="9bcb3-112">Die Einstellung **true** weist Netzwerkmonitor an, den internen Speicher der gesamten Statistik zu löschen, nachdem die aktuellen Informationen abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="9bcb3-112">A setting of **TRUE** tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bcb3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9bcb3-113">Return value</span></span>

<span data-ttu-id="9bcb3-114">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="9bcb3-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="9bcb3-115">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="9bcb3-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="9bcb3-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9bcb3-116">Return code</span></span>                                                                                          | <span data-ttu-id="9bcb3-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9bcb3-117">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9bcb3-118"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="9bcb3-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="9bcb3-119">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="9bcb3-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="9bcb3-120">Wenden Sie [idelta-DC:: Connect](idelaydc-connect.md) an, um eine Verbindung mit dem Netzwerk herzustellen.</span><span class="sxs-lookup"><span data-stu-id="9bcb3-120">Call [IDelaydC::Connect](idelaydc-connect.md) to connect to the network.</span></span><br/> |
| <dl> <span data-ttu-id="9bcb3-121"><dt>**nmerr \_ nicht \_ verzögert**</dt></span><span class="sxs-lookup"><span data-stu-id="9bcb3-121"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="9bcb3-122">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [idelta aydc:: Connect](idelaydc-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9bcb3-122">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>             |
| <dl> <span data-ttu-id="9bcb3-123"><dt>**nmerr wird \_ nicht \_ erfasst**</dt></span><span class="sxs-lookup"><span data-stu-id="9bcb3-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="9bcb3-124">Der NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="9bcb3-124">The NPP is not capturing data.</span></span> <span data-ttu-id="9bcb3-125">Nennen Sie [idelta aydc:: Start](idelaydc-start.md) , um mit dem Erfassen von Daten zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="9bcb3-125">Call [IDelaydC::Start](idelaydc-start.md) to start capturing data.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="9bcb3-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9bcb3-126">Remarks</span></span>

<span data-ttu-id="9bcb3-127">Diese Methode gibt nur Daten zurück, während eine Erfassung ausgeführt wird. Wenn die Erfassung angehalten wird, werden Aufrufe dieser Methode nicht erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9bcb3-127">This method returns data only while a capture is in progress; when the capture is paused, calls to this method will not succeed.</span></span>

<span data-ttu-id="9bcb3-128">Netzwerkmonitor speichert auch [*Konversations Statistiken*](c.md), die durch Aufrufen der [idelta aydc:: getconversation ationstatistics](idelaydc-getconversationstatistics.md) -Methode abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="9bcb3-128">Network Monitor also stores [*conversation statistics*](c.md), which can be retrieved by calling the [IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bcb3-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9bcb3-129">Requirements</span></span>



| <span data-ttu-id="9bcb3-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9bcb3-130">Requirement</span></span> | <span data-ttu-id="9bcb3-131">Wert</span><span class="sxs-lookup"><span data-stu-id="9bcb3-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bcb3-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9bcb3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9bcb3-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9bcb3-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="9bcb3-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9bcb3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9bcb3-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9bcb3-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="9bcb3-136">Header</span><span class="sxs-lookup"><span data-stu-id="9bcb3-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bcb3-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bcb3-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="9bcb3-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9bcb3-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bcb3-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bcb3-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bcb3-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9bcb3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bcb3-141">Idelta-DC</span><span class="sxs-lookup"><span data-stu-id="9bcb3-141">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="9bcb3-142">Idelta aydc:: Connect</span><span class="sxs-lookup"><span data-stu-id="9bcb3-142">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="9bcb3-143">Idelta aydc:: getconversation ationstatistics</span><span class="sxs-lookup"><span data-stu-id="9bcb3-143">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="9bcb3-144">Idelta aydc:: Start</span><span class="sxs-lookup"><span data-stu-id="9bcb3-144">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="9bcb3-145">Kam</span><span class="sxs-lookup"><span data-stu-id="9bcb3-145">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




