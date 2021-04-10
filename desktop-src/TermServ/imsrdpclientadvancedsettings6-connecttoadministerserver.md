---
title: IMsRdpClientAdvancedSettings6 Connect-Administrator Server Eigenschaft
description: Ruft ab oder legt fest, ob das ActiveX-Steuerelement versuchen soll, eine Verbindung mit dem Server zu Verwaltungszwecken herzustellen.
ms.assetid: b98f9b9b-a3e7-4a3c-a7e3-e388ce53c5c9
ms.tgt_platform: multiple
keywords:
- Connect-Administrator Server-Eigenschaft Remotedesktopdienste
- ConnectRemotedesktopdienste Administration Server-Eigenschaft, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste, connecttadministration-Server Eigenschaft
- ConnectRemotedesktopdienste Administration Server-Eigenschaft, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste, connecttadministration-Server Eigenschaft
- ConnectRemotedesktopdienste Administration Server-Eigenschaft, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste, connecttadministration-Server Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.put_ConnectToAdministerServer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9cad8d50e2e0a4c1ec18fbd33733dc394101a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040614"
---
# <a name="imsrdpclientadvancedsettings6connecttoadministerserver-property"></a><span data-ttu-id="9c7df-110">IMsRdpClientAdvancedSettings6:: ConnectTo Administration Server-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9c7df-110">IMsRdpClientAdvancedSettings6::ConnectToAdministerServer property</span></span>

<span data-ttu-id="9c7df-111">Ruft ab oder legt fest, ob das ActiveX-Steuerelement versuchen soll, eine Verbindung mit dem Server zu Verwaltungszwecken herzustellen.</span><span class="sxs-lookup"><span data-stu-id="9c7df-111">Retrieves or specifies whether the ActiveX control should attempt to connect to the server for administrative purposes.</span></span>

<span data-ttu-id="9c7df-112">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="9c7df-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c7df-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c7df-113">Syntax</span></span>


```C++
HRESULT put_ConnectToAdministerServer(
  [in]  VARIANT_BOOL connectToAdministerServer
);

HRESULT get_ConnectToAdministerServer(
  [out] VARIANT_BOOL *pConnectToAdministerServer
);
```



## <a name="property-value"></a><span data-ttu-id="9c7df-114">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="9c7df-114">Property value</span></span>

<span data-ttu-id="9c7df-115">**Variant \_ TRUE** , wenn das ActiveX-Steuerelement versucht, zu Verwaltungszwecken eine Verbindung mit dem Server herzustellen. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="9c7df-115">**VARIANT\_TRUE** to cause the ActiveX control to attempt to connect to the server for administrative purposes; otherwise **VARIANT\_FALSE**.</span></span> <span data-ttu-id="9c7df-116">Der Standardwert ist **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="9c7df-116">The default value is **VARIANT\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c7df-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c7df-117">Remarks</span></span>

<span data-ttu-id="9c7df-118">Zum Verwenden von **connectdeadministration Server** muss Remotedesktopverbindung (RDC)-Client Version 6,1 oder höher ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9c7df-118">To use **ConnectToAdministerServer**, you must be running Remote Desktop Connection (RDC) client version 6.1 or later.</span></span>

> [!Note]  
> <span data-ttu-id="9c7df-119">Die RDC-Version 6,1 (6.0.6001) unterstützt Remotedesktopprotokoll 6,1.</span><span class="sxs-lookup"><span data-stu-id="9c7df-119">RDC version 6.1 (6.0.6001) supports Remote Desktop Protocol 6.1.</span></span> <span data-ttu-id="9c7df-120">RDC 6,1 ist in Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) enthalten.</span><span class="sxs-lookup"><span data-stu-id="9c7df-120">RDC 6.1 is included with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

 

<span data-ttu-id="9c7df-121">**Verbindungs Server Server** stellt eine Verbindung mit einer Sitzung her, die für administrative Zwecke auf dem Remote Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9c7df-121">**ConnectToAdministerServer** connects you to a session that is used for administrative purposes on the remote server.</span></span> <span data-ttu-id="9c7df-122">Wenn der Remotedesktop-Sitzungshost (RD-Sitzungshost)-Rollen Dienst auf dem Remote Server installiert ist, führt **connectdeadministration** folgende Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="9c7df-122">If the Remote Desktop Session Host (RD Session Host) role service is installed on the remote server, **ConnectToAdministerServer** does the following:</span></span>

-   <span data-ttu-id="9c7df-123">Deaktiviert die Remotedesktopdienste Client Zugriffs Lizenzierung für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="9c7df-123">Disables Remote Desktop Services client access licensing for the session.</span></span>
-   <span data-ttu-id="9c7df-124">Deaktiviert die Zeit Zonen Umleitung für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="9c7df-124">Disables time zone redirection for the session.</span></span>
-   <span data-ttu-id="9c7df-125">Deaktiviert die Umleitung von Remotedesktopverbindung Broker (RD-Verbindungsbroker) für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="9c7df-125">Disables Remote Desktop Connection Broker (RD Connection Broker) redirection for the session.</span></span>
-   <span data-ttu-id="9c7df-126">Deaktiviert Plug & Play Geräte Umleitung für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="9c7df-126">Disables Plug and Play device redirection for the session.</span></span>
-   <span data-ttu-id="9c7df-127">Ändert das Remote Sitzungs Design in Windows Classic für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="9c7df-127">Changes the remote session theme to Windows Classic for the session.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c7df-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c7df-128">Requirements</span></span>



| <span data-ttu-id="9c7df-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c7df-129">Requirement</span></span> | <span data-ttu-id="9c7df-130">Wert</span><span class="sxs-lookup"><span data-stu-id="9c7df-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c7df-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9c7df-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9c7df-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c7df-132">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="9c7df-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9c7df-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9c7df-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c7df-134">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="9c7df-135">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9c7df-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="9c7df-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c7df-136"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="9c7df-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9c7df-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c7df-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c7df-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="9c7df-139">IID</span><span class="sxs-lookup"><span data-stu-id="9c7df-139">IID</span></span><br/>                      | <span data-ttu-id="9c7df-140">IID \_ IMsRdpClientAdvancedSettings6 ist als 222c4b5d-45d9-4df0-a7c6-60cf9089d285 definiert.</span><span class="sxs-lookup"><span data-stu-id="9c7df-140">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9c7df-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c7df-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c7df-142">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="9c7df-142">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="9c7df-143">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="9c7df-143">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="9c7df-144">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="9c7df-144">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





