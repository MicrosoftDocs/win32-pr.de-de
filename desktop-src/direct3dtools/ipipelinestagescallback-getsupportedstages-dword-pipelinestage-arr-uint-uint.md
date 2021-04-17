---
description: Ein Rückruf, der den Host darüber benachrichtigt, welche Pipeline Stufen vom zeichnen-Befehl der assocaas-Anforderung verwendet werden.
MS-HAID: vspixengine.IPipeLineStagesCallback\_GetSupportedStages\_DWORD\_PipeLineStage\_arr\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ipipelinestagescallback:: getsupportedstages-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7046A41-5C9C-42FE-B1E2-879A47CE08E3
api_name:
- IPipeLineStagesCallback.GetSupportedStages
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c55c7f8bfa6b5b69ea2a46dd6023021a6b4ab6c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521136"
---
# <a name="span-idvspixengineipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uintspanipipelinestagescallbackgetsupportedstages-method"></a><span data-ttu-id="94ecd-103"><span id="vspixengine.ipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uint"></span>Ipipelinestagescallback:: getsupportedstages-Methode</span><span class="sxs-lookup"><span data-stu-id="94ecd-103"><span id="vspixengine.ipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uint"></span>IPipeLineStagesCallback::GetSupportedStages method</span></span>

<span data-ttu-id="94ecd-104">Ein Rückruf, der den Host darüber benachrichtigt, welche Pipeline Stufen vom zeichnen-Befehl der assocaas-Anforderung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="94ecd-104">A callback that notifies the host of which pipeline stages are used by the draw call of the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="94ecd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="94ecd-105">Syntax</span></span>


```C++
HRESULT GetSupportedStages(
   DWORD            numColumns,
   PipeLineStage [] count0_pStages,
   UINT             swapChainWidth,
   UINT             swapChainHeight
);
```

## <a name="parameters"></a><span data-ttu-id="94ecd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="94ecd-106">Parameters</span></span>

<span data-ttu-id="94ecd-107">*NumColumns* </span><span class="sxs-lookup"><span data-stu-id="94ecd-107">*numColumns* </span></span>  
<span data-ttu-id="94ecd-108">Die Anzahl der zurückgegebenen Stufen.</span><span class="sxs-lookup"><span data-stu-id="94ecd-108">The number of stages returned.</span></span>

<span data-ttu-id="94ecd-109">*count0 \_ pstufen* </span><span class="sxs-lookup"><span data-stu-id="94ecd-109">*count0\_pStages* </span></span>  
<span data-ttu-id="94ecd-110">Die Pipeline Stufen.</span><span class="sxs-lookup"><span data-stu-id="94ecd-110">The pipeline stages.</span></span>

<span data-ttu-id="94ecd-111">*Swap-chainwidth* </span><span class="sxs-lookup"><span data-stu-id="94ecd-111">*swapChainWidth* </span></span>  
<span data-ttu-id="94ecd-112">Die Breite der Austausch Kette mit dem Draw-Befehl.</span><span class="sxs-lookup"><span data-stu-id="94ecd-112">The width of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="94ecd-113">Diese wird verwendet, wenn Pipeline-Vorschau Bilder angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="94ecd-113">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="94ecd-114">*Swap-chainheight* </span><span class="sxs-lookup"><span data-stu-id="94ecd-114">*swapChainHeight* </span></span>  
<span data-ttu-id="94ecd-115">Die Höhe der Austausch Kette mit dem Draw-Befehl.</span><span class="sxs-lookup"><span data-stu-id="94ecd-115">The height of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="94ecd-116">Diese wird verwendet, wenn Pipeline-Vorschau Bilder angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="94ecd-116">This is used when requesting pipeline preview images.</span></span>

## <a name="return-value"></a><span data-ttu-id="94ecd-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94ecd-117">Return value</span></span>

<span data-ttu-id="94ecd-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="94ecd-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="94ecd-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="94ecd-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="94ecd-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94ecd-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="94ecd-121">Header</span><span class="sxs-lookup"><span data-stu-id="94ecd-121">Header</span></span></p></td><td><span data-ttu-id="94ecd-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="94ecd-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="94ecd-123"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94ecd-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="94ecd-124">**Ipipelinestagescallback**</span><span class="sxs-lookup"><span data-stu-id="94ecd-124">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
