---
title: Imstscnonscriptable binarypassword (Eigenschaft)
description: Diese Eigenschaft ist nicht mehr zur Verwendung verfügbar. | Imstscnonscriptable binarypassword (Eigenschaft)
ms.assetid: b3be7323-a75f-4ec2-9d58-e8ff3338d6ff
ms.tgt_platform: multiple
keywords:
- Binarypassword-Eigenschaft Remotedesktopdienste
- Binarypassword-Eigenschaft Remotedesktopdienste, imstscnonscriptable-Schnittstelle
- Imstscnonscriptable-Schnittstelle Remotedesktopdienste, binarypassword-Eigenschaft
- Binarypassword-Eigenschaft Remotedesktopdienste, mstscax-Objekt
- Mstscax-Objekt Remotedesktopdienste, binarypassword-Eigenschaft
- Binarypassword-Eigenschaft Remotedesktopdienste, imsrdpclientnonscriptable-Schnittstelle
- Imsrdpclientnonscriptable-Schnittstelle Remotedesktopdienste, binarypassword-Eigenschaft
- Binarypassword-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable2-Schnittstelle
- IMsRdpClientNonScriptable2 Interface Remotedesktopdienste, binarypassword (Eigenschaft)
- Binarypassword-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3 Interface Remotedesktopdienste, binarypassword (Eigenschaft)
- Binarypassword-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, binarypassword (Eigenschaft)
- Binarypassword-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, binarypassword (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.BinaryPassword
- IMsTscNonScriptable.get_BinaryPassword
- IMsTscNonScriptable.put_BinaryPassword
- MsTscAx.BinaryPassword
- IMsRdpClientNonScriptable.BinaryPassword
- IMsRdpClientNonScriptable.get_BinaryPassword
- IMsRdpClientNonScriptable.put_BinaryPassword
- IMsRdpClientNonScriptable2.BinaryPassword
- IMsRdpClientNonScriptable2.get_BinaryPassword
- IMsRdpClientNonScriptable2.put_BinaryPassword
- IMsRdpClientNonScriptable3.BinaryPassword
- IMsRdpClientNonScriptable3.get_BinaryPassword
- IMsRdpClientNonScriptable3.put_BinaryPassword
- IMsRdpClientNonScriptable4.BinaryPassword
- IMsRdpClientNonScriptable4.get_BinaryPassword
- IMsRdpClientNonScriptable4.put_BinaryPassword
- IMsRdpClientNonScriptable5.BinaryPassword
- IMsRdpClientNonScriptable5.get_BinaryPassword
- IMsRdpClientNonScriptable5.put_BinaryPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d6eab2a3902968ef4d4c953a8da8b9c884a497
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361798"
---
# <a name="imstscnonscriptablebinarypassword-property"></a><span data-ttu-id="2cfab-119">Imstscnonscriptable:: binarypassword (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2cfab-119">IMsTscNonScriptable::BinaryPassword property</span></span>

<span data-ttu-id="2cfab-120">Diese Eigenschaft ist nicht mehr zur Verwendung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cfab-120">This property is no longer available for use.</span></span>

<span data-ttu-id="2cfab-121">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="2cfab-121">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cfab-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cfab-122">Syntax</span></span>


```C++
HRESULT put_BinaryPassword(
  [in]  BSTR newPassword
);

HRESULT get_BinaryPassword(
  [out] BSTR *pBinaryPassword
);
```



## <a name="property-value"></a><span data-ttu-id="2cfab-123">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2cfab-123">Property value</span></span>

<span data-ttu-id="2cfab-124">Der neue Kenn Wort Teil im Binärformat.</span><span class="sxs-lookup"><span data-stu-id="2cfab-124">The new password part, in binary encoded format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2cfab-125">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="2cfab-125">Error codes</span></span>

<span data-ttu-id="2cfab-126">Gibt " **E \_ notimpl**" zurück.</span><span class="sxs-lookup"><span data-stu-id="2cfab-126">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cfab-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2cfab-127">Requirements</span></span>



| <span data-ttu-id="2cfab-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2cfab-128">Requirement</span></span> | <span data-ttu-id="2cfab-129">Wert</span><span class="sxs-lookup"><span data-stu-id="2cfab-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cfab-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2cfab-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2cfab-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2cfab-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2cfab-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2cfab-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2cfab-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2cfab-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2cfab-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="2cfab-134">End of client support</span></span><br/>    | <span data-ttu-id="2cfab-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2cfab-135">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2cfab-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="2cfab-136">End of server support</span></span><br/>    | <span data-ttu-id="2cfab-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2cfab-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2cfab-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2cfab-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="2cfab-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cfab-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2cfab-140">DLL</span><span class="sxs-lookup"><span data-stu-id="2cfab-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cfab-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cfab-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2cfab-142">IID</span><span class="sxs-lookup"><span data-stu-id="2cfab-142">IID</span></span><br/>                      | <span data-ttu-id="2cfab-143">IID \_ imstscnonscriptable ist als c1e6743a-41c1-4a74-832a-0dd06c1c7a0e definiert.</span><span class="sxs-lookup"><span data-stu-id="2cfab-143">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2cfab-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cfab-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cfab-145">**Imsrdpclientnonscriptable**</span><span class="sxs-lookup"><span data-stu-id="2cfab-145">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="2cfab-146">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="2cfab-146">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="2cfab-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="2cfab-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="2cfab-148">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="2cfab-148">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="2cfab-149">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="2cfab-149">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="2cfab-150">**Imstscnonscriptable**</span><span class="sxs-lookup"><span data-stu-id="2cfab-150">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





