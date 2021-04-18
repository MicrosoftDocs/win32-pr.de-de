---
description: Fordert eine Liste der Pixel Verlaufs Ergebnisse im angegebenen Pixel, Rendern von Ziel-/UAV und Frame an.
MS-HAID: vspixengine.IPixelHistoryRequest\_RequestAsync\_DWORD\_Point2D\_DWORD\_IPixelHistoryCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ipixelhistoryrequest:: requestasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 00A90033-FC57-4BEE-B950-82E678437F2A
api_name:
- IPixelHistoryRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f0209730e0e388b67281451a0337928257c1bae7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522728"
---
# <a name="span-idvspixengineipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dwordspanipixelhistoryrequestrequestasync-method"></a><span data-ttu-id="51022-103"><span id="vspixengine.ipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dword"></span>Ipixelhistoryrequest:: requestasync-Methode</span><span class="sxs-lookup"><span data-stu-id="51022-103"><span id="vspixengine.ipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dword"></span>IPixelHistoryRequest::RequestAsync method</span></span>

<span data-ttu-id="51022-104">Fordert eine Liste der Pixel Verlaufs Ergebnisse im angegebenen Pixel, Rendern von Ziel-/UAV und Frame an.</span><span class="sxs-lookup"><span data-stu-id="51022-104">Requests a list of pixel history results in the specified pixel, render tartget /UAV, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="51022-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="51022-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                   frameNumber,
   Point2D                 pixel,
   DWORD                   renderTargetPtr,
   IPixelHistoryCallback * requestCallback,
   DWORD                   requestCookie,
   DWORD                   progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="51022-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="51022-106">Parameters</span></span>

<span data-ttu-id="51022-107">*Framezahl* </span><span class="sxs-lookup"><span data-stu-id="51022-107">*frameNumber* </span></span>  
<span data-ttu-id="51022-108">Der angegebene Frame.</span><span class="sxs-lookup"><span data-stu-id="51022-108">The specified frame.</span></span>

<span data-ttu-id="51022-109">*Megapixel* </span><span class="sxs-lookup"><span data-stu-id="51022-109">*pixel* </span></span>  
<span data-ttu-id="51022-110">Das angegebene Pixel.</span><span class="sxs-lookup"><span data-stu-id="51022-110">The specified pixel.</span></span>

<span data-ttu-id="51022-111">*rendertargetptr* </span><span class="sxs-lookup"><span data-stu-id="51022-111">*renderTargetPtr* </span></span>  
<span data-ttu-id="51022-112">Das angegebene Renderziel.</span><span class="sxs-lookup"><span data-stu-id="51022-112">The specified render target.</span></span>

<span data-ttu-id="51022-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="51022-113">*requestCallback* </span></span>  
<span data-ttu-id="51022-114">Die Adresse eines Rückrufs, der zum Benachrichtigen des Host der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51022-114">The address of a callback used to notifify the host of results.</span></span>

<span data-ttu-id="51022-115">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="51022-115">*requestCookie* </span></span>  
<span data-ttu-id="51022-116">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="51022-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="51022-117">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="51022-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="51022-118">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51022-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="51022-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51022-119">Return value</span></span>

<span data-ttu-id="51022-120">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="51022-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="51022-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="51022-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="51022-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51022-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="51022-123">Header</span><span class="sxs-lookup"><span data-stu-id="51022-123">Header</span></span></p></td><td><span data-ttu-id="51022-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="51022-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="51022-125"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51022-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="51022-126">**Ipixelhistoryrequest**</span><span class="sxs-lookup"><span data-stu-id="51022-126">**IPixelHistoryRequest**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest)

 

 
