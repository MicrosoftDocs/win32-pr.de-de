---
description: Eine asynchrone Anforderung, um Informationen darüber zu erhalten, welche Spalten (Felder) dieser Frame Ereignis Anforderungstyp unterstützt.
MS-HAID: vspixengine.IFrameEventsRequest\_RequestSupportedColumnsAsync\_IFrameEventsCallback\_ptr\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iframeeventsrequest:: requestsupportedcolumnsasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8F8ED8F7-F764-4CC8-891B-F0582F6B1337
api_name:
- IFrameEventsRequest.RequestSupportedColumnsAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 13d4c797e338f6b0901781760a39511a1f136174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746729"
---
# <a name="span-idvspixengineiframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dwordspaniframeeventsrequestrequestsupportedcolumnsasync-method"></a><span data-ttu-id="2b375-103"><span id="vspixengine.iframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dword"></span>Iframeeventsrequest:: requestsupportedcolumnsasync-Methode</span><span class="sxs-lookup"><span data-stu-id="2b375-103"><span id="vspixengine.iframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dword"></span>IFrameEventsRequest::RequestSupportedColumnsAsync method</span></span>

<span data-ttu-id="2b375-104">Eine asynchrone Anforderung, um Informationen darüber zu erhalten, welche Spalten (Felder) dieser Frame Ereignis Anforderungstyp unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2b375-104">An asynchronous request to get information about what columns (fields) this frame events request type supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b375-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b375-105">Syntax</span></span>


```C++
HRESULT RequestSupportedColumnsAsync(
   IFrameEventsCallback * requestCallback,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="2b375-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b375-106">Parameters</span></span>

<span data-ttu-id="2b375-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="2b375-107">*requestCallback* </span></span>  
<span data-ttu-id="2b375-108">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2b375-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="2b375-109">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="2b375-109">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="2b375-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b375-110">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b375-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b375-111">Return value</span></span>

<span data-ttu-id="2b375-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2b375-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2b375-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2b375-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b375-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b375-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="2b375-115">Header</span><span class="sxs-lookup"><span data-stu-id="2b375-115">Header</span></span></p></td><td><span data-ttu-id="2b375-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="2b375-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="2b375-117"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b375-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="2b375-118">**Iframeeventsrequest**</span><span class="sxs-lookup"><span data-stu-id="2b375-118">**IFrameEventsRequest**</span></span>](/windows/desktop/direct3dtools/iframeeventsrequest)

 

 
