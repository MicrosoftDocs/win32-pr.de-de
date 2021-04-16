---
description: Ein Rückruf, der den Host über eine abgebrochene Anforderung benachrichtigt, indem er ein Cookie verwendet, das die Anforderung eindeutig identifiziert.
MS-HAID: vspixengine.INewFramesCallback\_CancelUsingCookie\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Inewframescallback:: cancelusingcookie-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36176554-BB4F-40CB-AB7B-4957DA84BAA8
api_name:
- INewFramesCallback.CancelUsingCookie
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dfbbbda1a11244088dccad640be348da1e4d8313
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481283"
---
# <a name="span-idvspixengineinewframescallback_cancelusingcookie_dwordspaninewframescallbackcancelusingcookie-method"></a><span data-ttu-id="c05f0-103"><span id="vspixengine.inewframescallback_cancelusingcookie_dword"></span>Inewframescallback:: cancelusingcookie-Methode</span><span class="sxs-lookup"><span data-stu-id="c05f0-103"><span id="vspixengine.inewframescallback_cancelusingcookie_dword"></span>INewFramesCallback::CancelUsingCookie method</span></span>

<span data-ttu-id="c05f0-104">Ein Rückruf, der den Host über eine abgebrochene Anforderung benachrichtigt, indem er ein Cookie verwendet, das die Anforderung eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c05f0-104">A callback that notifies the host of a canceled request by using a cookie that uniquely identifies the request.</span></span>

## <a name="syntax"></a><span data-ttu-id="c05f0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c05f0-105">Syntax</span></span>


```C++
HRESULT CancelUsingCallback(
   IUnknown * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="c05f0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c05f0-106">Parameters</span></span>

<span data-ttu-id="c05f0-107">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="c05f0-107">*requestCookie* </span></span>  
<span data-ttu-id="c05f0-108">Das Cookie, das die abgebrochene Anforderung eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c05f0-108">The cookie which uniquely idenfies the cancelled request.</span></span>

## <a name="return-value"></a><span data-ttu-id="c05f0-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c05f0-109">Return value</span></span>

<span data-ttu-id="c05f0-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c05f0-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c05f0-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c05f0-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c05f0-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c05f0-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c05f0-113">Header</span><span class="sxs-lookup"><span data-stu-id="c05f0-113">Header</span></span></p></td><td><span data-ttu-id="c05f0-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c05f0-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c05f0-115"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c05f0-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c05f0-116">**Inewframescallback**</span><span class="sxs-lookup"><span data-stu-id="c05f0-116">**INewFramesCallback**</span></span>](/windows/desktop/direct3dtools/inewframescallback)

 

 
