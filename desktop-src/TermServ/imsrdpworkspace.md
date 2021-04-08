---
title: Imsrdpworkspace-Schnittstelle
description: Macht Methoden verfügbar, die RemoteApp-und Desktopverbindung Anmelde Informationen und Verbindungen verwalten.
ms.assetid: cddcdfc2-b30a-4d00-84c2-ad036ab6288f
ms.tgt_platform: multiple
keywords:
- Imsrdpworkspace-Schnittstelle Remotedesktopdienste
- Imsrdpworkspace-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba55a02c5d984bc87aa05caffd42b3a3b965c43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949500"
---
# <a name="imsrdpworkspace-interface"></a><span data-ttu-id="eb562-105">Imsrdpworkspace-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="eb562-105">IMsRdpWorkspace interface</span></span>

<span data-ttu-id="eb562-106">Macht Methoden verfügbar, die RemoteApp-und Desktopverbindung Anmelde Informationen und Verbindungen verwalten.</span><span class="sxs-lookup"><span data-stu-id="eb562-106">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span> <span data-ttu-id="eb562-107">Diese Schnittstelle wird von der Remotedesktopdienste Webzugriff-Steuerelement implementiert.</span><span class="sxs-lookup"><span data-stu-id="eb562-107">This interface is implemented by the Remote Desktop Services Web Access Control.</span></span> <span data-ttu-id="eb562-108">Dieses Steuerelement ist ein Wrapper um den Remotedesktopverbindung Client (MsTscAx.dll) und den Lauf Zeit Proxy für RemoteApp-und Desktop Verbindungen (Tswbprxy.exe).</span><span class="sxs-lookup"><span data-stu-id="eb562-108">This control is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="members"></a><span data-ttu-id="eb562-109">Member</span><span class="sxs-lookup"><span data-stu-id="eb562-109">Members</span></span>

<span data-ttu-id="eb562-110">Die **imsrdpworkspace** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="eb562-110">The **IMsRdpWorkspace** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="eb562-111">**Imsrdpworkspace** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="eb562-111">**IMsRdpWorkspace** also has these types of members:</span></span>

-   [<span data-ttu-id="eb562-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="eb562-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="eb562-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="eb562-113">Methods</span></span>

<span data-ttu-id="eb562-114">Die **imsrdpworkspace** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="eb562-114">The **IMsRdpWorkspace** interface has these methods.</span></span>



| <span data-ttu-id="eb562-115">Methode</span><span class="sxs-lookup"><span data-stu-id="eb562-115">Method</span></span>                                                                                   | <span data-ttu-id="eb562-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb562-116">Description</span></span>                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb562-117">[**Clearworkspacecredential**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eb562-117">[**ClearWorkspaceCredential**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))</span></span>             | <span data-ttu-id="eb562-118">Löscht die Benutzer Anmelde Informationen, die der angegebenen Verbindungs-ID zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="eb562-118">Deletes the user credentials associated with the specified connection ID.</span></span><br/>                                                                                  |
| <span data-ttu-id="eb562-119">[**Disconnectworkspace**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eb562-119">[**DisconnectWorkspace**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))</span></span>                       | <span data-ttu-id="eb562-120">Trennt alle vorhandenen Verbindungen, die mit der angegebenen Verbindungs-ID verknüpft sind, und löscht die entsprechenden Benutzer Anmelde Informationen aus dem Anmelde Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="eb562-120">Disconnects all existing connections associated with the specified connection ID and deletes the corresponding user credentials from the credential store.</span></span><br/> |
| <span data-ttu-id="eb562-121">[**Isworkspacecredentialspezifiziert**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eb562-121">[**IsWorkspaceCredentialSpecified**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85))</span></span> | <span data-ttu-id="eb562-122">Bestimmt, ob Benutzer Anmelde Informationen für die angegebene Verbindungs-ID vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="eb562-122">Determines whether user credentials exist for the specified connection ID.</span></span><br/>                                                                                 |
| <span data-ttu-id="eb562-123">[**Isworkspacessoaktivierte**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eb562-123">[**IsWorkspaceSSOEnabled**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))</span></span>                   | <span data-ttu-id="eb562-124">Bestimmt, ob einmaliges Anmelden (Single Sign on, SSO) für RemoteApp-und Desktopverbindung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="eb562-124">Determines whether single sign on (SSO) is enabled for RemoteApp and Desktop Connection.</span></span><br/>                                                                   |
| <span data-ttu-id="eb562-125">[**Onauthenticated**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eb562-125">[**OnAuthenticated**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))</span></span>                               | <span data-ttu-id="eb562-126">Markiert die Authentifizierung der Benutzer Anmelde Informationen für die Verbindungs-ID und zeigt anschließend die Verbindungs Benachrichtigung im Benachrichtigungsbereich der Taskleiste an.</span><span class="sxs-lookup"><span data-stu-id="eb562-126">Marks the authentication of user credentials for the connection ID, and subsequently shows the connect notification in the taskbar notification area.</span></span> <br/>     |
| <span data-ttu-id="eb562-127">[**Startworkspace**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eb562-127">[**StartWorkspace**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))</span></span>                                 | <span data-ttu-id="eb562-128">Ordnet Benutzer Anmelde Informationen und Zertifikate einer Verbindungs-ID zu.</span><span class="sxs-lookup"><span data-stu-id="eb562-128">Associates user credentials and certificates with a connection ID.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="eb562-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb562-129">Requirements</span></span>



| <span data-ttu-id="eb562-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb562-130">Requirement</span></span> | <span data-ttu-id="eb562-131">Wert</span><span class="sxs-lookup"><span data-stu-id="eb562-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb562-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb562-132">Minimum supported client</span></span><br/> | <span data-ttu-id="eb562-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="eb562-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="eb562-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb562-134">Minimum supported server</span></span><br/> | <span data-ttu-id="eb562-135">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="eb562-135">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="eb562-136">DLL</span><span class="sxs-lookup"><span data-stu-id="eb562-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb562-137"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb562-137"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |
| <span data-ttu-id="eb562-138">IID</span><span class="sxs-lookup"><span data-stu-id="eb562-138">IID</span></span><br/>                      | <span data-ttu-id="eb562-139">IID \_ imsrdpworkspace ist als 145d0621-04cf-4fc2-a766-a81a9069cdf8 definiert.</span><span class="sxs-lookup"><span data-stu-id="eb562-139">IID\_IMsRdpWorkspace is defined as 145D0621-04CF-4FC2-A766-A81A9069CDF8</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="eb562-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb562-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb562-141">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="eb562-141">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

