---
title: Verwenden von Remotedesktopdienste
description: Erfahren Sie, wie Sie in der Remotedesktopdienste Umgebung programmieren und Remotedesktopdienste (ehemals Terminaldienstetechnologie) mithilfe Remotedesktop-Webverbindung auf das Web erweitern.
ms.assetid: 17a8055c-3fde-4ba0-9ed9-af0ebe0a36b9
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste mit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac575a89d1ae8c7c065199aca136f2f0e5fc7459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338192"
---
# <a name="using-remote-desktop-services"></a><span data-ttu-id="cbbcc-104">Verwenden von Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="cbbcc-104">Using Remote Desktop Services</span></span>

<span data-ttu-id="cbbcc-105">In den folgenden Abschnitten wird beschrieben, wie Sie in der Remotedesktopdienste Umgebung programmieren und wie Sie Remotedesktopdienste (ehemals Terminaldienstetechnologie) mithilfe Remotedesktop-Webverbindung auf das Web erweitern.</span><span class="sxs-lookup"><span data-stu-id="cbbcc-105">The following sections describe how to program in the Remote Desktop Services environment and how to extend Remote Desktop Services (formerly known as Terminal Services) technology to the web by using Remote Desktop Web Connection.</span></span> <span data-ttu-id="cbbcc-106">Wenn Sie nach Benutzerinformationen für Remotedesktop-Verbindungen suchen, finden Sie weitere Informationen unter [Herstellen einer Verbindung mit einem anderen Computer mithilfe Remotedesktopverbindung](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).</span><span class="sxs-lookup"><span data-stu-id="cbbcc-106">If you are looking for user information for Remote Desktop connections, See [Connect to another computer using Remote Desktop Connection](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).</span></span>

> [!Note]  
> <span data-ttu-id="cbbcc-107">Dieses Thema ist für Softwareentwickler konzipiert.</span><span class="sxs-lookup"><span data-stu-id="cbbcc-107">This topic is for software developers.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="cbbcc-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="cbbcc-108">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="cbbcc-109">Erkennen, ob die Remotedesktopdienste Rolle installiert ist</span><span class="sxs-lookup"><span data-stu-id="cbbcc-109">Detecting Whether the Remote Desktop Services Role Is Installed</span></span>](detecting-whether-terminal-services-is-installed.md)
</dt> <dd>

<span data-ttu-id="cbbcc-110">C#-Codebeispiel, das eine Methode anzeigt, die **true** zurückgibt, wenn die Remotedesktopdienste Server-Rolle installiert ist und ausgeführt wird oder andernfalls **false** ist, beginnend mit Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cbbcc-110">C# code example that shows a method that returns **True** if the Remote Desktop Services server role is installed and running or **false** otherwise, beginning with Windows Server 2008.</span></span>

</dd> <dt>

[<span data-ttu-id="cbbcc-111">Erweitern des Terminal Dienste-Sitzungs Brokers</span><span class="sxs-lookup"><span data-stu-id="cbbcc-111">Extending Terminal Services Session Broker</span></span>](extending-ts-session-broker.md)
</dt> <dd>

<span data-ttu-id="cbbcc-112">Sie können den TS-Sitzungs Broker mithilfe der COM-Schnittstelle [**iwtssbplugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) erweitern.</span><span class="sxs-lookup"><span data-stu-id="cbbcc-112">You can extend TS Session Broker by using the [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) COM interface.</span></span>

</dd> <dt>

[<span data-ttu-id="cbbcc-113">Implementieren eines benutzerdefinierten audioendpunkt-Enumerators</span><span class="sxs-lookup"><span data-stu-id="cbbcc-113">Implementing a Custom Audio Endpoint Enumerator</span></span>](implementing-an-audio-endpoint-enumerator.md)
</dt> <dd>

<span data-ttu-id="cbbcc-114">Ab Windows Server 2008 R2 können Sie einen benutzerdefinierten remoteaudioendpunkt-Enumerator als Teil eines Remotedesktop Protokoll Anbieters implementieren.</span><span class="sxs-lookup"><span data-stu-id="cbbcc-114">Beginning with Windows Server 2008 R2, you can implement a custom remote audio endpoint enumerator as part of a Remote Desktop protocol provider.</span></span>

</dd> <dt>

[<span data-ttu-id="cbbcc-115">Sitzungsmoniker</span><span class="sxs-lookup"><span data-stu-id="cbbcc-115">Session Monikers</span></span>](session-monikers.md)
</dt> <dd>

<span data-ttu-id="cbbcc-116">Verteiltes com (DCOM) ermöglicht die Objekt Aktivierung pro Sitzung mithilfe eines vom System bereitgestellten sitzungsmonikers.</span><span class="sxs-lookup"><span data-stu-id="cbbcc-116">Distributed COM (DCOM) enables object activation on a per-session basis by using a system-supplied session moniker.</span></span>

</dd> <dt>

[<span data-ttu-id="cbbcc-117">Verwenden der ADSI-Erweiterung für Remotedesktopdienste Benutzerkonfiguration</span><span class="sxs-lookup"><span data-stu-id="cbbcc-117">Using the ADSI Extension for Remote Desktop Services User Configuration</span></span>](using-the-adsi-extension-for-terminal-services-user-configuration.md)
</dt> <dd>

<span data-ttu-id="cbbcc-118">Die Verwaltung Remotedesktopdienste spezifischer Benutzereigenschaften ist möglich, indem die von der ADSI-Erweiterung (Active Directory Service Interfaces) implementierten Methoden verwendet werden, die mit der Dynamic Link Library-Tsuserex.dll verpackt werden.</span><span class="sxs-lookup"><span data-stu-id="cbbcc-118">Administration of Remote Desktop Services-specific user properties is possible by using the methods implemented by the Active Directory Service Interfaces (ADSI) extension, which is packaged with the dynamic-link library Tsuserex.dll.</span></span>

</dd> <dt>

[<span data-ttu-id="cbbcc-119">Verwenden der Remotedesktopdienste-API</span><span class="sxs-lookup"><span data-stu-id="cbbcc-119">Using the Remote Desktop Services API</span></span>](using-the-terminal-services-api.md)
</dt> <dd>

<span data-ttu-id="cbbcc-120">Beschreibt, wie Sie mit der Remotedesktopdienste-API Anwendungen in einer Remotedesktopdienste Umgebung ausführen können.</span><span class="sxs-lookup"><span data-stu-id="cbbcc-120">Describes how you can use the Remote Desktop Services API to enable applications to perform tasks in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="cbbcc-121">Verwenden der Remotedesktop Virtualization-API</span><span class="sxs-lookup"><span data-stu-id="cbbcc-121">Using the Remote Desktop Virtualization API</span></span>](using-the-remote-desktop-virtualization-api.md)
</dt> <dd>

<span data-ttu-id="cbbcc-122">Entwickler können diese API verwenden, um die Logik anzupassen, die Remotedesktopverbindung Broker (RD-Verbindungsbroker) verwendet, um das beste Ziel für eine eingehende Client Verbindung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="cbbcc-122">Developers can use this API to customize the logic that Remote Desktop Connection Broker (RD Connection Broker) uses to determine the best destination for an incoming client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="cbbcc-123">WSDL-Schnittstelle für benutzerdefinierte VDI-Lösungen</span><span class="sxs-lookup"><span data-stu-id="cbbcc-123">WSDL Interface for Custom VDI Solutions</span></span>](wsdl-interface-for-custom-vdi-solutions.md)
</dt> <dd>

<span data-ttu-id="cbbcc-124">Entwickler können benutzerdefinierte Webdienste erstellen, die VDI-Lösungen (Virtual Desktop Infrastructure) verwalten.</span><span class="sxs-lookup"><span data-stu-id="cbbcc-124">Developers can create custom web services that manage virtual desktop infrastructure (VDI) solutions.</span></span>

</dd> </dl>

<span data-ttu-id="cbbcc-125">Weitere Informationen finden Sie unter [Remotedesktopdienste-Programmier Richtlinien](terminal-services-programming-guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="cbbcc-125">For more information, see [Remote Desktop Services Programming Guidelines](terminal-services-programming-guidelines.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbbcc-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cbbcc-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbbcc-127">Terminal Dienste sind jetzt Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="cbbcc-127">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[<span data-ttu-id="cbbcc-128">Erkennen der Remotedesktopdienste Umgebung</span><span class="sxs-lookup"><span data-stu-id="cbbcc-128">Detecting the Remote Desktop Services Environment</span></span>](detecting-the-terminal-services-environment.md)
</dt> </dl>

 

 




