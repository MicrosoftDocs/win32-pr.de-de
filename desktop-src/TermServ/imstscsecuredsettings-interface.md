---
title: Imstscsecuredsettings-Schnittstelle
description: Enthält Methoden zum Abrufen und Festlegen der Eigenschaften des Remotedesktop ActiveX-Steuer Elements, die auf bestimmte Internet Explorer-URL-Sicherheitszonen beschränkt sind. | Imstscsecuredsettings-Schnittstelle
ms.assetid: 1136dbc5-abe6-40e0-b44f-700a1460fbd2
ms.tgt_platform: multiple
keywords:
- Imstscsecuredsettings-Schnittstelle Remotedesktopdienste
- Imstscsecuredsettings-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2037393147bd5a2e35d6eb803951890c9b5e7de5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106355759"
---
# <a name="imstscsecuredsettings-interface"></a><span data-ttu-id="10018-106">Imstscsecuredsettings-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="10018-106">IMsTscSecuredSettings interface</span></span>

<span data-ttu-id="10018-107">Enthält Methoden zum Abrufen und Festlegen der Eigenschaften des Remotedesktop ActiveX-Steuer Elements, die auf bestimmte Internet Explorer-URL-Sicherheitszonen beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="10018-107">Includes methods to retrieve and set properties of the Remote Desktop ActiveX control that are restricted to specific Internet Explorer URL security zones.</span></span> <span data-ttu-id="10018-108">Zu den Eigenschaften gehören diejenigen, die den Modus des Client Steuer Elements (Vollbildmodus oder Fenstermodus) und das Programm angeben, das bei der Verbindung mit dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="10018-108">Properties include those that specify the mode of the client control (full-screen mode or window mode) and the program to start upon connection to the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="10018-109">Diese Methoden sind auch über die [**imsrdpclientsecuredsettings**](imsrdpclientsecuredsettings-interface.md) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="10018-109">These methods are also available through the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="10018-110">Member</span><span class="sxs-lookup"><span data-stu-id="10018-110">Members</span></span>

<span data-ttu-id="10018-111">Die **imstscsecuredsettings** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="10018-111">The **IMsTscSecuredSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="10018-112">**Imstscsecuredsettings** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="10018-112">**IMsTscSecuredSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="10018-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="10018-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10018-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="10018-114">Properties</span></span>

<span data-ttu-id="10018-115">Die **imstscsecuredsettings** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="10018-115">The **IMsTscSecuredSettings** interface has these properties.</span></span>



| <span data-ttu-id="10018-116">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="10018-116">Property</span></span>                                                              | <span data-ttu-id="10018-117">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="10018-117">Access type</span></span>           | <span data-ttu-id="10018-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10018-118">Description</span></span>                                                                |
|:----------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="10018-119">**FullScreen**</span><span class="sxs-lookup"><span data-stu-id="10018-119">**FullScreen**</span></span>](imstscsecuredsettings-fullscreen.md)<br/>     | <span data-ttu-id="10018-120">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="10018-120">Read/write</span></span><br/> | <span data-ttu-id="10018-121">Der voll Bild Zustand des Client Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="10018-121">The full-screen state of the client control.</span></span><br/>                    |
| [<span data-ttu-id="10018-122">**StartProgram**</span><span class="sxs-lookup"><span data-stu-id="10018-122">**StartProgram**</span></span>](imstscsecuredsettings-startprogram.md)<br/> | <span data-ttu-id="10018-123">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="10018-123">Read/write</span></span><br/> | <span data-ttu-id="10018-124">Das Programm, das auf dem Remote Server bei der Verbindung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="10018-124">The program to be started on the remote server upon connection.</span></span><br/> |
| [<span data-ttu-id="10018-125">**WorkDir**</span><span class="sxs-lookup"><span data-stu-id="10018-125">**WorkDir**</span></span>](imstscsecuredsettings-workdir.md)<br/>           | <span data-ttu-id="10018-126">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="10018-126">Read/write</span></span><br/> | <span data-ttu-id="10018-127">Das Arbeitsverzeichnis des Start Programms.</span><span class="sxs-lookup"><span data-stu-id="10018-127">The working directory of the start program.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="10018-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10018-128">Remarks</span></span>

<span data-ttu-id="10018-129">Weitere Informationen zu den Methoden dieser Schnittstelle finden Sie unter [Bereitstellen der RDP-Client Sicherheit](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="10018-129">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information about the methods of this interface.</span></span>

<span data-ttu-id="10018-130">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="10018-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="10018-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10018-131">Requirements</span></span>



| <span data-ttu-id="10018-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10018-132">Requirement</span></span> | <span data-ttu-id="10018-133">Wert</span><span class="sxs-lookup"><span data-stu-id="10018-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="10018-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10018-134">Minimum supported client</span></span><br/> | <span data-ttu-id="10018-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10018-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="10018-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10018-136">Minimum supported server</span></span><br/> | <span data-ttu-id="10018-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10018-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="10018-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="10018-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="10018-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10018-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="10018-140">DLL</span><span class="sxs-lookup"><span data-stu-id="10018-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10018-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10018-141"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10018-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10018-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10018-143">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="10018-143">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="10018-144">Remotedesktop-Webverbindung Referenz</span><span class="sxs-lookup"><span data-stu-id="10018-144">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

