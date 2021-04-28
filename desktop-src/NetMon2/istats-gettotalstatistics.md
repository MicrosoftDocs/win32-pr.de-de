---
description: 'IStats::GetTotalStatistics-Methode: Die GetTotalStatistics-Methode ruft die Gesamtstatistik für die aktuelle Erfassung ab.'
ms.assetid: 494634f6-a9b3-4a50-8920-2387be9ba30f
title: IStats::GetTotalStatistics-Methode (Netmon.h)
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
ms.openlocfilehash: e6566a58212e8f20d0d999302f41ab97cb9f005e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098408"
---
# <a name="istatsgettotalstatistics-method"></a><span data-ttu-id="76a59-103">IStats::GetTotalStatistics-Methode</span><span class="sxs-lookup"><span data-stu-id="76a59-103">IStats::GetTotalStatistics method</span></span>

<span data-ttu-id="76a59-104">Die **GetTotalStatistics-Methode** ruft die [*Gesamtstatistik für*](t.md) die aktuelle Erfassung [*ab.*](c.md)</span><span class="sxs-lookup"><span data-stu-id="76a59-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="76a59-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76a59-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="76a59-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="76a59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76a59-107">*lpStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="76a59-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76a59-108">Zeiger auf eine [STATISTICS-Struktur,](statistics.md)die die Gesamtstatistik für die Erfassung enthält.</span><span class="sxs-lookup"><span data-stu-id="76a59-108">Pointer to a [STATISTICS](statistics.md)structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="76a59-109">Der Aufrufer ist dafür verantwortlich, den von der STATISTICS-Struktur verwendeten Arbeitsspeicher zu reservieren **und frei** zu geben.</span><span class="sxs-lookup"><span data-stu-id="76a59-109">It is the caller's responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="76a59-110">*fClearAfterReading* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="76a59-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76a59-111">Flag, das verwendet wird, Netzwerkmonitor, wie der interne Speicher der Gesamtstatistik behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="76a59-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="76a59-112">Die Einstellung TRUE weist Netzwerkmonitor, den internen Speicher der Gesamtstatistik zu löschen, nachdem die aktuellen Informationen abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="76a59-112">A setting of TRUE tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76a59-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76a59-113">Return value</span></span>

<span data-ttu-id="76a59-114">Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="76a59-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="76a59-115">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="76a59-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="76a59-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="76a59-116">Return code</span></span>                                                                                            | <span data-ttu-id="76a59-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76a59-117">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="76a59-118"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="76a59-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="76a59-119">Der NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="76a59-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="76a59-120">Rufen Sie [die IStats::Connect-Methode auf,](istats-connect.md) um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="76a59-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="76a59-121"><dt>**NMERR \_ NICHT \_ NUR STATISTIKEN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="76a59-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="76a59-122">Der NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IStats::Connect-Methode.](istats-connect.md)</span><span class="sxs-lookup"><span data-stu-id="76a59-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |
| <dl> <span data-ttu-id="76a59-123"><dt>**NMERR NOT CAPTURING (NMERR \_ WIRD NICHT \_ ERFASST)**</dt></span><span class="sxs-lookup"><span data-stu-id="76a59-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="76a59-124">Der NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="76a59-124">The NPP is not capturing data.</span></span> <span data-ttu-id="76a59-125">Rufen Sie die [IStats::Start-Methode auf,](istats-start.md) um mit dem Erfassen von Daten zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="76a59-125">Call the [IStats::Start](istats-start.md) method to start capturing data.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="76a59-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76a59-126">Remarks</span></span>

<span data-ttu-id="76a59-127">Diese Methode gibt Daten nur zurück, während eine Erfassung in Bearbeitung ist, einschließlich, während die Erfassung angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="76a59-127">This method returns data only while a capture is in progress, including while the capture is paused.</span></span>

<span data-ttu-id="76a59-128">Netzwerkmonitor werden [*auch*](c.md)Konversationsstatistiken gespeichert, die durch Aufrufen der [IStats::GetConversationStatistics-Methode abgerufen werden](istats-getconversationstatistics.md) können.</span><span class="sxs-lookup"><span data-stu-id="76a59-128">Network Monitor also stores [*conversation statistics*](c.md), which can be retrieved by calling the [IStats::GetConversationStatistics](istats-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="76a59-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76a59-129">Requirements</span></span>



| <span data-ttu-id="76a59-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76a59-130">Requirement</span></span> | <span data-ttu-id="76a59-131">Wert</span><span class="sxs-lookup"><span data-stu-id="76a59-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76a59-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76a59-132">Minimum supported client</span></span><br/> | <span data-ttu-id="76a59-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76a59-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="76a59-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76a59-134">Minimum supported server</span></span><br/> | <span data-ttu-id="76a59-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76a59-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="76a59-136">Header</span><span class="sxs-lookup"><span data-stu-id="76a59-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="76a59-137"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="76a59-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="76a59-138">DLL</span><span class="sxs-lookup"><span data-stu-id="76a59-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76a59-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76a59-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76a59-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="76a59-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76a59-141">IStats</span><span class="sxs-lookup"><span data-stu-id="76a59-141">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="76a59-142">IStats::Connect</span><span class="sxs-lookup"><span data-stu-id="76a59-142">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="76a59-143">IStats::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="76a59-143">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="76a59-144">IStats::Start,</span><span class="sxs-lookup"><span data-stu-id="76a59-144">IStats::Start,</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="76a59-145">Statistiken</span><span class="sxs-lookup"><span data-stu-id="76a59-145">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




