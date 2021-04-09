---
title: IMsRdpClientAdvancedSettings3 connectionbarshowminimizebutton (Eigenschaft)
description: Gibt an, ob die Schaltfläche Minimieren auf der Verbindungs Leiste angezeigt werden soll.
ms.assetid: 3ad89f25-f1ff-4bfc-ae86-09603058c9b5
ms.tgt_platform: multiple
keywords:
- Connectionbarshowminimizebutton-Eigenschaft Remotedesktopdienste
- Connectionbarshowminimizebutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, connectionbarshowminimizebutton-Eigenschaft
- Connectionbarshowminimizebutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, connectionbarshowminimizebutton-Eigenschaft
- Connectionbarshowminimizebutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, connectionbarshowminimizebutton-Eigenschaft
- Connectionbarshowminimizebutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, connectionbarshowminimizebutton-Eigenschaft
- Connectionbarshowminimizebutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, connectionbarshowminimizebutton-Eigenschaft
- Connectionbarshowminimizebutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, connectionbarshowminimizebutton-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings3.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings3.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowMinimizeButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc3cb600a853e4bc2dea7c693e676f992db85f48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740009"
---
# <a name="imsrdpclientadvancedsettings3connectionbarshowminimizebutton-property"></a><span data-ttu-id="9bf82-116">IMsRdpClientAdvancedSettings3:: connectionbarshowminimizebutton-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9bf82-116">IMsRdpClientAdvancedSettings3::ConnectionBarShowMinimizeButton property</span></span>

<span data-ttu-id="9bf82-117">Gibt an, ob die Schaltfläche **minimieren** auf der Verbindungs Leiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9bf82-117">Specifies whether to display the **Minimize** button on the connection bar.</span></span>

<span data-ttu-id="9bf82-118">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="9bf82-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bf82-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bf82-119">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowMinimizeButton(
  [in]  VARIANT_BOOL fShowMinimize
);

HRESULT get_ConnectionBarShowMinimizeButton(
  [out] VARIANT_BOOL *pfShowMinimize
);
```



## <a name="property-value"></a><span data-ttu-id="9bf82-120">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="9bf82-120">Property value</span></span>

<span data-ttu-id="9bf82-121">Legen Sie diesen Parameter **auf Variant \_ true** fest, um die Schaltfläche **minimieren** anzuzeigen, und auf **Variant \_ false** , um die Anzeige der Schaltfläche **minimieren** zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="9bf82-121">Set this parameter to **VARIANT\_TRUE** to display the **Minimize** button, and to **VARIANT\_FALSE** to disable the display of the **Minimize** button.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9bf82-122">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="9bf82-122">Error codes</span></span>

<span data-ttu-id="9bf82-123">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="9bf82-123">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bf82-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9bf82-124">Remarks</span></span>

<span data-ttu-id="9bf82-125">Diese Eigenschaft kann nicht festgelegt werden, wenn das Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="9bf82-125">This property cannot be set while the control is connected.</span></span>

<span data-ttu-id="9bf82-126">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9bf82-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9bf82-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9bf82-127">Requirements</span></span>



| <span data-ttu-id="9bf82-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9bf82-128">Requirement</span></span> | <span data-ttu-id="9bf82-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9bf82-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bf82-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9bf82-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9bf82-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9bf82-131">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="9bf82-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9bf82-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9bf82-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9bf82-133">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="9bf82-134">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9bf82-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="9bf82-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bf82-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="9bf82-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9bf82-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bf82-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bf82-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="9bf82-138">IID</span><span class="sxs-lookup"><span data-stu-id="9bf82-138">IID</span></span><br/>                      | <span data-ttu-id="9bf82-139">IID \_ IMsRdpClientAdvancedSettings3 ist als 19cd856b-c542-4c53-ACee-B127 e3be1a59 definiert.</span><span class="sxs-lookup"><span data-stu-id="9bf82-139">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9bf82-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9bf82-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bf82-141">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="9bf82-141">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="9bf82-142">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="9bf82-142">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="9bf82-143">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="9bf82-143">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="9bf82-144">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="9bf82-144">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="9bf82-145">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="9bf82-145">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="9bf82-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="9bf82-146">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> </dl>

 

 





