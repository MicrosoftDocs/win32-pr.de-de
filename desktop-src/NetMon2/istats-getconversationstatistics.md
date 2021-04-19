---
description: Ruft Sitzungs-und Stations Informationen zur aktuellen Erfassung ab.
ms.assetid: 7fc436fc-b569-402d-a1ea-c1bb65de8a9e
title: 'IStats:: getconversation ationstatistics-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 030fafb4ccf041c2804179f8adf0088ca3fba845
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366519"
---
# <a name="istatsgetconversationstatistics-method"></a><span data-ttu-id="ce902-103">IStats:: getconversation ationstatistics-Methode</span><span class="sxs-lookup"><span data-stu-id="ce902-103">IStats::GetConversationStatistics method</span></span>

<span data-ttu-id="ce902-104">Die **getconversation ationstatistics** -Methode ruft Sitzungs-und Stations Informationen zur aktuellen Erfassung ab.</span><span class="sxs-lookup"><span data-stu-id="ce902-104">The **GetConversationStatistics** method retrieves session and station information about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce902-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce902-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="ce902-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce902-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce902-107">*nsitzungen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ce902-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce902-108">Ein Zeiger auf ein DWORD, das die Anzahl der [*Sitzungen*](s.md) enthält, die für die aktuelle Erfassung aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="ce902-108">A pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="ce902-109">*lpsessionstats* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ce902-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce902-110">Ein Zeiger auf eine [**sessionstats**](sessionstats.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ce902-110">A pointer to a [**SESSIONSTATS**](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ce902-111">*nstations* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ce902-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce902-112">Ein Zeiger auf ein DWORD, das die Anzahl der [*Stationen*](s.md) enthält, die für die aktuelle Erfassung aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="ce902-112">A pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="ce902-113">*lpstationstats* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ce902-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce902-114">Ein Zeiger auf eine [**stationstats**](stationstats.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ce902-114">A pointer to a [**STATIONSTATS**](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ce902-115">*f/oder Lese* \[ Vorgänge in\]</span><span class="sxs-lookup"><span data-stu-id="ce902-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce902-116">Flag, das verwendet wird, um Netzwerkmonitor anzuweisen, den internen Speicher der [**sessionstats**](sessionstats.md) -und [**stationstats**](stationstats.md) -Strukturen nach dem Abrufen der aktuellen Daten zu löschen.</span><span class="sxs-lookup"><span data-stu-id="ce902-116">Flag used to instruct Network Monitor to clear the internal storage of the [**SESSIONSTATS**](sessionstats.md) and [**STATIONSTATS**](stationstats.md) structures after the current data is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce902-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce902-117">Return value</span></span>

<span data-ttu-id="ce902-118">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="ce902-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ce902-119">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="ce902-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="ce902-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ce902-120">Return code</span></span>                                                                                                   | <span data-ttu-id="ce902-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce902-121">Description</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ce902-122"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="ce902-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="ce902-123">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="ce902-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="ce902-124">Wenden Sie [**iStats:: Connect**](istats-connect.md) an, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="ce902-124">Call [**IStats::Connect**](istats-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="ce902-125"><dt>**nmerr wird \_ nicht \_ erfasst**</dt></span><span class="sxs-lookup"><span data-stu-id="ce902-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="ce902-126">Der NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="ce902-126">The NPP is not capturing data.</span></span> <span data-ttu-id="ce902-127">Nennen Sie [**iStats:: Start**](istats-start.md) , um die Erfassung zu starten.</span><span class="sxs-lookup"><span data-stu-id="ce902-127">Call [**IStats::Start**](istats-start.md) to start the capture.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="ce902-128"><dt>**nmerr \_ nicht \_ \_ nur Statistiken**</dt></span><span class="sxs-lookup"><span data-stu-id="ce902-128"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl>        | <span data-ttu-id="ce902-129">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [**iStats:: Connect**](istats-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ce902-129">The NPP is connected to the network, but not with the [**IStats::Connect**](istats-connect.md) method.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="ce902-130"><dt>**nmerr \_ keine \_ Konversations \_ Statistik**</dt></span><span class="sxs-lookup"><span data-stu-id="ce902-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="ce902-131">Die Konfiguration für diese Verbindung ist so festgelegt, dass keine Konversations Statistiken gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ce902-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="ce902-132">Wenn Sie die Konversations Statistik speichern möchten, legen Sie die Erfassung fest, legen Sie im konfigurationsblob **NoConversation ationstats = Yes** fest, und starten Sie die Erfassung erneut.</span><span class="sxs-lookup"><span data-stu-id="ce902-132">To save conversation statistics, stop the capture, set **NoConversationStats = YES** in the configuration BLOB, and then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ce902-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce902-133">Remarks</span></span>

<span data-ttu-id="ce902-134">Diese Methode kann nur aufgerufen werden, während die Datenerfassung ausgeführt wird. Wenn die aktuelle Erfassung angehalten ist, wird ein-Rückruf dieser Methode nicht erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce902-134">This method can be called only while data capture is in progress; when the current capture is paused, a call to this method will not succeed.</span></span>

<span data-ttu-id="ce902-135">Um eine Aufzeichnung zu starten, müssen Sie die [**iStats:: Start**](istats-start.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="ce902-135">To start a capture, call the [**IStats::Start**](istats-start.md) method.</span></span> <span data-ttu-id="ce902-136">Um andere Statistik Typen abzurufen, rufen Sie [**iStats:: gettotalstatistics**](istats-gettotalstatistics.md)auf.</span><span class="sxs-lookup"><span data-stu-id="ce902-136">To retrieve other types of statistics, call [**IStats::GetTotalStatistics**](istats-gettotalstatistics.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce902-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce902-137">Requirements</span></span>



| <span data-ttu-id="ce902-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce902-138">Requirement</span></span> | <span data-ttu-id="ce902-139">Wert</span><span class="sxs-lookup"><span data-stu-id="ce902-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce902-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce902-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ce902-141">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce902-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="ce902-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce902-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ce902-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce902-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="ce902-144">Header</span><span class="sxs-lookup"><span data-stu-id="ce902-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce902-145"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce902-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="ce902-146">DLL</span><span class="sxs-lookup"><span data-stu-id="ce902-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce902-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce902-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce902-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce902-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce902-149">**IStats**</span><span class="sxs-lookup"><span data-stu-id="ce902-149">**IStats**</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="ce902-150">**IStats:: gettotalstatistics**</span><span class="sxs-lookup"><span data-stu-id="ce902-150">**IStats::GetTotalStatistics**</span></span>](istats-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="ce902-151">**IStats:: Start**</span><span class="sxs-lookup"><span data-stu-id="ce902-151">**IStats::Start**</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="ce902-152">**IStats:: Connect**</span><span class="sxs-lookup"><span data-stu-id="ce902-152">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="ce902-153">**Sessionstats**</span><span class="sxs-lookup"><span data-stu-id="ce902-153">**SESSIONSTATS**</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="ce902-154">**Stationstats**</span><span class="sxs-lookup"><span data-stu-id="ce902-154">**STATIONSTATS**</span></span>](stationstats.md)
</dt> </dl>

 

 




