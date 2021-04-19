---
description: Eine asynchrone Anforderung zum Abruf der Quelldateien, die mit dem Aufruf Stapel eines Ereignisses verknüpft sind.
MS-HAID: vspixengine.ISourceFileInfoRequest\_RequestAsync\_EventID\_ISourceFileInfoCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Isourcefilinput forequest:: requestasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 257361ED-7400-4320-8433-59A9A07E69E4
api_name:
- ISourceFileInfoRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ba5fddf153b2a771ab54bf89036f8087ad0f7524
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344930"
---
# <a name="span-idvspixengineisourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dwordspanisourcefileinforequestrequestasync-method"></a><span data-ttu-id="29832-103"><span id="vspixengine.isourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dword"></span>Isourcefilinput forequest:: requestasync-Methode</span><span class="sxs-lookup"><span data-stu-id="29832-103"><span id="vspixengine.isourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dword"></span>ISourceFileInfoRequest::RequestAsync method</span></span>

<span data-ttu-id="29832-104">Eine asynchrone Anforderung zum Abruf der Quelldateien, die mit dem Aufruf Stapel eines Ereignisses verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="29832-104">An asynchronous request to get the source files associated with the callstack of an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="29832-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="29832-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID                   eventID,
   ISourceFileInfoCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="29832-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="29832-106">Parameters</span></span>

<span data-ttu-id="29832-107">*EventID* </span><span class="sxs-lookup"><span data-stu-id="29832-107">*eventID* </span></span>  
<span data-ttu-id="29832-108">Das angegebene Ereignis.</span><span class="sxs-lookup"><span data-stu-id="29832-108">The specified event.</span></span>

<span data-ttu-id="29832-109">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="29832-109">*requestCallback* </span></span>  
<span data-ttu-id="29832-110">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="29832-110">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="29832-111">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="29832-111">*requestCookie* </span></span>  
<span data-ttu-id="29832-112">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="29832-112">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="29832-113">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="29832-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="29832-114">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="29832-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="29832-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29832-115">Return value</span></span>

<span data-ttu-id="29832-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="29832-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="29832-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="29832-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="29832-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29832-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="29832-119">Header</span><span class="sxs-lookup"><span data-stu-id="29832-119">Header</span></span></p></td><td><span data-ttu-id="29832-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="29832-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="29832-121"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29832-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="29832-122">**Isourcefileingeforequest**</span><span class="sxs-lookup"><span data-stu-id="29832-122">**ISourceFileInfoRequest**</span></span>](/windows/desktop/direct3dtools/isourcefileinforequest)

 

 
