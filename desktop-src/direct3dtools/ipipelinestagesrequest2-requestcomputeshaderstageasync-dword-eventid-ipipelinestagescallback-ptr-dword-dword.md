---
description: Eine asynchrone Anforderung, um zu erhalten, ob die Compute-Shader-Phase für den angegebenen Frame und das angegebene Ereignis verwendet wurde.
MS-HAID: vspixengine.IPipeLineStagesRequest2\_RequestComputeShaderStageAsync\_DWORD\_EventID\_IPipeLineStagesCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesRequest2:: requestcomputeshaderstageasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: EC5695A6-70B5-4F7D-A235-974A0A59A44F
api_name:
- IPipeLineStagesRequest2.RequestComputeShaderStageAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ec7fe36a35e73ae2d047be11a2d5cf72f65825f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482022"
---
# <a name="span-idvspixengineipipelinestagesrequest2_requestcomputeshaderstageasync_dword_eventid_ipipelinestagescallback_ptr_dword_dwordspanipipelinestagesrequest2requestcomputeshaderstageasync-method"></a><span data-ttu-id="a35f1-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderstageasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>IPipeLineStagesRequest2:: requestcomputeshaderstageasync-Methode</span><span class="sxs-lookup"><span data-stu-id="a35f1-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderstageasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>IPipeLineStagesRequest2::RequestComputeShaderStageAsync method</span></span>

<span data-ttu-id="a35f1-104">Eine asynchrone Anforderung, um zu erhalten, ob die Compute-Shader-Phase für den angegebenen Frame und das angegebene Ereignis verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="a35f1-104">An asynchronous request to get whether the compute shader stage was used for the specified frame and event.</span></span>

## <a name="syntax"></a><span data-ttu-id="a35f1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a35f1-105">Syntax</span></span>


```C++
HRESULT RequestComputeShaderStageAsync(
   DWORD                     frameNumber,
   EventID                   eventID,
   IPipeLineStagesCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="a35f1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a35f1-106">Parameters</span></span>

<span data-ttu-id="a35f1-107">*Framezahl* </span><span class="sxs-lookup"><span data-stu-id="a35f1-107">*frameNumber* </span></span>  
<span data-ttu-id="a35f1-108">Der angegebene Frame.</span><span class="sxs-lookup"><span data-stu-id="a35f1-108">The specified frame.</span></span>

<span data-ttu-id="a35f1-109">*EventID* </span><span class="sxs-lookup"><span data-stu-id="a35f1-109">*eventID* </span></span>  
<span data-ttu-id="a35f1-110">Das angegebene Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a35f1-110">The specified event.</span></span>

<span data-ttu-id="a35f1-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="a35f1-111">*requestCallback* </span></span>  
<span data-ttu-id="a35f1-112">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a35f1-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="a35f1-113">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="a35f1-113">*requestCookie* </span></span>  
<span data-ttu-id="a35f1-114">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a35f1-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="a35f1-115">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="a35f1-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="a35f1-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a35f1-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="a35f1-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a35f1-117">Return value</span></span>

<span data-ttu-id="a35f1-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a35f1-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a35f1-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a35f1-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a35f1-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a35f1-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a35f1-121">Header</span><span class="sxs-lookup"><span data-stu-id="a35f1-121">Header</span></span></p></td><td><span data-ttu-id="a35f1-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a35f1-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a35f1-123"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a35f1-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a35f1-124">**IPipeLineStagesRequest2**</span><span class="sxs-lookup"><span data-stu-id="a35f1-124">**IPipeLineStagesRequest2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest2)

 

 
