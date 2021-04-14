---
title: IMsRdpClientNonScriptable4 promptforkredsonclient (Eigenschaft)
description: Gibt an, ob das Client Steuerelement ein Dialogfeld anzeigt, in dem Anmelde Informationen angefordert werden.
ms.assetid: 426676be-0150-4a33-acd0-26423966f32a
ms.tgt_platform: multiple
keywords:
- Promptforkredsonclient-Eigenschaft Remotedesktopdienste
- Promptforkredsonclient-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, promptforkredsonclient-Eigenschaft
- Promptforkredsonclient-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, promptforkredsonclient-Eigenschaft
- Promptforkredsonclient-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, promptforkredsonclient-Eigenschaft
- Promptforkredsonclient-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, promptforkredsonclient-Eigenschaft
- Promptforkredsonclient-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, promptforkredsonclient-Eigenschaft
- Promptforkredsonclient-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, promptforkredsonclient-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PromptForCredsOnClient
- IMsRdpClientNonScriptable4.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable4.put_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.PromptForCredsOnClient
- IMsRdpClientNonScriptable5.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.put_PromptForCredsOnClient
- MsRdpClient6.PromptForCredsOnClient
- MsRdpClient7.PromptForCredsOnClient
- MsRdpClient8.PromptForCredsOnClient
- MsRdpClient9.PromptForCredsOnClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6443c503e107bb2edb164a17beedddb1bbbc88a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392030"
---
# <a name="imsrdpclientnonscriptable4promptforcredsonclient-property"></a><span data-ttu-id="636b0-116">IMsRdpClientNonScriptable4::P romptforkredsonclient-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="636b0-116">IMsRdpClientNonScriptable4::PromptForCredsOnClient property</span></span>

<span data-ttu-id="636b0-117">Gibt an, ob das Client Steuerelement ein Dialogfeld anzeigt, in dem Anmelde Informationen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="636b0-117">Specifies whether the client control displays a dialog box that prompts for credentials.</span></span>

<span data-ttu-id="636b0-118">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="636b0-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="636b0-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="636b0-119">Syntax</span></span>


```C++
HRESULT put_PromptForCredsOnClient(
  [in]  VARIANT_BOOL fPromptForCredsOnClient
);

HRESULT get_PromptForCredsOnClient(
  [out] VARIANT_BOOL *pfPromptForCredsOnClient
);
```



## <a name="property-value"></a><span data-ttu-id="636b0-120">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="636b0-120">Property value</span></span>

<span data-ttu-id="636b0-121">Legt fest, ob das Client Steuerelement ein Dialogfeld anzeigt, in dem Anmelde Informationen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="636b0-121">Sets whether the client control displays a dialog box that prompts for credentials.</span></span>

## <a name="error-codes"></a><span data-ttu-id="636b0-122">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="636b0-122">Error codes</span></span>

<span data-ttu-id="636b0-123">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="636b0-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="636b0-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="636b0-124">Requirements</span></span>



| <span data-ttu-id="636b0-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="636b0-125">Requirement</span></span> | <span data-ttu-id="636b0-126">Wert</span><span class="sxs-lookup"><span data-stu-id="636b0-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="636b0-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="636b0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="636b0-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="636b0-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="636b0-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="636b0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="636b0-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="636b0-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="636b0-131">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="636b0-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="636b0-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="636b0-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="636b0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="636b0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="636b0-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="636b0-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="636b0-135">IID</span><span class="sxs-lookup"><span data-stu-id="636b0-135">IID</span></span><br/>                      | <span data-ttu-id="636b0-136">IMsRdpClientNonScriptable4 ist als f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb definiert.</span><span class="sxs-lookup"><span data-stu-id="636b0-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="636b0-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="636b0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="636b0-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="636b0-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="636b0-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="636b0-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





