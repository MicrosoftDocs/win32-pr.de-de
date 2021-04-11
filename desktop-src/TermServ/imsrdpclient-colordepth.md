---
title: Imsrdpclient colortiefe-Eigenschaft
description: Die Farbtiefe (in Bits pro Pixel) für die Verbindung des-Steuer Elements.
ms.assetid: 9ba4d8fe-20cd-40e9-a71a-0dce0ddd29fc
ms.tgt_platform: multiple
keywords:
- Colortiefe-Eigenschaft Remotedesktopdienste
- Colortiefe-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, colortiefe-Eigenschaft
- Colortiefe-Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, colortiefe-Eigenschaft
- Colortiefe-Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, colortiefe-Eigenschaft
- Colortiefe-Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, colortiefe-Eigenschaft
- Colortiefe-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, colortiefe-Eigenschaft
- Colortiefe-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, colortiefe-Eigenschaft
- Colortiefe-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, colortiefe-Eigenschaft
- Colortiefe-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, colortiefe-Eigenschaft
- Colortiefe-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, colortiefe-Eigenschaft
- Colortiefe-Eigenschaft Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, colortiefe-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient.ColorDepth
- IMsRdpClient.get_ColorDepth
- IMsRdpClient.put_ColorDepth
- IMsRdpClient2.ColorDepth
- IMsRdpClient2.get_ColorDepth
- IMsRdpClient2.put_ColorDepth
- IMsRdpClient3.ColorDepth
- IMsRdpClient3.get_ColorDepth
- IMsRdpClient3.put_ColorDepth
- IMsRdpClient4.ColorDepth
- IMsRdpClient4.get_ColorDepth
- IMsRdpClient4.put_ColorDepth
- IMsRdpClient5.ColorDepth
- IMsRdpClient5.get_ColorDepth
- IMsRdpClient5.put_ColorDepth
- IMsRdpClient6.ColorDepth
- IMsRdpClient6.get_ColorDepth
- IMsRdpClient6.put_ColorDepth
- IMsRdpClient7.ColorDepth
- IMsRdpClient7.get_ColorDepth
- IMsRdpClient7.put_ColorDepth
- IMsRdpClient8.ColorDepth
- IMsRdpClient8.get_ColorDepth
- IMsRdpClient8.put_ColorDepth
- IMsRdpClient9.ColorDepth
- IMsRdpClient9.get_ColorDepth
- IMsRdpClient9.put_ColorDepth
- IMsRdpClient10.ColorDepth
- IMsRdpClient10.get_ColorDepth
- IMsRdpClient10.put_ColorDepth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5099deff3913d23173a466245cbf08fd5b95a6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105878"
---
# <a name="imsrdpclientcolordepth-property"></a><span data-ttu-id="066fd-124">Imsrdpclient:: colortiefe-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="066fd-124">IMsRdpClient::ColorDepth property</span></span>

<span data-ttu-id="066fd-125">Die Farbtiefe (in Bits pro Pixel) für die Verbindung des-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="066fd-125">The color depth (in bits per pixel) for the control's connection.</span></span>

<span data-ttu-id="066fd-126">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="066fd-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="066fd-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="066fd-127">Syntax</span></span>


```C++
HRESULT put_ColorDepth(
  [in]  LONG colorDepth
);

HRESULT get_ColorDepth(
  [out] LONG pcolorDepth
);
```



## <a name="property-value"></a><span data-ttu-id="066fd-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="066fd-128">Property value</span></span>

<span data-ttu-id="066fd-129">Die Farbtiefe.</span><span class="sxs-lookup"><span data-stu-id="066fd-129">The color depth.</span></span> <span data-ttu-id="066fd-130">Die Werte umfassen 8, 15, 16, 24 und 32 Bits pro Pixel.</span><span class="sxs-lookup"><span data-stu-id="066fd-130">Values include 8, 15, 16, 24, and 32 bits per pixel.</span></span>

## <a name="error-codes"></a><span data-ttu-id="066fd-131">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="066fd-131">Error codes</span></span>

<span data-ttu-id="066fd-132">Wenn die Methoden erfolgreich sind, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="066fd-132">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="066fd-133">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="066fd-133">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="066fd-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="066fd-134">Remarks</span></span>

<span data-ttu-id="066fd-135">Diese Eigenschaft kann nicht festgelegt werden, wenn das Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="066fd-135">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="066fd-136">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="066fd-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="066fd-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="066fd-137">Requirements</span></span>



| <span data-ttu-id="066fd-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="066fd-138">Requirement</span></span> | <span data-ttu-id="066fd-139">Wert</span><span class="sxs-lookup"><span data-stu-id="066fd-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="066fd-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="066fd-140">Minimum supported client</span></span><br/> | <span data-ttu-id="066fd-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="066fd-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="066fd-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="066fd-142">Minimum supported server</span></span><br/> | <span data-ttu-id="066fd-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="066fd-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="066fd-144">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="066fd-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="066fd-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="066fd-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="066fd-146">DLL</span><span class="sxs-lookup"><span data-stu-id="066fd-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="066fd-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="066fd-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="066fd-148">IID</span><span class="sxs-lookup"><span data-stu-id="066fd-148">IID</span></span><br/>                      | <span data-ttu-id="066fd-149">IID \_ imsrdpclient ist als 92b4a539-7115-4b7c-a5a9-e5d9efc2780a definiert.</span><span class="sxs-lookup"><span data-stu-id="066fd-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="066fd-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="066fd-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="066fd-151">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="066fd-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="066fd-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="066fd-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="066fd-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="066fd-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="066fd-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="066fd-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="066fd-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="066fd-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="066fd-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="066fd-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="066fd-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="066fd-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="066fd-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="066fd-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="066fd-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="066fd-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="066fd-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="066fd-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





