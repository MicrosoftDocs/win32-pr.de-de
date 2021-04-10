---
title: IMsRdpClient5 msrdpclientshell (Eigenschaft)
description: Ruft die Skript fähige-Client Einstellungs Schnittstelle imsrdpclientshell ab.
ms.assetid: cc56cec4-779d-4b51-8e94-ae0dd9bae997
ms.tgt_platform: multiple
keywords:
- Msrdpclientshell-Eigenschaft Remotedesktopdienste
- Msrdpclientshell-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, msrdpclientshell (Eigenschaft)
- Msrdpclientshell-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, msrdpclientshell (Eigenschaft)
- Msrdpclientshell-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, msrdpclientshell (Eigenschaft)
- Msrdpclientshell-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, msrdpclientshell (Eigenschaft)
- Msrdpclientshell-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, msrdpclientshell (Eigenschaft)
- Msrdpclientshell-Eigenschaft Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10 Interface Remotedesktopdienste, msrdpclientshell (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClient5.MsRdpClientShell
- IMsRdpClient5.get_MsRdpClientShell
- IMsRdpClient6.MsRdpClientShell
- IMsRdpClient6.get_MsRdpClientShell
- IMsRdpClient7.MsRdpClientShell
- IMsRdpClient7.get_MsRdpClientShell
- IMsRdpClient8.MsRdpClientShell
- IMsRdpClient8.get_MsRdpClientShell
- IMsRdpClient9.MsRdpClientShell
- IMsRdpClient9.get_MsRdpClientShell
- IMsRdpClient10.MsRdpClientShell
- IMsRdpClient10.get_MsRdpClientShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46129dc4736b50e8b6a650cc7a59f9b238da56e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106178"
---
# <a name="imsrdpclient5msrdpclientshell-property"></a><span data-ttu-id="2cc8a-116">IMsRdpClient5:: msrdpclientshell (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2cc8a-116">IMsRdpClient5::MsRdpClientShell property</span></span>

<span data-ttu-id="2cc8a-117">Ruft die Skript fähige-Client Einstellungs Schnittstelle [**imsrdpclientshell**](imsrdpclientshell.md)ab.</span><span class="sxs-lookup"><span data-stu-id="2cc8a-117">Retrieves the scriptable client setting interface [**IMsRdpClientShell**](imsrdpclientshell.md).</span></span>

<span data-ttu-id="2cc8a-118">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2cc8a-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cc8a-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cc8a-119">Syntax</span></span>


```C++
HRESULT get_MsRdpClientShell(
  [out] IMsRdpClientShell **ppLauncher
);
```



## <a name="property-value"></a><span data-ttu-id="2cc8a-120">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2cc8a-120">Property value</span></span>

<span data-ttu-id="2cc8a-121">Ein [**imsrdpclientshell**](imsrdpclientshell.md) -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="2cc8a-121">An [**IMsRdpClientShell**](imsrdpclientshell.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cc8a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2cc8a-122">Requirements</span></span>



| <span data-ttu-id="2cc8a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2cc8a-123">Requirement</span></span> | <span data-ttu-id="2cc8a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2cc8a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc8a-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2cc8a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2cc8a-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2cc8a-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2cc8a-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2cc8a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2cc8a-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2cc8a-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2cc8a-129">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2cc8a-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="2cc8a-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cc8a-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2cc8a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2cc8a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cc8a-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cc8a-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2cc8a-133">IID</span><span class="sxs-lookup"><span data-stu-id="2cc8a-133">IID</span></span><br/>                      | <span data-ttu-id="2cc8a-134">IID \_ IMsRdpClient5 ist als 4eb5335b-6429-477d-B922-e06a28ecd8bf definiert.</span><span class="sxs-lookup"><span data-stu-id="2cc8a-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2cc8a-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cc8a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cc8a-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="2cc8a-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="2cc8a-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="2cc8a-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="2cc8a-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="2cc8a-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="2cc8a-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="2cc8a-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="2cc8a-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="2cc8a-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="2cc8a-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="2cc8a-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





