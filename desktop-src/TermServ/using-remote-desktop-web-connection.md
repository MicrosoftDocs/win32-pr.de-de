---
title: Verwenden des Remotedesktop ActiveX-Steuer Elements
description: So können Sie das Remotedesktop ActiveX-Steuerelement verwenden, um die Remotedesktopdienste Benutzer Darstellung anzupassen.
ms.assetid: ea80a99a-7bf6-48e2-8bd0-c9a158bcf475
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste mit Remotedesktop ActiveX-Steuerelement
- Remotedesktop-Webverbindung Remotedesktopdienste mit
- Remotedesktopprotokoll Remotedesktopdienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b06f575d5cffc16bd19f6bbe5fd4b3237dda7b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339799"
---
# <a name="using-the-remote-desktop-activex-control"></a><span data-ttu-id="e477a-106">Verwenden des Remotedesktop ActiveX-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="e477a-106">Using the Remote Desktop ActiveX control</span></span>

<span data-ttu-id="e477a-107">Die folgenden Themen enthalten Informationen dazu, wie Sie das Remotedesktop ActiveX-Steuerelement verwenden können, um die Remotedesktopdienste Benutzer Darstellung anzupassen.</span><span class="sxs-lookup"><span data-stu-id="e477a-107">The following topics contain information about how you can use the Remote Desktop ActiveX control to customize the Remote Desktop Services user experience.</span></span>

<span data-ttu-id="e477a-108">Das Remotedesktop ActiveX-Steuerelement ist in den folgenden Formularen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="e477a-108">The Remote Desktop ActiveX control is available in the following forms:</span></span>

-   <span data-ttu-id="e477a-109">**Das Skript fähige-Steuer** Element – implementiert Schnittstellen, die für die Skripterstellung sicher sind.</span><span class="sxs-lookup"><span data-stu-id="e477a-109">**The scriptable control**—implements interfaces that are safe for scripting.</span></span> <span data-ttu-id="e477a-110">Diese Form des Steuer Elements kann von Webclients oder Skript Erstellungs Hosts (z. b. VBScript) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e477a-110">This form of the control can be used by web clients or scripting (such as VBScript) hosts.</span></span>
-   <span data-ttu-id="e477a-111">**Das nicht Scriptable-Steuer** Element – bietet zusätzliche Funktionen, die für die Skripterstellung nicht sicher sind.</span><span class="sxs-lookup"><span data-stu-id="e477a-111">**The nonscriptable control**—offers additional functionality that is not safe for scripting.</span></span> <span data-ttu-id="e477a-112">Diese Form des Steuer Elements kann von System eigenem oder verwaltetem Code verwendet werden. dieses Formular kann jedoch nicht von Webclients oder reinen Skript Hosts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e477a-112">This form of the control can be used from native or managed code, but this form cannot be used by web clients or scripting-only hosts.</span></span>

<span data-ttu-id="e477a-113">Die folgende Liste enthält die **CLSID**-e für die verschiedenen Steuerelemente für verschiedene Betriebssystemversionen.</span><span class="sxs-lookup"><span data-stu-id="e477a-113">The following list contains the **CLSID** s for the different controls for different operating system versions.</span></span> <span data-ttu-id="e477a-114">Alle **CLSID**-e sind mit neueren Systemversionen kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e477a-114">Each of the **CLSID** s is compatible with later system versions.</span></span> <span data-ttu-id="e477a-115">Beispielsweise kann die **CLSID** für das Skript fähige-Steuerelement unter Windows Vista in späteren Systemversionen wie Windows 7 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e477a-115">For example, the **CLSID** for the scriptable control on Windows Vista will work on later system versions, such as Windows 7.</span></span>



| <span data-ttu-id="e477a-116">System Version</span><span class="sxs-lookup"><span data-stu-id="e477a-116">System version</span></span>                          | <span data-ttu-id="e477a-117">Scriptable-Steuerelement-CLSID</span><span class="sxs-lookup"><span data-stu-id="e477a-117">Scriptable control CLSID</span></span>             | <span data-ttu-id="e477a-118">CLSID für nicht Scriptable-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="e477a-118">Nonscriptable control CLSID</span></span>          |
|-----------------------------------------|--------------------------------------|--------------------------------------|
| <span data-ttu-id="e477a-119">Windows 8.1, Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e477a-119">Windows 8.1, Windows Server 2012 R2</span></span>     | <span data-ttu-id="e477a-120">301b94ba-5d25-4a12-bffe-3b6e7a616585</span><span class="sxs-lookup"><span data-stu-id="e477a-120">301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span> | <span data-ttu-id="e477a-121">8b918b82-7985-4c24-89df-c33ad2bbfbcd</span><span class="sxs-lookup"><span data-stu-id="e477a-121">8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span> |
| <span data-ttu-id="e477a-122">Windows 8, Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e477a-122">Windows 8, Windows Server 2012</span></span>          | <span data-ttu-id="e477a-123">5f681803-2900-4c43-a1cc-cf405404a676</span><span class="sxs-lookup"><span data-stu-id="e477a-123">5F681803-2900-4C43-A1CC-CF405404A676</span></span> | <span data-ttu-id="e477a-124">A3BC03A0-041D-42E3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="e477a-124">A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span> |
| <span data-ttu-id="e477a-125">Windows 7, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e477a-125">Windows 7, Windows Server 2008</span></span>          | <span data-ttu-id="e477a-126">A9D7038D-B5ED-472E-9C47-94BEA90A5910</span><span class="sxs-lookup"><span data-stu-id="e477a-126">A9D7038D-B5ED-472E-9C47-94BEA90A5910</span></span> | <span data-ttu-id="e477a-127">54d38bf 7-b1ef-4479-9674-1bd6ea465258</span><span class="sxs-lookup"><span data-stu-id="e477a-127">54D38BF7-B1EF-4479-9674-1BD6EA465258</span></span> |
| <span data-ttu-id="e477a-128">Windows Vista mit Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="e477a-128">Windows Vista with Service Pack 1 (SP1)</span></span> | <span data-ttu-id="e477a-129">7390f3d8-0439-4c05-91E3-cf5cb290c3d0</span><span class="sxs-lookup"><span data-stu-id="e477a-129">7390F3D8-0439-4C05-91E3-CF5CB290C3D0</span></span> | <span data-ttu-id="e477a-130">D2EA46A7-C2BF-426B-AF24-E19C44456399</span><span class="sxs-lookup"><span data-stu-id="e477a-130">D2EA46A7-C2BF-426B-AF24-E19C44456399</span></span> |
| <span data-ttu-id="e477a-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e477a-131">Windows Vista</span></span>                           | <span data-ttu-id="e477a-132">4eb89ff4-7f78-4a0f-8b8d-2bf02e94e4b2</span><span class="sxs-lookup"><span data-stu-id="e477a-132">4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2</span></span> | <span data-ttu-id="e477a-133">4eb2f 086-C818-447e-b32c-c51ce2b30d31</span><span class="sxs-lookup"><span data-stu-id="e477a-133">4EB2F086-C818-447E-B32C-C51CE2B30D31</span></span> |



 

## <a name="in-this-section"></a><span data-ttu-id="e477a-134">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="e477a-134">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="e477a-135">Einbetten des Remotedesktop ActiveX-Steuer Elements in eine Webseite</span><span class="sxs-lookup"><span data-stu-id="e477a-135">Embedding the Remote Desktop ActiveX control in a webpage</span></span>](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dd>

<span data-ttu-id="e477a-136">Beispiel, das die Verwendung der Skript fähigen Schnittstellen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="e477a-136">Example that demonstrates the use of the scriptable interfaces.</span></span>

</dd> <dt>

[<span data-ttu-id="e477a-137">Implementieren von Skript fähigen virtuellen Kanälen mithilfe von Remotedesktop-Webverbindung</span><span class="sxs-lookup"><span data-stu-id="e477a-137">Implementing scriptable virtual channels by using Remote Desktop Web Connection</span></span>](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
</dt> <dd>

<span data-ttu-id="e477a-138">Code Beispiele, die die Schritte zum Implementieren von Skript fähigen virtuellen Kanälen mit Remotedesktop-Webverbindung veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="e477a-138">Code examples that show the steps for implementing scriptable virtual channels with Remote Desktop Web Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="e477a-139">Verwenden des Remotedesktop ActiveX-Steuer Elements mit virtuellen Kanälen</span><span class="sxs-lookup"><span data-stu-id="e477a-139">Using the Remote Desktop ActiveX control with virtual channels</span></span>](using-the-remote-desktop-activex-control-with-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="e477a-140">Wenn Sie in der Remotedesktopdienste-Bereitstellung eine virtuelle Channels-Anwendung aktiviert haben, können Sie diese Anwendung für Client Computer zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="e477a-140">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make this application available to client computers.</span></span>

</dd> <dt>

[<span data-ttu-id="e477a-141">Beispiel Webseite, die im Remotedesktop ActiveX-Steuerelement enthalten ist</span><span class="sxs-lookup"><span data-stu-id="e477a-141">Sample webpage included with the Remote Desktop ActiveX control</span></span>](sample-web-page-included-with-the-remote-desktop-activex-control.md)
</dt> <dd>

<span data-ttu-id="e477a-142">Eine Beispiel Webseite (Default.htm) befindet sich im Verzeichnis, in dem Remotedesktop-Webverbindung installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e477a-142">A sample webpage (Default.htm) is in the directory where Remote Desktop Web Connection is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="e477a-143">Bereitstellen der RDP-Client Sicherheit</span><span class="sxs-lookup"><span data-stu-id="e477a-143">Providing for RDP client security</span></span>](providing-for-rdp-client-security.md)
</dt> <dd>

<span data-ttu-id="e477a-144">Einige Eigenschaften des Remotedesktop ActiveX-Steuerelement Objekts sind auf bestimmte Internet Explorer-URL-Sicherheitszonen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="e477a-144">Some properties of the Remote Desktop ActiveX control object are restricted to specific Internet Explorer URL security zones.</span></span>

</dd> <dt>

[<span data-ttu-id="e477a-145">Deaktivieren von Remotedesktopdienste Features</span><span class="sxs-lookup"><span data-stu-id="e477a-145">Disabling Remote Desktop Services features</span></span>](disabling-terminal-services-features.md)
</dt> <dd>

<span data-ttu-id="e477a-146">Zur Erhöhung der Sicherheit können Sie Remotedesktopdienste Funktionen deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="e477a-146">For enhanced security, you might choose to disable Remote Desktop Services features.</span></span>

</dd> </dl>

<span data-ttu-id="e477a-147">Weitere Informationen zur Beispiel Webseite, die in der Installation des Remotedesktop ActiveX-Steuer Elements enthalten ist, finden Sie unter [Sample-Webseite, die im Remotedesktop ActiveX-Steuerelement enthalten](sample-web-page-included-with-the-remote-desktop-activex-control.md)ist.</span><span class="sxs-lookup"><span data-stu-id="e477a-147">For more information about the sample webpage that is included with the installation of the Remote Desktop ActiveX control, see [Sample webpage included with the Remote Desktop ActiveX control](sample-web-page-included-with-the-remote-desktop-activex-control.md).</span></span>

 

 




