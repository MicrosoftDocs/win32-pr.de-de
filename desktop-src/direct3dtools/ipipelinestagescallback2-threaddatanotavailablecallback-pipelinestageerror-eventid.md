---
description: Ein Rückruf, der den Host benachrichtigt, dass threaddata für eine bestimmte Pipeline Phase und ein bestimmtes Ereignis nicht verfügbar ist.
MS-HAID: vspixengine.IPipeLineStagesCallback2\_ThreadDataNotAvailableCallback\_PipeLineStageError\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback2:: threaddatanotavailablecallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 231DC830-5F1A-4DDA-B5D0-C7FBCEDCB2A0
api_name:
- IPipeLineStagesCallback2.ThreadDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a0c9cc0bc32b6d01394be1403e961d7ae37a1d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346617"
---
# <a name="span-idvspixengineipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventidspanipipelinestagescallback2threaddatanotavailablecallback-method"></a><span data-ttu-id="9606f-103"><span id="vspixengine.ipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventid"></span>IPipeLineStagesCallback2:: threaddatanotavailablecallback-Methode</span><span class="sxs-lookup"><span data-stu-id="9606f-103"><span id="vspixengine.ipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventid"></span>IPipeLineStagesCallback2::ThreadDataNotAvailableCallback method</span></span>

<span data-ttu-id="9606f-104">Ein Rückruf, der den Host benachrichtigt, dass threaddata für eine bestimmte Pipeline Phase und ein bestimmtes Ereignis nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9606f-104">A callback that notifies the host that ThreadData is unavailable for a particular pipeline stage and event.</span></span>

## <a name="syntax"></a><span data-ttu-id="9606f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9606f-105">Syntax</span></span>


```C++
HRESULT ThreadDataNotAvailableCallback(
   PipeLineStageError error,
   EventID            eid
);
```

## <a name="parameters"></a><span data-ttu-id="9606f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9606f-106">Parameters</span></span>

<span data-ttu-id="9606f-107">*Zeit* </span><span class="sxs-lookup"><span data-stu-id="9606f-107">*error* </span></span>  
<span data-ttu-id="9606f-108">Fehler bei der Pipeline Stufe.</span><span class="sxs-lookup"><span data-stu-id="9606f-108">The pipeline stage error.</span></span>

<span data-ttu-id="9606f-109">*VEI* </span><span class="sxs-lookup"><span data-stu-id="9606f-109">*eid* </span></span>  
<span data-ttu-id="9606f-110">Das in den Ergebnissen dargestellte Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9606f-110">The event represented in the results.</span></span>

## <a name="return-value"></a><span data-ttu-id="9606f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9606f-111">Return value</span></span>

<span data-ttu-id="9606f-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="9606f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9606f-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9606f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9606f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9606f-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9606f-115">Header</span><span class="sxs-lookup"><span data-stu-id="9606f-115">Header</span></span></p></td><td><span data-ttu-id="9606f-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="9606f-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9606f-117"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9606f-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9606f-118">**IPipeLineStagesCallback2**</span><span class="sxs-lookup"><span data-stu-id="9606f-118">**IPipeLineStagesCallback2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback2)

 

 
