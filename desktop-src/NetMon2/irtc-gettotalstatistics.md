---
description: Die gettotalstatistics-Methode ruft die Gesamtstatistik für die aktuelle Erfassung ab.
ms.assetid: e5098984-c69e-4cd5-9143-d85dfcbd7b92
title: 'Untc:: gettotalstatistics-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 27128048b4326aae14ae6a2e2e6c0540b1105538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358826"
---
# <a name="irtcgettotalstatistics-method"></a><span data-ttu-id="9beec-103">Untc:: gettotalstatistics-Methode</span><span class="sxs-lookup"><span data-stu-id="9beec-103">IRTC::GetTotalStatistics method</span></span>

<span data-ttu-id="9beec-104">Die **gettotalstatistics** -Methode ruft die [*Gesamtstatistik*](t.md) für die aktuelle [*Erfassung*](c.md)ab.</span><span class="sxs-lookup"><span data-stu-id="9beec-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9beec-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9beec-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="9beec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9beec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9beec-107">*lpstats* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9beec-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9beec-108">Zeiger auf eine [Statistik](statistics.md) Struktur, die die Gesamtstatistik für die Erfassung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9beec-108">Pointer to a [STATISTICS](statistics.md) structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="9beec-109">Die Aufrufer sind dafür verantwortlich, den von der **Statistik** Struktur genutzten Arbeitsspeicher zuzuordnen und freizugeben.</span><span class="sxs-lookup"><span data-stu-id="9beec-109">It is the callers responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="9beec-110">*f/oder Lese* \[ Vorgänge in\]</span><span class="sxs-lookup"><span data-stu-id="9beec-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9beec-111">Flag, mit dem Netzwerkmonitor wird, wie der interne Speicher der gesamten Statistik behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9beec-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="9beec-112">Die Einstellung **true** weist Netzwerkmonitor an, den internen Speicher der gesamten Statistik zu löschen, nachdem die aktuellen Informationen abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="9beec-112">A setting of **TRUE** tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9beec-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9beec-113">Return value</span></span>

<span data-ttu-id="9beec-114">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="9beec-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="9beec-115">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="9beec-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="9beec-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9beec-116">Return code</span></span>                                                                                          | <span data-ttu-id="9beec-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9beec-117">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9beec-118"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="9beec-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="9beec-119">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="9beec-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="9beec-120">Wenden [Sie](irtc-connect.md) sich an, um den NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="9beec-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="9beec-121"><dt>**nmerr \_ nicht in \_ Echtzeit**</dt></span><span class="sxs-lookup"><span data-stu-id="9beec-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="9beec-122">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der Methode " [iritc:: Connect](irtc-connect.md) ".</span><span class="sxs-lookup"><span data-stu-id="9beec-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |
| <dl> <span data-ttu-id="9beec-123"><dt>**nmerr wird \_ nicht \_ erfasst**</dt></span><span class="sxs-lookup"><span data-stu-id="9beec-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="9beec-124">Der NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="9beec-124">The NPP is not capturing data.</span></span> <span data-ttu-id="9beec-125">Nennen Sie " [untc:: Start](irtc-start.md) ", um die Datenerfassung zu starten</span><span class="sxs-lookup"><span data-stu-id="9beec-125">Call [IRTC::Start](irtc-start.md) to start capturing data.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="9beec-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9beec-126">Remarks</span></span>

<span data-ttu-id="9beec-127">Diese Methode gibt nur Daten zurück, während eine Erfassung ausgeführt wird, einschließlich der Pause, während die Erfassung angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="9beec-127">This method returns data only while a capture is in progress, including while the capture is paused.</span></span>

<span data-ttu-id="9beec-128">Netzwerkmonitor speichert auch [*Konversations Statistiken*](c.md).</span><span class="sxs-lookup"><span data-stu-id="9beec-128">Network Monitor also stores [*conversation statistics*](c.md).</span></span> <span data-ttu-id="9beec-129">Um Konversations Statistiken abzurufen, rufen Sie die Methode " [iritc:: getconversation ationstatistics](irtc-getconversationstatistics.md) " auf.</span><span class="sxs-lookup"><span data-stu-id="9beec-129">To retrieve conversation statistics, call the [IRTC::GetConversationStatistics](irtc-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9beec-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9beec-130">Requirements</span></span>



| <span data-ttu-id="9beec-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9beec-131">Requirement</span></span> | <span data-ttu-id="9beec-132">Wert</span><span class="sxs-lookup"><span data-stu-id="9beec-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9beec-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9beec-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9beec-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9beec-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="9beec-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9beec-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9beec-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9beec-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="9beec-137">Header</span><span class="sxs-lookup"><span data-stu-id="9beec-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="9beec-138"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9beec-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="9beec-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9beec-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9beec-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9beec-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9beec-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9beec-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9beec-142">"Iran"</span><span class="sxs-lookup"><span data-stu-id="9beec-142">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="9beec-143">Iran:: Connect</span><span class="sxs-lookup"><span data-stu-id="9beec-143">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="9beec-144">"Irren:: getconversation ationstatistics"</span><span class="sxs-lookup"><span data-stu-id="9beec-144">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="9beec-145">"Iran:: Start"</span><span class="sxs-lookup"><span data-stu-id="9beec-145">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="9beec-146">Kam</span><span class="sxs-lookup"><span data-stu-id="9beec-146">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




