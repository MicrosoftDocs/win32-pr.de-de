---
description: Nicht verwendet.
MS-HAID: vspixengine.ISingleEventRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IFrameEventsCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Isingleeventrequest:: requestasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C85CAF18-6953-4C5D-9491-5F5A5F28C580
api_name:
- ISingleEventRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6e6c78a7402082e4ca5222038bd3f5bd63c3cf7b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521520"
---
# <a name="span-idvspixengineisingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dwordspanisingleeventrequestrequestasync-method"></a><span data-ttu-id="c5ac2-103"><span id="vspixengine.isingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>Isingleeventrequest:: requestasync-Methode</span><span class="sxs-lookup"><span data-stu-id="c5ac2-103"><span id="vspixengine.isingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>ISingleEventRequest::RequestAsync method</span></span>

<span data-ttu-id="c5ac2-104">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5ac2-104">Not used.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ac2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5ac2-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  eventId,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IFrameEventsCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="c5ac2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5ac2-106">Parameters</span></span>

<span data-ttu-id="c5ac2-107">*EventID* </span><span class="sxs-lookup"><span data-stu-id="c5ac2-107">*eventId* </span></span>  
<span data-ttu-id="c5ac2-108">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5ac2-108">Not used.</span></span>

<span data-ttu-id="c5ac2-109">*NumColumns* </span><span class="sxs-lookup"><span data-stu-id="c5ac2-109">*numColumns* </span></span>  
<span data-ttu-id="c5ac2-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5ac2-110">Not used.</span></span>

<span data-ttu-id="c5ac2-111">*count1- \_ Spalten* </span><span class="sxs-lookup"><span data-stu-id="c5ac2-111">*count1\_columns* </span></span>  
<span data-ttu-id="c5ac2-112">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5ac2-112">Not used.</span></span>

<span data-ttu-id="c5ac2-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="c5ac2-113">*requestCallback* </span></span>  
<span data-ttu-id="c5ac2-114">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5ac2-114">Not used.</span></span>

<span data-ttu-id="c5ac2-115">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="c5ac2-115">*requestCookie* </span></span>  
<span data-ttu-id="c5ac2-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5ac2-116">Not used.</span></span>

<span data-ttu-id="c5ac2-117">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="c5ac2-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="c5ac2-118">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5ac2-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="c5ac2-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5ac2-119">Return value</span></span>

<span data-ttu-id="c5ac2-120">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c5ac2-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c5ac2-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c5ac2-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ac2-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5ac2-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c5ac2-123">Header</span><span class="sxs-lookup"><span data-stu-id="c5ac2-123">Header</span></span></p></td><td><span data-ttu-id="c5ac2-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c5ac2-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c5ac2-125"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5ac2-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c5ac2-126">**Isingleeventrequest**</span><span class="sxs-lookup"><span data-stu-id="c5ac2-126">**ISingleEventRequest**</span></span>](/windows/desktop/direct3dtools/isingleeventrequest)

 

 
