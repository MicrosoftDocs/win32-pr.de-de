---
description: Ein Rückruf, der den Host der Bild Informationen von Pipeline Stufen benachrichtigt, die von der assocaas-Anforderung zurückgegeben werden.
MS-HAID: vspixengine.IPipeLineStagesCallback\_ResultCallback\_PipeLineStagesID\_EventID\_DWORD\_DWORD\_DWORD\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ipipelinestagescallback:: resultCallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 922DBEE0-CE47-4292-A5E6-4503E6F77A23
api_name:
- IPipeLineStagesCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c9c09c0fe1e68dc0d0613589ff8b3d5037face9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104342048"
---
# <a name="span-idvspixengineipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arrspanipipelinestagescallbackresultcallback-method"></a><span data-ttu-id="96140-103"><span id="vspixengine.ipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arr"></span>Ipipelinestagescallback:: resultCallback-Methode</span><span class="sxs-lookup"><span data-stu-id="96140-103"><span id="vspixengine.ipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arr"></span>IPipeLineStagesCallback::ResultCallback method</span></span>

<span data-ttu-id="96140-104">Ein Rückruf, der den Host der Bild Informationen von Pipeline Stufen benachrichtigt, die von der assocaas-Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="96140-104">A callback that notifies the host of pipeline stages image information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="96140-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="96140-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   PipeLineStagesID stageId,
   EventID          eid,
   DWORD            width,
   DWORD            height,
   DWORD            format,
   DWORD            size,
   BYTE []          count5_buffer
);
```

## <a name="parameters"></a><span data-ttu-id="96140-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="96140-106">Parameters</span></span>

<span data-ttu-id="96140-107">*stageid* </span><span class="sxs-lookup"><span data-stu-id="96140-107">*stageId* </span></span>  
<span data-ttu-id="96140-108">Die in den Ergebnissen dargestellte Pipeline Stufe.</span><span class="sxs-lookup"><span data-stu-id="96140-108">The pipeline stage represented in the results.</span></span>

<span data-ttu-id="96140-109">*VEI* </span><span class="sxs-lookup"><span data-stu-id="96140-109">*eid* </span></span>  
<span data-ttu-id="96140-110">Das in den Ergebnissen dargestellte Ereignis.</span><span class="sxs-lookup"><span data-stu-id="96140-110">The event represented in the results.</span></span>

<span data-ttu-id="96140-111">*Breite* </span><span class="sxs-lookup"><span data-stu-id="96140-111">*width* </span></span>  
<span data-ttu-id="96140-112">Die Breite des Bild der Pipeline Visualisierung.</span><span class="sxs-lookup"><span data-stu-id="96140-112">The width of the pipeline visualization image.</span></span>

<span data-ttu-id="96140-113">*Flugh* </span><span class="sxs-lookup"><span data-stu-id="96140-113">*height* </span></span>  
<span data-ttu-id="96140-114">Die Höhe des Bild der Pipeline Visualisierung.</span><span class="sxs-lookup"><span data-stu-id="96140-114">The height of the pipeline visualization image.</span></span>

<span data-ttu-id="96140-115">*Ges* </span><span class="sxs-lookup"><span data-stu-id="96140-115">*format* </span></span>  
<span data-ttu-id="96140-116">Das Format des Pipeline Visualisierungs Bilds.</span><span class="sxs-lookup"><span data-stu-id="96140-116">The format of the pipeline visualization image.</span></span>

<span data-ttu-id="96140-117">*Größe* </span><span class="sxs-lookup"><span data-stu-id="96140-117">*size* </span></span>  
<span data-ttu-id="96140-118">Die Größe des Bilds in Bytes.</span><span class="sxs-lookup"><span data-stu-id="96140-118">The size of the image in bytes.</span></span>

<span data-ttu-id="96140-119">*count5- \_ Puffer* </span><span class="sxs-lookup"><span data-stu-id="96140-119">*count5\_buffer* </span></span>  
<span data-ttu-id="96140-120">Das Bild der Pipeline Visualisierung.</span><span class="sxs-lookup"><span data-stu-id="96140-120">The pipeline visualization image.</span></span>

## <a name="return-value"></a><span data-ttu-id="96140-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96140-121">Return value</span></span>

<span data-ttu-id="96140-122">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="96140-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="96140-123">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="96140-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="96140-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96140-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="96140-125">Header</span><span class="sxs-lookup"><span data-stu-id="96140-125">Header</span></span></p></td><td><span data-ttu-id="96140-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="96140-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="96140-127"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96140-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="96140-128">**Ipipelinestagescallback**</span><span class="sxs-lookup"><span data-stu-id="96140-128">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
