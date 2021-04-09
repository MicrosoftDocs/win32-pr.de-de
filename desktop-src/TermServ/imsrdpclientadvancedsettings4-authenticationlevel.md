---
title: IMsRdpClientAdvancedSettings4 AuthenticationLevel (Eigenschaft)
description: Gibt die Authentifizierungs Ebene an, die für die Verbindung verwendet werden soll.
ms.assetid: 09ff1508-f13d-4bb0-8458-6f5a5e099bae
ms.tgt_platform: multiple
keywords:
- AuthenticationLevel-Eigenschaft Remotedesktopdienste
- AuthenticationLevel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste, AuthenticationLevel-Eigenschaft
- AuthenticationLevel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste, AuthenticationLevel-Eigenschaft
- AuthenticationLevel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste, AuthenticationLevel-Eigenschaft
- AuthenticationLevel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste, AuthenticationLevel-Eigenschaft
- AuthenticationLevel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste, AuthenticationLevel-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings4.AuthenticationLevel
- IMsRdpClientAdvancedSettings4.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings4.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings5.AuthenticationLevel
- IMsRdpClientAdvancedSettings5.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings5.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings6.AuthenticationLevel
- IMsRdpClientAdvancedSettings6.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings6.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings7.AuthenticationLevel
- IMsRdpClientAdvancedSettings7.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings7.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings8.AuthenticationLevel
- IMsRdpClientAdvancedSettings8.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings8.put_AuthenticationLevel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c748416650ec7e6ec3d26fe6236a254eb012d67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858842"
---
# <a name="imsrdpclientadvancedsettings4authenticationlevel-property"></a><span data-ttu-id="24783-114">IMsRdpClientAdvancedSettings4:: AuthenticationLevel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="24783-114">IMsRdpClientAdvancedSettings4::AuthenticationLevel property</span></span>

<span data-ttu-id="24783-115">Gibt die Authentifizierungs Ebene an, die für die Verbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="24783-115">Specifies the authentication level to use for the connection.</span></span>

<span data-ttu-id="24783-116">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="24783-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="24783-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="24783-117">Syntax</span></span>


```C++
HRESULT put_AuthenticationLevel(
  [in]  UINT uiAuthLevel
);

HRESULT get_AuthenticationLevel(
  [out] UINT *puiAuthLevel
);
```



## <a name="property-value"></a><span data-ttu-id="24783-118">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="24783-118">Property value</span></span>

<span data-ttu-id="24783-119">Der Wert der **AuthenticationLevel** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="24783-119">The value of the **AuthenticationLevel** property.</span></span>

<dt>

<span data-ttu-id="24783-120">0</span><span class="sxs-lookup"><span data-stu-id="24783-120">0</span></span>
</dt> <dd>

<span data-ttu-id="24783-121">Keine Authentifizierung des Servers.</span><span class="sxs-lookup"><span data-stu-id="24783-121">No authentication of the server.</span></span>

</dd> <dt>

<span data-ttu-id="24783-122">1</span><span class="sxs-lookup"><span data-stu-id="24783-122">1</span></span>
</dt> <dd>

<span data-ttu-id="24783-123">Die Server Authentifizierung ist erforderlich und muss erfolgreich abgeschlossen werden, damit die Verbindung fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="24783-123">Server authentication is required and must complete successfully for the connection to proceed.</span></span>

</dd> <dt>

<span data-ttu-id="24783-124">2</span><span class="sxs-lookup"><span data-stu-id="24783-124">2</span></span>
</dt> <dd>

<span data-ttu-id="24783-125">Versuchen Sie, die Authentifizierung des Servers durchführen.</span><span class="sxs-lookup"><span data-stu-id="24783-125">Attempt authentication of the server.</span></span> <span data-ttu-id="24783-126">Wenn die Authentifizierung fehlschlägt, wird der Benutzer aufgefordert, die Verbindung abzubrechen oder ohne Server Authentifizierung fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="24783-126">If authentication fails, the user will be prompted with the option to cancel the connection or to proceed without server authentication.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="24783-127">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="24783-127">Error codes</span></span>

<span data-ttu-id="24783-128">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="24783-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="24783-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24783-129">Remarks</span></span>

<span data-ttu-id="24783-130">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="24783-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="24783-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24783-131">Requirements</span></span>



| <span data-ttu-id="24783-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24783-132">Requirement</span></span> | <span data-ttu-id="24783-133">Wert</span><span class="sxs-lookup"><span data-stu-id="24783-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24783-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="24783-134">Minimum supported client</span></span><br/> | <span data-ttu-id="24783-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24783-135">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="24783-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="24783-136">Minimum supported server</span></span><br/> | <span data-ttu-id="24783-137">Windows Server 2008, Windows Server 2008 mit SP1</span><span class="sxs-lookup"><span data-stu-id="24783-137">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                     |
| <span data-ttu-id="24783-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="24783-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="24783-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24783-139"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="24783-140">DLL</span><span class="sxs-lookup"><span data-stu-id="24783-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24783-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24783-141"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="24783-142">IID</span><span class="sxs-lookup"><span data-stu-id="24783-142">IID</span></span><br/>                      | <span data-ttu-id="24783-143">IID \_ IMsRdpClientAdvancedSettings4 ist als FBA7F64E-7345-4405-AE50-FA4A763DC0DE definiert.</span><span class="sxs-lookup"><span data-stu-id="24783-143">IID\_IMsRdpClientAdvancedSettings4 is defined as FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="24783-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24783-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24783-145">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="24783-145">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="24783-146">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="24783-146">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="24783-147">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="24783-147">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="24783-148">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="24783-148">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="24783-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="24783-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> </dl>

 

 





