---
title: IMsRdpClient7 GetStatusText-Methode (OpenService. h)
description: Ruft den Status Text für den angegebenen Statuscode ab.
ms.assetid: 1da2280a-c26d-4caa-b227-c289055f3aa9
ms.tgt_platform: multiple
keywords:
- GetStatusText-Methode Remotedesktopdienste
- GetStatusText-Methode Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, GetStatusText-Methode
- GetStatusText-Methode Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, GetStatusText-Methode
- GetStatusText-Methode Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, GetStatusText-Methode
- GetStatusText-Methode Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10 Interface Remotedesktopdienste, GetStatusText-Methode
topic_type:
- apiref
api_name:
- IMsRdpClient7.GetStatusText
- IMsRdpClient8.GetStatusText
- IMsRdpClient9.GetStatusText
- IMsRdpClient10.GetStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820628bfba59ec980e5128b9d9df3ee21b49a064
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742144"
---
# <a name="imsrdpclient7getstatustext-method"></a><span data-ttu-id="63c3b-112">IMsRdpClient7:: GetStatusText-Methode</span><span class="sxs-lookup"><span data-stu-id="63c3b-112">IMsRdpClient7::GetStatusText method</span></span>

<span data-ttu-id="63c3b-113">Ruft den Status Text für den angegebenen Statuscode ab.</span><span class="sxs-lookup"><span data-stu-id="63c3b-113">Retrieves the status text for the specified status code.</span></span>

## <a name="syntax"></a><span data-ttu-id="63c3b-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="63c3b-114">Syntax</span></span>


```C++
HRESULT GetStatusText(
  [in]          UINT statusCode,
  [out, retval] BSTR *pBstrStatusText
);
```



## <a name="parameters"></a><span data-ttu-id="63c3b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="63c3b-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63c3b-116">*Statuscode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63c3b-116">*statusCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63c3b-117">Ein **uint** , der den Statuscode angibt, für den der Text abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="63c3b-117">A **UINT** that specifies the status code to retrieve the text for.</span></span>

</dd> <dt>

<span data-ttu-id="63c3b-118">*pbstraustatustext* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="63c3b-118">*pBstrStatusText* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="63c3b-119">Die Adresse eines **BSTR** , der den Status Text empfängt.</span><span class="sxs-lookup"><span data-stu-id="63c3b-119">The address of a **BSTR** that receives the status text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63c3b-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63c3b-120">Return value</span></span>

<span data-ttu-id="63c3b-121">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="63c3b-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="63c3b-122">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="63c3b-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="63c3b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63c3b-123">Requirements</span></span>



| <span data-ttu-id="63c3b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63c3b-124">Requirement</span></span> | <span data-ttu-id="63c3b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="63c3b-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="63c3b-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="63c3b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="63c3b-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="63c3b-127">Windows 7</span></span><br/>                                                                     |
| <span data-ttu-id="63c3b-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="63c3b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="63c3b-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="63c3b-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="63c3b-130">Header</span><span class="sxs-lookup"><span data-stu-id="63c3b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="63c3b-131"><dt>OpenService. h</dt></span><span class="sxs-lookup"><span data-stu-id="63c3b-131"><dt>Openservice.h</dt></span></span> </dl> |
| <span data-ttu-id="63c3b-132">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="63c3b-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="63c3b-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63c3b-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="63c3b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="63c3b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63c3b-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63c3b-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="63c3b-136">IID</span><span class="sxs-lookup"><span data-stu-id="63c3b-136">IID</span></span><br/>                      | <span data-ttu-id="63c3b-137">IID \_ IMsRdpClient7 ist als b2a5b5ce-3461-444a-91d4-add26d070638 definiert.</span><span class="sxs-lookup"><span data-stu-id="63c3b-137">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="63c3b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63c3b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63c3b-139">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="63c3b-139">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="63c3b-140">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="63c3b-140">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="63c3b-141">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="63c3b-141">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="63c3b-142">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="63c3b-142">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





