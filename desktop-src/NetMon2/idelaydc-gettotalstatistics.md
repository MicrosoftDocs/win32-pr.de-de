---
description: 'IDelaydC::GetTotalStatistics-Methode: Die GetTotalStatistics-Methode ruft die Gesamtstatistik für die aktuelle Erfassung ab.'
ms.assetid: 904c7496-5603-41b9-8481-06fa31f6f112
title: IDelaydC::GetTotalStatistics-Methode (Netmon.h)
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
ms.openlocfilehash: b3a0ce4f230236e276fede528a5e778ecafd51fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113528"
---
# <a name="idelaydcgettotalstatistics-method"></a><span data-ttu-id="dce0d-103">IDelaydC::GetTotalStatistics-Methode</span><span class="sxs-lookup"><span data-stu-id="dce0d-103">IDelaydC::GetTotalStatistics method</span></span>

<span data-ttu-id="dce0d-104">Die **GetTotalStatistics-Methode** ruft die [*Gesamtstatistik*](t.md) für die aktuelle [*Erfassung*](c.md)ab.</span><span class="sxs-lookup"><span data-stu-id="dce0d-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dce0d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dce0d-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="dce0d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dce0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dce0d-107">*lpStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dce0d-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dce0d-108">Zeiger auf eine [STATISTICS-Struktur,](statistics.md)die die Gesamtstatistik für die Erfassung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="dce0d-108">Pointer to a [STATISTICS](statistics.md)structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="dce0d-109">Der Aufrufer ist dafür verantwortlich, den von der **STATISTICS-Struktur** verwendeten Arbeitsspeicher zuzuordnen und freizugeben.</span><span class="sxs-lookup"><span data-stu-id="dce0d-109">It is the caller's responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="dce0d-110">*fClearAfterReading* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="dce0d-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce0d-111">Flag, das verwendet wird, um Netzwerkmonitor zu informieren, wie der interne Speicher der Gesamtstatistik behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dce0d-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="dce0d-112">Die Einstellung **TRUE** weist Netzwerkmonitor an, den internen Speicher der Gesamtstatistik zu löschen, nachdem die aktuellen Informationen abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="dce0d-112">A setting of **TRUE** tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dce0d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dce0d-113">Return value</span></span>

<span data-ttu-id="dce0d-114">Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="dce0d-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="dce0d-115">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="dce0d-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="dce0d-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="dce0d-116">Return code</span></span>                                                                                          | <span data-ttu-id="dce0d-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dce0d-117">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dce0d-118"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="dce0d-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="dce0d-119">Das NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="dce0d-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="dce0d-120">Rufen Sie [IDelaydC::Connect](idelaydc-connect.md) auf, um eine Verbindung mit dem Netzwerk herzustellen.</span><span class="sxs-lookup"><span data-stu-id="dce0d-120">Call [IDelaydC::Connect](idelaydc-connect.md) to connect to the network.</span></span><br/> |
| <dl> <span data-ttu-id="dce0d-121"><dt>**NMERR \_ NICHT \_ VERZÖGERT**</dt></span><span class="sxs-lookup"><span data-stu-id="dce0d-121"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="dce0d-122">Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IDelaydC::Connect-Methode.](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="dce0d-122">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>             |
| <dl> <span data-ttu-id="dce0d-123"><dt>**NMERR \_ NICHT \_ ERFASSEN**</dt></span><span class="sxs-lookup"><span data-stu-id="dce0d-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="dce0d-124">Das NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="dce0d-124">The NPP is not capturing data.</span></span> <span data-ttu-id="dce0d-125">Rufen Sie [IDelaydC::Start](idelaydc-start.md) auf, um mit der Erfassung von Daten zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="dce0d-125">Call [IDelaydC::Start](idelaydc-start.md) to start capturing data.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="dce0d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dce0d-126">Remarks</span></span>

<span data-ttu-id="dce0d-127">Diese Methode gibt Daten nur zurück, während eine Erfassung ausgeführt wird. Wenn die Erfassung angehalten wird, sind Aufrufe dieser Methode nicht erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dce0d-127">This method returns data only while a capture is in progress; when the capture is paused, calls to this method will not succeed.</span></span>

<span data-ttu-id="dce0d-128">Netzwerkmonitor speichert auch [*Konversationsstatistiken,*](c.md)die durch Aufrufen der [IDelaydC::GetConversationStatistics-Methode](idelaydc-getconversationstatistics.md) abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="dce0d-128">Network Monitor also stores [*conversation statistics*](c.md), which can be retrieved by calling the [IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dce0d-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dce0d-129">Requirements</span></span>



| <span data-ttu-id="dce0d-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dce0d-130">Requirement</span></span> | <span data-ttu-id="dce0d-131">Wert</span><span class="sxs-lookup"><span data-stu-id="dce0d-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce0d-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dce0d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="dce0d-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dce0d-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="dce0d-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dce0d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="dce0d-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dce0d-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="dce0d-136">Header</span><span class="sxs-lookup"><span data-stu-id="dce0d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="dce0d-137"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="dce0d-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="dce0d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="dce0d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dce0d-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dce0d-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dce0d-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dce0d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dce0d-141">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="dce0d-141">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="dce0d-142">IDelaydC::Connect</span><span class="sxs-lookup"><span data-stu-id="dce0d-142">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="dce0d-143">IDelaydC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="dce0d-143">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="dce0d-144">IDelaydC::Start</span><span class="sxs-lookup"><span data-stu-id="dce0d-144">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="dce0d-145">Statistiken</span><span class="sxs-lookup"><span data-stu-id="dce0d-145">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




