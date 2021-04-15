---
description: Eine asynchrone Anforderung zum erhalten von Vorschaubildern für das Fenstergrafik Pipeline Stufen.
MS-HAID: vspixengine.IPipeLineStagesRequest\_RequestAsync\_EventID\_DWORD\_PipeLineStagesID\_arr\_DWORD\_DWORD\_IPipeLineStagesCallback\_ptr\_BOOL\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ipipelinestagesrequest:: requestasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B725E541-EAC8-49DE-9EE7-C20698FE4A1F
api_name:
- IPipeLineStagesRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 89c67689668aa1c4227b33d861495c2504e5d626
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521851"
---
# <a name="span-idvspixengineipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dwordspanipipelinestagesrequestrequestasync-method"></a><span data-ttu-id="f8175-103"><span id="vspixengine.ipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dword"></span>Ipipelinestagesrequest:: requestasync-Methode</span><span class="sxs-lookup"><span data-stu-id="f8175-103"><span id="vspixengine.ipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dword"></span>IPipeLineStagesRequest::RequestAsync method</span></span>

<span data-ttu-id="f8175-104">Eine asynchrone Anforderung zum erhalten von Vorschaubildern für das Fenstergrafik Pipeline Stufen.</span><span class="sxs-lookup"><span data-stu-id="f8175-104">An asynchronous request to get preview images for the graphics pipeline stages window.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8175-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8175-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID                   eventID,
   DWORD                     numStages,
   PipeLineStagesID []       count1_stageIds,
   DWORD                     width,
   DWORD                     height,
   IPipeLineStagesCallback * requestCallback,
   BOOL                      getMeshData,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="f8175-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8175-106">Parameters</span></span>

<span data-ttu-id="f8175-107">*EventID* </span><span class="sxs-lookup"><span data-stu-id="f8175-107">*eventID* </span></span>  
<span data-ttu-id="f8175-108">Die ID des Grafik Ereignisses, für das Bilder angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f8175-108">The ID of the graphics event that images are being requested for.</span></span>

<span data-ttu-id="f8175-109">*numphasen* </span><span class="sxs-lookup"><span data-stu-id="f8175-109">*numStages* </span></span>  
<span data-ttu-id="f8175-110">Die Anzahl der Pipeline Stufen, für die Bilder angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f8175-110">The number of pipeline stages that images are being requested for.</span></span>

<span data-ttu-id="f8175-111">*count1 \_ stageids* </span><span class="sxs-lookup"><span data-stu-id="f8175-111">*count1\_stageIds* </span></span>  
<span data-ttu-id="f8175-112">IDs der Pipeline Stufen, für die Bilder angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f8175-112">IDs of the pipeline stages that images are being requested for.</span></span>

<span data-ttu-id="f8175-113">*Breite* </span><span class="sxs-lookup"><span data-stu-id="f8175-113">*width* </span></span>  
<span data-ttu-id="f8175-114">Die Breite der angeforderten Bilder.</span><span class="sxs-lookup"><span data-stu-id="f8175-114">The width of the requested images.</span></span>

<span data-ttu-id="f8175-115">*Flugh* </span><span class="sxs-lookup"><span data-stu-id="f8175-115">*height* </span></span>  
<span data-ttu-id="f8175-116">Die Höhe der angeforderten Bilder.</span><span class="sxs-lookup"><span data-stu-id="f8175-116">The height of the requested images.</span></span>

<span data-ttu-id="f8175-117">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="f8175-117">*requestCallback* </span></span>  
<span data-ttu-id="f8175-118">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f8175-118">The address of the callback used to notify the host of results.</span></span>

<span data-ttu-id="f8175-119">*getmeshdata* </span><span class="sxs-lookup"><span data-stu-id="f8175-119">*getMeshData* </span></span>  
<span data-ttu-id="f8175-120">true, um Mesh-Daten zurückzugeben. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="f8175-120">true to return mesh data; otherwise false.</span></span>

<span data-ttu-id="f8175-121">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="f8175-121">*requestCookie* </span></span>  
<span data-ttu-id="f8175-122">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8175-122">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="f8175-123">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="f8175-123">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="f8175-124">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8175-124">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8175-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8175-125">Return value</span></span>

<span data-ttu-id="f8175-126">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f8175-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f8175-127">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8175-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8175-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8175-128">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f8175-129">Header</span><span class="sxs-lookup"><span data-stu-id="f8175-129">Header</span></span></p></td><td><span data-ttu-id="f8175-130">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f8175-130">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f8175-131"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8175-131"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f8175-132">**Ipipelinestagesrequest**</span><span class="sxs-lookup"><span data-stu-id="f8175-132">**IPipeLineStagesRequest**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest)

 

 
