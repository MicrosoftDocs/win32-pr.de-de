---
description: Eine asynchrone Anforderung zum erhalten der angegebenen Informationen zu einem einzelnen angegebenen Frame.
MS-HAID: vspixengine.IFrameEventsRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IFrameEventsCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iframeeventsrequest:: requestasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 821E7674-A960-46F6-A7AF-386298902ED6
api_name:
- IFrameEventsRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a001f6a29d17806271ca4f5d29dc80d6e36251bf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123992"
---
# <a name="span-idvspixengineiframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dwordspaniframeeventsrequestrequestasync-method"></a><span data-ttu-id="40516-103"><span id="vspixengine.iframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>Iframeeventsrequest:: requestasync-Methode</span><span class="sxs-lookup"><span data-stu-id="40516-103"><span id="vspixengine.iframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>IFrameEventsRequest::RequestAsync method</span></span>

<span data-ttu-id="40516-104">Eine asynchrone Anforderung zum erhalten der angegebenen Informationen zu einem einzelnen angegebenen Frame.</span><span class="sxs-lookup"><span data-stu-id="40516-104">An asynchronous request to get specified information about a single specified frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="40516-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="40516-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  frameNumber,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IFrameEventsCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="40516-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="40516-106">Parameters</span></span>

<span data-ttu-id="40516-107">*Framezahl* </span><span class="sxs-lookup"><span data-stu-id="40516-107">*frameNumber* </span></span>  
<span data-ttu-id="40516-108">Der angegebene Frame.</span><span class="sxs-lookup"><span data-stu-id="40516-108">The specified frame.</span></span>

<span data-ttu-id="40516-109">*NumColumns* </span><span class="sxs-lookup"><span data-stu-id="40516-109">*numColumns* </span></span>  
<span data-ttu-id="40516-110">Die angegebenen Spalten (Felder).</span><span class="sxs-lookup"><span data-stu-id="40516-110">The specified columns (fields).</span></span>

<span data-ttu-id="40516-111">*count1- \_ Spalten* </span><span class="sxs-lookup"><span data-stu-id="40516-111">*count1\_columns* </span></span>  
<span data-ttu-id="40516-112">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="40516-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="40516-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="40516-113">*requestCallback* </span></span>  
<span data-ttu-id="40516-114">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="40516-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="40516-115">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="40516-115">*requestCookie* </span></span>  
<span data-ttu-id="40516-116">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="40516-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="40516-117">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="40516-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="40516-118">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="40516-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="40516-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40516-119">Return value</span></span>

<span data-ttu-id="40516-120">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="40516-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="40516-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="40516-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="40516-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40516-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="40516-123">Header</span><span class="sxs-lookup"><span data-stu-id="40516-123">Header</span></span></p></td><td><span data-ttu-id="40516-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="40516-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="40516-125"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40516-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="40516-126">**Iframeeventsrequest**</span><span class="sxs-lookup"><span data-stu-id="40516-126">**IFrameEventsRequest**</span></span>](/windows/desktop/direct3dtools/iframeeventsrequest)

 

 
