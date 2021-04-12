---
description: Anforderungen zum Abbrechen der Offline Analyse in einer Offline Analyse Anforderung.
MS-HAID: vspixengine.IOfflineAnalysisRequest\_CancelOfflineAnalysisAsync\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iofflineanalysisrequest:: cancelofflineanalysisasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 20107890-DF7B-4483-9D2C-1D9164366504
api_name:
- IOfflineAnalysisRequest.CancelOfflineAnalysisAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 79329d27aff74efb7d08c7cc182ddb6e21f96cba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481499"
---
# <a name="span-idvspixengineiofflineanalysisrequest_cancelofflineanalysisasync_dwordspaniofflineanalysisrequestcancelofflineanalysisasync-method"></a><span data-ttu-id="030ae-103"><span id="vspixengine.iofflineanalysisrequest_cancelofflineanalysisasync_dword"></span>Iofflineanalysisrequest:: cancelofflineanalysisasync-Methode</span><span class="sxs-lookup"><span data-stu-id="030ae-103"><span id="vspixengine.iofflineanalysisrequest_cancelofflineanalysisasync_dword"></span>IOfflineAnalysisRequest::CancelOfflineAnalysisAsync method</span></span>

<span data-ttu-id="030ae-104">Anforderungen zum Abbrechen der Offline Analyse in einer Offline Analyse Anforderung.</span><span class="sxs-lookup"><span data-stu-id="030ae-104">Requests to cancel offline analysis in an offline analysis request.</span></span>

## <a name="syntax"></a><span data-ttu-id="030ae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="030ae-105">Syntax</span></span>


```C++
HRESULT CancelOfflineAnalysisAsync(
   DWORD cookie
);
```

## <a name="parameters"></a><span data-ttu-id="030ae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="030ae-106">Parameters</span></span>

<span data-ttu-id="030ae-107">*KS* </span><span class="sxs-lookup"><span data-stu-id="030ae-107">*cookie* </span></span>  
<span data-ttu-id="030ae-108">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="030ae-108">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

## <a name="return-value"></a><span data-ttu-id="030ae-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="030ae-109">Return value</span></span>

<span data-ttu-id="030ae-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="030ae-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="030ae-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="030ae-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="030ae-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="030ae-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="030ae-113">Header</span><span class="sxs-lookup"><span data-stu-id="030ae-113">Header</span></span></p></td><td><span data-ttu-id="030ae-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="030ae-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="030ae-115"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="030ae-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="030ae-116">**Iofflineanalysisrequest**</span><span class="sxs-lookup"><span data-stu-id="030ae-116">**IOfflineAnalysisRequest**</span></span>](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
