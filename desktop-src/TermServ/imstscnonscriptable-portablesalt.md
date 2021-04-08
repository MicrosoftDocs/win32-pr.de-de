---
title: Imstscnonscriptable-portablesalt-Eigenschaft
description: Diese Eigenschaft wird nicht mehr unterstützt.
ms.assetid: 1f123ec8-27b6-4637-9c57-fe32a224be8a
ms.tgt_platform: multiple
keywords:
- Portablesalt-Eigenschaft Remotedesktopdienste
- Portablesalt-Eigenschaft Remotedesktopdienste, imstscnonscriptable-Schnittstelle
- Imstscnonscriptable-Schnittstelle Remotedesktopdienste, portablesalt-Eigenschaft
- Portablesalt-Eigenschaft Remotedesktopdienste, mstscax-Objekt
- Mstscax-Objekt Remotedesktopdienste, portablesalt-Eigenschaft
- Portablesalt-Eigenschaft Remotedesktopdienste, imsrdpclientnonscriptable-Schnittstelle
- Imsrdpclientnonscriptable-Schnittstelle Remotedesktopdienste, portablesalt-Eigenschaft
- Portablesalt-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable2-Schnittstelle
- IMsRdpClientNonScriptable2-Schnittstelle Remotedesktopdienste, portablesalt-Eigenschaft
- Portablesalt-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3-Schnittstelle Remotedesktopdienste, portablesalt-Eigenschaft
- Portablesalt-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4-Schnittstelle Remotedesktopdienste, portablesalt-Eigenschaft
- Portablesalt-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste, portablesalt-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.PortableSalt
- IMsTscNonScriptable.get_PortableSalt
- IMsTscNonScriptable.put_PortableSalt
- MsTscAx.PortableSalt
- IMsRdpClientNonScriptable.PortableSalt
- IMsRdpClientNonScriptable.get_PortableSalt
- IMsRdpClientNonScriptable.put_PortableSalt
- IMsRdpClientNonScriptable2.PortableSalt
- IMsRdpClientNonScriptable2.get_PortableSalt
- IMsRdpClientNonScriptable2.put_PortableSalt
- IMsRdpClientNonScriptable3.PortableSalt
- IMsRdpClientNonScriptable3.get_PortableSalt
- IMsRdpClientNonScriptable3.put_PortableSalt
- IMsRdpClientNonScriptable4.PortableSalt
- IMsRdpClientNonScriptable4.get_PortableSalt
- IMsRdpClientNonScriptable4.put_PortableSalt
- IMsRdpClientNonScriptable5.PortableSalt
- IMsRdpClientNonScriptable5.get_PortableSalt
- IMsRdpClientNonScriptable5.put_PortableSalt
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0162073b8361cc89f7ab2e33f60406c0db935bdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742385"
---
# <a name="imstscnonscriptableportablesalt-property"></a><span data-ttu-id="f6ac7-118">Imstscnonscriptable::P ortablesalt-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f6ac7-118">IMsTscNonScriptable::PortableSalt property</span></span>

<span data-ttu-id="f6ac7-119">Diese Eigenschaft wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-119">This property is no longer supported.</span></span>

<span data-ttu-id="f6ac7-120">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6ac7-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6ac7-121">Syntax</span></span>


```C++
HRESULT put_PortableSalt(
  [in]  BSTR newPortableSalt
);

HRESULT get_PortableSalt(
  [out] BSTR *pPortableSalt
);
```



## <a name="property-value"></a><span data-ttu-id="f6ac7-122">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f6ac7-122">Property value</span></span>

<span data-ttu-id="f6ac7-123">Der neue Portable Salt-Teil für ein portables codiertes Kennwort.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-123">The new portable salt part for a portable encoded password.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f6ac7-124">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f6ac7-124">Error codes</span></span>

<span data-ttu-id="f6ac7-125">Gibt " **E \_ notimpl**" zurück.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-125">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6ac7-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6ac7-126">Requirements</span></span>



| <span data-ttu-id="f6ac7-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6ac7-127">Requirement</span></span> | <span data-ttu-id="f6ac7-128">Wert</span><span class="sxs-lookup"><span data-stu-id="f6ac7-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6ac7-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f6ac7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f6ac7-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f6ac7-130">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f6ac7-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f6ac7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f6ac7-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f6ac7-132">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f6ac7-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f6ac7-133">End of client support</span></span><br/>    | <span data-ttu-id="f6ac7-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f6ac7-134">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f6ac7-135">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="f6ac7-135">End of server support</span></span><br/>    | <span data-ttu-id="f6ac7-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f6ac7-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f6ac7-137">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f6ac7-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="f6ac7-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6ac7-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f6ac7-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f6ac7-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6ac7-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6ac7-140"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f6ac7-141">IID</span><span class="sxs-lookup"><span data-stu-id="f6ac7-141">IID</span></span><br/>                      | <span data-ttu-id="f6ac7-142">IID \_ imstscnonscriptable ist als c1e6743a-41c1-4a74-832a-0dd06c1c7a0e definiert.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-142">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f6ac7-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6ac7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6ac7-144">**Imsrdpclientnonscriptable**</span><span class="sxs-lookup"><span data-stu-id="f6ac7-144">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="f6ac7-145">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="f6ac7-145">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="f6ac7-146">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="f6ac7-146">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="f6ac7-147">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="f6ac7-147">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="f6ac7-148">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="f6ac7-148">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="f6ac7-149">**Imstscnonscriptable**</span><span class="sxs-lookup"><span data-stu-id="f6ac7-149">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="f6ac7-150">**Portablepassword**</span><span class="sxs-lookup"><span data-stu-id="f6ac7-150">**PortablePassword**</span></span>](imstscnonscriptable-portablepassword.md)
</dt> </dl>

 

 





