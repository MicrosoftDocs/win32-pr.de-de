---
description: Eine asynchrone Anforderung zum erhalten der im Grafik Protokoll erfassten Listen Frames.
MS-HAID: vspixengine.IFrameListRequest\_RequestAsync\_IFrameListCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iframelistrequest:: requestasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 309C28F2-CE01-49E7-9A21-5053E3ED7721
api_name:
- IFrameListRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3627fc5ef3a425ae7607009b4ad382080ea99192
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041161"
---
# <a name="span-idvspixengineiframelistrequest_requestasync_iframelistcallback_ptr_dword_dwordspaniframelistrequestrequestasync-method"></a><span data-ttu-id="4a492-103"><span id="vspixengine.iframelistrequest_requestasync_iframelistcallback_ptr_dword_dword"></span>Iframelistrequest:: requestasync-Methode</span><span class="sxs-lookup"><span data-stu-id="4a492-103"><span id="vspixengine.iframelistrequest_requestasync_iframelistcallback_ptr_dword_dword"></span>IFrameListRequest::RequestAsync method</span></span>

<span data-ttu-id="4a492-104">Eine asynchrone Anforderung zum erhalten der im Grafik Protokoll erfassten Listen Frames.</span><span class="sxs-lookup"><span data-stu-id="4a492-104">An asynchronous request to get the list frames captured in the graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a492-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a492-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   IFrameListCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="4a492-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a492-106">Parameters</span></span>

<span data-ttu-id="4a492-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="4a492-107">*requestCallback* </span></span>  
<span data-ttu-id="4a492-108">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4a492-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="4a492-109">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="4a492-109">*requestCookie* </span></span>  
<span data-ttu-id="4a492-110">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a492-110">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="4a492-111">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="4a492-111">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="4a492-112">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a492-112">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="4a492-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a492-113">Return value</span></span>

<span data-ttu-id="4a492-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="4a492-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4a492-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4a492-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a492-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a492-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4a492-117">Header</span><span class="sxs-lookup"><span data-stu-id="4a492-117">Header</span></span></p></td><td><span data-ttu-id="4a492-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="4a492-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="4a492-119"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a492-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="4a492-120">**Iframelistrequest**</span><span class="sxs-lookup"><span data-stu-id="4a492-120">**IFrameListRequest**</span></span>](/windows/desktop/direct3dtools/iframelistrequest)

 

 
