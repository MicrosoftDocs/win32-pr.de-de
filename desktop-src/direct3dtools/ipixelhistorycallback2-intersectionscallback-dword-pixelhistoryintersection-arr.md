---
description: Ein Rückruf, der den Host über Schnittstellen Informationen des Pixel Verlaufs benachrichtigt, die von der assocaas-Anforderung zurückgegeben werden.
MS-HAID: vspixengine.IPixelHistoryCallback2\_IntersectionsCallback\_DWORD\_PixelHistoryIntersection\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixelHistoryCallback2:: intersectionscallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 478B2495-93E4-4BB1-BC86-802D2AFAF97D
api_name:
- IPixelHistoryCallback2.IntersectionsCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 30bde17a2c504b2afdaf9c13a7b6d7014590b1dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124345"
---
# <a name="span-idvspixengineipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arrspanipixelhistorycallback2intersectionscallback-method"></a><span data-ttu-id="0e809-103"><span id="vspixengine.ipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arr"></span>IPixelHistoryCallback2:: intersectionscallback-Methode</span><span class="sxs-lookup"><span data-stu-id="0e809-103"><span id="vspixengine.ipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arr"></span>IPixelHistoryCallback2::IntersectionsCallback method</span></span>

<span data-ttu-id="0e809-104">Ein Rückruf, der den Host über Schnittstellen Informationen des Pixel Verlaufs benachrichtigt, die von der assocaas-Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0e809-104">A callback that notifies the host of pixel history intersection information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e809-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e809-105">Syntax</span></span>


```C++
HRESULT IntersectionsCallback(
   DWORD                       count,
   PixelHistoryIntersection [] count0_intersections
);
```

## <a name="parameters"></a><span data-ttu-id="0e809-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e809-106">Parameters</span></span>

<span data-ttu-id="0e809-107">*Countdown* </span><span class="sxs-lookup"><span data-stu-id="0e809-107">*count* </span></span>  
<span data-ttu-id="0e809-108">Die Anzahl der Pixel Verlaufs-Schnittpunkte.</span><span class="sxs-lookup"><span data-stu-id="0e809-108">The number of pixel history intersections.</span></span>

<span data-ttu-id="0e809-109">*count0- \_ Schnittpunkte* </span><span class="sxs-lookup"><span data-stu-id="0e809-109">*count0\_intersections* </span></span>  
<span data-ttu-id="0e809-110">Die Pixel Verlaufs-Schnittpunkte.</span><span class="sxs-lookup"><span data-stu-id="0e809-110">The pixel history intersections.</span></span>

## <a name="return-value"></a><span data-ttu-id="0e809-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e809-111">Return value</span></span>

<span data-ttu-id="0e809-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="0e809-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0e809-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0e809-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e809-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e809-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0e809-115">Header</span><span class="sxs-lookup"><span data-stu-id="0e809-115">Header</span></span></p></td><td><span data-ttu-id="0e809-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0e809-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="0e809-117"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e809-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="0e809-118">**IPixelHistoryCallback2**</span><span class="sxs-lookup"><span data-stu-id="0e809-118">**IPixelHistoryCallback2**</span></span>](/windows/desktop/direct3dtools/ipixelhistorycallback2)

 

 
