---
title: IMsRdpClient5 GetErrorDescription-Methode
description: Ruft die Fehlerbeschreibung für die Sitzungs Trennungs Ereignisse ab.
ms.assetid: 8c8f7b10-7f79-4586-845e-e99f5ca81905
ms.tgt_platform: multiple
keywords:
- GetErrorDescription-Methode Remotedesktopdienste
- GetErrorDescription-Methode Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, GetErrorDescription-Methode
- GetErrorDescription-Methode Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, GetErrorDescription-Methode
- GetErrorDescription-Methode Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, GetErrorDescription-Methode
- GetErrorDescription-Methode Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, GetErrorDescription-Methode
- GetErrorDescription-Methode Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, GetErrorDescription-Methode
- GetErrorDescription-Methode Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10 Interface Remotedesktopdienste, GetErrorDescription-Methode
topic_type:
- apiref
api_name:
- IMsRdpClient5.GetErrorDescription
- IMsRdpClient6.GetErrorDescription
- IMsRdpClient7.GetErrorDescription
- IMsRdpClient8.GetErrorDescription
- IMsRdpClient9.GetErrorDescription
- IMsRdpClient10.GetErrorDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c402a0128286964ddeb1c53cd805e4ef6414bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392170"
---
# <a name="imsrdpclient5geterrordescription-method"></a><span data-ttu-id="3807a-116">IMsRdpClient5:: GetErrorDescription-Methode</span><span class="sxs-lookup"><span data-stu-id="3807a-116">IMsRdpClient5::GetErrorDescription method</span></span>

<span data-ttu-id="3807a-117">Ruft die Fehlerbeschreibung für die Sitzungs Trennungs Ereignisse ab.</span><span class="sxs-lookup"><span data-stu-id="3807a-117">Retrieves the error description for the session disconnect events.</span></span>

## <a name="syntax"></a><span data-ttu-id="3807a-118">Syntax</span><span class="sxs-lookup"><span data-stu-id="3807a-118">Syntax</span></span>


```C++
HRESULT GetErrorDescription(
  [in]  UINT disconnectReason,
  [in]  UINT extendedDisconnectReason,
  [out] BSTR *pBstrErrorMsg
);
```



## <a name="parameters"></a><span data-ttu-id="3807a-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="3807a-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3807a-120">*disconnecverrat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3807a-120">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3807a-121">Der Trennungsgrund.</span><span class="sxs-lookup"><span data-stu-id="3807a-121">The disconnect reason.</span></span>

</dd> <dt>

<span data-ttu-id="3807a-122">*extendeddisconnecverrat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3807a-122">*extendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3807a-123">Bietet ausführliche Informationen dazu, warum eine Trennung initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3807a-123">Provides detailed information about why a disconnect was initiated.</span></span>

</dd> <dt>

<span data-ttu-id="3807a-124">*pbstrauerrormsg* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3807a-124">*pBstrErrorMsg* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3807a-125">Ein Zeiger auf eine **BSTR** -Variable, die den Fehlermeldungs Text empfängt.</span><span class="sxs-lookup"><span data-stu-id="3807a-125">A pointer to a **BSTR** variable that receives the error message text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3807a-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3807a-126">Return value</span></span>

<span data-ttu-id="3807a-127">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3807a-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3807a-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3807a-128">Requirements</span></span>



| <span data-ttu-id="3807a-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3807a-129">Requirement</span></span> | <span data-ttu-id="3807a-130">Wert</span><span class="sxs-lookup"><span data-stu-id="3807a-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3807a-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3807a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3807a-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3807a-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3807a-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3807a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3807a-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3807a-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3807a-135">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="3807a-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="3807a-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3807a-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3807a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3807a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3807a-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3807a-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3807a-139">IID</span><span class="sxs-lookup"><span data-stu-id="3807a-139">IID</span></span><br/>                      | <span data-ttu-id="3807a-140">IID \_ IMsRdpClient5 ist als 4eb5335b-6429-477d-B922-e06a28ecd8bf definiert.</span><span class="sxs-lookup"><span data-stu-id="3807a-140">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3807a-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3807a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3807a-142">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="3807a-142">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="3807a-143">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="3807a-143">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="3807a-144">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="3807a-144">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="3807a-145">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="3807a-145">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="3807a-146">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="3807a-146">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="3807a-147">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="3807a-147">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





