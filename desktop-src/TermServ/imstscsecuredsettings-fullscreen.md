---
title: Imstscsecuredsettings-FullScreen-Eigenschaft
description: Gibt den voll Bild Zustand des Client Steuer Elements an.
ms.assetid: f65c2fa3-b2d0-4e64-bf1e-08394c91eda8
ms.tgt_platform: multiple
keywords:
- Voll Bildeigenschaften Remotedesktopdienste
- Voll Bildeigenschaften Remotedesktopdienste, imstscsecuredsettings-Schnittstelle
- Imstscsecuredsettings-Schnittstelle Remotedesktopdienste, FullScreen-Eigenschaft
- Voll Bildeigenschaften Remotedesktopdienste, imsrdpclientsecuredsettings-Schnittstelle
- Imsrdpclientsecuredsettings-Schnittstelle Remotedesktopdienste, FullScreen-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.Fullscreen
- IMsTscSecuredSettings.get_Fullscreen
- IMsTscSecuredSettings.put_Fullscreen
- IMsRdpClientSecuredSettings.Fullscreen
- IMsRdpClientSecuredSettings.get_Fullscreen
- IMsRdpClientSecuredSettings.put_Fullscreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c3b3208edf3476fcd110d7729d97d9817cb929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341028"
---
# <a name="imstscsecuredsettingsfullscreen-property"></a><span data-ttu-id="64e43-108">Imstscsecuredsettings:: FullScreen-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="64e43-108">IMsTscSecuredSettings::Fullscreen property</span></span>

<span data-ttu-id="64e43-109">Gibt den voll Bild Zustand des Client Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="64e43-109">Specifies the full-screen state of the client control.</span></span>

<span data-ttu-id="64e43-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="64e43-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="64e43-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="64e43-111">Syntax</span></span>


```C++
HRESULT put_Fullscreen(
  [in]  BOOL fFullScreen
);

HRESULT get_Fullscreen(
  [out] BOOL *pfFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="64e43-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="64e43-112">Property value</span></span>

<span data-ttu-id="64e43-113">Legen Sie diesen Parameter auf **true** fest, wenn das Steuerelement den Vollbildmodus verwenden soll, und andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="64e43-113">Set this parameter to **TRUE** if the control should use full-screen mode and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="64e43-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="64e43-114">Error codes</span></span>

<span data-ttu-id="64e43-115">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="64e43-115">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="64e43-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64e43-116">Remarks</span></span>

<span data-ttu-id="64e43-117">Weitere Informationen zu dieser Methode finden Sie unter [Bereitstellen von RDP-Client Sicherheit](providing-for-rdp-client-security.md).</span><span class="sxs-lookup"><span data-stu-id="64e43-117">For more information about this method, see [Providing for RDP Client Security](providing-for-rdp-client-security.md).</span></span>

<span data-ttu-id="64e43-118">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="64e43-118">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

<span data-ttu-id="64e43-119">Beachten Sie Folgendes: Obwohl die Verwendung dieser Eigenschaft auf die zulässigen Internet Explorer-URL-Sicherheitszonen beschränkt ist, kann ein Benutzer jederzeit in den Vollbildmodus wechseln, nachdem die Verbindung hergestellt wurde, indem er die [Tasten](terminal-services-shortcut-keys.md) Kombination für den Vollbildmodus gedrückt hat (Strg + Alt + untbuggung).</span><span class="sxs-lookup"><span data-stu-id="64e43-119">Note that although the use of this property is restricted to the allowed Internet Explorer URL security zones, a user can always change to full-screen mode after the connection has been established by pressing the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

<span data-ttu-id="64e43-120">Diese Methode kann aufgerufen werden, während die Client Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="64e43-120">This method can be called while the client connection is established.</span></span>

<span data-ttu-id="64e43-121">Sie müssen die [**IMsRdpClientNonScriptable3::p UT \_ connectionbartext**](imsrdpclientnonscriptable3-connectionbartext.md) -Methode anrufen, bevor Sie die **imstscsecuredsettings::p UT- \_ voll Bild** Methode oder die [**imsrdpclient::p UT- \_ voll Bild**](imsrdpclient-fullscreen.md) Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="64e43-121">You must call the [**IMsRdpClientNonScriptable3::put\_ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) method before you call the **IMsTscSecuredSettings::put\_Fullscreen** method or the [**IMsRdpClient::put\_Fullscreen**](imsrdpclient-fullscreen.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="64e43-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64e43-122">Requirements</span></span>



| <span data-ttu-id="64e43-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64e43-123">Requirement</span></span> | <span data-ttu-id="64e43-124">Wert</span><span class="sxs-lookup"><span data-stu-id="64e43-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="64e43-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64e43-125">Minimum supported client</span></span><br/> | <span data-ttu-id="64e43-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64e43-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="64e43-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64e43-127">Minimum supported server</span></span><br/> | <span data-ttu-id="64e43-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64e43-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="64e43-129">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="64e43-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="64e43-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64e43-130"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="64e43-131">DLL</span><span class="sxs-lookup"><span data-stu-id="64e43-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64e43-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64e43-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="64e43-133">IID</span><span class="sxs-lookup"><span data-stu-id="64e43-133">IID</span></span><br/>                      | <span data-ttu-id="64e43-134">IID \_ imstscsecuredsettings ist als c9d65442-a0f9-45b2-8f73-d61d2db8cbb6 definiert.</span><span class="sxs-lookup"><span data-stu-id="64e43-134">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="64e43-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64e43-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64e43-136">**Imsrdpclientsecuredsettings**</span><span class="sxs-lookup"><span data-stu-id="64e43-136">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="64e43-137">**Imstscsecuredsettings**</span><span class="sxs-lookup"><span data-stu-id="64e43-137">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





