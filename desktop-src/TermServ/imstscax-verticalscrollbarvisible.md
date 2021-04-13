---
title: Imstscax verticalscrollbarvisible (Eigenschaft)
description: Gibt an, ob das Steuerelement eine vertikale Bild Lauf Leiste anzeigt.
ms.assetid: b31e2db3-b367-4900-a2c6-51fd794341c2
ms.tgt_platform: multiple
keywords:
- Verticalscrollbarvisible-Eigenschaft Remotedesktopdienste
- Verticalscrollbarvisible-Eigenschaft Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, verticalscrollbarvisible (Eigenschaft)
- Verticalscrollbarvisible-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, verticalscrollbarvisible (Eigenschaft)
- Verticalscrollbarvisible-Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, verticalscrollbarvisible (Eigenschaft)
- Verticalscrollbarvisible-Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, verticalscrollbarvisible (Eigenschaft)
- Verticalscrollbarvisible-Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, verticalscrollbarvisible (Eigenschaft)
- Verticalscrollbarvisible-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, verticalscrollbarvisible (Eigenschaft)
- Verticalscrollbarvisible-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, verticalscrollbarvisible (Eigenschaft)
- Verticalscrollbarvisible-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, verticalscrollbarvisible (Eigenschaft)
- Verticalscrollbarvisible-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, verticalscrollbarvisible (Eigenschaft)
- Verticalscrollbarvisible-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, verticalscrollbarvisible (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsTscAx.VerticalScrollBarVisible
- IMsTscAx.get_VerticalScrollBarVisible
- IMsRdpClient.VerticalScrollBarVisible
- IMsRdpClient.get_VerticalScrollBarVisible
- IMsRdpClient2.VerticalScrollBarVisible
- IMsRdpClient2.get_VerticalScrollBarVisible
- IMsRdpClient3.VerticalScrollBarVisible
- IMsRdpClient3.get_VerticalScrollBarVisible
- IMsRdpClient4.VerticalScrollBarVisible
- IMsRdpClient4.get_VerticalScrollBarVisible
- IMsRdpClient5.VerticalScrollBarVisible
- IMsRdpClient5.get_VerticalScrollBarVisible
- IMsRdpClient6.VerticalScrollBarVisible
- IMsRdpClient6.get_VerticalScrollBarVisible
- IMsRdpClient7.VerticalScrollBarVisible
- IMsRdpClient7.get_VerticalScrollBarVisible
- IMsRdpClient8.VerticalScrollBarVisible
- IMsRdpClient8.get_VerticalScrollBarVisible
- IMsRdpClient9.VerticalScrollBarVisible
- IMsRdpClient9.get_VerticalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1365a0ab6d4a1411d78496cf157f3bc49fe5db15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475777"
---
# <a name="imstscaxverticalscrollbarvisible-property"></a><span data-ttu-id="0582b-124">Imstscax:: verticalscrollbarvisible (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0582b-124">IMsTscAx::VerticalScrollBarVisible property</span></span>

<span data-ttu-id="0582b-125">Gibt an, ob das Steuerelement eine vertikale Bild Lauf Leiste anzeigt.</span><span class="sxs-lookup"><span data-stu-id="0582b-125">Indicates whether the control displays a vertical scroll bar.</span></span>

<span data-ttu-id="0582b-126">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0582b-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0582b-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="0582b-127">Syntax</span></span>


```C++
HRESULT get_VerticalScrollBarVisible(
  [out] BOOL *pfVScrollVisible
);
```



## <a name="property-value"></a><span data-ttu-id="0582b-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0582b-128">Property value</span></span>

<span data-ttu-id="0582b-129">Der Wert dieses Parameters ist **true** , wenn die vertikale Schiebe Leiste sichtbar ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="0582b-129">The value of this parameter is **TRUE** if the vertical scroll bar is visible, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0582b-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="0582b-130">Error codes</span></span>

<span data-ttu-id="0582b-131">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0582b-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0582b-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0582b-132">Remarks</span></span>

<span data-ttu-id="0582b-133">Das-Steuerelement zeigt automatisch eine vertikale Schiebe Leiste an, wenn die Höhe des aktuellen Steuer Elements kleiner ist als die Höhe des Desktops.</span><span class="sxs-lookup"><span data-stu-id="0582b-133">The control automatically displays a vertical scroll bar if the height of the current control is less than the height of the desktop.</span></span>

<span data-ttu-id="0582b-134">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0582b-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0582b-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0582b-135">Requirements</span></span>



| <span data-ttu-id="0582b-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0582b-136">Requirement</span></span> | <span data-ttu-id="0582b-137">Wert</span><span class="sxs-lookup"><span data-stu-id="0582b-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0582b-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0582b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0582b-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0582b-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0582b-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0582b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0582b-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0582b-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0582b-142">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="0582b-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="0582b-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0582b-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0582b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0582b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0582b-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0582b-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0582b-146">IID</span><span class="sxs-lookup"><span data-stu-id="0582b-146">IID</span></span><br/>                      | <span data-ttu-id="0582b-147">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="0582b-147">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="0582b-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0582b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0582b-149">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="0582b-149">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="0582b-150">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="0582b-150">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="0582b-151">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="0582b-151">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="0582b-152">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="0582b-152">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="0582b-153">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="0582b-153">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="0582b-154">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="0582b-154">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="0582b-155">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="0582b-155">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="0582b-156">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="0582b-156">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="0582b-157">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="0582b-157">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="0582b-158">**Horizontalscrollbarvisible**</span><span class="sxs-lookup"><span data-stu-id="0582b-158">**HorizontalScrollBarVisible**</span></span>](imstscax-horizontalscrollbarvisible.md)
</dt> <dt>

[<span data-ttu-id="0582b-159">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="0582b-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





