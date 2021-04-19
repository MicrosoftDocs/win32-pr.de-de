---
description: Die getconversation ationstatistics-Methode ruft Sitzungs-und Stations Informationen zur aktuellen Erfassung ab.
ms.assetid: 0164fa0e-90f2-4b97-be9d-55d172f8112d
title: 'Idelta-DC:: getconversation ationstatistics-Methode (Netmon. h)'
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
ms.openlocfilehash: aaba5ccfbab48639f53395519f001f5f8e85e483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343039"
---
# <a name="idelaydcgetconversationstatistics-method"></a><span data-ttu-id="36bce-103">Idelta aydc:: getconversation ationstatistics-Methode</span><span class="sxs-lookup"><span data-stu-id="36bce-103">IDelaydC::GetConversationStatistics method</span></span>

<span data-ttu-id="36bce-104">Die **getconversation ationstatistics** -Methode ruft [*Sitzungs*](s.md) -und [*Stations Informationen*](s.md) zur aktuellen Erfassung ab.</span><span class="sxs-lookup"><span data-stu-id="36bce-104">The **GetConversationStatistics** method retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="36bce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="36bce-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="36bce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="36bce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36bce-107">*nsitzungen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="36bce-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36bce-108">Zeiger auf ein DWORD, das die Anzahl der für die aktuelle Erfassung aufgezeichneten [*Sitzungen*](s.md) enthält.</span><span class="sxs-lookup"><span data-stu-id="36bce-108">Pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="36bce-109">*lpsessionstats* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="36bce-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36bce-110">Zeiger auf eine [sessionstats](sessionstats.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="36bce-110">Pointer to a [SESSIONSTATS](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="36bce-111">*nstations* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="36bce-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36bce-112">Zeiger auf ein DWORD, das die Anzahl der [*Stationen*](s.md) enthält, die für die aktuelle Erfassung aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="36bce-112">Pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="36bce-113">*lpstationstats* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="36bce-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36bce-114">Zeiger auf eine [stationstats](stationstats.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="36bce-114">Pointer to a [STATIONSTATS](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="36bce-115">*f/oder Lese* \[ Vorgänge in\]</span><span class="sxs-lookup"><span data-stu-id="36bce-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36bce-116">Flag, das verwendet wird, um Netzwerkmonitor anzuweisen, den internen Speicher der [sessionstats](sessionstats.md) -und [stationstats](stationstats.md) -Strukturen zu löschen, nachdem die aktuellen Informationen abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="36bce-116">Flag used to tell Network Monitor to clear out the internal storage of the [SESSIONSTATS](sessionstats.md) and [STATIONSTATS](stationstats.md) structures after it retrieves the current information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36bce-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36bce-117">Return value</span></span>

<span data-ttu-id="36bce-118">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="36bce-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="36bce-119">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="36bce-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="36bce-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="36bce-120">Return code</span></span>                                                                                                   | <span data-ttu-id="36bce-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36bce-121">Description</span></span>                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="36bce-122"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="36bce-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="36bce-123">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="36bce-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="36bce-124">Wenden Sie [idelta-DC:: Connect](idelaydc-connect.md) an, um die NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="36bce-124">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="36bce-125"><dt>**nmerr wird \_ nicht \_ erfasst**</dt></span><span class="sxs-lookup"><span data-stu-id="36bce-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="36bce-126">Der NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="36bce-126">The NPP is not capturing data.</span></span> <span data-ttu-id="36bce-127">Wenden Sie [idelta-DC:: Start](idelaydc-start.md) an, um die Erfassung zu starten.</span><span class="sxs-lookup"><span data-stu-id="36bce-127">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="36bce-128"><dt>**nmerr \_ nicht \_ verzögert**</dt></span><span class="sxs-lookup"><span data-stu-id="36bce-128"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>            | <span data-ttu-id="36bce-129">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [idelta aydc:: Connect](idelaydc-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="36bce-129">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="36bce-130"><dt>**nmerr \_ keine \_ Konversations \_ Statistik**</dt></span><span class="sxs-lookup"><span data-stu-id="36bce-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="36bce-131">Die Konfiguration für diese Verbindung ist so festgelegt, dass keine Konversations Statistiken gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="36bce-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="36bce-132">Wenn Sie die Konversations Statistik speichern möchten, legen Sie die Erfassung fest, legen Sie im konfigurationsblob NoConversation ationstats = Yes fest, und starten Sie die Erfassung erneut.</span><span class="sxs-lookup"><span data-stu-id="36bce-132">To save conversation statistics, stop the capture, set NoConversationStats = YES in the configuration BLOB, and then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="36bce-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36bce-133">Remarks</span></span>

<span data-ttu-id="36bce-134">Diese Methode kann nur aufgerufen werden, während die Datenerfassung ausgeführt wird. Wenn die aktuelle Erfassung angehalten ist, werden Aufrufe dieser Methode nicht erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="36bce-134">This method can only be called only while data capture is in progress; when the current capture is paused, calls to this method will not succeed.</span></span> <span data-ttu-id="36bce-135">Um eine Aufzeichnung zu starten, müssen Sie die [idelta-DC:: Start](idelaydc-start.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="36bce-135">To start a capture, call the [IDelaydC::Start](idelaydc-start.md) method.</span></span>

<span data-ttu-id="36bce-136">Um andere Statistik Typen abzurufen, rufen Sie [idelta aydc:: gettotalstatistics](idelaydc-gettotalstatistics.md)auf.</span><span class="sxs-lookup"><span data-stu-id="36bce-136">To retrieve other types of statistics, call [IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="36bce-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36bce-137">Requirements</span></span>



| <span data-ttu-id="36bce-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36bce-138">Requirement</span></span> | <span data-ttu-id="36bce-139">Wert</span><span class="sxs-lookup"><span data-stu-id="36bce-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36bce-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36bce-140">Minimum supported client</span></span><br/> | <span data-ttu-id="36bce-141">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36bce-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="36bce-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36bce-142">Minimum supported server</span></span><br/> | <span data-ttu-id="36bce-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36bce-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="36bce-144">Header</span><span class="sxs-lookup"><span data-stu-id="36bce-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="36bce-145"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="36bce-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="36bce-146">DLL</span><span class="sxs-lookup"><span data-stu-id="36bce-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36bce-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36bce-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36bce-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36bce-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36bce-149">Idelta-DC</span><span class="sxs-lookup"><span data-stu-id="36bce-149">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="36bce-150">Idelta aydc:: Connect</span><span class="sxs-lookup"><span data-stu-id="36bce-150">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="36bce-151">Idelta-DC:: gettotalstatistics</span><span class="sxs-lookup"><span data-stu-id="36bce-151">IDelaydC::GetTotalStatistics</span></span>](idelaydc-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="36bce-152">Idelta aydc:: Start</span><span class="sxs-lookup"><span data-stu-id="36bce-152">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="36bce-153">Sessionstats</span><span class="sxs-lookup"><span data-stu-id="36bce-153">SESSIONSTATS</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="36bce-154">Stationstats</span><span class="sxs-lookup"><span data-stu-id="36bce-154">STATIONSTATS</span></span>](stationstats.md)
</dt> </dl>

 

 




