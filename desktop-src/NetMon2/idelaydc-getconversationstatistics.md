---
description: 'IDelaydC::GetConversationStatistics-Methode: Die GetConversationStatistics-Methode ruft Sitzungs- und Stationsinformationen zur aktuellen Erfassung ab.'
ms.assetid: 0164fa0e-90f2-4b97-be9d-55d172f8112d
title: IDelaydC::GetConversationStatistics-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d4d4c1bb1ad7ecb45b640c16322e297f9f640ef1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103808"
---
# <a name="idelaydcgetconversationstatistics-method"></a><span data-ttu-id="abd79-103">IDelaydC::GetConversationStatistics-Methode</span><span class="sxs-lookup"><span data-stu-id="abd79-103">IDelaydC::GetConversationStatistics method</span></span>

<span data-ttu-id="abd79-104">Die **GetConversationStatistics-Methode** ruft [*Sitzungs-*](s.md) und [*Stationsinformationen zur*](s.md) aktuellen Erfassung ab.</span><span class="sxs-lookup"><span data-stu-id="abd79-104">The **GetConversationStatistics** method retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="abd79-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="abd79-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="abd79-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="abd79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abd79-107">*nSessions* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="abd79-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abd79-108">Zeiger auf ein DWORD, das die Anzahl der [*für*](s.md) die aktuelle Erfassung aufgezeichneten Sitzungen enthält.</span><span class="sxs-lookup"><span data-stu-id="abd79-108">Pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="abd79-109">*lpSessionStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="abd79-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abd79-110">Zeiger auf eine [SESSIONSTATS-Struktur.](sessionstats.md)</span><span class="sxs-lookup"><span data-stu-id="abd79-110">Pointer to a [SESSIONSTATS](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="abd79-111">*nStations* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="abd79-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abd79-112">Zeiger auf ein DWORD, das die Anzahl der für die [*aktuelle*](s.md) Erfassung aufgezeichneten Stationen enthält.</span><span class="sxs-lookup"><span data-stu-id="abd79-112">Pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="abd79-113">*lpStationStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="abd79-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abd79-114">Zeiger auf eine [STATIONSTATS-Struktur.](stationstats.md)</span><span class="sxs-lookup"><span data-stu-id="abd79-114">Pointer to a [STATIONSTATS](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="abd79-115">*fClearAfterReading* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="abd79-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abd79-116">Flag, das verwendet wird, Netzwerkmonitor, den internen Speicher der [SESSIONSTATS-](sessionstats.md) und [STATIONSTATS-Strukturen](stationstats.md) zu löschen, nachdem die aktuellen Informationen abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="abd79-116">Flag used to tell Network Monitor to clear out the internal storage of the [SESSIONSTATS](sessionstats.md) and [STATIONSTATS](stationstats.md) structures after it retrieves the current information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abd79-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="abd79-117">Return value</span></span>

<span data-ttu-id="abd79-118">Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="abd79-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="abd79-119">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="abd79-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="abd79-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="abd79-120">Return code</span></span>                                                                                                   | <span data-ttu-id="abd79-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="abd79-121">Description</span></span>                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="abd79-122"><dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="abd79-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="abd79-123">Der NPP ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="abd79-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="abd79-124">Rufen [Sie IDelaydC::Connect auf,](idelaydc-connect.md) um das NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="abd79-124">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="abd79-125"><dt>**NMERR NOT CAPTURING (NMERR \_ WIRD NICHT \_ ERFASST)**</dt></span><span class="sxs-lookup"><span data-stu-id="abd79-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="abd79-126">Das NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="abd79-126">The NPP is not capturing data.</span></span> <span data-ttu-id="abd79-127">Rufen Sie [IDelaydC::Start](idelaydc-start.md) auf, um die Erfassung zu starten.</span><span class="sxs-lookup"><span data-stu-id="abd79-127">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="abd79-128"><dt>**NMERR \_ NICHT \_ VERZÖGERT**</dt></span><span class="sxs-lookup"><span data-stu-id="abd79-128"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>            | <span data-ttu-id="abd79-129">Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IDelaydC::Connect-Methode.](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="abd79-129">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="abd79-130"><dt>**NMERR \_ NO \_ CONVERSATION \_ STATS**</dt></span><span class="sxs-lookup"><span data-stu-id="abd79-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="abd79-131">Die Konfiguration für diese Verbindung ist so festgelegt, dass keine Konversationsstatistiken gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="abd79-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="abd79-132">Um Konversationsstatistiken zu speichern, beenden Sie die Erfassung, legen Sie NoConversationStats = YES im Konfigurations-BLOB fest, und starten Sie dann die Erfassung neu.</span><span class="sxs-lookup"><span data-stu-id="abd79-132">To save conversation statistics, stop the capture, set NoConversationStats = YES in the configuration BLOB, and then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="abd79-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="abd79-133">Remarks</span></span>

<span data-ttu-id="abd79-134">Diese Methode kann nur aufgerufen werden, während die Datenerfassung ausgeführt wird. Wenn die aktuelle Erfassung angehalten wird, sind Aufrufe dieser Methode nicht erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="abd79-134">This method can only be called only while data capture is in progress; when the current capture is paused, calls to this method will not succeed.</span></span> <span data-ttu-id="abd79-135">Um eine Erfassung zu starten, rufen Sie die [IDelaydC::Start-Methode](idelaydc-start.md) auf.</span><span class="sxs-lookup"><span data-stu-id="abd79-135">To start a capture, call the [IDelaydC::Start](idelaydc-start.md) method.</span></span>

<span data-ttu-id="abd79-136">Um andere Arten von Statistiken abzurufen, rufen [Sie IDelaydC::GetTotalStatistics auf.](idelaydc-gettotalstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="abd79-136">To retrieve other types of statistics, call [IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="abd79-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abd79-137">Requirements</span></span>



| <span data-ttu-id="abd79-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abd79-138">Requirement</span></span> | <span data-ttu-id="abd79-139">Wert</span><span class="sxs-lookup"><span data-stu-id="abd79-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abd79-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abd79-140">Minimum supported client</span></span><br/> | <span data-ttu-id="abd79-141">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abd79-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="abd79-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abd79-142">Minimum supported server</span></span><br/> | <span data-ttu-id="abd79-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abd79-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="abd79-144">Header</span><span class="sxs-lookup"><span data-stu-id="abd79-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="abd79-145"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="abd79-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="abd79-146">DLL</span><span class="sxs-lookup"><span data-stu-id="abd79-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abd79-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abd79-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abd79-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="abd79-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abd79-149">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="abd79-149">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="abd79-150">IDelaydC::Connect</span><span class="sxs-lookup"><span data-stu-id="abd79-150">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="abd79-151">IDelaydC::GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="abd79-151">IDelaydC::GetTotalStatistics</span></span>](idelaydc-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="abd79-152">IDelaydC::Start</span><span class="sxs-lookup"><span data-stu-id="abd79-152">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="abd79-153">SESSIONSTATS</span><span class="sxs-lookup"><span data-stu-id="abd79-153">SESSIONSTATS</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="abd79-154">STATIONSTATS</span><span class="sxs-lookup"><span data-stu-id="abd79-154">STATIONSTATS</span></span>](stationstats.md)
</dt> </dl>

 

 




