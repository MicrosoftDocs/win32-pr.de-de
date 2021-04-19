---
title: Imsrdpclientsecuredsettings-Schnittstelle
description: Enthält Methoden zum Abrufen und Festlegen der Eigenschaften des Remotedesktop ActiveX-Steuer Elements, die auf bestimmte Internet Explorer-URL-Sicherheitszonen beschränkt sind. | Imsrdpclientsecuredsettings-Schnittstelle
ms.assetid: 56d3193d-a0fb-468a-9fb3-c080db5500b7
ms.tgt_platform: multiple
keywords:
- Imsrdpclientsecuredsettings-Schnittstelle Remotedesktopdienste
- Imsrdpclientsecuredsettings-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396e6b58b2be0122076b5529b910423377417fa6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366594"
---
# <a name="imsrdpclientsecuredsettings-interface"></a><span data-ttu-id="b25f3-106">Imsrdpclientsecuredsettings-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b25f3-106">IMsRdpClientSecuredSettings interface</span></span>

<span data-ttu-id="b25f3-107">Enthält Methoden zum Abrufen und Festlegen der Eigenschaften des Remotedesktop ActiveX-Steuer Elements, die auf bestimmte Internet Explorer-URL-Sicherheitszonen beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="b25f3-107">Includes methods to retrieve and set properties of the Remote Desktop ActiveX control that are restricted to specific Internet Explorer URL security zones.</span></span>

## <a name="members"></a><span data-ttu-id="b25f3-108">Member</span><span class="sxs-lookup"><span data-stu-id="b25f3-108">Members</span></span>

<span data-ttu-id="b25f3-109">Die **imsrdpclientsecuredsettings** -Schnittstelle erbt von [**imstscsecuredsettings**](imstscsecuredsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="b25f3-109">The **IMsRdpClientSecuredSettings** interface inherits from [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span></span> <span data-ttu-id="b25f3-110">**Imsrdpclientsecuredsettings** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b25f3-110">**IMsRdpClientSecuredSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="b25f3-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b25f3-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b25f3-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b25f3-112">Properties</span></span>

<span data-ttu-id="b25f3-113">Die **imsrdpclientsecuredsettings** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b25f3-113">The **IMsRdpClientSecuredSettings** interface has these properties.</span></span>



| <span data-ttu-id="b25f3-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b25f3-114">Property</span></span>                                                                                   | <span data-ttu-id="b25f3-115">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="b25f3-115">Access type</span></span>           | <span data-ttu-id="b25f3-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b25f3-116">Description</span></span>                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [<span data-ttu-id="b25f3-117">**Audioredirectionmode**</span><span class="sxs-lookup"><span data-stu-id="b25f3-117">**AudioRedirectionMode**</span></span>](imsrdpclientsecuredsettings-autoredirectionmode.md)<br/> | <span data-ttu-id="b25f3-118">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b25f3-118">Read/write</span></span><br/> | <span data-ttu-id="b25f3-119">Die audioumleitungs Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="b25f3-119">The audio redirection settings.</span></span><br/>    |
| [<span data-ttu-id="b25f3-120">**Keyboardhuokmode**</span><span class="sxs-lookup"><span data-stu-id="b25f3-120">**KeyboardHookMode**</span></span>](imsrdpclientsecuredsettings-keyboardhookmode.md)<br/>        | <span data-ttu-id="b25f3-121">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b25f3-121">Read/write</span></span><br/> | <span data-ttu-id="b25f3-122">Die Einstellungen der Tastatur Umleitung.</span><span class="sxs-lookup"><span data-stu-id="b25f3-122">The keyboard redirection settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b25f3-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b25f3-123">Remarks</span></span>

<span data-ttu-id="b25f3-124">Diese Eigenschaften können nicht festgelegt werden, wenn das Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="b25f3-124">These properties cannot be set when the control is connected.</span></span>

<span data-ttu-id="b25f3-125">Weitere Informationen zu den Methoden dieser Schnittstelle finden Sie unter [Bereitstellen der RDP-Client Sicherheit](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="b25f3-125">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information about the methods of this interface.</span></span>

<span data-ttu-id="b25f3-126">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b25f3-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b25f3-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b25f3-127">Requirements</span></span>



| <span data-ttu-id="b25f3-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b25f3-128">Requirement</span></span> | <span data-ttu-id="b25f3-129">Wert</span><span class="sxs-lookup"><span data-stu-id="b25f3-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b25f3-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b25f3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b25f3-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b25f3-131">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="b25f3-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b25f3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b25f3-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b25f3-133">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="b25f3-134">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b25f3-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="b25f3-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b25f3-135"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="b25f3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b25f3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b25f3-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b25f3-137"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="b25f3-138">IID</span><span class="sxs-lookup"><span data-stu-id="b25f3-138">IID</span></span><br/>                      | <span data-ttu-id="b25f3-139">IID \_ imsrdpclientsecuredsettings ist als 605befcf-39c1-45cc-a811-068fb7be346d definiert.</span><span class="sxs-lookup"><span data-stu-id="b25f3-139">IID\_IMsRdpClientSecuredSettings is defined as 605befcf-39c1-45cc-a811-068fb7be346d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b25f3-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b25f3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b25f3-141">**Imstscsecuredsettings**</span><span class="sxs-lookup"><span data-stu-id="b25f3-141">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="b25f3-142">Remotedesktop-Webverbindung Referenz</span><span class="sxs-lookup"><span data-stu-id="b25f3-142">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





