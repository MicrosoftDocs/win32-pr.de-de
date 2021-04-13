---
title: Imstscax cipherstärke (Eigenschaft)
description: Ruft die maximale Verschlüsselungsstärke des aktuellen Steuer Elements ab.
ms.assetid: 94efe3e5-4074-4187-b58a-b812f37f3622
ms.tgt_platform: multiple
keywords:
- Eigenschaft "cipherstärke" Remotedesktopdienste
- Eigenschaften Remotedesktopdienste cipherstärke, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, cipherstärke (Eigenschaft)
- Cipherstärke-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, Eigenschaft "cipherstärke"
- Eigenschaften Remotedesktopdienste cipherstärke, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, Eigenschaft "cipherstärke"
- Eigenschaften Remotedesktopdienste cipherstärke, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, Eigenschaft "cipherstärke"
- Eigenschaften Remotedesktopdienste cipherstärke, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, Eigenschaft "cipherstärke"
- Eigenschaften Remotedesktopdienste cipherstärke, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, Eigenschaft "cipherstärke"
- Eigenschaften Remotedesktopdienste cipherstärke, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, Eigenschaft "cipherstärke"
- Eigenschaften Remotedesktopdienste cipherstärke, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, Eigenschaft "cipherstärke"
- Eigenschaften Remotedesktopdienste cipherstärke, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, Eigenschaft "cipherstärke"
- Eigenschaften Remotedesktopdienste cipherstärke, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, Eigenschaft "cipherstärke"
topic_type:
- apiref
api_name:
- IMsTscAx.CipherStrength
- IMsTscAx.get_CipherStrength
- IMsRdpClient.CipherStrength
- IMsRdpClient.get_CipherStrength
- IMsRdpClient2.CipherStrength
- IMsRdpClient2.get_CipherStrength
- IMsRdpClient3.CipherStrength
- IMsRdpClient3.get_CipherStrength
- IMsRdpClient4.CipherStrength
- IMsRdpClient4.get_CipherStrength
- IMsRdpClient5.CipherStrength
- IMsRdpClient5.get_CipherStrength
- IMsRdpClient6.CipherStrength
- IMsRdpClient6.get_CipherStrength
- IMsRdpClient7.CipherStrength
- IMsRdpClient7.get_CipherStrength
- IMsRdpClient8.CipherStrength
- IMsRdpClient8.get_CipherStrength
- IMsRdpClient9.CipherStrength
- IMsRdpClient9.get_CipherStrength
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401cf3796d349aaa6764eae46a371a9d485f763c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391599"
---
# <a name="imstscaxcipherstrength-property"></a><span data-ttu-id="8e1bf-124">Imstscax:: cipherstärke (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8e1bf-124">IMsTscAx::CipherStrength property</span></span>

<span data-ttu-id="8e1bf-125">Ruft die maximale Verschlüsselungsstärke des aktuellen Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-125">Retrieves the maximum encryption strength of the current control.</span></span>

<span data-ttu-id="8e1bf-126">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e1bf-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e1bf-127">Syntax</span></span>


```C++
HRESULT get_CipherStrength(
  [out] LONG *pCipherStrength
);
```



## <a name="property-value"></a><span data-ttu-id="8e1bf-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8e1bf-128">Property value</span></span>

<span data-ttu-id="8e1bf-129">Die Verschlüsselungsstärke.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-129">The encryption strength.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8e1bf-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="8e1bf-130">Error codes</span></span>

<span data-ttu-id="8e1bf-131">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e1bf-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e1bf-132">Remarks</span></span>

<span data-ttu-id="8e1bf-133">Bei Remotedesktop-Webverbindung ist die Verschlüsselungsstärke immer 128, da das Remotedesktop ActiveX-Steuerelement die Verschlüsselung bis einschließlich 128 Bits unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-133">For Remote Desktop Web Connection, the cipher strength is always 128 because the Remote Desktop ActiveX control supports encryption up to and including 128 bits.</span></span> <span data-ttu-id="8e1bf-134">Das 128-Bit-Steuerelement kann weiterhin eine Verbindung mit 56 Bit Encryption Remotedesktop-Sitzungshost (RD-Sitzungshost)-Servern herstellen.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-134">The 128-bit control can still connect to 56 bit encryption Remote Desktop Session Host (RD Session Host) servers.</span></span>

<span data-ttu-id="8e1bf-135">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="8e1bf-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e1bf-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e1bf-136">Requirements</span></span>



| <span data-ttu-id="8e1bf-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e1bf-137">Requirement</span></span> | <span data-ttu-id="8e1bf-138">Wert</span><span class="sxs-lookup"><span data-stu-id="8e1bf-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e1bf-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e1bf-139">Minimum supported client</span></span><br/> | <span data-ttu-id="8e1bf-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e1bf-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8e1bf-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e1bf-141">Minimum supported server</span></span><br/> | <span data-ttu-id="8e1bf-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e1bf-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8e1bf-143">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="8e1bf-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="8e1bf-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e1bf-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8e1bf-145">DLL</span><span class="sxs-lookup"><span data-stu-id="8e1bf-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e1bf-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e1bf-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8e1bf-147">IID</span><span class="sxs-lookup"><span data-stu-id="8e1bf-147">IID</span></span><br/>                      | <span data-ttu-id="8e1bf-148">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="8e1bf-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e1bf-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e1bf-150">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="8e1bf-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="8e1bf-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="8e1bf-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="8e1bf-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="8e1bf-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="8e1bf-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="8e1bf-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="8e1bf-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="8e1bf-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="8e1bf-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="8e1bf-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="8e1bf-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="8e1bf-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="8e1bf-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="8e1bf-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="8e1bf-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="8e1bf-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="8e1bf-159">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="8e1bf-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





