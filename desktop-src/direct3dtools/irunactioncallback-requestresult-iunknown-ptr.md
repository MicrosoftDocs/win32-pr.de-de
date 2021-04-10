---
description: Eine Rückruffunktion, die verwendet wird, um den Host über Ergebnisse einer Aktion zu benachrichtigen (z. b. einen Frame erfassen), die er angefordert hat.
MS-HAID: vspixengine.IRunActionCallback\_RequestResult\_IUnknown\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ununaktioncallback:: RequestResult-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5D6B1599-2CF4-46E7-92DB-5D93DD5AD0EE
api_name:
- IRunActionCallback.RequestResult
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8f2d5eea98b167af30bfe0412acb10f83f83d3db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125365"
---
# <a name="span-idvspixengineirunactioncallback_requestresult_iunknown_ptrspanirunactioncallbackrequestresult-method"></a><span data-ttu-id="eabcc-103"><span id="vspixengine.irunactioncallback_requestresult_iunknown_ptr"></span>Ununaktioncallback:: RequestResult-Methode</span><span class="sxs-lookup"><span data-stu-id="eabcc-103"><span id="vspixengine.irunactioncallback_requestresult_iunknown_ptr"></span>IRunActionCallback::RequestResult method</span></span>

<span data-ttu-id="eabcc-104">Eine Rückruffunktion, die verwendet wird, um den Host über Ergebnisse einer Aktion zu benachrichtigen (z. b. einen Frame erfassen), die er angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="eabcc-104">A callback function used to notify the host of results from an action (for example, capture a frame) that it requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="eabcc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eabcc-105">Syntax</span></span>


```C++
HRESULT RequestResult(
   IUnknown * actionResult
);
```

## <a name="parameters"></a><span data-ttu-id="eabcc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eabcc-106">Parameters</span></span>

<span data-ttu-id="eabcc-107">*actionResult* </span><span class="sxs-lookup"><span data-stu-id="eabcc-107">*actionResult* </span></span>  
<span data-ttu-id="eabcc-108">Das Ergebnis der Aktion.</span><span class="sxs-lookup"><span data-stu-id="eabcc-108">The result of the action.</span></span>

## <a name="return-value"></a><span data-ttu-id="eabcc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eabcc-109">Return value</span></span>

<span data-ttu-id="eabcc-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="eabcc-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eabcc-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eabcc-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="eabcc-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eabcc-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="eabcc-113">Header</span><span class="sxs-lookup"><span data-stu-id="eabcc-113">Header</span></span></p></td><td><span data-ttu-id="eabcc-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="eabcc-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="eabcc-115"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eabcc-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="eabcc-116">**Nicht aktionrückruf**</span><span class="sxs-lookup"><span data-stu-id="eabcc-116">**IRunActionCallback**</span></span>](/windows/desktop/direct3dtools/irunactioncallback)

 

 
