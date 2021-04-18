---
title: IMsRdpClientNonScriptable3 warnaboutsending-Anmelde Informationen (Eigenschaft)
description: Gibt an oder Ruft ab, ob das Dialogfeld Sicherheitswarnung eine Warnung zum Senden von Anmelde Informationen an den Remote Server enthalten soll, bevor eine Sitzung gestartet wird.
ms.assetid: b97baef5-4a51-4e5c-bd53-10cff175533c
ms.tgt_platform: multiple
keywords:
- Eigenschaften Remotedesktopdienste warnaboutsending-Anmelde Informationen
- Warnaboutsendinganmelde-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3 Interface Remotedesktopdienste, warnaboutsending-Anmelde Informationen (Eigenschaft)
- Warnaboutsendinganmelde-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, warnaboutsending-Anmelde Informationen (Eigenschaft)
- Warnaboutsendinganmelde-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, warnaboutsending-Anmelde Informationen (Eigenschaft)
- Warnaboutsendinganmelde-Eigenschaft Remotedesktopdienste, MsRdpClient5-Objekt
- MsRdpClient5-Objekt Remotedesktopdienste, warnaboutsending-Anmelde Informationen (Eigenschaft)
- Warnaboutsendinganmelde-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, warnaboutsending-Anmelde Informationen (Eigenschaft)
- Warnaboutsendinganmelde-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, warnaboutsending-Anmelde Informationen (Eigenschaft)
- Warnaboutsendinganmelde-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, warnaboutsending-Anmelde Informationen (Eigenschaft)
- Warnaboutsendinganmelde-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, warnaboutsending-Anmelde Informationen (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.put_WarnAboutSendingCredentials
- MsRdpClient5.WarnAboutSendingCredentials
- MsRdpClient6.WarnAboutSendingCredentials
- MsRdpClient7.WarnAboutSendingCredentials
- MsRdpClient8.WarnAboutSendingCredentials
- MsRdpClient9.WarnAboutSendingCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d9d2fcfe158f5a0bb6812002bfcc160f1c9009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339549"
---
# <a name="imsrdpclientnonscriptable3warnaboutsendingcredentials-property"></a><span data-ttu-id="6dd28-120">IMsRdpClientNonScriptable3:: warnaboutsendinganmeldeinformationen (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6dd28-120">IMsRdpClientNonScriptable3::WarnAboutSendingCredentials property</span></span>

<span data-ttu-id="6dd28-121">Gibt an oder Ruft ab, ob das Dialogfeld Sicherheitswarnung eine Warnung zum Senden von Anmelde Informationen an den Remote Server enthalten soll, bevor eine Sitzung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="6dd28-121">Specifies or retrieves whether the security warning dialog box should include a warning about sending credentials to the remote server before starting a session.</span></span>

<span data-ttu-id="6dd28-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6dd28-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dd28-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="6dd28-123">Syntax</span></span>


```C++
HRESULT put_WarnAboutSendingCredentials(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutSendingCredentials(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="6dd28-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6dd28-124">Property value</span></span>

<span data-ttu-id="6dd28-125">Gibt an, ob das Dialogfeld Sicherheitswarnung eine Warnung zum Senden von Anmelde Informationen an den Remote Server enthalten soll, bevor eine Sitzung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="6dd28-125">Specifies whether the security warning dialog box should include a warning about sending credentials to the remote server before starting a session.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dd28-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6dd28-126">Requirements</span></span>



| <span data-ttu-id="6dd28-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6dd28-127">Requirement</span></span> | <span data-ttu-id="6dd28-128">Wert</span><span class="sxs-lookup"><span data-stu-id="6dd28-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dd28-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6dd28-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6dd28-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6dd28-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="6dd28-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6dd28-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6dd28-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6dd28-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="6dd28-133">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6dd28-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="6dd28-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6dd28-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="6dd28-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6dd28-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dd28-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6dd28-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="6dd28-137">IID</span><span class="sxs-lookup"><span data-stu-id="6dd28-137">IID</span></span><br/>                      | <span data-ttu-id="6dd28-138">IID \_ IMsRdpClientNonScriptable3 ist als b3378d90-0728-45c7-8ed7-b6159fb92219 definiert.</span><span class="sxs-lookup"><span data-stu-id="6dd28-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6dd28-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6dd28-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dd28-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="6dd28-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="6dd28-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="6dd28-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="6dd28-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="6dd28-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





