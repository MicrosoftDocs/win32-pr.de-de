---
title: Iconnectionbrokerrequest checkStatus-Methode (cbclient. h)
description: Wird aufgerufen, um den Status einer asynchronen Anforderung zu bestimmen.
ms.assetid: 6B0DDDB2-9905-4B48-8CCB-D6A6591B7723
ms.tgt_platform: multiple
keywords:
- CheckStatus-Methode Remotedesktopdienste
- CheckStatus-Methode Remotedesktopdienste, iconnectionbrokerrequest-Schnittstelle
- Iconnectionbrokerrequest-Schnittstelle Remotedesktopdienste, checkStatus-Methode
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest.CheckStatus
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27816ad95bbf3ef506f93d7fd4f4261709b1f476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392172"
---
# <a name="iconnectionbrokerrequestcheckstatus-method"></a><span data-ttu-id="51f9e-106">Iconnectionbrokerrequest:: checkStatus-Methode</span><span class="sxs-lookup"><span data-stu-id="51f9e-106">IConnectionBrokerRequest::CheckStatus method</span></span>

<span data-ttu-id="51f9e-107">Wird aufgerufen, um den Status einer asynchronen Anforderung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="51f9e-107">Called to determine the status of an asynchronous request.</span></span>

## <a name="syntax"></a><span data-ttu-id="51f9e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="51f9e-108">Syntax</span></span>


```C++
HRESULT CheckStatus(
  [out] CB_REQUEST_STATUS *pReqStatus
);
```



## <a name="parameters"></a><span data-ttu-id="51f9e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="51f9e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51f9e-110">*preqstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="51f9e-110">*pReqStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51f9e-111">Die Adresse einer Variablen, die einen Wert der CB- [**\_ Anforderungs \_ Status**](cb-request-status.md) -Enumeration empfängt, der den Status der Anforderung angibt.</span><span class="sxs-lookup"><span data-stu-id="51f9e-111">The address of a variable that receives a value of the [**CB\_REQUEST\_STATUS**](cb-request-status.md) enumeration that indicates the status of the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51f9e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51f9e-112">Return value</span></span>

<span data-ttu-id="51f9e-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="51f9e-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="51f9e-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="51f9e-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="51f9e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51f9e-115">Requirements</span></span>



| <span data-ttu-id="51f9e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51f9e-116">Requirement</span></span> | <span data-ttu-id="51f9e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="51f9e-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51f9e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51f9e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="51f9e-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="51f9e-119">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="51f9e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51f9e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="51f9e-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="51f9e-121">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="51f9e-122">Header</span><span class="sxs-lookup"><span data-stu-id="51f9e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="51f9e-123"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="51f9e-123"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="51f9e-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="51f9e-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="51f9e-125"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51f9e-125"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="51f9e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="51f9e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51f9e-127"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51f9e-127"><dt>Cbclient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51f9e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51f9e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51f9e-129">**Iconnectionbrokerrequest**</span><span class="sxs-lookup"><span data-stu-id="51f9e-129">**IConnectionBrokerRequest**</span></span>](iconnectionbrokerrequest.md)
</dt> </dl>

 

 





