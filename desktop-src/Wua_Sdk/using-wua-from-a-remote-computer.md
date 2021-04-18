---
description: Die Windows Update-Agent-API (WUA) kann von einem Benutzer auf einem Remote Computer oder von einer Anwendung verwendet werden, die auf einem Remote Computer ausgeführt wird. Der Remote Benutzer oder die Anwendung muss jedoch über Administratorrechte verfügen.
ms.assetid: 15f86590-bed8-4506-916d-43b0bac5db2a
title: Verwenden von WUA auf einem Remote Computer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb14c019e48d6c36b210633ab9d57dcd157585a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344401"
---
# <a name="using-wua-from-a-remote-computer"></a><span data-ttu-id="241ad-104">Verwenden von WUA auf einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="241ad-104">Using WUA From a Remote Computer</span></span>

<span data-ttu-id="241ad-105">Die Windows Update-Agent-API (WUA) kann von einem Benutzer auf einem Remote Computer oder von einer Anwendung verwendet werden, die auf einem Remote Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="241ad-105">The Windows Update Agent (WUA) API can be used by a user on a remote computer or by an application that is running on a remote computer.</span></span> <span data-ttu-id="241ad-106">Der Remote Benutzer oder die Anwendung muss jedoch über Administratorrechte verfügen.</span><span class="sxs-lookup"><span data-stu-id="241ad-106">However, the remote user or application must have administrator privileges.</span></span>

<span data-ttu-id="241ad-107">Die folgende Liste enthält Schnittstellen, die für Remote Benutzer und Anwendungen verfügbar sind:</span><span class="sxs-lookup"><span data-stu-id="241ad-107">The following list contains interfaces that are available to remote users and applications:</span></span>

-   [<span data-ttu-id="241ad-108">**Iupdatesession**</span><span class="sxs-lookup"><span data-stu-id="241ad-108">**IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)
-   [<span data-ttu-id="241ad-109">**IUpdateSession2**</span><span class="sxs-lookup"><span data-stu-id="241ad-109">**IUpdateSession2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [<span data-ttu-id="241ad-110">**Iupdatesearcher**</span><span class="sxs-lookup"><span data-stu-id="241ad-110">**IUpdateSearcher**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [<span data-ttu-id="241ad-111">**Iautomaticupdates**</span><span class="sxs-lookup"><span data-stu-id="241ad-111">**IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [<span data-ttu-id="241ad-112">**Isearchresult**</span><span class="sxs-lookup"><span data-stu-id="241ad-112">**ISearchResult**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)
-   [<span data-ttu-id="241ad-113">**Iupdatecollection**</span><span class="sxs-lookup"><span data-stu-id="241ad-113">**IUpdateCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)
-   [<span data-ttu-id="241ad-114">**Iupdate**</span><span class="sxs-lookup"><span data-stu-id="241ad-114">**IUpdate**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)
-   [<span data-ttu-id="241ad-115">**IUpdate2**</span><span class="sxs-lookup"><span data-stu-id="241ad-115">**IUpdate2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdate2)
-   [<span data-ttu-id="241ad-116">**Iwindowsdriverupdate**</span><span class="sxs-lookup"><span data-stu-id="241ad-116">**IWindowsDriverUpdate**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate)
-   [<span data-ttu-id="241ad-117">**IWindowsDriverUpdate2**</span><span class="sxs-lookup"><span data-stu-id="241ad-117">**IWindowsDriverUpdate2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate2)
-   [<span data-ttu-id="241ad-118">**Iupdateidentity**</span><span class="sxs-lookup"><span data-stu-id="241ad-118">**IUpdateIdentity**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateidentity)
-   [<span data-ttu-id="241ad-119">**Iimageinformation**</span><span class="sxs-lookup"><span data-stu-id="241ad-119">**IImageInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iimageinformation)
-   [<span data-ttu-id="241ad-120">**Iinstallationbehavior**</span><span class="sxs-lookup"><span data-stu-id="241ad-120">**IInstallationBehavior**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior)
-   [<span data-ttu-id="241ad-121">**Istringcollection**</span><span class="sxs-lookup"><span data-stu-id="241ad-121">**IStringCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection)
-   [<span data-ttu-id="241ad-122">**Iupdatehistoryentrycollection**</span><span class="sxs-lookup"><span data-stu-id="241ad-122">**IUpdateHistoryEntryCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection)
-   [<span data-ttu-id="241ad-123">**Iupdatehistoryentry**</span><span class="sxs-lookup"><span data-stu-id="241ad-123">**IUpdateHistoryEntry**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)
-   [<span data-ttu-id="241ad-124">**Icategorycollection**</span><span class="sxs-lookup"><span data-stu-id="241ad-124">**ICategoryCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)
-   [<span data-ttu-id="241ad-125">**Icategory**</span><span class="sxs-lookup"><span data-stu-id="241ad-125">**ICategory**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-icategory)
-   [<span data-ttu-id="241ad-126">**Iupdateexceptioncollection**</span><span class="sxs-lookup"><span data-stu-id="241ad-126">**IUpdateExceptionCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)
-   [<span data-ttu-id="241ad-127">**Iupdateexception**</span><span class="sxs-lookup"><span data-stu-id="241ad-127">**IUpdateException**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)
-   [<span data-ttu-id="241ad-128">**Iupdatedownloadcontentcollection**</span><span class="sxs-lookup"><span data-stu-id="241ad-128">**IUpdateDownloadContentCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontentcollection)
-   [<span data-ttu-id="241ad-129">**Iupdatedownloadcontent**</span><span class="sxs-lookup"><span data-stu-id="241ad-129">**IUpdateDownloadContent**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontent)
-   [<span data-ttu-id="241ad-130">**Iupdateservicemanager**</span><span class="sxs-lookup"><span data-stu-id="241ad-130">**IUpdateServiceManager**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager)
-   [<span data-ttu-id="241ad-131">**Iupdateservicecollection**</span><span class="sxs-lookup"><span data-stu-id="241ad-131">**IUpdateServiceCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicecollection)
-   [<span data-ttu-id="241ad-132">**Iupdateservice**</span><span class="sxs-lookup"><span data-stu-id="241ad-132">**IUpdateService**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice)
-   [<span data-ttu-id="241ad-133">**Iwindowsupdateagentinfo**</span><span class="sxs-lookup"><span data-stu-id="241ad-133">**IWindowsUpdateAgentInfo**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo)

<span data-ttu-id="241ad-134">In der folgenden Liste sind Schnittstellen und Eigenschaften enthalten, die für Remote Benutzer und-Anwendungen nicht verfügbar sind:</span><span class="sxs-lookup"><span data-stu-id="241ad-134">The following list contains interfaces and properties that are not available to remote users and applications:</span></span>

-   [<span data-ttu-id="241ad-135">**Iupdatesession:: kreateupdatedownloader**</span><span class="sxs-lookup"><span data-stu-id="241ad-135">**IUpdateSession::CreateUpdateDownloader**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdatedownloader)
-   [<span data-ttu-id="241ad-136">**Iupdatesession:: kreateupdateinstaller**</span><span class="sxs-lookup"><span data-stu-id="241ad-136">**IUpdateSession::CreateUpdateInstaller**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdateinstaller)
-   [<span data-ttu-id="241ad-137">**WebProxy-Eigenschaft von iupdatesession**</span><span class="sxs-lookup"><span data-stu-id="241ad-137">**WebProxy Property of IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-get_webproxy)
-   [<span data-ttu-id="241ad-138">**Iupdatesearcher:: beginsearch**</span><span class="sxs-lookup"><span data-stu-id="241ad-138">**IUpdateSearcher::BeginSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)
-   [<span data-ttu-id="241ad-139">**Iupdatesearcher:: endsearch**</span><span class="sxs-lookup"><span data-stu-id="241ad-139">**IUpdateSearcher::EndSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)
-   <span data-ttu-id="241ad-140">Die [**IsHidden-Eigenschaft von iupdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden) (**IsHidden** ist schreibgeschützt, wenn Sie Remote aufgerufen wird.)</span><span class="sxs-lookup"><span data-stu-id="241ad-140">[**IsHidden Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden) (**IsHidden** is read-only when it is called remotely.)</span></span>
-   [<span data-ttu-id="241ad-141">**Iupdate:: akzepteula**</span><span class="sxs-lookup"><span data-stu-id="241ad-141">**IUpdate::AcceptEula**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
-   [<span data-ttu-id="241ad-142">**Iupdate:: copyfromcache**</span><span class="sxs-lookup"><span data-stu-id="241ad-142">**IUpdate::CopyFromCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [<span data-ttu-id="241ad-143">**IUpdate2:: copytocache**</span><span class="sxs-lookup"><span data-stu-id="241ad-143">**IUpdate2::CopyToCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate2-copytocache)
-   [<span data-ttu-id="241ad-144">**IWindowsDriverUpdate2:: copytocache**</span><span class="sxs-lookup"><span data-stu-id="241ad-144">**IWindowsDriverUpdate2::CopyToCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-copytocache)
-   [<span data-ttu-id="241ad-145">**Iupdateservicemanager:: AddService**</span><span class="sxs-lookup"><span data-stu-id="241ad-145">**IUpdateServiceManager::AddService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)
-   [<span data-ttu-id="241ad-146">**Iupdateservicemanager:: registerservicewithau**</span><span class="sxs-lookup"><span data-stu-id="241ad-146">**IUpdateServiceManager::RegisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)
-   [<span data-ttu-id="241ad-147">**Iupdateservicemanager:: unregisterservicewithau**</span><span class="sxs-lookup"><span data-stu-id="241ad-147">**IUpdateServiceManager::UnregisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau)
-   [<span data-ttu-id="241ad-148">**Iautomaticupdate::P ause**</span><span class="sxs-lookup"><span data-stu-id="241ad-148">**IAutomaticUpdate::Pause**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [<span data-ttu-id="241ad-149">**Iautomaticupdates:: Resume**</span><span class="sxs-lookup"><span data-stu-id="241ad-149">**IAutomaticUpdates::Resume**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [<span data-ttu-id="241ad-150">**Iautomaticupdates:: showsettingsdialog**</span><span class="sxs-lookup"><span data-stu-id="241ad-150">**IAutomaticUpdates::ShowSettingsDialog**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-showsettingsdialog)
-   [<span data-ttu-id="241ad-151">**Settings-Eigenschaft von iautomaticupdates**</span><span class="sxs-lookup"><span data-stu-id="241ad-151">**Settings Property of IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_settings)
-   [<span data-ttu-id="241ad-152">**Serviceaktivierte Eigenschaft von iautomaticupdates**</span><span class="sxs-lookup"><span data-stu-id="241ad-152">**ServiceEnabled Property of IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_serviceenabled)
-   [<span data-ttu-id="241ad-153">**Iautomaticupdates:: enableservice**</span><span class="sxs-lookup"><span data-stu-id="241ad-153">**IAutomaticUpdates::EnableService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [<span data-ttu-id="241ad-154">**Isysteminformation**</span><span class="sxs-lookup"><span data-stu-id="241ad-154">**ISystemInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)

<span data-ttu-id="241ad-155">Die folgenden Ports und Ausnahmen müssen den Windows-Firewall-Einstellungen für Windows Vista und Windows Server 2008 hinzugefügt werden, damit die WUA-API Remote aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="241ad-155">The following ports and exceptions must be added to the Windows firewall settings for Windows Vista and Windows Server 2008 for the WUA API to be called remotely.</span></span>

<dl> <dt>

<span data-ttu-id="241ad-156"><span id="Exception_1"></span><span id="exception_1"></span><span id="EXCEPTION_1"></span>Ausnahme 1</span><span class="sxs-lookup"><span data-stu-id="241ad-156"><span id="Exception_1"></span><span id="exception_1"></span><span id="EXCEPTION_1"></span>Exception 1</span></span>
</dt> <dd> <dl> <dd><span data-ttu-id="241ad-157">Lokaler Port: 135</span><span class="sxs-lookup"><span data-stu-id="241ad-157">Local port: 135</span></span></dd> <dd><span data-ttu-id="241ad-158">Remoteport: alle</span><span class="sxs-lookup"><span data-stu-id="241ad-158">Remote port: ALL</span></span></dd> <dd><span data-ttu-id="241ad-159">Protokollnummer: 6</span><span class="sxs-lookup"><span data-stu-id="241ad-159">Protocol number: 6</span></span></dd> <dd><span data-ttu-id="241ad-160">Ausführbare Datei:% windir% \\ system32 \\svchost.exe</span><span class="sxs-lookup"><span data-stu-id="241ad-160">Executable: %windir%\\system32\\svchost.exe</span></span></dd> <dd><span data-ttu-id="241ad-161">Dienst: RPCSS</span><span class="sxs-lookup"><span data-stu-id="241ad-161">Service: rpcss</span></span></dd> <dd><span data-ttu-id="241ad-162">Remote Berechtigung: Administrator</span><span class="sxs-lookup"><span data-stu-id="241ad-162">Remote privilege: Administrator</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="241ad-163"><span id="Exception_2"></span><span id="exception_2"></span><span id="EXCEPTION_2"></span>Ausnahme 2</span><span class="sxs-lookup"><span data-stu-id="241ad-163"><span id="Exception_2"></span><span id="exception_2"></span><span id="EXCEPTION_2"></span>Exception 2</span></span>
</dt> <dd> <dl> <dd><span data-ttu-id="241ad-164">Lokaler Port: dynamisches RPC</span><span class="sxs-lookup"><span data-stu-id="241ad-164">Local port: Dynamic RPC</span></span></dd> <dd><span data-ttu-id="241ad-165">Remoteport: alle</span><span class="sxs-lookup"><span data-stu-id="241ad-165">Remote port: ALL</span></span></dd> <dd><span data-ttu-id="241ad-166">Protokollnummer: 6</span><span class="sxs-lookup"><span data-stu-id="241ad-166">Protocol number: 6</span></span></dd> <dd><span data-ttu-id="241ad-167">Ausführbare Datei:% windir% \\ system32 \\dllhost.exe</span><span class="sxs-lookup"><span data-stu-id="241ad-167">Executable: %windir%\\system32\\dllhost.exe</span></span></dd> <dd><span data-ttu-id="241ad-168">Remote Berechtigung: Administrator</span><span class="sxs-lookup"><span data-stu-id="241ad-168">Remote privilege: Administrator</span></span></dd> </dl> </dd> </dl>

<span data-ttu-id="241ad-169">Die folgende Liste enthält Tools, die zum Konfigurieren der Windows-Firewall-Einstellungen verwendet werden können:</span><span class="sxs-lookup"><span data-stu-id="241ad-169">The following list contains tools that can be used to configure Windows Firewall settings:</span></span>

-   <span data-ttu-id="241ad-170">Windows-Firewall mit erweitertem Sicherheits-Snap-In</span><span class="sxs-lookup"><span data-stu-id="241ad-170">Windows Firewall with Advanced Security snap-in</span></span>
-   <span data-ttu-id="241ad-171">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="241ad-171">Group Policy</span></span>
-   <span data-ttu-id="241ad-172">Netsh advfirewall-Befehlszeilen Tool</span><span class="sxs-lookup"><span data-stu-id="241ad-172">Netsh advfirewall command-line tool</span></span>

<span data-ttu-id="241ad-173">Weitere Informationen zur Verwendung von Tools zum Konfigurieren der Windows-Firewall-Einstellungen finden Sie unter [Getting Started with Windows Firewall with Advanced Security](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748991(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="241ad-173">For more information about how to use tools to configure Windows Firewall settings, see [Getting Started with Windows Firewall with Advanced Security](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748991(v=ws.10)).</span></span>

 

 
