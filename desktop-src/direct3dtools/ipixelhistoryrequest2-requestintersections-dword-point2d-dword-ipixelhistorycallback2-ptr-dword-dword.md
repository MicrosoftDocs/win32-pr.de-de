---
description: Fordert eine Liste von Ereignissen an, die eine Änderung im angegebenen Pixel, Renderziel/UAV und Frame auslösen.
MS-HAID: vspixengine.IPixelHistoryRequest2\_RequestIntersections\_DWORD\_Point2D\_DWORD\_IPixelHistoryCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixelHistoryRequest2:: requestinterabschnitts-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8E47935-DFA1-4A76-9D0A-3DF5833A1249
api_name:
- IPixelHistoryRequest2.RequestIntersections
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 56f8da17ca492ca15ca51676ae4f1e1654c6f41f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521555"
---
# <a name="span-idvspixengineipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dwordspanipixelhistoryrequest2requestintersections-method"></a><span data-ttu-id="14ba6-103"><span id="vspixengine.ipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2:: requestinterabschnitts-Methode</span><span class="sxs-lookup"><span data-stu-id="14ba6-103"><span id="vspixengine.ipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2::RequestIntersections method</span></span>

<span data-ttu-id="14ba6-104">Fordert eine Liste von Ereignissen an, die eine Änderung im angegebenen Pixel, Renderziel/UAV und Frame auslösen.</span><span class="sxs-lookup"><span data-stu-id="14ba6-104">Requests a list of events that cause a change in the specified pixel, render target / UAV, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="14ba6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="14ba6-105">Syntax</span></span>


```C++
HRESULT RequestIntersections(
   DWORD                    frameNumber,
   Point2D                  pixel,
   DWORD                    renderTargetPtr,
   IPixelHistoryCallback2 * requestCallback,
   DWORD                    requestCookie,
   DWORD                    progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="14ba6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="14ba6-106">Parameters</span></span>

<span data-ttu-id="14ba6-107">*Framezahl* </span><span class="sxs-lookup"><span data-stu-id="14ba6-107">*frameNumber* </span></span>  
<span data-ttu-id="14ba6-108">Der angegebene Frame.</span><span class="sxs-lookup"><span data-stu-id="14ba6-108">The specified frame.</span></span>

<span data-ttu-id="14ba6-109">*Megapixel* </span><span class="sxs-lookup"><span data-stu-id="14ba6-109">*pixel* </span></span>  
<span data-ttu-id="14ba6-110">Das angegebene Pixel.</span><span class="sxs-lookup"><span data-stu-id="14ba6-110">The specified pixel.</span></span>

<span data-ttu-id="14ba6-111">*rendertargetptr* </span><span class="sxs-lookup"><span data-stu-id="14ba6-111">*renderTargetPtr* </span></span>  
<span data-ttu-id="14ba6-112">Die Adresse des angegebenen Renderziels.</span><span class="sxs-lookup"><span data-stu-id="14ba6-112">The address of the specified render target</span></span>

<span data-ttu-id="14ba6-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="14ba6-113">*requestCallback* </span></span>  
<span data-ttu-id="14ba6-114">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="14ba6-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="14ba6-115">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="14ba6-115">*requestCookie* </span></span>  
<span data-ttu-id="14ba6-116">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="14ba6-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="14ba6-117">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="14ba6-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="14ba6-118">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="14ba6-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="14ba6-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14ba6-119">Return value</span></span>

<span data-ttu-id="14ba6-120">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="14ba6-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="14ba6-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="14ba6-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="14ba6-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14ba6-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="14ba6-123">Header</span><span class="sxs-lookup"><span data-stu-id="14ba6-123">Header</span></span></p></td><td><span data-ttu-id="14ba6-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="14ba6-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="14ba6-125"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14ba6-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="14ba6-126">**IPixelHistoryRequest2**</span><span class="sxs-lookup"><span data-stu-id="14ba6-126">**IPixelHistoryRequest2**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest2)

 

 
