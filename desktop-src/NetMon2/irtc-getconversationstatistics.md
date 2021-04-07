---
description: Die getconversation ationstatistics-Methode ruft Sitzungs-und Stations Informationen zur aktuellen Erfassung ab.
ms.assetid: 27f364cd-fee9-4262-b181-c5f15fb12e51
title: 'Untc:: getconversation ationstatistics-Methode (Netmon. h)'
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
ms.openlocfilehash: 758488cb3c3f65922bbf6aac4f39774a5430fc92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864071"
---
# <a name="irtcgetconversationstatistics-method"></a><span data-ttu-id="b56cb-103">Untc:: getconversation ationstatistics-Methode</span><span class="sxs-lookup"><span data-stu-id="b56cb-103">IRTC::GetConversationStatistics method</span></span>

<span data-ttu-id="b56cb-104">Die **getconversation ationstatistics** -Methode ruft [*Sitzungs*](s.md) -und [*Stations Informationen*](s.md) zur aktuellen Erfassung ab.</span><span class="sxs-lookup"><span data-stu-id="b56cb-104">The **GetConversationStatistics** method retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="b56cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b56cb-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="b56cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b56cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b56cb-107">*nsitzungen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b56cb-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b56cb-108">Zeiger auf ein DWORD, das die Anzahl der für die aktuelle Erfassung aufgezeichneten [*Sitzungen*](s.md) enthält.</span><span class="sxs-lookup"><span data-stu-id="b56cb-108">Pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="b56cb-109">*lpsessionstats* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b56cb-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b56cb-110">Zeiger auf eine [sessionstats](sessionstats.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b56cb-110">Pointer to a [SESSIONSTATS](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b56cb-111">*nstations* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b56cb-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b56cb-112">Zeiger auf ein DWORD, das die Anzahl der [*Stationen*](s.md) enthält, die für die aktuelle Erfassung aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="b56cb-112">Pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="b56cb-113">*lpstationstats* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b56cb-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b56cb-114">Zeiger auf eine [stationstats](stationstats.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b56cb-114">Pointer to a [STATIONSTATS](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b56cb-115">*f/oder Lese* \[ Vorgänge in\]</span><span class="sxs-lookup"><span data-stu-id="b56cb-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b56cb-116">Flag, das verwendet wird, um Netzwerkmonitor anzuweisen, den internen Speicher der [sessionstats](sessionstats.md) -und [stationstats](stationstats.md) -Strukturen zu löschen, nachdem die aktuellen Informationen abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="b56cb-116">Flag used to tell Network Monitor to clear out the internal storage of the [SESSIONSTATS](sessionstats.md) and [STATIONSTATS](stationstats.md) structures after it retrieves the current information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b56cb-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b56cb-117">Return value</span></span>

<span data-ttu-id="b56cb-118">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b56cb-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b56cb-119">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="b56cb-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="b56cb-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b56cb-120">Return code</span></span>                                                                                                   | <span data-ttu-id="b56cb-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b56cb-121">Description</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b56cb-122"><dt>**nmerr \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="b56cb-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="b56cb-123">Der npp ist nicht mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="b56cb-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="b56cb-124">Wenden [Sie](irtc-connect.md) sich an, um den NPP mit dem Netzwerk zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="b56cb-124">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="b56cb-125"><dt>**nmerr wird \_ nicht \_ erfasst**</dt></span><span class="sxs-lookup"><span data-stu-id="b56cb-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="b56cb-126">Der NPP erfasst keine Daten.</span><span class="sxs-lookup"><span data-stu-id="b56cb-126">The NPP is not capturing data.</span></span> <span data-ttu-id="b56cb-127">Wenden Sie zum Starten der Erfassung den Befehl " [irren:: Start](irtc-start.md) " an.</span><span class="sxs-lookup"><span data-stu-id="b56cb-127">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="b56cb-128"><dt>**nmerr \_ nicht in \_ Echtzeit**</dt></span><span class="sxs-lookup"><span data-stu-id="b56cb-128"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>           | <span data-ttu-id="b56cb-129">Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der Methode " [iritc:: Connect](irtc-connect.md) ".</span><span class="sxs-lookup"><span data-stu-id="b56cb-129">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                                                                                                                          |
| <dl> <span data-ttu-id="b56cb-130"><dt>**nmerr \_ keine \_ Konversations \_ Statistik**</dt></span><span class="sxs-lookup"><span data-stu-id="b56cb-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="b56cb-131">Die Konfiguration für diese Verbindung ist so festgelegt, dass keine Konversations Statistiken gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b56cb-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="b56cb-132">Um Konversations Statistiken zu speichern, legen Sie die Erfassung fest, legen Sie im konfigurationsblob NoConversation ationstats = Yes fest, und starten Sie die Erfassung erneut.</span><span class="sxs-lookup"><span data-stu-id="b56cb-132">To save conversation statistics, stop the capture, set NoConversationStats = YES in the configuration BLOB, then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b56cb-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b56cb-133">Remarks</span></span>

<span data-ttu-id="b56cb-134">Diese Methode kann nur beim Erfassen von Daten aufgerufen werden. Wenn Sie diese Methode beim Anhalten der aktuellen Erfassung aufzurufen, wird die Methode nicht erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b56cb-134">This method can only be called while you are capturing data; if you call this method while the current capture is paused, the method will not succeed.</span></span> <span data-ttu-id="b56cb-135">Um eine Aufzeichnung zu starten, wenden Sie die Methode " [untc:: Start](irtc-start.md) " an.</span><span class="sxs-lookup"><span data-stu-id="b56cb-135">To start a capture, call the [IRTC::Start](irtc-start.md) method.</span></span>

<span data-ttu-id="b56cb-136">Um andere Statistik Typen abzurufen, rufen Sie die Methode " [iritc:: gettotalstatistics](irtc-gettotalstatistics.md) " auf.</span><span class="sxs-lookup"><span data-stu-id="b56cb-136">To retrieve other types of statistics, call the [IRTC::GetTotalStatistics](irtc-gettotalstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b56cb-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b56cb-137">Requirements</span></span>



| <span data-ttu-id="b56cb-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b56cb-138">Requirement</span></span> | <span data-ttu-id="b56cb-139">Wert</span><span class="sxs-lookup"><span data-stu-id="b56cb-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b56cb-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b56cb-140">Minimum supported client</span></span><br/> | <span data-ttu-id="b56cb-141">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b56cb-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="b56cb-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b56cb-142">Minimum supported server</span></span><br/> | <span data-ttu-id="b56cb-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b56cb-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="b56cb-144">Header</span><span class="sxs-lookup"><span data-stu-id="b56cb-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="b56cb-145"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b56cb-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="b56cb-146">DLL</span><span class="sxs-lookup"><span data-stu-id="b56cb-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b56cb-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b56cb-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b56cb-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b56cb-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b56cb-149">"Iran"</span><span class="sxs-lookup"><span data-stu-id="b56cb-149">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="b56cb-150">Iran:: Connect</span><span class="sxs-lookup"><span data-stu-id="b56cb-150">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="b56cb-151">"Irren:: gettotalstatistics"</span><span class="sxs-lookup"><span data-stu-id="b56cb-151">IRTC::GetTotalStatistics</span></span>](irtc-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="b56cb-152">"Iran:: Start"</span><span class="sxs-lookup"><span data-stu-id="b56cb-152">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="b56cb-153">Sessionstats</span><span class="sxs-lookup"><span data-stu-id="b56cb-153">SESSIONSTATS</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="b56cb-154">Stationstats</span><span class="sxs-lookup"><span data-stu-id="b56cb-154">STATIONSTATS</span></span>](stationstats.md)
</dt> </dl>

 

 




