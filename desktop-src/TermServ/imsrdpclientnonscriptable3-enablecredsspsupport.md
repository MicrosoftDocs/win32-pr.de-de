---
title: IMsRdpClientNonScriptable3 enablekredsspsupport (Eigenschaft)
description: Gibt an oder Ruft ab, ob der Credential Security Service Provider (kredssp) für diese Verbindung aktiviert ist.
ms.assetid: 770da50b-2a93-4274-9b6f-c24c13f08549
ms.tgt_platform: multiple
keywords:
- Enablekredsspsupport-Eigenschaft Remotedesktopdienste
- Enablekredsspsupport-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3 Interface Remotedesktopdienste, enablekredsspsupport (Eigenschaft)
- Enablekredsspsupport-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, enablekredsspsupport (Eigenschaft)
- Enablekredsspsupport-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, enablekredsspsupport (Eigenschaft)
- Enablekredsspsupport-Eigenschaft Remotedesktopdienste, MsRdpClient5-Objekt
- MsRdpClient5-Objekt Remotedesktopdienste, enablekredsspsupport-Eigenschaft
- Enablekredsspsupport-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, enablekredsspsupport-Eigenschaft
- Enablekredsspsupport-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, enablekredsspsupport-Eigenschaft
- Enablekredsspsupport-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, enablekredsspsupport-Eigenschaft
- Enablekredsspsupport-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, enablekredsspsupport-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.EnableCredSspSupport
- IMsRdpClientNonScriptable3.get_EnableCredSspSupport
- IMsRdpClientNonScriptable3.put_EnableCredSspSupport
- IMsRdpClientNonScriptable4.EnableCredSspSupport
- IMsRdpClientNonScriptable4.get_EnableCredSspSupport
- IMsRdpClientNonScriptable4.put_EnableCredSspSupport
- IMsRdpClientNonScriptable5.EnableCredSspSupport
- IMsRdpClientNonScriptable5.get_EnableCredSspSupport
- IMsRdpClientNonScriptable5.put_EnableCredSspSupport
- MsRdpClient5.EnableCredSspSupport
- MsRdpClient6.EnableCredSspSupport
- MsRdpClient7.EnableCredSspSupport
- MsRdpClient8.EnableCredSspSupport
- MsRdpClient9.EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2330b800d15f95a7b59a01735de971dd4b212d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103534"
---
# <a name="imsrdpclientnonscriptable3enablecredsspsupport-property"></a><span data-ttu-id="7b6f8-120">IMsRdpClientNonScriptable3:: enablekredsspsupport (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7b6f8-120">IMsRdpClientNonScriptable3::EnableCredSspSupport property</span></span>

<span data-ttu-id="7b6f8-121">Gibt an oder Ruft ab, ob der Credential Security Service Provider (kredssp) für diese Verbindung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7b6f8-121">Specifies or retrieves whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span>

<span data-ttu-id="7b6f8-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7b6f8-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b6f8-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b6f8-123">Syntax</span></span>


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a><span data-ttu-id="7b6f8-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7b6f8-124">Property value</span></span>

<span data-ttu-id="7b6f8-125">Gibt an, ob "kredssp" für diese Verbindung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7b6f8-125">Specifies whether CredSSP is enabled for this connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b6f8-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b6f8-126">Requirements</span></span>



| <span data-ttu-id="7b6f8-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b6f8-127">Requirement</span></span> | <span data-ttu-id="7b6f8-128">Wert</span><span class="sxs-lookup"><span data-stu-id="7b6f8-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b6f8-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b6f8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7b6f8-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b6f8-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="7b6f8-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b6f8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7b6f8-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b6f8-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="7b6f8-133">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7b6f8-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="7b6f8-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b6f8-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="7b6f8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7b6f8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b6f8-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b6f8-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="7b6f8-137">IID</span><span class="sxs-lookup"><span data-stu-id="7b6f8-137">IID</span></span><br/>                      | <span data-ttu-id="7b6f8-138">IID \_ IMsRdpClientNonScriptable3 ist als b3378d90-0728-45c7-8ed7-b6159fb92219 definiert.</span><span class="sxs-lookup"><span data-stu-id="7b6f8-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b6f8-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b6f8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b6f8-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="7b6f8-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="7b6f8-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="7b6f8-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="7b6f8-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="7b6f8-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





