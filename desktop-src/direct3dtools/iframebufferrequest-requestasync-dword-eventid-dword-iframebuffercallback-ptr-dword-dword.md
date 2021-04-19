---
description: Fordert die Frame Puffer-Ausgabe des angegebenen Renderziels, Ereignisses und Rahmens an.
MS-HAID: vspixengine.IFrameBufferRequest\_RequestAsync\_DWORD\_EventID\_DWORD\_IFrameBufferCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iframebufferrequest:: requestasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 93E9BDFE-3913-4242-A973-7C113B6663FB
api_name:
- IFrameBufferRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 35c50b78486f25051e14ce2811382875e1fab240
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346604"
---
# <a name="span-idvspixengineiframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dwordspaniframebufferrequestrequestasync-method"></a><span data-ttu-id="ce64b-103"><span id="vspixengine.iframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dword"></span>Iframebufferrequest:: requestasync-Methode</span><span class="sxs-lookup"><span data-stu-id="ce64b-103"><span id="vspixengine.iframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dword"></span>IFrameBufferRequest::RequestAsync method</span></span>

<span data-ttu-id="ce64b-104">Fordert die Frame Puffer-Ausgabe des angegebenen Renderziels, Ereignisses und Rahmens an.</span><span class="sxs-lookup"><span data-stu-id="ce64b-104">Requests framebuffer output of the specified render target, event, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce64b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce64b-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  frameNumber,
   EventID                eventID,
   DWORD                  renderTargetIndex,
   IFrameBufferCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="ce64b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce64b-106">Parameters</span></span>

<span data-ttu-id="ce64b-107">*Framezahl* </span><span class="sxs-lookup"><span data-stu-id="ce64b-107">*frameNumber* </span></span>  
<span data-ttu-id="ce64b-108">Der angegebene Frame.</span><span class="sxs-lookup"><span data-stu-id="ce64b-108">The specified frame.</span></span>

<span data-ttu-id="ce64b-109">*EventID* </span><span class="sxs-lookup"><span data-stu-id="ce64b-109">*eventID* </span></span>  
<span data-ttu-id="ce64b-110">Das angegebene Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ce64b-110">The specified event.</span></span>

<span data-ttu-id="ce64b-111">*rendertargetindex* </span><span class="sxs-lookup"><span data-stu-id="ce64b-111">*renderTargetIndex* </span></span>  
<span data-ttu-id="ce64b-112">Der Index des angegebenen Renderziels.</span><span class="sxs-lookup"><span data-stu-id="ce64b-112">The index of the specified render target.</span></span>

<span data-ttu-id="ce64b-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="ce64b-113">*requestCallback* </span></span>  
<span data-ttu-id="ce64b-114">Die Adresse eines Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ce64b-114">The address of a callback used to notify the host of results.</span></span>

<span data-ttu-id="ce64b-115">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="ce64b-115">*requestCookie* </span></span>  
<span data-ttu-id="ce64b-116">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce64b-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="ce64b-117">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="ce64b-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="ce64b-118">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce64b-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="ce64b-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce64b-119">Return value</span></span>

<span data-ttu-id="ce64b-120">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ce64b-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ce64b-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ce64b-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce64b-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce64b-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ce64b-123">Header</span><span class="sxs-lookup"><span data-stu-id="ce64b-123">Header</span></span></p></td><td><span data-ttu-id="ce64b-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ce64b-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ce64b-125"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce64b-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ce64b-126">**Iframebufferrequest**</span><span class="sxs-lookup"><span data-stu-id="ce64b-126">**IFrameBufferRequest**</span></span>](/windows/desktop/direct3dtools/iframebufferrequest)

 

 
