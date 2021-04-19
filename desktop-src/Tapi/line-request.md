---
description: Die TAPI-Zeilen \_ Anforderungs Nachricht wird gesendet, um den Eingang einer neuen Anforderung von einer anderen Anwendung zu melden.
ms.assetid: d4dbba0d-8225-48d7-a66b-b189fdae70a8
title: LINE_REQUEST Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23987e370d5ae9c8eeb579780c5659f8075ac865
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356410"
---
# <a name="line_request-message"></a><span data-ttu-id="4f030-103">Zeilen \_ Anforderungs Nachricht</span><span class="sxs-lookup"><span data-stu-id="4f030-103">LINE\_REQUEST message</span></span>

<span data-ttu-id="4f030-104">Die TAPI- **Zeilen \_ Anforderungs** Nachricht wird gesendet, um den Eingang einer neuen Anforderung von einer anderen Anwendung zu melden.</span><span class="sxs-lookup"><span data-stu-id="4f030-104">The TAPI **LINE\_REQUEST** message is sent to report the arrival of a new request from another application.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="4f030-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f030-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f030-106">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="4f030-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="4f030-107">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4f030-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4f030-108">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="4f030-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="4f030-109">Die Registrierungs Instanz der Anwendung, die auf [**lineregisterrequestrecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4f030-109">The registration instance of the application specified on [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient).</span></span>

</dd> <dt>

<span data-ttu-id="4f030-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="4f030-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="4f030-111">Der Anforderungs Modus der neu ausstehenden Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4f030-111">The request mode of the newly pending request.</span></span> <span data-ttu-id="4f030-112">Dieser Parameter verwendet die [**linerequestmode- \_ Konstanten**](linerequestmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="4f030-112">This parameter uses the [**LINEREQUESTMODE\_ constants**](linerequestmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f030-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="4f030-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="4f030-114">Die Bedingungen für diesen Parameter lauten, wenn *dwParam1* auf linerequestmode Drop festgelegt ist \_ , *dwParam2* enthält das *HWND* der Anwendung, die den Löschvorgang anfordert.</span><span class="sxs-lookup"><span data-stu-id="4f030-114">The conditions for this parameter are, if *dwParam1* is set to LINEREQUESTMODE\_DROP, *dwParam2* contains the *hWnd* of the application requesting the drop.</span></span> <span data-ttu-id="4f030-115">Andernfalls wird *dwParam2* nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4f030-115">Otherwise, *dwParam2* is unused.</span></span>

</dd> <dt>

<span data-ttu-id="4f030-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="4f030-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="4f030-117">Wenn *dwParam1* auf linerequestmode Drop festgelegt ist \_ , enthält das nieder wertige Wort von *dwParam3* die *wrequestid* , wie von der Anwendung angegeben, die den Löschvorgang angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="4f030-117">If *dwParam1* is set to LINEREQUESTMODE\_DROP, the low-order word of *dwParam3* contains the *wRequestID* as specified by the application that requested the drop.</span></span> <span data-ttu-id="4f030-118">Andernfalls wird *dwParam3* nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4f030-118">Otherwise, *dwParam3* is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f030-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f030-119">Return value</span></span>

<span data-ttu-id="4f030-120">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="4f030-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f030-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f030-121">Remarks</span></span>

<span data-ttu-id="4f030-122">Die **Zeilen \_ Anforderungs** Nachricht wird an die Anwendung mit der höchsten Priorität gesendet, die sich für den entsprechenden Anforderungs Modus registriert hat.</span><span class="sxs-lookup"><span data-stu-id="4f030-122">The **LINE\_REQUEST** message is sent to the highest priority application that has registered for the corresponding request mode.</span></span> <span data-ttu-id="4f030-123">Diese Meldung gibt den Eingang einer unterstützten Telefonieanforderung im angegebenen Anforderungs Modus an.</span><span class="sxs-lookup"><span data-stu-id="4f030-123">This message indicates the arrival of an Assisted Telephony request of the specified request mode.</span></span> <span data-ttu-id="4f030-124">Wenn *dwParam1* linerequestmode \_ MakeCall ist, kann die Anwendung [**linegetrequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) mithilfe des entsprechenden Anforderungs Modus aufrufen, um die Anforderung zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="4f030-124">If *dwParam1* is LINEREQUESTMODE\_MAKECALL, the application can invoke [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) using the corresponding request mode to receive the request.</span></span> <span data-ttu-id="4f030-125">Wenn *dwParam1* auf linerequestmode \_ Drop gesetzt ist, enthält die Meldung alle Daten, die der Anforderungs Empfänger benötigt, um die Anforderung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4f030-125">If *dwParam1* is LINEREQUESTMODE\_DROP, the message contains all of the data the request recipient requires to perform the request.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f030-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f030-126">Requirements</span></span>



| <span data-ttu-id="4f030-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f030-127">Requirement</span></span> | <span data-ttu-id="4f030-128">Wert</span><span class="sxs-lookup"><span data-stu-id="4f030-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4f030-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="4f030-129">TAPI version</span></span><br/> | <span data-ttu-id="4f030-130">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="4f030-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="4f030-131">Header</span><span class="sxs-lookup"><span data-stu-id="4f030-131">Header</span></span><br/>       | <dl> <span data-ttu-id="4f030-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f030-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f030-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f030-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f030-134">**linegetrequest**</span><span class="sxs-lookup"><span data-stu-id="4f030-134">**lineGetRequest**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)
</dt> <dt>

[<span data-ttu-id="4f030-135">**lineregisterrequestrecipient**</span><span class="sxs-lookup"><span data-stu-id="4f030-135">**lineRegisterRequestRecipient**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)
</dt> <dt>

[<span data-ttu-id="4f030-136">**tapirequestmakecall**</span><span class="sxs-lookup"><span data-stu-id="4f030-136">**tapiRequestMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-tapirequestmakecall)
</dt> </dl>

 

 




