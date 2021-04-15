---
title: Imsrdpclientshell-Schnittstelle
description: Remotedesktopverbindung (RDC)-Client Einstellungen, die verwendet werden, um den Client über Remotedesktop Webzugriff (RD Webzugriff) oder andere Webportale zu starten.
ms.assetid: 05ca2e90-656a-40a3-a438-29d7985e9feb
ms.tgt_platform: multiple
keywords:
- Imsrdpclientshell-Schnittstelle Remotedesktopdienste
- Imsrdpclientshell-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b529ed1819864e5fc6106472b33ddd00312560c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477757"
---
# <a name="imsrdpclientshell-interface"></a><span data-ttu-id="aac5b-105">Imsrdpclientshell-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="aac5b-105">IMsRdpClientShell interface</span></span>

<span data-ttu-id="aac5b-106">Remotedesktopverbindung (RDC)-Client Einstellungen, die verwendet werden, um den Client über Remotedesktop Webzugriff (RD Webzugriff) oder andere Webportale zu starten.</span><span class="sxs-lookup"><span data-stu-id="aac5b-106">Remote Desktop Connection (RDC) client settings that are used to launch the client from Remote Desktop Web Access (RD Web Access) or from other web portals.</span></span>

## <a name="members"></a><span data-ttu-id="aac5b-107">Member</span><span class="sxs-lookup"><span data-stu-id="aac5b-107">Members</span></span>

<span data-ttu-id="aac5b-108">Die **imsrdpclientshell** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="aac5b-108">The **IMsRdpClientShell** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="aac5b-109">**Imsrdpclientshell** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="aac5b-109">**IMsRdpClientShell** also has these types of members:</span></span>

-   [<span data-ttu-id="aac5b-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="aac5b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="aac5b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aac5b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="aac5b-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="aac5b-112">Methods</span></span>

<span data-ttu-id="aac5b-113">Die **imsrdpclientshell** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="aac5b-113">The **IMsRdpClientShell** interface has these methods.</span></span>



| <span data-ttu-id="aac5b-114">Methode</span><span class="sxs-lookup"><span data-stu-id="aac5b-114">Method</span></span>                                                     | <span data-ttu-id="aac5b-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aac5b-115">Description</span></span>                                                  |
|:-----------------------------------------------------------|:-------------------------------------------------------------|
| <span data-ttu-id="aac5b-116">[**Getrdpproperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aac5b-116">[**GetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85))</span></span> | <span data-ttu-id="aac5b-117">Ruft eine einzelne RDP-Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="aac5b-117">Retrieves a single RDP property.</span></span><br/>                  |
| [<span data-ttu-id="aac5b-118">**Starten**</span><span class="sxs-lookup"><span data-stu-id="aac5b-118">**Launch**</span></span>](imsrdpclientshell-launch.md)                 | <span data-ttu-id="aac5b-119">Starten von Remote Dateiinhalt über das Webportal.</span><span class="sxs-lookup"><span data-stu-id="aac5b-119">Launches remote file content from the web portal.</span></span><br/> |
| <span data-ttu-id="aac5b-120">[**""-Eigenschaft ""**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aac5b-120">[**SetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85))</span></span> | <span data-ttu-id="aac5b-121">Legt eine einzelne RDP-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="aac5b-121">Sets a single RDP property.</span></span><br/>                       |



 

### <a name="properties"></a><span data-ttu-id="aac5b-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aac5b-122">Properties</span></span>

<span data-ttu-id="aac5b-123">Die **imsrdpclientshell** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aac5b-123">The **IMsRdpClientShell** interface has these properties.</span></span>



| <span data-ttu-id="aac5b-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="aac5b-124">Property</span></span>                                                                                              | <span data-ttu-id="aac5b-125">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="aac5b-125">Access type</span></span>           | <span data-ttu-id="aac5b-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aac5b-126">Description</span></span>                                                                                               |
|:------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aac5b-127">**Isremoteprogramclientinstalliert**</span><span class="sxs-lookup"><span data-stu-id="aac5b-127">**IsRemoteProgramClientInstalled**</span></span>](imsrdpclientshell-isremoteprogramclientinstalled.md)<br/> | <span data-ttu-id="aac5b-128">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aac5b-128">Read-only</span></span><br/>  | <span data-ttu-id="aac5b-129">Ruft ab, ob der Remotedesktopverbindung-Client (RDC) die RemoteApp-Funktionalität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aac5b-129">Retrieves whether the Remote Desktop Connection (RDC) client supports RemoteApp functionality.</span></span><br/> |
| [<span data-ttu-id="aac5b-130">**Publicmode**</span><span class="sxs-lookup"><span data-stu-id="aac5b-130">**PublicMode**</span></span>](imsrdpclientshell-publicmode.md)<br/>                                         | <span data-ttu-id="aac5b-131">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="aac5b-131">Read/write</span></span><br/> | <span data-ttu-id="aac5b-132">Ruft ab, ob der öffentliche Modus aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="aac5b-132">Retrieves whether public mode is enabled.</span></span><br/>                                                      |
| [<span data-ttu-id="aac5b-133">**Rdpfilecontents**</span><span class="sxs-lookup"><span data-stu-id="aac5b-133">**RdpFileContents**</span></span>](imsrdpclientshell-rdpfilecontents.md)<br/>                               | <span data-ttu-id="aac5b-134">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="aac5b-134">Read/write</span></span><br/> | <span data-ttu-id="aac5b-135">Streamversion der RDP-Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="aac5b-135">Stream version of the RDP configuration file.</span></span><br/>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="aac5b-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aac5b-136">Requirements</span></span>



| <span data-ttu-id="aac5b-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aac5b-137">Requirement</span></span> | <span data-ttu-id="aac5b-138">Wert</span><span class="sxs-lookup"><span data-stu-id="aac5b-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aac5b-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aac5b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="aac5b-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aac5b-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="aac5b-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aac5b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="aac5b-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aac5b-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="aac5b-143">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="aac5b-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="aac5b-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aac5b-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aac5b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="aac5b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aac5b-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aac5b-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aac5b-147">IID</span><span class="sxs-lookup"><span data-stu-id="aac5b-147">IID</span></span><br/>                      | <span data-ttu-id="aac5b-148">IID \_ imsrdpclientshell ist als d012ae6d-C19A-4bfe-b367-201f8911f134 definiert.</span><span class="sxs-lookup"><span data-stu-id="aac5b-148">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="aac5b-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aac5b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aac5b-150">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="aac5b-150">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="aac5b-151">Remotedesktop-Webverbindung Referenz</span><span class="sxs-lookup"><span data-stu-id="aac5b-151">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

