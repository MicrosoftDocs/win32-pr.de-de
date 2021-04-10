---
description: Eine asynchrone Anforderung zum Abrufen der RVAs (relative virtuelle Adressen) der aufrufsstapel des angegebenen Ereignisses.
MS-HAID: vspixengine.ICallStackRequest\_RequestAsync\_EventID\_ICallStackCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Icallstackrequest:: requestasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1951716F-5382-41EE-90BB-A9053DB38A78
api_name:
- ICallStackRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cad4007a8bc3d0e7b7c9cf1efc7218ce09813a5a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213923"
---
# <a name="span-idvspixengineicallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dwordspanicallstackrequestrequestasync-method"></a><span data-ttu-id="05665-103"><span id="vspixengine.icallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dword"></span>Icallstackrequest:: requestasync-Methode</span><span class="sxs-lookup"><span data-stu-id="05665-103"><span id="vspixengine.icallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dword"></span>ICallStackRequest::RequestAsync method</span></span>

<span data-ttu-id="05665-104">Eine asynchrone Anforderung zum Abrufen der RVAs (relative virtuelle Adressen) der aufrufsstapel des angegebenen Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="05665-104">An asynchronous request to get the call stack RVAs (relative virtual addresses) of the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="05665-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="05665-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID              eventID,
   ICallStackCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="05665-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="05665-106">Parameters</span></span>

<span data-ttu-id="05665-107">*EventID* </span><span class="sxs-lookup"><span data-stu-id="05665-107">*eventID* </span></span>  
<span data-ttu-id="05665-108">Das angegebene Ereignis.</span><span class="sxs-lookup"><span data-stu-id="05665-108">The specified event.</span></span>

<span data-ttu-id="05665-109">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="05665-109">*requestCallback* </span></span>  
<span data-ttu-id="05665-110">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="05665-110">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="05665-111">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="05665-111">*requestCookie* </span></span>  
<span data-ttu-id="05665-112">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="05665-112">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="05665-113">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="05665-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="05665-114">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="05665-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="05665-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05665-115">Return value</span></span>

<span data-ttu-id="05665-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="05665-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="05665-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="05665-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="05665-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05665-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="05665-119">Header</span><span class="sxs-lookup"><span data-stu-id="05665-119">Header</span></span></p></td><td><span data-ttu-id="05665-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="05665-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="05665-121"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05665-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="05665-122">**Icallstackrequest**</span><span class="sxs-lookup"><span data-stu-id="05665-122">**ICallStackRequest**</span></span>](/windows/desktop/direct3dtools/icallstackrequest)

 

 
