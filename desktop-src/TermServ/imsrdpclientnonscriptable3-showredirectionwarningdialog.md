---
title: IMsRdpClientNonScriptable3 showredirectionwarningdialog (Eigenschaft)
description: Gibt an oder Ruft ab, ob das Dialogfeld für die Weiterleitungs Warnung angezeigt werden soll.
ms.assetid: 7ed37288-77c3-4551-a553-1ca679e1047a
ms.tgt_platform: multiple
keywords:
- Showredirectionwarningdialog-Eigenschaft Remotedesktopdienste
- Showredirectionwarningdialog-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3 Interface Remotedesktopdienste, showredirectionwarningdialog-Eigenschaft
- Showredirectionwarningdialog-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, showredirectionwarningdialog-Eigenschaft
- Showredirectionwarningdialog-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, showredirectionwarningdialog-Eigenschaft
- Showredirectionwarningdialog-Eigenschaft Remotedesktopdienste, MsRdpClient5-Objekt
- MsRdpClient5-Objekt Remotedesktopdienste, showredirectionwarningdialog-Eigenschaft
- Showredirectionwarningdialog-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, showredirectionwarningdialog-Eigenschaft
- Showredirectionwarningdialog-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, showredirectionwarningdialog-Eigenschaft
- Showredirectionwarningdialog-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, showredirectionwarningdialog-Eigenschaft
- Showredirectionwarningdialog-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, showredirectionwarningdialog-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable3.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable3.put_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.put_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.put_ShowRedirectionWarningDialog
- MsRdpClient5.ShowRedirectionWarningDialog
- MsRdpClient6.ShowRedirectionWarningDialog
- MsRdpClient7.ShowRedirectionWarningDialog
- MsRdpClient8.ShowRedirectionWarningDialog
- MsRdpClient9.ShowRedirectionWarningDialog
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 468e1721de3395067ca570c2051f3906df626071
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040330"
---
# <a name="imsrdpclientnonscriptable3showredirectionwarningdialog-property"></a><span data-ttu-id="45b5c-120">IMsRdpClientNonScriptable3:: showredirectionwarningdialog-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="45b5c-120">IMsRdpClientNonScriptable3::ShowRedirectionWarningDialog property</span></span>

<span data-ttu-id="45b5c-121">Gibt an oder Ruft ab, ob das Dialogfeld für die Weiterleitungs Warnung angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="45b5c-121">Specifies or retrieves whether the redirection warning dialog box should be shown.</span></span>

<span data-ttu-id="45b5c-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="45b5c-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="45b5c-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="45b5c-123">Syntax</span></span>


```C++
HRESULT put_ShowRedirectionWarningDialog(
  [in]  VARIANT_BOOL fShowRdrDlg
);

HRESULT get_ShowRedirectionWarningDialog(
  [out] VARIANT_BOOL *pfShowRdrDlg
);
```



## <a name="property-value"></a><span data-ttu-id="45b5c-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="45b5c-124">Property value</span></span>

<span data-ttu-id="45b5c-125">Gibt an, ob das Dialogfeld für die Weiterleitungs Warnung angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="45b5c-125">Specifies whether the redirection warning dialog box should be shown.</span></span>

## <a name="requirements"></a><span data-ttu-id="45b5c-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45b5c-126">Requirements</span></span>



| <span data-ttu-id="45b5c-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45b5c-127">Requirement</span></span> | <span data-ttu-id="45b5c-128">Wert</span><span class="sxs-lookup"><span data-stu-id="45b5c-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="45b5c-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="45b5c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="45b5c-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45b5c-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="45b5c-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="45b5c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="45b5c-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45b5c-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="45b5c-133">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="45b5c-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="45b5c-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45b5c-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="45b5c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="45b5c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45b5c-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45b5c-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="45b5c-137">IID</span><span class="sxs-lookup"><span data-stu-id="45b5c-137">IID</span></span><br/>                      | <span data-ttu-id="45b5c-138">IID \_ IMsRdpClientNonScriptable3 ist als b3378d90-0728-45c7-8ed7-b6159fb92219 definiert.</span><span class="sxs-lookup"><span data-stu-id="45b5c-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="45b5c-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45b5c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45b5c-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="45b5c-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="45b5c-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="45b5c-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="45b5c-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="45b5c-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





