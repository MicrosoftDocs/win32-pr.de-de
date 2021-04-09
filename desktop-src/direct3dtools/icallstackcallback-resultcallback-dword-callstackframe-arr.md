---
description: Eine Rückruffunktion, die verwendet wird, um den Host über die aufrufstackinformationen zu Benachrichtigen
MS-HAID: vspixengine.ICallStackCallback\_ResultCallback\_DWORD\_CallStackFrame\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Icallstackcallback:: resultCallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9C083298-6FD5-4414-8E0C-625F6A144668
api_name:
- ICallStackCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4bd77ea22fd31b31081d72707b1fd7a2efbda607
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860307"
---
# <a name="span-idvspixengineicallstackcallback_resultcallback_dword_callstackframe_arrspanicallstackcallbackresultcallback-method"></a><span data-ttu-id="784f5-103"><span id="vspixengine.icallstackcallback_resultcallback_dword_callstackframe_arr"></span>Icallstackcallback:: resultCallback-Methode</span><span class="sxs-lookup"><span data-stu-id="784f5-103"><span id="vspixengine.icallstackcallback_resultcallback_dword_callstackframe_arr"></span>ICallStackCallback::ResultCallback method</span></span>

<span data-ttu-id="784f5-104">Eine Rückruffunktion, die verwendet wird, um den Host über die aufrufstackinformationen zu Benachrichtigen</span><span class="sxs-lookup"><span data-stu-id="784f5-104">A callback function used to notify the host of call stack information.</span></span>

## <a name="syntax"></a><span data-ttu-id="784f5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="784f5-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD             count,
   CallStackFrame [] count0_callStackFrameBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="784f5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="784f5-106">Parameters</span></span>

<span data-ttu-id="784f5-107">*Countdown* </span><span class="sxs-lookup"><span data-stu-id="784f5-107">*count* </span></span>  
<span data-ttu-id="784f5-108">Die Anzahl der zurückgegebenen Aufruf Liste-Framebuffers.</span><span class="sxs-lookup"><span data-stu-id="784f5-108">The number of callstack framebuffers returned.</span></span>

<span data-ttu-id="784f5-109">*count0 \_ callstackframebuffer* </span><span class="sxs-lookup"><span data-stu-id="784f5-109">*count0\_callStackFrameBuffer* </span></span>  
<span data-ttu-id="784f5-110">Die Aufruf Liste-Informationen.</span><span class="sxs-lookup"><span data-stu-id="784f5-110">The callstack information.</span></span>

## <a name="return-value"></a><span data-ttu-id="784f5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="784f5-111">Return value</span></span>

<span data-ttu-id="784f5-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="784f5-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="784f5-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="784f5-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="784f5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="784f5-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="784f5-115">Header</span><span class="sxs-lookup"><span data-stu-id="784f5-115">Header</span></span></p></td><td><span data-ttu-id="784f5-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="784f5-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="784f5-117"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="784f5-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="784f5-118">**Icallstackcallback**</span><span class="sxs-lookup"><span data-stu-id="784f5-118">**ICallStackCallback**</span></span>](/windows/desktop/direct3dtools/icallstackcallback)

 

 
