---
title: Imstscnonscriptable binarysalt-Eigenschaft
description: Diese Eigenschaft ist nicht mehr zur Verwendung verfügbar. | Imstscnonscriptable binarysalt-Eigenschaft
ms.assetid: 7af2e5be-9ddb-46ab-947c-f79ab890d7bc
ms.tgt_platform: multiple
keywords:
- Binarysalt-Eigenschaft Remotedesktopdienste
- Binarysalt-Eigenschaft Remotedesktopdienste, imstscnonscriptable-Schnittstelle
- Imstscnonscriptable-Schnittstelle Remotedesktopdienste, binarysalt-Eigenschaft
- Binarysalt-Eigenschaft Remotedesktopdienste, mstscax-Objekt
- Mstscax-Objekt Remotedesktopdienste, binarysalt-Eigenschaft
- Binarysalt-Eigenschaft Remotedesktopdienste, imsrdpclientnonscriptable-Schnittstelle
- Imsrdpclientnonscriptable-Schnittstelle Remotedesktopdienste, binarysalt-Eigenschaft
- Binarysalt-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable2-Schnittstelle
- IMsRdpClientNonScriptable2 Interface Remotedesktopdienste, binarysalt (Eigenschaft)
- Binarysalt-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3 Interface Remotedesktopdienste, binarysalt (Eigenschaft)
- Binarysalt-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, binarysalt (Eigenschaft)
- Binarysalt-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, binarysalt (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.BinarySalt
- IMsTscNonScriptable.get_BinarySalt
- IMsTscNonScriptable.put_BinarySalt
- MsTscAx.BinarySalt
- IMsRdpClientNonScriptable.BinarySalt
- IMsRdpClientNonScriptable.get_BinarySalt
- IMsRdpClientNonScriptable.put_BinarySalt
- IMsRdpClientNonScriptable2.BinarySalt
- IMsRdpClientNonScriptable2.get_BinarySalt
- IMsRdpClientNonScriptable2.put_BinarySalt
- IMsRdpClientNonScriptable3.BinarySalt
- IMsRdpClientNonScriptable3.get_BinarySalt
- IMsRdpClientNonScriptable3.put_BinarySalt
- IMsRdpClientNonScriptable4.BinarySalt
- IMsRdpClientNonScriptable4.get_BinarySalt
- IMsRdpClientNonScriptable4.put_BinarySalt
- IMsRdpClientNonScriptable5.BinarySalt
- IMsRdpClientNonScriptable5.get_BinarySalt
- IMsRdpClientNonScriptable5.put_BinarySalt
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eb13ccb79a9cf2c309a32772a73b393756c7bdd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366399"
---
# <a name="imstscnonscriptablebinarysalt-property"></a><span data-ttu-id="65399-119">Imstscnonscriptable:: binarysalt-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="65399-119">IMsTscNonScriptable::BinarySalt property</span></span>

<span data-ttu-id="65399-120">Diese Eigenschaft ist nicht mehr zur Verwendung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="65399-120">This property is no longer available for use.</span></span>

<span data-ttu-id="65399-121">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="65399-121">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="65399-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="65399-122">Syntax</span></span>


```C++
HRESULT put_BinarySalt(
  [in]  BSTR newSalt
);

HRESULT get_BinarySalt(
  [out] BSTR *pSalt
);
```



## <a name="property-value"></a><span data-ttu-id="65399-123">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="65399-123">Property value</span></span>

<span data-ttu-id="65399-124">Der neue binäre Salt-Teil für ein Binär codiertes Kennwort.</span><span class="sxs-lookup"><span data-stu-id="65399-124">The new binary salt part for a binary encoded password.</span></span>

## <a name="error-codes"></a><span data-ttu-id="65399-125">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="65399-125">Error codes</span></span>

<span data-ttu-id="65399-126">Gibt " **E \_ notimpl**" zurück.</span><span class="sxs-lookup"><span data-stu-id="65399-126">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="65399-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65399-127">Requirements</span></span>



| <span data-ttu-id="65399-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65399-128">Requirement</span></span> | <span data-ttu-id="65399-129">Wert</span><span class="sxs-lookup"><span data-stu-id="65399-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65399-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="65399-130">Minimum supported client</span></span><br/> | <span data-ttu-id="65399-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="65399-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="65399-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="65399-132">Minimum supported server</span></span><br/> | <span data-ttu-id="65399-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="65399-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="65399-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="65399-134">End of client support</span></span><br/>    | <span data-ttu-id="65399-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="65399-135">None supported</span></span><br/>                                                              |
| <span data-ttu-id="65399-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="65399-136">End of server support</span></span><br/>    | <span data-ttu-id="65399-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="65399-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="65399-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="65399-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="65399-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65399-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="65399-140">DLL</span><span class="sxs-lookup"><span data-stu-id="65399-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65399-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65399-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="65399-142">IID</span><span class="sxs-lookup"><span data-stu-id="65399-142">IID</span></span><br/>                      | <span data-ttu-id="65399-143">IID \_ imstscnonscriptable ist als c1e6743a-41c1-4a74-832a-0dd06c1c7a0e definiert.</span><span class="sxs-lookup"><span data-stu-id="65399-143">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65399-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65399-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65399-145">**Imsrdpclientnonscriptable**</span><span class="sxs-lookup"><span data-stu-id="65399-145">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="65399-146">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="65399-146">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="65399-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="65399-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="65399-148">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="65399-148">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="65399-149">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="65399-149">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="65399-150">**Imstscnonscriptable**</span><span class="sxs-lookup"><span data-stu-id="65399-150">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





