---
title: Imstscax horizontalscrollbarvisible (Eigenschaft)
description: Gibt an, ob das Steuerelement eine horizontale Schiebe Leiste angezeigt hat.
ms.assetid: d3c22c5f-321f-476e-bcdb-224eb988a7bb
ms.tgt_platform: multiple
keywords:
- Horizontalscrollbarvisible-Eigenschaft Remotedesktopdienste
- Horizontalscrollbarvisible-Eigenschaft Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, horizontalscrollbarvisible (Eigenschaft)
- Horizontalscrollbarvisible-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient Interface Remotedesktopdienste, horizontalscrollbarvisible (Eigenschaft)
- Horizontalscrollbarvisible-Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, horizontalscrollbarvisible (Eigenschaft)
- Horizontalscrollbarvisible-Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, horizontalscrollbarvisible (Eigenschaft)
- Horizontalscrollbarvisible-Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, horizontalscrollbarvisible (Eigenschaft)
- Horizontalscrollbarvisible-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, horizontalscrollbarvisible (Eigenschaft)
- Horizontalscrollbarvisible-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, horizontalscrollbarvisible (Eigenschaft)
- Horizontalscrollbarvisible-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, horizontalscrollbarvisible (Eigenschaft)
- Horizontalscrollbarvisible-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, horizontalscrollbarvisible (Eigenschaft)
- Horizontalscrollbarvisible-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, horizontalscrollbarvisible (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsTscAx.HorizontalScrollBarVisible
- IMsTscAx.get_HorizontalScrollBarVisible
- IMsRdpClient.HorizontalScrollBarVisible
- IMsRdpClient.get_HorizontalScrollBarVisible
- IMsRdpClient2.HorizontalScrollBarVisible
- IMsRdpClient2.get_HorizontalScrollBarVisible
- IMsRdpClient3.HorizontalScrollBarVisible
- IMsRdpClient3.get_HorizontalScrollBarVisible
- IMsRdpClient4.HorizontalScrollBarVisible
- IMsRdpClient4.get_HorizontalScrollBarVisible
- IMsRdpClient5.HorizontalScrollBarVisible
- IMsRdpClient5.get_HorizontalScrollBarVisible
- IMsRdpClient6.HorizontalScrollBarVisible
- IMsRdpClient6.get_HorizontalScrollBarVisible
- IMsRdpClient7.HorizontalScrollBarVisible
- IMsRdpClient7.get_HorizontalScrollBarVisible
- IMsRdpClient8.HorizontalScrollBarVisible
- IMsRdpClient8.get_HorizontalScrollBarVisible
- IMsRdpClient9.HorizontalScrollBarVisible
- IMsRdpClient9.get_HorizontalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08fa2abb97a28af013e5791bcbd643f3f479d5c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040534"
---
# <a name="imstscaxhorizontalscrollbarvisible-property"></a><span data-ttu-id="7e0f4-124">Imstscax:: horizontalscrollbarvisible (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7e0f4-124">IMsTscAx::HorizontalScrollBarVisible property</span></span>

<span data-ttu-id="7e0f4-125">Gibt an, ob das Steuerelement eine horizontale Schiebe Leiste angezeigt hat.</span><span class="sxs-lookup"><span data-stu-id="7e0f4-125">Indicates whether the control has displayed a horizontal scroll bar.</span></span>

<span data-ttu-id="7e0f4-126">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7e0f4-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e0f4-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e0f4-127">Syntax</span></span>


```C++
HRESULT get_HorizontalScrollBarVisible(
  [out] BOOL *pfHScrollVisible
);
```



## <a name="property-value"></a><span data-ttu-id="7e0f4-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7e0f4-128">Property value</span></span>

<span data-ttu-id="7e0f4-129">Der Wert dieses Parameters ist **true** , wenn die horizontale Schiebe Leiste sichtbar ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="7e0f4-129">The value of this parameter is **TRUE** if the horizontal scroll bar is visible, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7e0f4-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="7e0f4-130">Error codes</span></span>

<span data-ttu-id="7e0f4-131">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7e0f4-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e0f4-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e0f4-132">Remarks</span></span>

<span data-ttu-id="7e0f4-133">Das-Steuerelement zeigt automatisch eine horizontale Schiebe Leiste an, wenn die Breite des-Steuer Elements kleiner als die Desktop Breite ist.</span><span class="sxs-lookup"><span data-stu-id="7e0f4-133">The control automatically displays a horizontal scroll bar if the width of the control is less than the desktop width.</span></span>

<span data-ttu-id="7e0f4-134">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7e0f4-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e0f4-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e0f4-135">Requirements</span></span>



| <span data-ttu-id="7e0f4-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e0f4-136">Requirement</span></span> | <span data-ttu-id="7e0f4-137">Wert</span><span class="sxs-lookup"><span data-stu-id="7e0f4-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e0f4-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e0f4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7e0f4-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e0f4-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7e0f4-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e0f4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7e0f4-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e0f4-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7e0f4-142">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7e0f4-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="7e0f4-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e0f4-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7e0f4-144">DLL</span><span class="sxs-lookup"><span data-stu-id="7e0f4-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e0f4-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e0f4-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7e0f4-146">IID</span><span class="sxs-lookup"><span data-stu-id="7e0f4-146">IID</span></span><br/>                      | <span data-ttu-id="7e0f4-147">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="7e0f4-147">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="7e0f4-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e0f4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e0f4-149">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="7e0f4-149">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="7e0f4-150">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="7e0f4-150">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="7e0f4-151">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="7e0f4-151">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="7e0f4-152">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="7e0f4-152">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="7e0f4-153">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="7e0f4-153">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="7e0f4-154">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="7e0f4-154">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="7e0f4-155">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="7e0f4-155">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="7e0f4-156">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="7e0f4-156">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="7e0f4-157">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="7e0f4-157">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="7e0f4-158">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="7e0f4-158">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="7e0f4-159">**Verticalscrollbarvisible**</span><span class="sxs-lookup"><span data-stu-id="7e0f4-159">**VerticalScrollBarVisible**</span></span>](imstscax-verticalscrollbarvisible.md)
</dt> </dl>

 

 





