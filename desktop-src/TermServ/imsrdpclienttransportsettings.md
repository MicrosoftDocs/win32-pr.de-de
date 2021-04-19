---
title: Imsrdpclienttransportsettings-Schnittstelle
description: Verwaltet die Client Transport Einstellungen für den Remotedesktop Gateway-Server (RD-Gateway). | Imsrdpclienttransportsettings-Schnittstelle
ms.assetid: d2573727-1dcc-4d4d-af5c-038e9467ba84
ms.tgt_platform: multiple
keywords:
- Imsrdpclienttransportsettings-Schnittstelle Remotedesktopdienste
- Imsrdpclienttransportsettings-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec240d008ef2f9469fb67f4041cfb33c08383079
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106350612"
---
# <a name="imsrdpclienttransportsettings-interface"></a><span data-ttu-id="acede-106">Imsrdpclienttransportsettings-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="acede-106">IMsRdpClientTransportSettings interface</span></span>

<span data-ttu-id="acede-107">Verwaltet die Client Transport Einstellungen für den Remotedesktop Gateway-Server (RD-Gateway).</span><span class="sxs-lookup"><span data-stu-id="acede-107">Manages client transport settings for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="acede-108">Member</span><span class="sxs-lookup"><span data-stu-id="acede-108">Members</span></span>

<span data-ttu-id="acede-109">Die **imsrdpclienttransportsettings** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="acede-109">The **IMsRdpClientTransportSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="acede-110">**Imsrdpclienttransportsettings** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="acede-110">**IMsRdpClientTransportSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="acede-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="acede-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="acede-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="acede-112">Properties</span></span>

<span data-ttu-id="acede-113">Die **imsrdpclienttransportsettings** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="acede-113">The **IMsRdpClientTransportSettings** interface has these properties.</span></span>



| <span data-ttu-id="acede-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="acede-114">Property</span></span>                                                                                                          | <span data-ttu-id="acede-115">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="acede-115">Access type</span></span>           | <span data-ttu-id="acede-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="acede-116">Description</span></span>                                                 |
|:------------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------|
| [<span data-ttu-id="acede-117">**Gatewaykredssource**</span><span class="sxs-lookup"><span data-stu-id="acede-117">**GatewayCredsSource**</span></span>](imsrdpclienttransportsettings-gatewaycredssource.md)<br/>                         | <span data-ttu-id="acede-118">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="acede-118">Read/write</span></span><br/> | <span data-ttu-id="acede-119">Die RD-Gateway Server-Authentifizierungsmethode.</span><span class="sxs-lookup"><span data-stu-id="acede-119">The RD Gateway server authentication method.</span></span><br/>     |
| [<span data-ttu-id="acede-120">**Gatewaydefaultusagemethod**</span><span class="sxs-lookup"><span data-stu-id="acede-120">**GatewayDefaultUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewaydefaultusagemethod.md)<br/>           | <span data-ttu-id="acede-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="acede-121">Read-only</span></span><br/>  | <span data-ttu-id="acede-122">Die Standard-RD-Gateway Verwendungs Methode.</span><span class="sxs-lookup"><span data-stu-id="acede-122">The default RD Gateway usage method.</span></span><br/>             |
| [<span data-ttu-id="acede-123">**Gatewayhostname**</span><span class="sxs-lookup"><span data-stu-id="acede-123">**GatewayHostname**</span></span>](imsrdpclienttransportsettings-gatewayhostname.md)<br/>                               | <span data-ttu-id="acede-124">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="acede-124">Read/write</span></span><br/> | <span data-ttu-id="acede-125">Der Hostname des RD-Gateway Servers.</span><span class="sxs-lookup"><span data-stu-id="acede-125">Host name of the RD Gateway server.</span></span><br/>              |
| [<span data-ttu-id="acede-126">**Gatewayissupported**</span><span class="sxs-lookup"><span data-stu-id="acede-126">**GatewayIsSupported**</span></span>](imsrdpclienttransportsettings-gatewayissupported.md)<br/>                         | <span data-ttu-id="acede-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="acede-127">Read-only</span></span><br/>  | <span data-ttu-id="acede-128">Gibt an, ob RD-Gateway unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="acede-128">Indicates whether RD Gateway is supported.</span></span><br/>       |
| [<span data-ttu-id="acede-129">**Gatewayprofileusagemethod**</span><span class="sxs-lookup"><span data-stu-id="acede-129">**GatewayProfileUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewayprofileusagemethod.md)<br/>           | <span data-ttu-id="acede-130">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="acede-130">Read/write</span></span><br/> | <span data-ttu-id="acede-131">Die RD-Gateway Profil Verwendungs Methode.</span><span class="sxs-lookup"><span data-stu-id="acede-131">The RD Gateway profile usage method.</span></span><br/>             |
| [<span data-ttu-id="acede-132">**GatewayUsageMethod**</span><span class="sxs-lookup"><span data-stu-id="acede-132">**GatewayUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewayusagemethod.md)<br/>                         | <span data-ttu-id="acede-133">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="acede-133">Read/write</span></span><br/> | <span data-ttu-id="acede-134">Die RD-Gateway Server-Verwendungs Methode.</span><span class="sxs-lookup"><span data-stu-id="acede-134">The RD Gateway server usage method.</span></span><br/>              |
| [<span data-ttu-id="acede-135">**Gatewayuserselectedkredssource**</span><span class="sxs-lookup"><span data-stu-id="acede-135">**GatewayUserSelectedCredsSource**</span></span>](imsrdpclienttransportsettings-gatewayuserselectedcredssource.md)<br/> | <span data-ttu-id="acede-136">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="acede-136">Read/write</span></span><br/> | <span data-ttu-id="acede-137">Der benutzerdefinierte RD-Gateway Anmelde Informationsquelle.</span><span class="sxs-lookup"><span data-stu-id="acede-137">The user-specified RD Gateway credential source.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="acede-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="acede-138">Requirements</span></span>



| <span data-ttu-id="acede-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="acede-139">Requirement</span></span> | <span data-ttu-id="acede-140">Wert</span><span class="sxs-lookup"><span data-stu-id="acede-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acede-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="acede-141">Minimum supported client</span></span><br/> | <span data-ttu-id="acede-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="acede-142">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="acede-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="acede-143">Minimum supported server</span></span><br/> | <span data-ttu-id="acede-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="acede-144">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="acede-145">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="acede-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="acede-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acede-146"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="acede-147">DLL</span><span class="sxs-lookup"><span data-stu-id="acede-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acede-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acede-148"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="acede-149">IID</span><span class="sxs-lookup"><span data-stu-id="acede-149">IID</span></span><br/>                      | <span data-ttu-id="acede-150">IID \_ imsrdpclienttransportsettings ist definiert als 720298c0-A099-46f 5-9F 82-96921bae4701</span><span class="sxs-lookup"><span data-stu-id="acede-150">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="acede-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="acede-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acede-152">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="acede-152">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="acede-153">Remotedesktop-Webverbindung Referenz</span><span class="sxs-lookup"><span data-stu-id="acede-153">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="acede-154">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="acede-154">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

