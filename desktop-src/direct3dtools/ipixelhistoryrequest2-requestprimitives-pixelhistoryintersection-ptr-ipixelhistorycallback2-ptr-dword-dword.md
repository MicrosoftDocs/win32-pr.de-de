---
description: Fordert eine Liste von primitiven aus einer bestimmten Schnittmenge an. Weitere Informationen finden Sie unter der requestinterabschnitts-Member-Funktion.
MS-HAID: vspixengine.IPixelHistoryRequest2\_RequestPrimitives\_PixelHistoryIntersection\_ptr\_IPixelHistoryCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixelHistoryRequest2:: requestprimitives-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CFEB833C-1747-4153-A691-7529AA3F4095
api_name:
- IPixelHistoryRequest2.RequestPrimitives
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 71b248f86e20e560238a1c59b1a0199f285493a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344779"
---
# <a name="span-idvspixengineipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dwordspanipixelhistoryrequest2requestprimitives-method"></a><span data-ttu-id="50450-104"><span id="vspixengine.ipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2:: requestprimitives-Methode</span><span class="sxs-lookup"><span data-stu-id="50450-104"><span id="vspixengine.ipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2::RequestPrimitives method</span></span>

<span data-ttu-id="50450-105">Fordert eine Liste von primitiven aus einer bestimmten Schnittmenge an.</span><span class="sxs-lookup"><span data-stu-id="50450-105">Requests a list of primitives from a particular intersection.</span></span> <span data-ttu-id="50450-106">Weitere Informationen finden Sie unter der requestinterabschnitts-Member-Funktion.</span><span class="sxs-lookup"><span data-stu-id="50450-106">For more information, see the RequestIntersections member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="50450-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="50450-107">Syntax</span></span>


```C++
HRESULT RequestPrimitives(
   PixelHistoryIntersection * intersection,
   IPixelHistoryCallback2 *   requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="50450-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="50450-108">Parameters</span></span>

<span data-ttu-id="50450-109">*Kreuz* </span><span class="sxs-lookup"><span data-stu-id="50450-109">*intersection* </span></span>  
<span data-ttu-id="50450-110">Die Adresse der angegebenen Schnittmenge.</span><span class="sxs-lookup"><span data-stu-id="50450-110">The address of the specified intersection.</span></span>

<span data-ttu-id="50450-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="50450-111">*requestCallback* </span></span>  
<span data-ttu-id="50450-112">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="50450-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="50450-113">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="50450-113">*requestCookie* </span></span>  
<span data-ttu-id="50450-114">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="50450-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="50450-115">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="50450-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="50450-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="50450-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="50450-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50450-117">Return value</span></span>

<span data-ttu-id="50450-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="50450-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="50450-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="50450-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="50450-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50450-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="50450-121">Header</span><span class="sxs-lookup"><span data-stu-id="50450-121">Header</span></span></p></td><td><span data-ttu-id="50450-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="50450-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="50450-123"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50450-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="50450-124">**IPixelHistoryRequest2**</span><span class="sxs-lookup"><span data-stu-id="50450-124">**IPixelHistoryRequest2**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest2)

 

 
