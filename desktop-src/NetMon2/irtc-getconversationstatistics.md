---
description: 'IRTC::GetConversationStatistics-Methode: Die GetConversationStatistics-Methode ruft Sitzungs- und Stationsinformationen zur aktuellen Erfassung ab.'
ms.assetid: 27f364cd-fee9-4262-b181-c5f15fb12e51
title: IRTC::GetConversationStatistics-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 4d2476f4eb33d7e74d0de8363fa88d5e688a2e73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110698"
---
# <a name="irtcgetconversationstatistics-method"></a><span data-ttu-id="9b4c0-103">IRTC::GetConversationStatistics-Methode</span><span class="sxs-lookup"><span data-stu-id="9b4c0-103">IRTC::GetConversationStatistics method</span></span>

<span data-ttu-id="9b4c0-104">Die **GetConversationStatistics-Methode** ruft [*Sitzungs-*](s.md) und [*Stationsinformationen*](s.md) zur aktuellen Erfassung ab.</span><span class="sxs-lookup"><span data-stu-id="9b4c0-104">The **GetConversationStatistics** method retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b4c0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b4c0-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="9b4c0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b4c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b4c0-107">*nSessions* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9b4c0-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b4c0-108">Zeiger auf ein DWORD, das die Anzahl der [*sitzungen*](s.md) enthält, die für die aktuelle Erfassung aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="9b4c0-108">Pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="9b4c0-109">*lpSessionStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9b4c0-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b4c0-110">Zeiger auf eine [SESSIONSTATS-Struktur.](sessionstats.md)</span><span class="sxs-lookup"><span data-stu-id="9b4c0-110">Pointer to a [SESSIONSTATS](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9b4c0-111">*nStations* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9b4c0-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b4c0-112">Zeiger auf ein DWORD, das die Anzahl der für die aktuelle Erfassung [*aufgezeichneten Stationen*](s.md) enthält.</span><span class="sxs-lookup"><span data-stu-id="9b4c0-112">Pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="9b4c0-113">*lpStationStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9b4c0-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b4c0-114">Zeiger auf eine [STATIONSTATS-Struktur.](stationstats.md)</span><span class="sxs-lookup"><span data-stu-id="9b4c0-114">Pointer to a [STATIONSTATS](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9b4c0-115">*fClearAfterReading* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9b4c0-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b4c0-116">Flag, das Netzwerkmonitor anweisen soll, den internen Speicher der [SESSIONSTATS-](sessionstats.md) und [STATIONSTATS-Strukturen](stationstats.md) zu löschen, nachdem die aktuellen Informationen abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="9b4c0-116">Flag used to tell Network Monitor to clear out the internal storage of the [SESSIONSTATS](sessionstats.md) and [STATIONSTATS](stationstats.md) structures after it retrieves the current information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b4c0-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9b4c0-117">Return value</span></span>

<span data-ttu-id="9b4c0-118">Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="9b4c0-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="9b4c0-119">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="9b4c0-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="9b4c0-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9b4c0-120">Return code</span></span>                                                                                                   | <span data-ttu-id="9b4c0-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b4c0-121">Description</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9b4c0-122"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="9b4c0-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="9b4c0-123">Das NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="9b4c0-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="9b4c0-124">Rufen Sie [IRTC::Connect](irtc-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="9b4c0-124">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="9b4c0-125"><dt>**NMERR \_ NICHT \_ ERFASSEN**</dt></span><span class="sxs-lookup"><span data-stu-id="9b4c0-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="9b4c0-126">Das NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="9b4c0-126">The NPP is not capturing data.</span></span> <span data-ttu-id="9b4c0-127">Rufen Sie [IRTC::Start](irtc-start.md) auf, um die Erfassung zu starten.</span><span class="sxs-lookup"><span data-stu-id="9b4c0-127">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="9b4c0-128"><dt>**NMERR \_ NOT \_ REALTIME**</dt></span><span class="sxs-lookup"><span data-stu-id="9b4c0-128"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>           | <span data-ttu-id="9b4c0-129">Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IRTC::Connect-Methode.](irtc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="9b4c0-129">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                                                                                                                          |
| <dl> <span data-ttu-id="9b4c0-130"><dt>**NMERR \_ NO \_ CONVERSATION \_ STATS**</dt></span><span class="sxs-lookup"><span data-stu-id="9b4c0-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="9b4c0-131">Die Konfiguration für diese Verbindung ist so festgelegt, dass keine Konversationsstatistiken gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="9b4c0-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="9b4c0-132">Um Konversationsstatistiken zu speichern, beenden Sie die Erfassung, legen Sie NoConversationStats = YES im Konfigurations-BLOB fest, und starten Sie dann die Erfassung neu.</span><span class="sxs-lookup"><span data-stu-id="9b4c0-132">To save conversation statistics, stop the capture, set NoConversationStats = YES in the configuration BLOB, then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9b4c0-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b4c0-133">Remarks</span></span>

<span data-ttu-id="9b4c0-134">Diese Methode kann nur aufgerufen werden, während Sie Daten erfassen. Wenn Sie diese Methode aufrufen, während die aktuelle Erfassung angehalten wird, ist die Methode nicht erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9b4c0-134">This method can only be called while you are capturing data; if you call this method while the current capture is paused, the method will not succeed.</span></span> <span data-ttu-id="9b4c0-135">Um eine Erfassung zu starten, rufen Sie die [IRTC::Start-Methode](irtc-start.md) auf.</span><span class="sxs-lookup"><span data-stu-id="9b4c0-135">To start a capture, call the [IRTC::Start](irtc-start.md) method.</span></span>

<span data-ttu-id="9b4c0-136">Um andere Arten von Statistiken abzurufen, rufen Sie die [IRTC::GetTotalStatistics-Methode](irtc-gettotalstatistics.md) auf.</span><span class="sxs-lookup"><span data-stu-id="9b4c0-136">To retrieve other types of statistics, call the [IRTC::GetTotalStatistics](irtc-gettotalstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b4c0-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b4c0-137">Requirements</span></span>



| <span data-ttu-id="9b4c0-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b4c0-138">Requirement</span></span> | <span data-ttu-id="9b4c0-139">Wert</span><span class="sxs-lookup"><span data-stu-id="9b4c0-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b4c0-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b4c0-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9b4c0-141">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b4c0-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="9b4c0-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b4c0-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9b4c0-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b4c0-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="9b4c0-144">Header</span><span class="sxs-lookup"><span data-stu-id="9b4c0-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b4c0-145"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="9b4c0-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="9b4c0-146">DLL</span><span class="sxs-lookup"><span data-stu-id="9b4c0-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b4c0-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b4c0-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b4c0-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9b4c0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b4c0-149">IRTC</span><span class="sxs-lookup"><span data-stu-id="9b4c0-149">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="9b4c0-150">IRTC::Connect</span><span class="sxs-lookup"><span data-stu-id="9b4c0-150">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="9b4c0-151">IRTC::GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="9b4c0-151">IRTC::GetTotalStatistics</span></span>](irtc-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="9b4c0-152">IRTC::Start</span><span class="sxs-lookup"><span data-stu-id="9b4c0-152">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="9b4c0-153">SESSIONSTATS</span><span class="sxs-lookup"><span data-stu-id="9b4c0-153">SESSIONSTATS</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="9b4c0-154">STATIONSTATS</span><span class="sxs-lookup"><span data-stu-id="9b4c0-154">STATIONSTATS</span></span>](stationstats.md)
</dt> </dl>

 

 




