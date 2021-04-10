---
description: Eine asynchrone Anforderung, eine Aktion (z. b. einen Frame erfassen) in der Engine zu initiieren.
MS-HAID: vspixengine.IRunActionRequest\_RequestAsync\_REFGUID\_IUnknown\_ptr\_IRunActionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ununaktionrequest:: requestasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4A4DF4BE-383D-4B36-9195-61720C3B4D97
api_name:
- IRunActionRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 179abf44231d122ca82527fc5739b876395c327b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125360"
---
# <a name="span-idvspixengineirunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dwordspanirunactionrequestrequestasync-method"></a><span data-ttu-id="e73c7-103"><span id="vspixengine.irunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dword"></span>Ununaktionrequest:: requestasync-Methode</span><span class="sxs-lookup"><span data-stu-id="e73c7-103"><span id="vspixengine.irunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dword"></span>IRunActionRequest::RequestAsync method</span></span>

<span data-ttu-id="e73c7-104">Eine asynchrone Anforderung, eine Aktion (z. b. einen Frame erfassen) in der Engine zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="e73c7-104">An asynchronous request to initiate an action (for example, capture a frame) in the engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="e73c7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e73c7-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   REFGUID              action,
   IUnknown *           actionPayload,
   IRunActionCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="e73c7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e73c7-106">Parameters</span></span>

<span data-ttu-id="e73c7-107">*Hinspiel* </span><span class="sxs-lookup"><span data-stu-id="e73c7-107">*action* </span></span>  
<span data-ttu-id="e73c7-108">Die angegebene Aktion.</span><span class="sxs-lookup"><span data-stu-id="e73c7-108">The specified action.</span></span>

<span data-ttu-id="e73c7-109">*Aktions Nutzlast* </span><span class="sxs-lookup"><span data-stu-id="e73c7-109">*actionPayload* </span></span>  
<span data-ttu-id="e73c7-110">Die Nutzlast der angegebenen Aktion.</span><span class="sxs-lookup"><span data-stu-id="e73c7-110">The payload of the specified action.</span></span>

<span data-ttu-id="e73c7-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="e73c7-111">*requestCallback* </span></span>  
<span data-ttu-id="e73c7-112">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e73c7-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="e73c7-113">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="e73c7-113">*requestCookie* </span></span>  
<span data-ttu-id="e73c7-114">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e73c7-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="e73c7-115">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="e73c7-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="e73c7-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e73c7-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="e73c7-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e73c7-117">Return value</span></span>

<span data-ttu-id="e73c7-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="e73c7-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e73c7-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e73c7-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e73c7-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e73c7-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e73c7-121">Header</span><span class="sxs-lookup"><span data-stu-id="e73c7-121">Header</span></span></p></td><td><span data-ttu-id="e73c7-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e73c7-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e73c7-123"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e73c7-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e73c7-124">**Nicht aktionrequest**</span><span class="sxs-lookup"><span data-stu-id="e73c7-124">**IRunActionRequest**</span></span>](/windows/desktop/direct3dtools/irunactionrequest)

 

 
