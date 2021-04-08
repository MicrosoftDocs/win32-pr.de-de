---
title: IMsRdpClientTransportSettings3-Schnittstelle
description: Definiert zusätzliche Eigenschaften für den Remotedesktop Gateway-Server (RD-Gateway). | IMsRdpClientTransportSettings3-Schnittstelle
ms.assetid: c0bdfe23-9a26-4feb-b9b7-e52f04f23aa1
ms.tgt_platform: multiple
keywords:
- IMsRdpClientTransportSettings3-Schnittstelle Remotedesktopdienste
- IMsRdpClientTransportSettings3 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7498db4b39a4ad0e89761cbec439895e4e9a152
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869755"
---
# <a name="imsrdpclienttransportsettings3-interface"></a><span data-ttu-id="f73ac-106">IMsRdpClientTransportSettings3-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f73ac-106">IMsRdpClientTransportSettings3 interface</span></span>

<span data-ttu-id="f73ac-107">Definiert zusätzliche Eigenschaften für den Remotedesktop Gateway-Server (RD-Gateway).</span><span class="sxs-lookup"><span data-stu-id="f73ac-107">Defines additional properties for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="f73ac-108">Member</span><span class="sxs-lookup"><span data-stu-id="f73ac-108">Members</span></span>

<span data-ttu-id="f73ac-109">Die **IMsRdpClientTransportSettings3** -Schnittstelle erbt von [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md).</span><span class="sxs-lookup"><span data-stu-id="f73ac-109">The **IMsRdpClientTransportSettings3** interface inherits from [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md).</span></span> <span data-ttu-id="f73ac-110">**IMsRdpClientTransportSettings3** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f73ac-110">**IMsRdpClientTransportSettings3** also has these types of members:</span></span>

-   [<span data-ttu-id="f73ac-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f73ac-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f73ac-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f73ac-112">Properties</span></span>

<span data-ttu-id="f73ac-113">Die **IMsRdpClientTransportSettings3** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f73ac-113">The **IMsRdpClientTransportSettings3** interface has these properties.</span></span>



| <span data-ttu-id="f73ac-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f73ac-114">Property</span></span>                                                                                                           | <span data-ttu-id="f73ac-115">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="f73ac-115">Access type</span></span>           | <span data-ttu-id="f73ac-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f73ac-116">Description</span></span>                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f73ac-117">**Gatewayauthcookieserveraddr**</span><span class="sxs-lookup"><span data-stu-id="f73ac-117">**GatewayAuthCookieServerAddr**</span></span>](imsrdpclienttransportsettings3-gatewayauthcookieserveraddr.md)<br/>       | <span data-ttu-id="f73ac-118">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f73ac-118">Read/write</span></span><br/> | <span data-ttu-id="f73ac-119">Die Server Adresse für die cookiebasierte Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="f73ac-119">The server address for cookie-based authentication.</span></span><br/>                                                                                       |
| [<span data-ttu-id="f73ac-120">**Gatewayauthloginpage**</span><span class="sxs-lookup"><span data-stu-id="f73ac-120">**GatewayAuthLoginPage**</span></span>](imsrdpclienttransportsettings3-gatewayauthloginpage.md)<br/>                     | <span data-ttu-id="f73ac-121">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f73ac-121">Read/write</span></span><br/> | <span data-ttu-id="f73ac-122">Die Adresse der Anmelde Webseite, die zum Authentifizieren eines Benutzers verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f73ac-122">The address of the login webpage to use to authenticate a user.</span></span><br/>                                                                           |
| [<span data-ttu-id="f73ac-123">**Gatewaykredsourcecookie**</span><span class="sxs-lookup"><span data-stu-id="f73ac-123">**GatewayCredSourceCookie**</span></span>](imsrdpclienttransportsettings3-gatewaycredsourcecookie.md)<br/>               | <span data-ttu-id="f73ac-124">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f73ac-124">Read/write</span></span><br/> | <span data-ttu-id="f73ac-125">Gibt an, ob die Anmelde Informationsquelle cookiebasiert ist.</span><span class="sxs-lookup"><span data-stu-id="f73ac-125">Specifies if the credential source is cookie based.</span></span><br/>                                                                                       |
| [<span data-ttu-id="f73ac-126">**Gatewayverschlüsseltedauthcookie**</span><span class="sxs-lookup"><span data-stu-id="f73ac-126">**GatewayEncryptedAuthCookie**</span></span>](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md)<br/>         | <span data-ttu-id="f73ac-127">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f73ac-127">Read/write</span></span><br/> | <span data-ttu-id="f73ac-128">Das verschlüsselte Authentifizierungs Cookie.</span><span class="sxs-lookup"><span data-stu-id="f73ac-128">The encrypted authentication cookie.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="f73ac-129">**Gatewayverschlüsseltedauthcookiesize**</span><span class="sxs-lookup"><span data-stu-id="f73ac-129">**GatewayEncryptedAuthCookieSize**</span></span>](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)<br/> | <span data-ttu-id="f73ac-130">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f73ac-130">Read/write</span></span><br/> | <span data-ttu-id="f73ac-131">Die Größe der [**gatewayverschlüsseltedauthcookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) -Eigenschaft in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f73ac-131">The size, in characters, of the [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) property.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f73ac-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f73ac-132">Requirements</span></span>



| <span data-ttu-id="f73ac-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f73ac-133">Requirement</span></span> | <span data-ttu-id="f73ac-134">Wert</span><span class="sxs-lookup"><span data-stu-id="f73ac-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f73ac-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f73ac-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f73ac-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f73ac-136">Windows 7</span></span><br/>                                                                              |
| <span data-ttu-id="f73ac-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f73ac-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f73ac-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f73ac-138">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="f73ac-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f73ac-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="f73ac-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f73ac-140"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="f73ac-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f73ac-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f73ac-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f73ac-142"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="f73ac-143">IID</span><span class="sxs-lookup"><span data-stu-id="f73ac-143">IID</span></span><br/>                      | <span data-ttu-id="f73ac-144">IID \_ IMsRdpClientTransportSettings3 ist als 3d5b21ac-748d-41to-8l30e15169586bd4 definiert.</span><span class="sxs-lookup"><span data-stu-id="f73ac-144">IID\_IMsRdpClientTransportSettings3 is defined as 3D5B21AC-748D-41DE-8F30-E15169586BD4</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f73ac-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f73ac-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f73ac-146">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="f73ac-146">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





