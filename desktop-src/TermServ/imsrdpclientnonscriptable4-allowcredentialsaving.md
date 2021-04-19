---
title: IMsRdpClientNonScriptable4 allowkredentialsave (Eigenschaft)
description: Gibt an, ob im Dialogfeld Anmelde Informationen ein Kontrollkästchen angezeigt wird, das das Speichern von Anmelde Informationen ermöglicht.
ms.assetid: c5148ff0-0d7f-413d-b2a8-ff942668bee6
ms.tgt_platform: multiple
keywords:
- Allowkredentialsave-Eigenschaft Remotedesktopdienste
- Allowkredentialsave-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, allowkredentialsave (Eigenschaft)
- Allowkredentialsave-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, allowkredentialsave (Eigenschaft)
- Allowkredentialsave-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, allowkredentialsave (Eigenschaft)
- Allowkredentialsave-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, allowkredentialsave (Eigenschaft)
- Allowkredentialsave-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, allowkredentialsave (Eigenschaft)
- Allowkredentialsave-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, allowkredentialsave (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.AllowCredentialSaving
- IMsRdpClientNonScriptable4.get_AllowCredentialSaving
- IMsRdpClientNonScriptable4.put_AllowCredentialSaving
- IMsRdpClientNonScriptable5.AllowCredentialSaving
- IMsRdpClientNonScriptable5.get_AllowCredentialSaving
- IMsRdpClientNonScriptable5.put_AllowCredentialSaving
- MsRdpClient6.AllowCredentialSaving
- MsRdpClient7.AllowCredentialSaving
- MsRdpClient8.AllowCredentialSaving
- MsRdpClient9.AllowCredentialSaving
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 240e2eb8e80209ee5c90d63f2996231cf84bb2dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339340"
---
# <a name="imsrdpclientnonscriptable4allowcredentialsaving-property"></a><span data-ttu-id="e852a-116">IMsRdpClientNonScriptable4:: allowkredentialsave (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e852a-116">IMsRdpClientNonScriptable4::AllowCredentialSaving property</span></span>

<span data-ttu-id="e852a-117">Gibt an, ob im Dialogfeld Anmelde Informationen ein Kontrollkästchen angezeigt wird, das das Speichern von Anmelde Informationen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="e852a-117">Specifies whether the credentials dialog box displays a check box that enables the saving of credentials.</span></span>

<span data-ttu-id="e852a-118">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e852a-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e852a-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="e852a-119">Syntax</span></span>


```C++
HRESULT put_AllowCredentialSaving(
  [in]  VARIANT_BOOL fAllowSave
);

HRESULT get_AllowCredentialSaving(
  [out] VARIANT_BOOL *pfAllowSave
);
```



## <a name="property-value"></a><span data-ttu-id="e852a-120">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e852a-120">Property value</span></span>

<span data-ttu-id="e852a-121">Legt fest, ob im Dialogfeld Anmelde Informationen ein Kontrollkästchen angezeigt wird, das das Speichern von Anmelde Informationen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="e852a-121">Sets whether the credentials dialog box displays a check box that enables the saving of credentials.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e852a-122">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="e852a-122">Error codes</span></span>

<span data-ttu-id="e852a-123">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="e852a-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="e852a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e852a-124">Requirements</span></span>



| <span data-ttu-id="e852a-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e852a-125">Requirement</span></span> | <span data-ttu-id="e852a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e852a-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e852a-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e852a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e852a-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e852a-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="e852a-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e852a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e852a-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e852a-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e852a-131">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="e852a-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="e852a-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e852a-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="e852a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e852a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e852a-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e852a-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="e852a-135">IID</span><span class="sxs-lookup"><span data-stu-id="e852a-135">IID</span></span><br/>                      | <span data-ttu-id="e852a-136">IMsRdpClientNonScriptable4 ist als f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb definiert.</span><span class="sxs-lookup"><span data-stu-id="e852a-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e852a-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e852a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e852a-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="e852a-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="e852a-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="e852a-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





