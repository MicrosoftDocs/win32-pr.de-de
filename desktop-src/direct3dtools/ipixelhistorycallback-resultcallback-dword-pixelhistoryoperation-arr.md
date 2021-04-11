---
description: Ein Rückruf, der den Host über Ergebnisse der Pixel Verlaufs Anforderung benachrichtigt.
MS-HAID: vspixengine.IPixelHistoryCallback\_ResultCallback\_DWORD\_PixelHistoryOperation\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ipixelhistorycallback:: resultCallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1F7D0EA5-402A-49C4-A83E-91596AE9536B
api_name:
- IPixelHistoryCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c43947148e2eb8139f3ad46157f19b1621a6c91e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341978"
---
# <a name="span-idvspixengineipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arrspanipixelhistorycallbackresultcallback-method"></a><span data-ttu-id="b111c-103"><span id="vspixengine.ipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arr"></span>Ipixelhistorycallback:: resultCallback-Methode</span><span class="sxs-lookup"><span data-stu-id="b111c-103"><span id="vspixengine.ipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback::ResultCallback method</span></span>

<span data-ttu-id="b111c-104">Ein Rückruf, der den Host über Ergebnisse der Pixel Verlaufs Anforderung benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="b111c-104">A callback that notifies the host of pixel history request results.</span></span>

## <a name="syntax"></a><span data-ttu-id="b111c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b111c-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD                    count,
   PixelHistoryOperation [] count0_pixelHistoryOperation
);
```

## <a name="parameters"></a><span data-ttu-id="b111c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b111c-106">Parameters</span></span>

<span data-ttu-id="b111c-107">*Countdown* </span><span class="sxs-lookup"><span data-stu-id="b111c-107">*count* </span></span>  
<span data-ttu-id="b111c-108">Die Anzahl der Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="b111c-108">The number of results.</span></span>

<span data-ttu-id="b111c-109">*count0 \_ pixelhistoryoperation* </span><span class="sxs-lookup"><span data-stu-id="b111c-109">*count0\_pixelHistoryOperation* </span></span>  
<span data-ttu-id="b111c-110">Die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="b111c-110">The results.</span></span>

## <a name="return-value"></a><span data-ttu-id="b111c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b111c-111">Return value</span></span>

<span data-ttu-id="b111c-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b111c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b111c-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b111c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b111c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b111c-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b111c-115">Header</span><span class="sxs-lookup"><span data-stu-id="b111c-115">Header</span></span></p></td><td><span data-ttu-id="b111c-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b111c-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b111c-117"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b111c-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b111c-118">**Ipixelhistorycallback**</span><span class="sxs-lookup"><span data-stu-id="b111c-118">**IPixelHistoryCallback**</span></span>](/windows/desktop/direct3dtools/ipixelhistorycallback)

 

 
