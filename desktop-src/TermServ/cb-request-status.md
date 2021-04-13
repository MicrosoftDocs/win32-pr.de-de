---
title: CB_REQUEST_STATUS-Enumeration (cbclient. h)
description: Gibt den Status einer asynchronen Anforderung an.
ms.assetid: 35FAC8EA-BA17-405F-AE10-33A816029F62
ms.tgt_platform: multiple
keywords:
- CB_REQUEST_STATUS Enumeration Remotedesktopdienste
topic_type:
- apiref
api_name:
- CB_REQUEST_STATUS
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd57efd12d3fb5c708d5c4861ee144543bb49f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340537"
---
# <a name="cb_request_status-enumeration"></a><span data-ttu-id="f71c4-104">CB- \_ Anforderungs \_ Status-Enumeration</span><span class="sxs-lookup"><span data-stu-id="f71c4-104">CB\_REQUEST\_STATUS enumeration</span></span>

<span data-ttu-id="f71c4-105">Gibt den Status einer asynchronen Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="f71c4-105">Specifies the status of an asynchronous request.</span></span> <span data-ttu-id="f71c4-106">Diese Enumeration wird mit der [**iconnectionbrokerrequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="f71c4-106">This enumeration is used with the [**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f71c4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f71c4-107">Syntax</span></span>


```C++
typedef enum _CB_REQUEST_STATUS { 
  CB_STATUS_INVALID                     = 1,
  CB_STATUS_INITIATING_REQUEST          = 0,
  CB_STATUS_REQUEST_COMPLETED,
  CB_STATUS_REQUEST_FAILED,
  CB_STATUS_REQUEST_ABORTED,
  CB_STATUS_FINDING_DESTINATION,
  CB_STATUS_LOADING_DESTINATION,
  CB_STATUS_BRINGING_SESSION_ONLINE,
  CB_STATUS_REDIRECTING_TO_DESTINATION
} CB_REQUEST_STATUS;
```



## <a name="constants"></a><span data-ttu-id="f71c4-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="f71c4-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f71c4-109"><span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**CB- \_ Status \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="f71c4-109"><span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**CB\_STATUS\_INVALID**</span></span>
</dt> <dd>

<span data-ttu-id="f71c4-110">Das Anforderungs Objekt ist nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="f71c4-110">The request object is not initialized.</span></span>

</dd> <dt>

<span data-ttu-id="f71c4-111"><span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**CB- \_ Status \_ Initiierungs \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="f71c4-111"><span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**CB\_STATUS\_INITIATING\_REQUEST**</span></span>
</dt> <dd>

<span data-ttu-id="f71c4-112">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f71c4-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f71c4-113"><span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**CB- \_ Status \_ Anforderung \_ abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="f71c4-113"><span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**CB\_STATUS\_REQUEST\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="f71c4-114">Die Anforderung ist fertiggestellt.</span><span class="sxs-lookup"><span data-stu-id="f71c4-114">The request is complete.</span></span>

</dd> <dt>

<span data-ttu-id="f71c4-115"><span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**Fehler bei der CB- \_ Status \_ Anforderung \_**</span><span class="sxs-lookup"><span data-stu-id="f71c4-115"><span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**CB\_STATUS\_REQUEST\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="f71c4-116">Fehler bei der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f71c4-116">The request failed.</span></span>

</dd> <dt>

<span data-ttu-id="f71c4-117"><span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**CB- \_ Status \_ Anforderung \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="f71c4-117"><span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**CB\_STATUS\_REQUEST\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="f71c4-118">Die Anforderung wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="f71c4-118">The request was aborted.</span></span>

</dd> <dt>

<span data-ttu-id="f71c4-119"><span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**CB \_ - \_ Status \_ Suchziel**</span><span class="sxs-lookup"><span data-stu-id="f71c4-119"><span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**CB\_STATUS\_FINDING\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="f71c4-120">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f71c4-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f71c4-121"><span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**CB- \_ Status \_ Lade \_ Ziel**</span><span class="sxs-lookup"><span data-stu-id="f71c4-121"><span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**CB\_STATUS\_LOADING\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="f71c4-122">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f71c4-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f71c4-123"><span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**CB \_ -Status der \_ \_ Sitzung \_ Online**</span><span class="sxs-lookup"><span data-stu-id="f71c4-123"><span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**CB\_STATUS\_BRINGING\_SESSION\_ONLINE**</span></span>
</dt> <dd>

<span data-ttu-id="f71c4-124">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f71c4-124">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f71c4-125"><span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**CB- \_ Status Umleitung \_ \_ zum \_ Ziel**</span><span class="sxs-lookup"><span data-stu-id="f71c4-125"><span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**CB\_STATUS\_REDIRECTING\_TO\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="f71c4-126">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f71c4-126">Not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f71c4-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f71c4-127">Requirements</span></span>



| <span data-ttu-id="f71c4-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f71c4-128">Requirement</span></span> | <span data-ttu-id="f71c4-129">Wert</span><span class="sxs-lookup"><span data-stu-id="f71c4-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f71c4-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f71c4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f71c4-131">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f71c4-131">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="f71c4-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f71c4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f71c4-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f71c4-133">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="f71c4-134">Header</span><span class="sxs-lookup"><span data-stu-id="f71c4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f71c4-135"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="f71c4-135"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f71c4-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f71c4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f71c4-137">**Iconnectionbrokerrequest:: CheckStatus**</span><span class="sxs-lookup"><span data-stu-id="f71c4-137">**IConnectionBrokerRequest::CheckStatus**</span></span>](iconnectionbrokerrequest-checkstatus.md)
</dt> </dl>

 

 





