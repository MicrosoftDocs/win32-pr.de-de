---
title: IMsRdpClientShell2-Schnittstelle
description: Macht Eigenschaften verfügbar, die den Remotedesktopverbindung Client über Remotedesktop Webzugriff (RD-Webzugriff) oder andere Webportale starten.
ms.assetid: cc8ef78f-b7d6-42cd-bb67-8a8e1f33be08
ms.tgt_platform: multiple
keywords:
- IMsRdpClientShell2-Schnittstelle Remotedesktopdienste
- IMsRdpClientShell2 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientShell2
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb93fd938602b195f60877be884dbe0bd458a598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740552"
---
# <a name="imsrdpclientshell2-interface"></a><span data-ttu-id="51fbf-105">IMsRdpClientShell2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="51fbf-105">IMsRdpClientShell2 interface</span></span>

<span data-ttu-id="51fbf-106">Macht Eigenschaften verfügbar, die den Remotedesktopverbindung Client über Remotedesktop Webzugriff (RD-Webzugriff) oder andere Webportale starten.</span><span class="sxs-lookup"><span data-stu-id="51fbf-106">Exposes properties that launch the Remote Desktop Connection client from Remote Desktop Web Access (RD Web Access) or from other web portals.</span></span>

<span data-ttu-id="51fbf-107">Diese Schnittstelle wird durch das Remotedesktopdienste Webzugriff-Steuerelement implementiert. Hierbei handelt es sich um einen Wrapper um den Remotedesktopverbindung Client (MsTscAx.dll) und den Lauf Zeit Proxy für RemoteApp-und Desktop Verbindungen (Tswbprxy.exe).</span><span class="sxs-lookup"><span data-stu-id="51fbf-107">This interface is implemented by the Remote Desktop Services Web Access Control, which is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="members"></a><span data-ttu-id="51fbf-108">Member</span><span class="sxs-lookup"><span data-stu-id="51fbf-108">Members</span></span>

<span data-ttu-id="51fbf-109">Die **IMsRdpClientShell2** -Schnittstelle erbt von **imsrdpclientshell**.</span><span class="sxs-lookup"><span data-stu-id="51fbf-109">The **IMsRdpClientShell2** interface inherits from **IMsRdpClientShell**.</span></span> <span data-ttu-id="51fbf-110">**IMsRdpClientShell2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="51fbf-110">**IMsRdpClientShell2** also has these types of members:</span></span>

-   [<span data-ttu-id="51fbf-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51fbf-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51fbf-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51fbf-112">Properties</span></span>

<span data-ttu-id="51fbf-113">Die **IMsRdpClientShell2** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="51fbf-113">The **IMsRdpClientShell2** interface has these properties.</span></span>



| <span data-ttu-id="51fbf-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="51fbf-114">Property</span></span>                                                                               | <span data-ttu-id="51fbf-115">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="51fbf-115">Access type</span></span>          | <span data-ttu-id="51fbf-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51fbf-116">Description</span></span>                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51fbf-117">**Msrdpworkspace**</span><span class="sxs-lookup"><span data-stu-id="51fbf-117">**MsRdpWorkspace**</span></span>](imsrdpclientshell2-msrdpworkspace.md)<br/>                 | <span data-ttu-id="51fbf-118">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51fbf-118">Read-only</span></span><br/> | <span data-ttu-id="51fbf-119">Ruft einen Zeiger auf die [**imsrdpworkspace**](imsrdpworkspace.md) -Schnittstelle ab, die zum Verwalten von RemoteApp-und Desktopverbindung Anmelde Informationen und Verbindungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51fbf-119">Retrieves a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface, which is used to manage RemoteApp and Desktop Connection credentials and connections.</span></span><br/> |
| [<span data-ttu-id="51fbf-120">**Securedsettingsenabled**</span><span class="sxs-lookup"><span data-stu-id="51fbf-120">**SecuredSettingsEnabled**</span></span>](imsrdpclientshell2-securedsettingsenabled.md)<br/> | <span data-ttu-id="51fbf-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51fbf-121">Read-only</span></span><br/> | <span data-ttu-id="51fbf-122">Ruft einen Wert ab, der angibt, ob sich die aktuelle Webseite in einer vertrauenswürdigen Internet Explorer-URL-Sicherheitszone befindet.</span><span class="sxs-lookup"><span data-stu-id="51fbf-122">Retrieves a value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span><br/>                                                      |



 

## <a name="requirements"></a><span data-ttu-id="51fbf-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51fbf-123">Requirements</span></span>



| <span data-ttu-id="51fbf-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51fbf-124">Requirement</span></span> | <span data-ttu-id="51fbf-125">Wert</span><span class="sxs-lookup"><span data-stu-id="51fbf-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="51fbf-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51fbf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="51fbf-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="51fbf-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="51fbf-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51fbf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="51fbf-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="51fbf-129">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="51fbf-130">DLL</span><span class="sxs-lookup"><span data-stu-id="51fbf-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51fbf-131"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51fbf-131"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51fbf-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51fbf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51fbf-133">**Imsrdpworkspace**</span><span class="sxs-lookup"><span data-stu-id="51fbf-133">**IMsRdpWorkspace**</span></span>](imsrdpworkspace.md)
</dt> </dl>

 

 





