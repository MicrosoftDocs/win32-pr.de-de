---
title: IMsRdpClientTransportSettings2-Schnittstelle
description: Verwaltet die Client Transport Einstellungen für den Remotedesktop Gateway-Server (RD-Gateway). | IMsRdpClientTransportSettings2-Schnittstelle
ms.assetid: 4f9f1905-2693-4666-9f6f-6e00b1eb6a0f
ms.tgt_platform: multiple
keywords:
- IMsRdpClientTransportSettings2-Schnittstelle Remotedesktopdienste
- IMsRdpClientTransportSettings2 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f2f4887c6a4f55f3b9c97c389e9afd702d2ffab
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366581"
---
# <a name="imsrdpclienttransportsettings2-interface"></a><span data-ttu-id="bee39-106">IMsRdpClientTransportSettings2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="bee39-106">IMsRdpClientTransportSettings2 interface</span></span>

<span data-ttu-id="bee39-107">Verwaltet die Client Transport Einstellungen für den Remotedesktop Gateway-Server (RD-Gateway).</span><span class="sxs-lookup"><span data-stu-id="bee39-107">Manages client transport settings for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="bee39-108">Member</span><span class="sxs-lookup"><span data-stu-id="bee39-108">Members</span></span>

<span data-ttu-id="bee39-109">Die **IMsRdpClientTransportSettings2** -Schnittstelle erbt von [**imsrdpclienttransportsettings**](imsrdpclienttransportsettings.md).</span><span class="sxs-lookup"><span data-stu-id="bee39-109">The **IMsRdpClientTransportSettings2** interface inherits from [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md).</span></span> <span data-ttu-id="bee39-110">**IMsRdpClientTransportSettings2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bee39-110">**IMsRdpClientTransportSettings2** also has these types of members:</span></span>

-   [<span data-ttu-id="bee39-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bee39-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bee39-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bee39-112">Properties</span></span>

<span data-ttu-id="bee39-113">Die **IMsRdpClientTransportSettings2** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bee39-113">The **IMsRdpClientTransportSettings2** interface has these properties.</span></span>



| <span data-ttu-id="bee39-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bee39-114">Property</span></span>                                                                                                    | <span data-ttu-id="bee39-115">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="bee39-115">Access type</span></span>           | <span data-ttu-id="bee39-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bee39-116">Description</span></span>                                                                                       |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bee39-117">**Gatewaykredsharing**</span><span class="sxs-lookup"><span data-stu-id="bee39-117">**GatewayCredSharing**</span></span>](imsrdpclienttransportsettings2-gatewaycredsharing.md)<br/>                  | <span data-ttu-id="bee39-118">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bee39-118">Read/write</span></span><br/> | <span data-ttu-id="bee39-119">Gibt an, ob das Single Sign-On Feature für RD-Gateway aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="bee39-119">Indicates whether the single sign-on feature for RD Gateway is enabled.</span></span><br/>                |
| [<span data-ttu-id="bee39-120">**Gatewaydomain**</span><span class="sxs-lookup"><span data-stu-id="bee39-120">**GatewayDomain**</span></span>](imsrdpclienttransportsettings2-gatewaydomain.md)<br/>                            | <span data-ttu-id="bee39-121">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bee39-121">Read/write</span></span><br/> | <span data-ttu-id="bee39-122">Der Domänen Name, der von einem Benutzer zum Herstellen einer Verbindung mit dem RD-Gateway Server bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="bee39-122">The domain name that a user provides to connect to the RD Gateway server.</span></span><br/>              |
| [<span data-ttu-id="bee39-123">**Gatewayverschlüsseltedotpcookie**</span><span class="sxs-lookup"><span data-stu-id="bee39-123">**GatewayEncryptedOtpCookie**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>     | <span data-ttu-id="bee39-124">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bee39-124">Read/write</span></span><br/> | <span data-ttu-id="bee39-125">Das verschlüsselte OTP-Cookie.</span><span class="sxs-lookup"><span data-stu-id="bee39-125">The encrypted OTP cookie.</span></span><br/>                                                              |
| [<span data-ttu-id="bee39-126">**Gatewayverschlüsseltedotpcookiesize**</span><span class="sxs-lookup"><span data-stu-id="bee39-126">**GatewayEncryptedOtpCookieSize**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/> | <span data-ttu-id="bee39-127">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bee39-127">Read/write</span></span><br/> | <span data-ttu-id="bee39-128">Die Größe des verschlüsselten OTP-Cookies in Bytes.</span><span class="sxs-lookup"><span data-stu-id="bee39-128">The size, in bytes, of the encrypted OTP cookie.</span></span><br/>                                       |
| [<span data-ttu-id="bee39-129">**Gatewaypassword**</span><span class="sxs-lookup"><span data-stu-id="bee39-129">**GatewayPassword**</span></span>](imsrdpclienttransportsettings2-gatewaypassword.md)<br/>                        | <span data-ttu-id="bee39-130">Lesegeschützt</span><span class="sxs-lookup"><span data-stu-id="bee39-130">Write-only</span></span><br/> | <span data-ttu-id="bee39-131">Das Kennwort, das ein Benutzer zum Herstellen einer Verbindung mit dem RD-Gateway-Server bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="bee39-131">The password that a user provides to connect to the RD Gateway server.</span></span><br/>                 |
| [<span data-ttu-id="bee39-132">**Gatewaypreauthrequirement**</span><span class="sxs-lookup"><span data-stu-id="bee39-132">**GatewayPreAuthRequirement**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthrequirement.md)<br/>    | <span data-ttu-id="bee39-133">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bee39-133">Read/write</span></span><br/> | <span data-ttu-id="bee39-134">Gibt an, ob das RD-Gateway Feature für einmal Kennwort (One-time password, OTP) aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="bee39-134">Indicates whether the RD Gateway one-time password (OTP) feature is enabled.</span></span><br/>           |
| [<span data-ttu-id="bee39-135">**Gatewaypreauthserveraddr**</span><span class="sxs-lookup"><span data-stu-id="bee39-135">**GatewayPreAuthServerAddr**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>      | <span data-ttu-id="bee39-136">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bee39-136">Read/write</span></span><br/> | <span data-ttu-id="bee39-137">Die Webadresse des Servers, der vor der Authentifizierung steht.</span><span class="sxs-lookup"><span data-stu-id="bee39-137">The web address of the pre-authentication server.</span></span><br/>                                      |
| [<span data-ttu-id="bee39-138">**Gatewaysupporturl**</span><span class="sxs-lookup"><span data-stu-id="bee39-138">**GatewaySupportUrl**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>             | <span data-ttu-id="bee39-139">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bee39-139">Read/write</span></span><br/> | <span data-ttu-id="bee39-140">Die Webadresse der Website, die technischen Support für den RD-Gateway Server bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="bee39-140">The web address of the site that provides technical support for the RD Gateway server.</span></span><br/> |
| [<span data-ttu-id="bee39-141">**Gatewayusername**</span><span class="sxs-lookup"><span data-stu-id="bee39-141">**GatewayUsername**</span></span>](imsrdpclienttransportsettings2-gatewayusername.md)<br/>                        | <span data-ttu-id="bee39-142">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bee39-142">Read/write</span></span><br/> | <span data-ttu-id="bee39-143">Der Benutzername, den ein Benutzer zum Herstellen einer Verbindung mit dem RD-Gateway Server bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="bee39-143">The user name that a user provides to connect to the RD Gateway server.</span></span><br/>                |



 

## <a name="requirements"></a><span data-ttu-id="bee39-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bee39-144">Requirements</span></span>



| <span data-ttu-id="bee39-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bee39-145">Requirement</span></span> | <span data-ttu-id="bee39-146">Wert</span><span class="sxs-lookup"><span data-stu-id="bee39-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bee39-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bee39-147">Minimum supported client</span></span><br/> | <span data-ttu-id="bee39-148">Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="bee39-148">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="bee39-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bee39-149">Minimum supported server</span></span><br/> | <span data-ttu-id="bee39-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bee39-150">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="bee39-151">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="bee39-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="bee39-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bee39-152"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="bee39-153">DLL</span><span class="sxs-lookup"><span data-stu-id="bee39-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bee39-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bee39-154"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="bee39-155">IID</span><span class="sxs-lookup"><span data-stu-id="bee39-155">IID</span></span><br/>                      | <span data-ttu-id="bee39-156">IID \_ IMsRdpClientTransportSettings2 ist als 67341688-D606-4c73-A5D2-2e0489009319 definiert.</span><span class="sxs-lookup"><span data-stu-id="bee39-156">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bee39-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bee39-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bee39-158">**Imsrdpclienttransportsettings**</span><span class="sxs-lookup"><span data-stu-id="bee39-158">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





