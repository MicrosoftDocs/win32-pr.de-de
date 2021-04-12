---
description: Ein Rückruf, der den Host darüber benachrichtigt, welche Pipeline Stufen keine Mesh-Daten für das in der zugeordneten Anforderung angegebene Ereignis zurückgeben können.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataNotAvailableCallback\_UINT\_PipeLineStageError\_arr\_UINT\_UINT\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ipipelinestagescallback:: meshdatanotavailablecallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A51E7C45-C1F0-4576-8638-9C3B185385BA
api_name:
- IPipeLineStagesCallback.MeshDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 42391c342e2f11b39d1535b5286a92e161d0fd9b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482582"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventidspanipipelinestagescallbackmeshdatanotavailablecallback-method"></a><span data-ttu-id="2219c-103"><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>Ipipelinestagescallback:: meshdatanotavailablecallback-Methode</span><span class="sxs-lookup"><span data-stu-id="2219c-103"><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>IPipeLineStagesCallback::MeshDataNotAvailableCallback method</span></span>

<span data-ttu-id="2219c-104">Ein Rückruf, der den Host darüber benachrichtigt, welche Pipeline Stufen keine Mesh-Daten für das in der zugeordneten Anforderung angegebene Ereignis zurückgeben können.</span><span class="sxs-lookup"><span data-stu-id="2219c-104">A callback that notifies the host of which pipeline stages are not able to return mesh data for the event specified in the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="2219c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2219c-105">Syntax</span></span>


```C++
HRESULT MeshDataNotAvailableCallback(
   UINT                  numberStages,
   PipeLineStageError [] count0_errors,
   UINT                  width,
   UINT                  height,
   EventID               eid
);
```

## <a name="parameters"></a><span data-ttu-id="2219c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2219c-106">Parameters</span></span>

<span data-ttu-id="2219c-107">*anzahlphasen* </span><span class="sxs-lookup"><span data-stu-id="2219c-107">*numberStages* </span></span>  
<span data-ttu-id="2219c-108">Die Anzahl der zurückgegebenen Phasenfehler.</span><span class="sxs-lookup"><span data-stu-id="2219c-108">The number of stage errors returned.</span></span>

<span data-ttu-id="2219c-109">*count0- \_ Fehler* </span><span class="sxs-lookup"><span data-stu-id="2219c-109">*count0\_errors* </span></span>  
<span data-ttu-id="2219c-110">Fehler in der Pipeline Stufe.</span><span class="sxs-lookup"><span data-stu-id="2219c-110">The pipeline stage errors.</span></span>

<span data-ttu-id="2219c-111">*Breite* </span><span class="sxs-lookup"><span data-stu-id="2219c-111">*width* </span></span>  
<span data-ttu-id="2219c-112">Die Breite der Austausch Kette mit dem Draw-Befehl.</span><span class="sxs-lookup"><span data-stu-id="2219c-112">The width of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="2219c-113">Diese wird verwendet, wenn Pipeline-Vorschau Bilder angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="2219c-113">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="2219c-114">*Flugh* </span><span class="sxs-lookup"><span data-stu-id="2219c-114">*height* </span></span>  
<span data-ttu-id="2219c-115">Die Höhe der Austausch Kette mit dem Draw-Befehl.</span><span class="sxs-lookup"><span data-stu-id="2219c-115">The height of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="2219c-116">Diese wird verwendet, wenn Pipeline-Vorschau Bilder angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="2219c-116">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="2219c-117">*VEI* </span><span class="sxs-lookup"><span data-stu-id="2219c-117">*eid* </span></span>  
<span data-ttu-id="2219c-118">Das in den Ergebnissen dargestellte Ereignis.</span><span class="sxs-lookup"><span data-stu-id="2219c-118">The event represented in the results.</span></span>

## <a name="return-value"></a><span data-ttu-id="2219c-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2219c-119">Return value</span></span>

<span data-ttu-id="2219c-120">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2219c-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2219c-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2219c-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2219c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2219c-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="2219c-123">Header</span><span class="sxs-lookup"><span data-stu-id="2219c-123">Header</span></span></p></td><td><span data-ttu-id="2219c-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="2219c-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="2219c-125"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2219c-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="2219c-126">**Ipipelinestagescallback**</span><span class="sxs-lookup"><span data-stu-id="2219c-126">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
