---
title: IMsRdpClientNonScriptable3 promptforanmelde-Eigenschaft (wuapi. h)
description: Gibt an oder Ruft ab, ob das Dialogfeld Eingabeaufforderung für Anmelde Informationen für die Verbindung aktiviert ist.
ms.assetid: 252ec5bd-bd52-40d4-ae48-b2c00c0720c0
ms.tgt_platform: multiple
keywords:
- Promptforanmelde-Eigenschaft Remotedesktopdienste
- Promptfor-Anmelde Informationen-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3 Interface Remotedesktopdienste, promptforanmeldeinformationen (Eigenschaft)
- Promptfor-Anmelde Informationen-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, promptforanmeldeinformationen (Eigenschaft)
- Promptfor-Anmelde Informationen-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, promptforanmeldeinformationen (Eigenschaft)
- Promptfor-Anmelde Informationen (Eigenschaft Remotedesktopdienste, MsRdpClient5-Objekt
- MsRdpClient5-Objekt Remotedesktopdienste, promptforanmeldeinformationen (Eigenschaft)
- Promptfor-Anmelde Informationen (Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, promptforanmeldeinformationen (Eigenschaft)
- Promptfor-Anmelde Informationen (Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, promptforanmeldeinformationen (Eigenschaft)
- Promptfor-Anmelde Informationen (Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, promptforanmeldeinformationen (Eigenschaft)
- Promptfor-Anmelde Informationen (Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, promptforanmeldeinformationen (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.PromptForCredentials
- IMsRdpClientNonScriptable3.get_PromptForCredentials
- IMsRdpClientNonScriptable3.put_PromptForCredentials
- IMsRdpClientNonScriptable4.PromptForCredentials
- IMsRdpClientNonScriptable4.get_PromptForCredentials
- IMsRdpClientNonScriptable4.put_PromptForCredentials
- IMsRdpClientNonScriptable5.PromptForCredentials
- IMsRdpClientNonScriptable5.get_PromptForCredentials
- IMsRdpClientNonScriptable5.put_PromptForCredentials
- MsRdpClient5.PromptForCredentials
- MsRdpClient6.PromptForCredentials
- MsRdpClient7.PromptForCredentials
- MsRdpClient8.PromptForCredentials
- MsRdpClient9.PromptForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62f913937c9a2ff01d4aabeaba48dcbdc8ddb21d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340368"
---
# <a name="imsrdpclientnonscriptable3promptforcredentials-property"></a><span data-ttu-id="dbf52-120">IMsRdpClientNonScriptable3::P romptforanmeldeinformationen (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dbf52-120">IMsRdpClientNonScriptable3::PromptForCredentials property</span></span>

<span data-ttu-id="dbf52-121">Gibt an oder Ruft ab, ob das Dialogfeld Eingabeaufforderung für Anmelde Informationen für die Verbindung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="dbf52-121">Specifies or retrieves whether the prompt for credentials dialog is enabled for the connection.</span></span>

<span data-ttu-id="dbf52-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="dbf52-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbf52-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbf52-123">Syntax</span></span>


```C++
HRESULT put_PromptForCredentials(
  [in]  VARIANT_BOOL fPrompt
);

HRESULT get_PromptForCredentials(
  [out] VARIANT_BOOL *pfPrompt
);
```



## <a name="property-value"></a><span data-ttu-id="dbf52-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="dbf52-124">Property value</span></span>

<span data-ttu-id="dbf52-125">Gibt an, ob das Dialogfeld zur Eingabe der Anmelde Informationen für die Verbindung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="dbf52-125">Specifies whether the prompt for credentials dialog is enabled for the connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dbf52-126">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="dbf52-126">Error codes</span></span>

## <a name="requirements"></a><span data-ttu-id="dbf52-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbf52-127">Requirements</span></span>



| <span data-ttu-id="dbf52-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbf52-128">Requirement</span></span> | <span data-ttu-id="dbf52-129">Wert</span><span class="sxs-lookup"><span data-stu-id="dbf52-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbf52-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dbf52-130">Minimum supported client</span></span><br/> | <span data-ttu-id="dbf52-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dbf52-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="dbf52-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dbf52-132">Minimum supported server</span></span><br/> | <span data-ttu-id="dbf52-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbf52-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="dbf52-134">Header</span><span class="sxs-lookup"><span data-stu-id="dbf52-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbf52-135"><dt>Wuapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbf52-135"><dt>Wuapi.h</dt></span></span> </dl>            |
| <span data-ttu-id="dbf52-136">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="dbf52-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="dbf52-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbf52-137"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="dbf52-138">DLL</span><span class="sxs-lookup"><span data-stu-id="dbf52-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbf52-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbf52-139"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="dbf52-140">IID</span><span class="sxs-lookup"><span data-stu-id="dbf52-140">IID</span></span><br/>                      | <span data-ttu-id="dbf52-141">IID \_ IMsRdpClientNonScriptable3 ist als b3378d90-0728-45c7-8ed7-b6159fb92219 definiert.</span><span class="sxs-lookup"><span data-stu-id="dbf52-141">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dbf52-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbf52-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbf52-143">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="dbf52-143">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="dbf52-144">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="dbf52-144">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="dbf52-145">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="dbf52-145">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





