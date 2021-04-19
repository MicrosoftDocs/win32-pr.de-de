---
description: Die gettotalstatistics-Methode ruft die Gesamtstatistik für die aktuelle Erfassung ab.
ms.assetid: 494634f6-a9b3-4a50-8920-2387be9ba30f
title: 'IStats:: gettotalstatistics-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 51cdbfdcc796aa7d8091e8da5837809efaa63379
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353622"
---
# <a name="istatsgettotalstatistics-method"></a><span data-ttu-id="bf0af-103">IStats:: gettotalstatistics-Methode</span><span class="sxs-lookup"><span data-stu-id="bf0af-103">IStats::GetTotalStatistics method</span></span>

<span data-ttu-id="bf0af-104">Die **gettotalstatistics** -Methode ruft die [*Gesamtstatistik*](t.md) für die aktuelle [*Erfassung*](c.md)ab.</span><span class="sxs-lookup"><span data-stu-id="bf0af-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bf0af-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf0af-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="bf0af-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf0af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf0af-107">*lpstats* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bf0af-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf0af-108">Zeiger auf eine [Statistik](statistics.md)Struktur, die die Gesamtstatistik für die Erfassung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="bf0af-108">Pointer to a [STATISTICS](statistics.md)structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="bf0af-109">Es liegt in der Verantwortung des Aufrufers, den von der **Statistik** Struktur genutzten Arbeitsspeicher zuzuordnen und freizugeben.</span><span class="sxs-lookup"><span data-stu-id="bf0af-109">It is the caller's responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="bf0af-110">*f/oder Lese* \[ Vorgänge in\]</span><span class="sxs-lookup"><span data-stu-id="bf0af-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf0af-111">Flag, mit dem Netzwerkmonitor wird, wie der interne Speicher der gesamten Statistik behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf0af-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="bf0af-112">Die Einstellung true weist Netzwerkmonitor an, den internen Speicher der gesamten Statistik zu löschen, nachdem die aktuellen Informationen abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="bf0af-112">A setting of TRUE tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf0af-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bf0af-113">Return value</span></span>

<span data-ttu-id="bf0af-114">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="bf0af-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="bf0af-115">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="bf0af-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="bf0af-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bf0af-116">Return code</span></span>                                                                                            | <span data-ttu-id="bf0af-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf0af-117">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bf0af-118"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="bf0af-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="bf0af-119">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="bf0af-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="bf0af-120">Wenden Sie die [iStats:: Connect](istats-connect.md) -Methode an, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="bf0af-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="bf0af-121"><dt>**nmerr \_ nicht \_ \_ nur Statistiken**</dt></span><span class="sxs-lookup"><span data-stu-id="bf0af-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="bf0af-122">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iStats:: Connect](istats-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="bf0af-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |
| <dl> <span data-ttu-id="bf0af-123"><dt>**nmerr wird \_ nicht \_ erfasst**</dt></span><span class="sxs-lookup"><span data-stu-id="bf0af-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="bf0af-124">Der NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="bf0af-124">The NPP is not capturing data.</span></span> <span data-ttu-id="bf0af-125">Um mit dem Erfassen von Daten zu beginnen, müssen Sie die [iStats:: Start](istats-start.md) -Methode</span><span class="sxs-lookup"><span data-stu-id="bf0af-125">Call the [IStats::Start](istats-start.md) method to start capturing data.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="bf0af-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf0af-126">Remarks</span></span>

<span data-ttu-id="bf0af-127">Diese Methode gibt nur Daten zurück, während eine Erfassung ausgeführt wird, einschließlich der Pause, während die Erfassung angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="bf0af-127">This method returns data only while a capture is in progress, including while the capture is paused.</span></span>

<span data-ttu-id="bf0af-128">Netzwerkmonitor speichert auch [*Konversations Statistiken*](c.md), die durch Aufrufen der [iStats:: getconversation ationstatistics](istats-getconversationstatistics.md) -Methode abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="bf0af-128">Network Monitor also stores [*conversation statistics*](c.md), which can be retrieved by calling the [IStats::GetConversationStatistics](istats-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf0af-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf0af-129">Requirements</span></span>



| <span data-ttu-id="bf0af-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf0af-130">Requirement</span></span> | <span data-ttu-id="bf0af-131">Wert</span><span class="sxs-lookup"><span data-stu-id="bf0af-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf0af-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bf0af-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bf0af-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf0af-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="bf0af-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bf0af-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bf0af-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf0af-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="bf0af-136">Header</span><span class="sxs-lookup"><span data-stu-id="bf0af-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf0af-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf0af-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="bf0af-138">DLL</span><span class="sxs-lookup"><span data-stu-id="bf0af-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf0af-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf0af-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf0af-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf0af-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf0af-141">IStats</span><span class="sxs-lookup"><span data-stu-id="bf0af-141">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="bf0af-142">IStats:: Connect</span><span class="sxs-lookup"><span data-stu-id="bf0af-142">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="bf0af-143">IStats:: getconversation ationstatistics</span><span class="sxs-lookup"><span data-stu-id="bf0af-143">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="bf0af-144">IStats:: Start,</span><span class="sxs-lookup"><span data-stu-id="bf0af-144">IStats::Start,</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="bf0af-145">Kam</span><span class="sxs-lookup"><span data-stu-id="bf0af-145">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




