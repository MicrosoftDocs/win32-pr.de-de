---
title: Imsrdpclient-FullScreen-Eigenschaft
description: Bestimmt, ob sich das Client Steuerelement im Vollbildmodus befindet.
ms.assetid: 64fe2835-c00e-4d21-812d-dcf160147d93
ms.tgt_platform: multiple
keywords:
- Voll Bildeigenschaften Remotedesktopdienste
- Voll Bildeigenschaften Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, FullScreen-Eigenschaft
- Voll Bildeigenschaften Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, FullScreen-Eigenschaft
- Voll Bildeigenschaften Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, FullScreen-Eigenschaft
- Voll Bildeigenschaften Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, FullScreen-Eigenschaft
- Voll Bildeigenschaften Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, FullScreen-Eigenschaft
- Voll Bildeigenschaften Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, FullScreen-Eigenschaft
- Voll Bildeigenschaften Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, FullScreen-Eigenschaft
- Voll Bildeigenschaften Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, FullScreen-Eigenschaft
- Voll Bildeigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, FullScreen-Eigenschaft
- Voll Bildeigenschaften Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, FullScreen-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient.FullScreen
- IMsRdpClient.get_FullScreen
- IMsRdpClient.put_FullScreen
- IMsRdpClient2.FullScreen
- IMsRdpClient2.get_FullScreen
- IMsRdpClient2.put_FullScreen
- IMsRdpClient3.FullScreen
- IMsRdpClient3.get_FullScreen
- IMsRdpClient3.put_FullScreen
- IMsRdpClient4.FullScreen
- IMsRdpClient4.get_FullScreen
- IMsRdpClient4.put_FullScreen
- IMsRdpClient5.FullScreen
- IMsRdpClient5.get_FullScreen
- IMsRdpClient5.put_FullScreen
- IMsRdpClient6.FullScreen
- IMsRdpClient6.get_FullScreen
- IMsRdpClient6.put_FullScreen
- IMsRdpClient7.FullScreen
- IMsRdpClient7.get_FullScreen
- IMsRdpClient7.put_FullScreen
- IMsRdpClient8.FullScreen
- IMsRdpClient8.get_FullScreen
- IMsRdpClient8.put_FullScreen
- IMsRdpClient9.FullScreen
- IMsRdpClient9.get_FullScreen
- IMsRdpClient9.put_FullScreen
- IMsRdpClient10.FullScreen
- IMsRdpClient10.get_FullScreen
- IMsRdpClient10.put_FullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adbc8e11d2cc4fb4a8071372777a01d81b5edad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105873"
---
# <a name="imsrdpclientfullscreen-property"></a><span data-ttu-id="4f9a4-124">Imsrdpclient:: FullScreen-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4f9a4-124">IMsRdpClient::FullScreen property</span></span>

<span data-ttu-id="4f9a4-125">Bestimmt, ob sich das Client Steuerelement im Vollbildmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-125">Determines whether the client control is in full-screen mode.</span></span>

<span data-ttu-id="4f9a4-126">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f9a4-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f9a4-127">Syntax</span></span>


```C++
HRESULT put_FullScreen(
  [in]  VARIANT_BOOL fFullScreen
);

HRESULT get_FullScreen(
  [out] VARIANT_BOOL *pfFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="4f9a4-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4f9a4-128">Property value</span></span>

<span data-ttu-id="4f9a4-129">**True** , um in den Vollbildmodus zu wechseln, **false** , um den Vollbildmodus zu verlassen und zum Fenstermodus zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-129">**True** to enter full-screen mode, **False** to leave full-screen mode and return to window mode.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4f9a4-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="4f9a4-130">Error codes</span></span>

<span data-ttu-id="4f9a4-131">Wenn die Methoden erfolgreich sind, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-131">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="4f9a4-132">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-132">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f9a4-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f9a4-133">Remarks</span></span>

<span data-ttu-id="4f9a4-134">Sie können diese Eigenschaft festlegen, wenn das Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-134">You can set this property when the control is connected.</span></span>

<span data-ttu-id="4f9a4-135">Sie müssen die [**IMsRdpClientNonScriptable3::p UT \_ connectionbartext**](imsrdpclientnonscriptable3-connectionbartext.md) -Methode anrufen, bevor Sie die [**imstscsecuredsettings::p UT- \_ voll Bild**](imstscsecuredsettings-fullscreen.md) Methode oder die **imsrdpclient::p UT- \_ voll Bild** Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-135">You must call the [**IMsRdpClientNonScriptable3::put\_ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) method before you call the [**IMsTscSecuredSettings::put\_Fullscreen**](imstscsecuredsettings-fullscreen.md) method or the **IMsRdpClient::put\_Fullscreen** method.</span></span>

<span data-ttu-id="4f9a4-136">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4f9a4-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f9a4-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f9a4-137">Requirements</span></span>



| <span data-ttu-id="4f9a4-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f9a4-138">Requirement</span></span> | <span data-ttu-id="4f9a4-139">Wert</span><span class="sxs-lookup"><span data-stu-id="4f9a4-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f9a4-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f9a4-140">Minimum supported client</span></span><br/> | <span data-ttu-id="4f9a4-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f9a4-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4f9a4-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f9a4-142">Minimum supported server</span></span><br/> | <span data-ttu-id="4f9a4-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f9a4-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4f9a4-144">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="4f9a4-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="4f9a4-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f9a4-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4f9a4-146">DLL</span><span class="sxs-lookup"><span data-stu-id="4f9a4-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f9a4-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f9a4-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4f9a4-148">IID</span><span class="sxs-lookup"><span data-stu-id="4f9a4-148">IID</span></span><br/>                      | <span data-ttu-id="4f9a4-149">IID \_ imsrdpclient ist als 92b4a539-7115-4b7c-a5a9-e5d9efc2780a definiert.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="4f9a4-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f9a4-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f9a4-151">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="4f9a4-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="4f9a4-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="4f9a4-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="4f9a4-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="4f9a4-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="4f9a4-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="4f9a4-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="4f9a4-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="4f9a4-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="4f9a4-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="4f9a4-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="4f9a4-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="4f9a4-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="4f9a4-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="4f9a4-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="4f9a4-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="4f9a4-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="4f9a4-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="4f9a4-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





