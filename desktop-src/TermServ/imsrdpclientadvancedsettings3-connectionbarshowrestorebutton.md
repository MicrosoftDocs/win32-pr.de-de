---
title: IMsRdpClientAdvancedSettings3 connectionbarshowrestorebutton (Eigenschaft)
description: Gibt an, ob die Schaltfläche Wiederherstellen auf der Verbindungs Leiste angezeigt werden soll.
ms.assetid: a56c3c05-d253-404a-bf49-9c1d804802e0
ms.tgt_platform: multiple
keywords:
- Connectionbarshowrestorebutton-Eigenschaft Remotedesktopdienste
- Connectionbarshowrestorebutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, connectionbarshowrestorebutton-Eigenschaft
- Connectionbarshowrestorebutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, connectionbarshowrestorebutton-Eigenschaft
- Connectionbarshowrestorebutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, connectionbarshowrestorebutton-Eigenschaft
- Connectionbarshowrestorebutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, connectionbarshowrestorebutton-Eigenschaft
- Connectionbarshowrestorebutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, connectionbarshowrestorebutton-Eigenschaft
- Connectionbarshowrestorebutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, connectionbarshowrestorebutton-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings3.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings3.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowRestoreButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae83ecde31461eff9c553782b8bfa3ae760fb54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391602"
---
# <a name="imsrdpclientadvancedsettings3connectionbarshowrestorebutton-property"></a><span data-ttu-id="071a6-116">IMsRdpClientAdvancedSettings3:: connectionbarshowrestorebutton-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="071a6-116">IMsRdpClientAdvancedSettings3::ConnectionBarShowRestoreButton property</span></span>

<span data-ttu-id="071a6-117">Gibt an, ob die Schaltfläche **Wiederherstellen** auf der Verbindungs Leiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="071a6-117">Specifies whether to display the **Restore** button on the connection bar.</span></span>

<span data-ttu-id="071a6-118">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="071a6-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="071a6-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="071a6-119">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowRestoreButton(
  [in]  VARIANT_BOOL fShowRestore
);

HRESULT get_ConnectionBarShowRestoreButton(
  [out] VARIANT_BOOL *pfShowRestore
);
```



## <a name="property-value"></a><span data-ttu-id="071a6-120">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="071a6-120">Property value</span></span>

<span data-ttu-id="071a6-121">Legen Sie **auf Variant \_ true** fest, um die Schaltfläche **Wiederherstellen** anzuzeigen, und auf **Variant \_ false** , um die Anzeige der Schaltfläche **Wiederherstellen** zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="071a6-121">Set to **VARIANT\_TRUE** to display the **Restore** button, and to **VARIANT\_FALSE** to disable the display of the **Restore** button.</span></span>

## <a name="error-codes"></a><span data-ttu-id="071a6-122">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="071a6-122">Error codes</span></span>

<span data-ttu-id="071a6-123">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="071a6-123">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="071a6-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="071a6-124">Remarks</span></span>

<span data-ttu-id="071a6-125">Diese Eigenschaft kann nicht festgelegt werden, wenn das Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="071a6-125">This property cannot be set while the control is connected.</span></span>

<span data-ttu-id="071a6-126">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="071a6-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="071a6-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="071a6-127">Requirements</span></span>



| <span data-ttu-id="071a6-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="071a6-128">Requirement</span></span> | <span data-ttu-id="071a6-129">Wert</span><span class="sxs-lookup"><span data-stu-id="071a6-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="071a6-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="071a6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="071a6-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="071a6-131">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="071a6-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="071a6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="071a6-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="071a6-133">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="071a6-134">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="071a6-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="071a6-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="071a6-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="071a6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="071a6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="071a6-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="071a6-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="071a6-138">IID</span><span class="sxs-lookup"><span data-stu-id="071a6-138">IID</span></span><br/>                      | <span data-ttu-id="071a6-139">IID \_ IMsRdpClientAdvancedSettings3 ist als 19cd856b-c542-4c53-ACee-B127 e3be1a59 definiert.</span><span class="sxs-lookup"><span data-stu-id="071a6-139">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="071a6-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="071a6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="071a6-141">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="071a6-141">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="071a6-142">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="071a6-142">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="071a6-143">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="071a6-143">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="071a6-144">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="071a6-144">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="071a6-145">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="071a6-145">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="071a6-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="071a6-146">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> </dl>

 

 





