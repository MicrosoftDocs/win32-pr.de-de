---
description: 'IRTC::GetTotalStatistics-Methode: Die GetTotalStatistics-Methode ruft die Gesamtstatistik für die aktuelle Erfassung ab.'
ms.assetid: e5098984-c69e-4cd5-9143-d85dfcbd7b92
title: IRTC::GetTotalStatistics-Methode (Netmon.h)
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
ms.openlocfilehash: 8ed659efe388f4eb9c9ac8afd6aa2c74fd0af7d3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110688"
---
# <a name="irtcgettotalstatistics-method"></a><span data-ttu-id="d04db-103">IRTC::GetTotalStatistics-Methode</span><span class="sxs-lookup"><span data-stu-id="d04db-103">IRTC::GetTotalStatistics method</span></span>

<span data-ttu-id="d04db-104">Die **GetTotalStatistics-Methode** ruft die [*Gesamtstatistik*](t.md) für die aktuelle [*Erfassung*](c.md)ab.</span><span class="sxs-lookup"><span data-stu-id="d04db-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d04db-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d04db-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="d04db-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d04db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d04db-107">*lpStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d04db-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d04db-108">Zeiger auf eine [STATISTICS-Struktur,](statistics.md) die die Gesamtstatistik für die Erfassung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="d04db-108">Pointer to a [STATISTICS](statistics.md) structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="d04db-109">Es liegt in der Verantwortung der Aufrufer, den von der **STATISTICS-Struktur** verwendeten Arbeitsspeicher zuzuordnen und freizugeben.</span><span class="sxs-lookup"><span data-stu-id="d04db-109">It is the callers responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="d04db-110">*fClearAfterReading* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d04db-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d04db-111">Flag, das verwendet wird, um Netzwerkmonitor zu informieren, wie der interne Speicher der Gesamtstatistik behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d04db-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="d04db-112">Die Einstellung **TRUE** weist Netzwerkmonitor an, den internen Speicher der Gesamtstatistik zu löschen, nachdem die aktuellen Informationen abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="d04db-112">A setting of **TRUE** tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d04db-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d04db-113">Return value</span></span>

<span data-ttu-id="d04db-114">Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="d04db-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d04db-115">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="d04db-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="d04db-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d04db-116">Return code</span></span>                                                                                          | <span data-ttu-id="d04db-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d04db-117">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d04db-118"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="d04db-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="d04db-119">Das NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="d04db-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="d04db-120">Rufen Sie [IRTC::Connect](irtc-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="d04db-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="d04db-121"><dt>**NMERR \_ NOT \_ REALTIME**</dt></span><span class="sxs-lookup"><span data-stu-id="d04db-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="d04db-122">Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IRTC::Connect-Methode.](irtc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="d04db-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |
| <dl> <span data-ttu-id="d04db-123"><dt>**NMERR \_ NICHT \_ ERFASSEN**</dt></span><span class="sxs-lookup"><span data-stu-id="d04db-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="d04db-124">Das NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="d04db-124">The NPP is not capturing data.</span></span> <span data-ttu-id="d04db-125">Rufen Sie [IRTC::Start](irtc-start.md) auf, um mit der Erfassung von Daten zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="d04db-125">Call [IRTC::Start](irtc-start.md) to start capturing data.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="d04db-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d04db-126">Remarks</span></span>

<span data-ttu-id="d04db-127">Diese Methode gibt Daten nur zurück, während eine Erfassung in Bearbeitung ist, einschließlich, während die Erfassung angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="d04db-127">This method returns data only while a capture is in progress, including while the capture is paused.</span></span>

<span data-ttu-id="d04db-128">Netzwerkmonitor speichert auch [*Konversationsstatistiken.*](c.md)</span><span class="sxs-lookup"><span data-stu-id="d04db-128">Network Monitor also stores [*conversation statistics*](c.md).</span></span> <span data-ttu-id="d04db-129">Rufen Sie zum Abrufen von Konversationsstatistiken die [IRTC::GetConversationStatistics-Methode](irtc-getconversationstatistics.md) auf.</span><span class="sxs-lookup"><span data-stu-id="d04db-129">To retrieve conversation statistics, call the [IRTC::GetConversationStatistics](irtc-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d04db-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d04db-130">Requirements</span></span>



| <span data-ttu-id="d04db-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d04db-131">Requirement</span></span> | <span data-ttu-id="d04db-132">Wert</span><span class="sxs-lookup"><span data-stu-id="d04db-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d04db-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d04db-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d04db-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d04db-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="d04db-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d04db-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d04db-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d04db-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="d04db-137">Header</span><span class="sxs-lookup"><span data-stu-id="d04db-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="d04db-138"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="d04db-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="d04db-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d04db-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d04db-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d04db-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d04db-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d04db-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d04db-142">IRTC</span><span class="sxs-lookup"><span data-stu-id="d04db-142">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="d04db-143">IRTC::Connect</span><span class="sxs-lookup"><span data-stu-id="d04db-143">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="d04db-144">IRTC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="d04db-144">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="d04db-145">IRTC::Start</span><span class="sxs-lookup"><span data-stu-id="d04db-145">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="d04db-146">Statistiken</span><span class="sxs-lookup"><span data-stu-id="d04db-146">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




