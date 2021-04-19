---
title: Imstscnonscriptable-portablepassword-Eigenschaft
description: Diese Eigenschaft ist nicht mehr zur Verwendung verfügbar. | Imstscnonscriptable-portablepassword-Eigenschaft
ms.assetid: 8d831ed3-1f4a-41a9-b283-507c5d9eea22
ms.tgt_platform: multiple
keywords:
- Portablepassword-Eigenschaft Remotedesktopdienste
- Portablepassword-Eigenschaft Remotedesktopdienste, imstscnonscriptable-Schnittstelle
- Imstscnonscriptable-Schnittstelle Remotedesktopdienste, portablepassword-Eigenschaft
- Portablepassword-Eigenschaft Remotedesktopdienste, mstscax-Objekt
- Mstscax-Objekt Remotedesktopdienste, portablepassword-Eigenschaft
- Portablepassword-Eigenschaft Remotedesktopdienste, imsrdpclientnonscriptable-Schnittstelle
- Imsrdpclientnonscriptable-Schnittstelle Remotedesktopdienste, portablepassword-Eigenschaft
- Portablepassword-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable2-Schnittstelle
- IMsRdpClientNonScriptable2 Interface Remotedesktopdienste, portablepassword (Eigenschaft)
- Portablepassword-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3 Interface Remotedesktopdienste, portablepassword (Eigenschaft)
- Portablepassword-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, portablepassword (Eigenschaft)
- Portablepassword-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, portablepassword (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.PortablePassword
- IMsTscNonScriptable.get_PortablePassword
- IMsTscNonScriptable.put_PortablePassword
- MsTscAx.PortablePassword
- IMsRdpClientNonScriptable.PortablePassword
- IMsRdpClientNonScriptable.get_PortablePassword
- IMsRdpClientNonScriptable.put_PortablePassword
- IMsRdpClientNonScriptable2.PortablePassword
- IMsRdpClientNonScriptable2.get_PortablePassword
- IMsRdpClientNonScriptable2.put_PortablePassword
- IMsRdpClientNonScriptable3.PortablePassword
- IMsRdpClientNonScriptable3.get_PortablePassword
- IMsRdpClientNonScriptable3.put_PortablePassword
- IMsRdpClientNonScriptable4.PortablePassword
- IMsRdpClientNonScriptable4.get_PortablePassword
- IMsRdpClientNonScriptable4.put_PortablePassword
- IMsRdpClientNonScriptable5.PortablePassword
- IMsRdpClientNonScriptable5.get_PortablePassword
- IMsRdpClientNonScriptable5.put_PortablePassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5259e83087287395e6114bb8ffe3eb7e859ab52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106355137"
---
# <a name="imstscnonscriptableportablepassword-property"></a><span data-ttu-id="1f377-119">Imstscnonscriptable::P ortablepassword-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1f377-119">IMsTscNonScriptable::PortablePassword property</span></span>

<span data-ttu-id="1f377-120">Diese Eigenschaft ist nicht mehr zur Verwendung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1f377-120">This property is no longer available for use.</span></span>

<span data-ttu-id="1f377-121">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1f377-121">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f377-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f377-122">Syntax</span></span>


```C++
HRESULT put_PortablePassword(
  [in]  BSTR newPortablePassVal
);

HRESULT get_PortablePassword(
  [out] BSTR *pPortablePass
);
```



## <a name="property-value"></a><span data-ttu-id="1f377-123">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1f377-123">Property value</span></span>

<span data-ttu-id="1f377-124">Der neue Kenn Wort Teil im portablen codierten Format.</span><span class="sxs-lookup"><span data-stu-id="1f377-124">The new password part, in portable encoded format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1f377-125">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="1f377-125">Error codes</span></span>

<span data-ttu-id="1f377-126">Gibt " **E \_ notimpl**" zurück.</span><span class="sxs-lookup"><span data-stu-id="1f377-126">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f377-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f377-127">Requirements</span></span>



| <span data-ttu-id="1f377-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f377-128">Requirement</span></span> | <span data-ttu-id="1f377-129">Wert</span><span class="sxs-lookup"><span data-stu-id="1f377-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f377-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f377-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1f377-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1f377-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1f377-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f377-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1f377-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1f377-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1f377-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="1f377-134">End of client support</span></span><br/>    | <span data-ttu-id="1f377-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1f377-135">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1f377-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="1f377-136">End of server support</span></span><br/>    | <span data-ttu-id="1f377-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1f377-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1f377-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="1f377-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="1f377-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f377-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1f377-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1f377-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f377-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f377-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1f377-142">IID</span><span class="sxs-lookup"><span data-stu-id="1f377-142">IID</span></span><br/>                      | <span data-ttu-id="1f377-143">IID \_ imstscnonscriptable ist als c1e6743a-41c1-4a74-832a-0dd06c1c7a0e definiert.</span><span class="sxs-lookup"><span data-stu-id="1f377-143">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1f377-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f377-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f377-145">**Imsrdpclientnonscriptable**</span><span class="sxs-lookup"><span data-stu-id="1f377-145">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="1f377-146">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="1f377-146">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="1f377-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="1f377-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="1f377-148">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="1f377-148">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="1f377-149">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="1f377-149">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="1f377-150">**Imstscnonscriptable**</span><span class="sxs-lookup"><span data-stu-id="1f377-150">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





