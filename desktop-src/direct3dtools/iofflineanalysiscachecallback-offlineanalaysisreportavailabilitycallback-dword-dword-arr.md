---
description: Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, welche Frames Offline Analyseberichte enthalten.
MS-HAID: vspixengine.IOfflineAnalysisCacheCallback\_OfflineAnalaysisReportAvailabilityCallback\_DWORD\_DWORD\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iofflineanalysiscachecallback:: offlineanalaysisreportavailabilitycallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2061EB62-4CBD-4668-BFCD-6E43014BB406
api_name:
- IOfflineAnalysisCacheCallback.OfflineAnalaysisReportAvailabilityCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: adbffbeb79aaf648c3319cf572dcbc905e9fd307
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344798"
---
# <a name="span-idvspixengineiofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arrspaniofflineanalysiscachecallbackofflineanalaysisreportavailabilitycallback-method"></a><span data-ttu-id="3396b-103"><span id="vspixengine.iofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arr"></span>Iofflineanalysiscachecallback:: offlineanalaysisreportavailabilitycallback-Methode</span><span class="sxs-lookup"><span data-stu-id="3396b-103"><span id="vspixengine.iofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arr"></span>IOfflineAnalysisCacheCallback::OfflineAnalaysisReportAvailabilityCallback method</span></span>

<span data-ttu-id="3396b-104">Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, welche Frames Offline Analyseberichte enthalten.</span><span class="sxs-lookup"><span data-stu-id="3396b-104">A callback function used to notify the host about which frames have offline analysis reports available.</span></span>

## <a name="syntax"></a><span data-ttu-id="3396b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3396b-105">Syntax</span></span>


```C++
HRESULT OfflineAnalaysisReportAvailabilityCallback(
   DWORD    numFramesWithReports,
   DWORD [] count0_framesWithReports
);
```

## <a name="parameters"></a><span data-ttu-id="3396b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3396b-106">Parameters</span></span>

<span data-ttu-id="3396b-107">*numframeswithreports* </span><span class="sxs-lookup"><span data-stu-id="3396b-107">*numFramesWithReports* </span></span>  
<span data-ttu-id="3396b-108">Die Anzahl der Frames in count0 \_ frameswithreports.</span><span class="sxs-lookup"><span data-stu-id="3396b-108">The number of frames in count0\_framesWithReports.</span></span>

<span data-ttu-id="3396b-109">*count0 \_ frameswithreports* </span><span class="sxs-lookup"><span data-stu-id="3396b-109">*count0\_framesWithReports* </span></span>  
<span data-ttu-id="3396b-110">Ein Array, das die Frame Nummern der Frames enthält, für die Offline Analyseberichte verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3396b-110">An array containing the frame numbers of the frames that have offline analysis reports available.</span></span>

## <a name="return-value"></a><span data-ttu-id="3396b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3396b-111">Return value</span></span>

<span data-ttu-id="3396b-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="3396b-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3396b-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3396b-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3396b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3396b-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3396b-115">Header</span><span class="sxs-lookup"><span data-stu-id="3396b-115">Header</span></span></p></td><td><span data-ttu-id="3396b-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="3396b-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3396b-117"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3396b-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3396b-118">**Iofflineanalysiscachecallback**</span><span class="sxs-lookup"><span data-stu-id="3396b-118">**IOfflineAnalysisCacheCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscachecallback)

 

 
