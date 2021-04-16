---
description: Anforderungen zum Zwischenspeichern des Offline Analyse Berichts der angegebenen Frames.
MS-HAID: vspixengine.IOfflineAnalysisCacheRequest\_RequestOfflineAnalysisReportAvailabilityAsync\_DWORD\_DWORD\_arr\_IOfflineAnalysisCacheCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iofflineanalysiscacherequest:: requestofflineanalysisreportavailabilityasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10FA71F8-813D-4788-92C8-00B30A9AE5CC
api_name:
- IOfflineAnalysisCacheRequest.RequestOfflineAnalysisReportAvailabilityAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6e2dfdb1e2a2cc113f9585a818550dd60aa73ae2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522744"
---
# <a name="span-idvspixengineiofflineanalysiscacherequest_requestofflineanalysisreportavailabilityasync_dword_dword_arr_iofflineanalysiscachecallback_ptrspaniofflineanalysiscacherequestrequestofflineanalysisreportavailabilityasync-method"></a><span data-ttu-id="a9d73-103"><span id="vspixengine.iofflineanalysiscacherequest_requestofflineanalysisreportavailabilityasync_dword_dword_arr_iofflineanalysiscachecallback_ptr"></span>Iofflineanalysiscacherequest:: requestofflineanalysisreportavailabilityasync-Methode</span><span class="sxs-lookup"><span data-stu-id="a9d73-103"><span id="vspixengine.iofflineanalysiscacherequest_requestofflineanalysisreportavailabilityasync_dword_dword_arr_iofflineanalysiscachecallback_ptr"></span>IOfflineAnalysisCacheRequest::RequestOfflineAnalysisReportAvailabilityAsync method</span></span>

<span data-ttu-id="a9d73-104">Anforderungen zum Zwischenspeichern des Offline Analyse Berichts der angegebenen Frames.</span><span class="sxs-lookup"><span data-stu-id="a9d73-104">Requests to cache offline analysis report of the specified frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9d73-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9d73-105">Syntax</span></span>


```C++
HRESULT RequestOfflineAnalysisReportAvailabilityAsync(
   DWORD                           numFrames,
   DWORD []                        count0_frameNumbers,
   IOfflineAnalysisCacheCallback * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="a9d73-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9d73-106">Parameters</span></span>

<span data-ttu-id="a9d73-107">*numFrames* </span><span class="sxs-lookup"><span data-stu-id="a9d73-107">*numFrames* </span></span>  
<span data-ttu-id="a9d73-108">Die Anzahl der Frames, für die Analyseberichte generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a9d73-108">The number of frames to generate analysis reports for.</span></span>

<span data-ttu-id="a9d73-109">*count0 \_ frameNum* </span><span class="sxs-lookup"><span data-stu-id="a9d73-109">*count0\_frameNumbers* </span></span>  
<span data-ttu-id="a9d73-110">Die angegebenen Frames.</span><span class="sxs-lookup"><span data-stu-id="a9d73-110">The specified frames.</span></span>

<span data-ttu-id="a9d73-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="a9d73-111">*requestCallback* </span></span>  
<span data-ttu-id="a9d73-112">Die Adresse eines Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9d73-112">The address of a callback used to notify the host of results.</span></span>

## <a name="return-value"></a><span data-ttu-id="a9d73-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9d73-113">Return value</span></span>

<span data-ttu-id="a9d73-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a9d73-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a9d73-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a9d73-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9d73-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9d73-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a9d73-117">Header</span><span class="sxs-lookup"><span data-stu-id="a9d73-117">Header</span></span></p></td><td><span data-ttu-id="a9d73-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a9d73-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a9d73-119"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9d73-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a9d73-120">**Iofflineanalysiscacherequest**</span><span class="sxs-lookup"><span data-stu-id="a9d73-120">**IOfflineAnalysisCacheRequest**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscacherequest)

 

 
