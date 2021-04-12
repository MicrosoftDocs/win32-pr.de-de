---
title: IMsRdpClientNonScriptable4 markrdpsettingssecure (Eigenschaft)
description: Gibt an, ob die Einstellungen für Remotedesktopprotokoll (RDP) als sicher gekennzeichnet sind.
ms.assetid: 04b419ed-821e-43e0-ac76-b8d6f6dfcc30
ms.tgt_platform: multiple
keywords:
- Markrdpsettingssecure-Eigenschaft Remotedesktopdienste
- Markrdpsettingssecure-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, markrdpsettingssecure (Eigenschaft)
- Markrdpsettingssecure-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, markrdpsettingssecure (Eigenschaft)
- Markrdpsettingssecure-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, markrdpsettingssecure-Eigenschaft
- Markrdpsettingssecure-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, markrdpsettingssecure-Eigenschaft
- Markrdpsettingssecure-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, markrdpsettingssecure-Eigenschaft
- Markrdpsettingssecure-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, markrdpsettingssecure-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.MarkRdpSettingsSecure
- IMsRdpClientNonScriptable4.get_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable4.put_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.get_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.put_MarkRdpSettingsSecure
- MsRdpClient6.MarkRdpSettingsSecure
- MsRdpClient7.MarkRdpSettingsSecure
- MsRdpClient8.MarkRdpSettingsSecure
- MsRdpClient9.MarkRdpSettingsSecure
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b551e043432b6f6e66efbbe5a6e0f9095024a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518065"
---
# <a name="imsrdpclientnonscriptable4markrdpsettingssecure-property"></a><span data-ttu-id="400a4-116">IMsRdpClientNonScriptable4:: markrdpsettingssecure (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="400a4-116">IMsRdpClientNonScriptable4::MarkRdpSettingsSecure property</span></span>

<span data-ttu-id="400a4-117">Gibt an, ob die Einstellungen für [Remotedesktopprotokoll](remote-desktop-protocol.md) (RDP) als sicher gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="400a4-117">Specifies whether [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP) settings are marked as secure.</span></span> <span data-ttu-id="400a4-118">Dies gibt an, dass die auf das Steuerelement angewendeten Einstellungen von einem Drittanbieter oder einem vertrauenswürdigen Herausgeber signiert wurden.</span><span class="sxs-lookup"><span data-stu-id="400a4-118">This indicates that the settings applied to the control have been signed by a third-party or trusted publisher.</span></span>

<span data-ttu-id="400a4-119">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="400a4-119">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="400a4-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="400a4-120">Syntax</span></span>


```C++
HRESULT put_MarkRdpSettingsSecure(
  [in]  VARIANT_BOOL fRdpSecure
);

HRESULT get_MarkRdpSettingsSecure(
  [out] VARIANT_BOOL *pfRdpSecure
);
```



## <a name="property-value"></a><span data-ttu-id="400a4-121">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="400a4-121">Property value</span></span>

<span data-ttu-id="400a4-122">Legt fest, ob RDP-Einstellungen als sicher gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="400a4-122">Sets whether RDP settings are marked as secure.</span></span>

## <a name="error-codes"></a><span data-ttu-id="400a4-123">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="400a4-123">Error codes</span></span>

<span data-ttu-id="400a4-124">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="400a4-124">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="400a4-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="400a4-125">Requirements</span></span>



| <span data-ttu-id="400a4-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="400a4-126">Requirement</span></span> | <span data-ttu-id="400a4-127">Wert</span><span class="sxs-lookup"><span data-stu-id="400a4-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="400a4-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="400a4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="400a4-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="400a4-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="400a4-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="400a4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="400a4-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="400a4-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="400a4-132">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="400a4-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="400a4-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="400a4-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="400a4-134">DLL</span><span class="sxs-lookup"><span data-stu-id="400a4-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="400a4-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="400a4-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="400a4-136">IID</span><span class="sxs-lookup"><span data-stu-id="400a4-136">IID</span></span><br/>                      | <span data-ttu-id="400a4-137">IMsRdpClientNonScriptable4 ist als f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb definiert.</span><span class="sxs-lookup"><span data-stu-id="400a4-137">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="400a4-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="400a4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="400a4-139">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="400a4-139">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="400a4-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="400a4-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





