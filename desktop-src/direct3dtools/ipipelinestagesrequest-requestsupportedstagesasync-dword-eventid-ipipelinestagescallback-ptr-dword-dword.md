---
description: Eine asynchrone Anforderung zum erhalten einer Liste von Stufen, die für den angegebenen Frame und das angegebene Ereignis verwendet werden.
MS-HAID: vspixengine.IPipeLineStagesRequest\_RequestSupportedStagesAsync\_DWORD\_EventID\_IPipeLineStagesCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ipipelinestagesrequest:: requestsupportedstagesasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C636FC40-0505-486B-B25D-9B424F5A584D
api_name:
- IPipeLineStagesRequest.RequestSupportedStagesAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0c3ebedee8dba4d7630d1bdff60bdaf479ea3561
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345417"
---
# <a name="span-idvspixengineipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dwordspanipipelinestagesrequestrequestsupportedstagesasync-method"></a><span data-ttu-id="288e1-103"><span id="vspixengine.ipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>Ipipelinestagesrequest:: requestsupportedstagesasync-Methode</span><span class="sxs-lookup"><span data-stu-id="288e1-103"><span id="vspixengine.ipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>IPipeLineStagesRequest::RequestSupportedStagesAsync method</span></span>

<span data-ttu-id="288e1-104">Eine asynchrone Anforderung zum erhalten einer Liste von Stufen, die für den angegebenen Frame und das angegebene Ereignis verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="288e1-104">An asynchronous request to get a list of stages used for the specified frame and event.</span></span>

## <a name="syntax"></a><span data-ttu-id="288e1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="288e1-105">Syntax</span></span>


```C++
HRESULT RequestSupportedStagesAsync(
   DWORD                     frameNumber,
   EventID                   eventID,
   IPipeLineStagesCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="288e1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="288e1-106">Parameters</span></span>

<span data-ttu-id="288e1-107">*Framezahl* </span><span class="sxs-lookup"><span data-stu-id="288e1-107">*frameNumber* </span></span>  
<span data-ttu-id="288e1-108">Der angegebene Frame.</span><span class="sxs-lookup"><span data-stu-id="288e1-108">The specified frame.</span></span>

<span data-ttu-id="288e1-109">*EventID* </span><span class="sxs-lookup"><span data-stu-id="288e1-109">*eventID* </span></span>  
<span data-ttu-id="288e1-110">Das angegebene Ereignis.</span><span class="sxs-lookup"><span data-stu-id="288e1-110">The specified event.</span></span>

<span data-ttu-id="288e1-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="288e1-111">*requestCallback* </span></span>  
<span data-ttu-id="288e1-112">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="288e1-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="288e1-113">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="288e1-113">*requestCookie* </span></span>  
<span data-ttu-id="288e1-114">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="288e1-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="288e1-115">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="288e1-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="288e1-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="288e1-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="288e1-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="288e1-117">Return value</span></span>

<span data-ttu-id="288e1-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="288e1-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="288e1-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="288e1-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="288e1-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="288e1-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="288e1-121">Header</span><span class="sxs-lookup"><span data-stu-id="288e1-121">Header</span></span></p></td><td><span data-ttu-id="288e1-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="288e1-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="288e1-123"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="288e1-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="288e1-124">**Ipipelinestagesrequest**</span><span class="sxs-lookup"><span data-stu-id="288e1-124">**IPipeLineStagesRequest**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest)

 

 
