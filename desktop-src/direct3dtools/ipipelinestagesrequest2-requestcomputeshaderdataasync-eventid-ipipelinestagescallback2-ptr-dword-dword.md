---
description: Eine asynchrone Anforderung zum Aufrufen von Compute-shaderdaten für die angegebene Verteilung.
MS-HAID: vspixengine.IPipeLineStagesRequest2\_RequestComputeShaderDataAsync\_EventID\_IPipeLineStagesCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesRequest2:: requestcomputeshaderdataasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F73EA7B4-9E20-4BFD-8F87-20CE0B6C96D8
api_name:
- IPipeLineStagesRequest2.RequestComputeShaderDataAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cf0d4725d8d2172900a96e58b4c8786ca2a9c851
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346205"
---
# <a name="span-idvspixengineipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dwordspanipipelinestagesrequest2requestcomputeshaderdataasync-method"></a><span data-ttu-id="844c2-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dword"></span>IPipeLineStagesRequest2:: requestcomputeshaderdataasync-Methode</span><span class="sxs-lookup"><span data-stu-id="844c2-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dword"></span>IPipeLineStagesRequest2::RequestComputeShaderDataAsync method</span></span>

<span data-ttu-id="844c2-104">Eine asynchrone Anforderung zum Aufrufen von Compute-shaderdaten für die angegebene Verteilung.</span><span class="sxs-lookup"><span data-stu-id="844c2-104">An asynchronous request to get compute shader data for the specified dispatch.</span></span>

## <a name="syntax"></a><span data-ttu-id="844c2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="844c2-105">Syntax</span></span>


```C++
HRESULT RequestComputeShaderDataAsync(
   EventID                    eventID,
   IPipeLineStagesCallback2 * requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="844c2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="844c2-106">Parameters</span></span>

<span data-ttu-id="844c2-107">*EventID* </span><span class="sxs-lookup"><span data-stu-id="844c2-107">*eventID* </span></span>  
<span data-ttu-id="844c2-108">Das angegebene Dispatch-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="844c2-108">The specified dispatch event.</span></span>

<span data-ttu-id="844c2-109">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="844c2-109">*requestCallback* </span></span>  
<span data-ttu-id="844c2-110">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="844c2-110">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="844c2-111">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="844c2-111">*requestCookie* </span></span>  
<span data-ttu-id="844c2-112">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="844c2-112">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="844c2-113">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="844c2-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="844c2-114">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="844c2-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="844c2-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="844c2-115">Return value</span></span>

<span data-ttu-id="844c2-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="844c2-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="844c2-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="844c2-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="844c2-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="844c2-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="844c2-119">Header</span><span class="sxs-lookup"><span data-stu-id="844c2-119">Header</span></span></p></td><td><span data-ttu-id="844c2-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="844c2-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="844c2-121"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="844c2-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="844c2-122">**IPipeLineStagesRequest2**</span><span class="sxs-lookup"><span data-stu-id="844c2-122">**IPipeLineStagesRequest2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest2)

 

 
