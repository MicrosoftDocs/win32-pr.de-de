---
title: Remotedesktopdienste (Remotedesktopdienste)
description: Microsoft-Remotedesktop Services ist eine Remote-PC-Zugriffssoftware, die den Remote Desktop Zugriff unterstützt. Remotedesktopdienste verbindet mehrere Clients mit einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server.
ms.assetid: 90c40b7a-e324-43fc-a1e6-f29997ed9436
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste
- Remotedesktopdienste Remotedesktopdienste, Startseite
- Terminal Dienste finden Sie unter Remotedesktopdienste Remotedesktopdienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f39e176473c98f1e240d58592463df749a95f939
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341577"
---
# <a name="remote-desktop-services-remote-desktop-services"></a><span data-ttu-id="94787-107">Remotedesktopdienste (Remotedesktopdienste)</span><span class="sxs-lookup"><span data-stu-id="94787-107">Remote Desktop Services (Remote Desktop Services)</span></span>

## <a name="purpose"></a><span data-ttu-id="94787-108">Zweck</span><span class="sxs-lookup"><span data-stu-id="94787-108">Purpose</span></span>

<span data-ttu-id="94787-109">Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 oder Windows Server 2008 mit Remotedesktopdienste (früher als "Terminal Services" bezeichnet) ermöglichen es einem Server, mehrere gleichzeitige Client Sitzungen zu hosten.</span><span class="sxs-lookup"><span data-stu-id="94787-109">Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 with Remote Desktop Services (formerly known as Terminal Services) allow a server to host multiple, simultaneous client sessions.</span></span> <span data-ttu-id="94787-110">Remotedesktop verwendet Remotedesktopdienste Technologie, um eine Remote-Remote Sitzung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="94787-110">Remote Desktop uses Remote Desktop Services technology to allow a single session to run remotely.</span></span> <span data-ttu-id="94787-111">Ein Benutzer kann eine Verbindung mit einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server (früher als Terminal Server bezeichnet) herstellen, indem er Remotedesktopverbindung (RDC)-Client Software verwendet.</span><span class="sxs-lookup"><span data-stu-id="94787-111">A user can connect to a Remote Desktop Session Host (RD Session Host) server (formerly known as a terminal server) by using Remote Desktop Connection (RDC) client software.</span></span> <span data-ttu-id="94787-112">Der Remotedesktop-Webverbindung erweitert Remotedesktopdienste Technologie auf das Web.</span><span class="sxs-lookup"><span data-stu-id="94787-112">The Remote Desktop Web Connection extends Remote Desktop Services technology to the web.</span></span>

> [!Note]  
> <span data-ttu-id="94787-113">Dieses Thema ist für Softwareentwickler konzipiert.</span><span class="sxs-lookup"><span data-stu-id="94787-113">This topic is for software developers.</span></span> <span data-ttu-id="94787-114">Wenn Sie nach Benutzerinformationen für Remotedesktop-Verbindungen suchen, finden Sie weitere Informationen unter [Remotedesktopverbindung: häufig gestellte Fragen](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8).</span><span class="sxs-lookup"><span data-stu-id="94787-114">If you are looking for user information for Remote Desktop connections, See [Remote Desktop Connection: frequently asked questions](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="94787-115">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="94787-115">Where applicable</span></span>

<span data-ttu-id="94787-116">Ein Remotedesktopverbindung-Client (RDC) kann in einer Vielzahl von Formularen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="94787-116">A Remote Desktop Connection (RDC) client can exist in a variety of forms.</span></span> <span data-ttu-id="94787-117">Bei Thin Client-Hardware Geräten, auf denen ein eingebettetes Windows-basiertes Betriebssystem ausgeführt wird, kann die RDC-Client Software ausgeführt werden, um eine Verbindung mit einem RD-Sitzungshost Server herzustellen</span><span class="sxs-lookup"><span data-stu-id="94787-117">Thin-client hardware devices that run an embedded Windows-based operating system can run the RDC client software to connect to an RD Session Host server.</span></span> <span data-ttu-id="94787-118">Auf Windows-, Macintosh-oder UNIX-basierten Computern kann eine RDC-Client Software ausgeführt werden, um eine Verbindung mit einem RD-Sitzungshost Server herzustellen und Windows-basierte Anwendungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="94787-118">Windows-, Macintosh-, or UNIX-based computers can run RDC client software to connect to an RD Session Host server to display Windows-based applications.</span></span> <span data-ttu-id="94787-119">Diese Kombination aus RDC-Clients ermöglicht praktisch jedem Betriebssystem den Zugriff auf Windows-basierte Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="94787-119">This combination of RDC clients provides access to Windows-based applications from virtually any operating system.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="94787-120">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="94787-120">Developer audience</span></span>

<span data-ttu-id="94787-121">Entwickler, die Remotedesktopdienste verwenden, sollten mit den Programmiersprachen C und C++ und der Windows-basierten Programmierumgebung vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="94787-121">Developers who use Remote Desktop Services should be familiar with the C and C++ programming languages and the Windows-based programming environment.</span></span> <span data-ttu-id="94787-122">Vertrautheit mit der Client/Server-Architektur ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="94787-122">Familiarity with client/server architecture is required.</span></span> <span data-ttu-id="94787-123">Der Remotedesktop-Webverbindung enthält Skript fähige Schnittstellen zum Erstellen und Bereitstellen von Skript fähigen virtuellen Kanälen in Remotedesktopdienste Webanwendungen.</span><span class="sxs-lookup"><span data-stu-id="94787-123">The Remote Desktop Web Connection includes scriptable interfaces to create and deploy scriptable virtual channels within Remote Desktop Services web applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="94787-124">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="94787-124">Run-time requirements</span></span>

<span data-ttu-id="94787-125">Anwendungen, die Remotedesktopdienste verwenden, erfordern Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="94787-125">Applications that use Remote Desktop Services require Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, or Windows Vista.</span></span> <span data-ttu-id="94787-126">Um Remotedesktop-Webverbindung Funktionalität verwenden zu können, benötigt die Remotedesktopdienste Client Anwendung Internet Explorer und eine Verbindung mit dem World Wide Web.</span><span class="sxs-lookup"><span data-stu-id="94787-126">To use Remote Desktop Web Connection functionality, the Remote Desktop Services client application requires Internet Explorer and a connection to the World Wide Web.</span></span> <span data-ttu-id="94787-127">Informationen zu den Lauf Zeitanforderungen für ein bestimmtes Programmier Element finden Sie im Abschnitt "Anforderungen" der Referenzseite für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="94787-127">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="94787-128">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="94787-128">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="94787-129">Remotedesktop ActiveX-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="94787-129">Remote Desktop ActiveX control</span></span>](remote-desktop-activex-control.md)
</dt> <dd>

<span data-ttu-id="94787-130">Beschreibt, wie das Remotedesktop ActiveX-Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="94787-130">Describes how to use the Remote Desktop ActiveX control.</span></span>

</dd> <dt>

[<span data-ttu-id="94787-131">Remotedesktopprotokoll Anbieter-API</span><span class="sxs-lookup"><span data-stu-id="94787-131">Remote Desktop Protocol Provider API</span></span>](custom-remote-desktop-protocols.md)
</dt> <dd>

<span data-ttu-id="94787-132">Verwenden Sie die Remotedesktopprotokoll Anbieter-API, um ein Protokoll zu erstellen, um die Kommunikation zwischen dem Remotedesktopdienste-Dienst und mehreren Clients bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="94787-132">You use the Remote Desktop Protocol Provider API to create a protocol to provide communication between the Remote Desktop Services service and multiple clients.</span></span>

</dd> <dt>

[<span data-ttu-id="94787-133">Virtuelle Kanäle Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="94787-133">Remote Desktop Services virtual channels</span></span>](terminal-services-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="94787-134">*Virtuelle Kanäle* sind Software Erweiterungen, die verwendet werden können, um einer Remotedesktopdienste Anwendung funktionale Verbesserungen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="94787-134">*Virtual channels* are software extensions that can be used to add functional enhancements to a Remote Desktop Services application.</span></span>

</dd> <dt>

[<span data-ttu-id="94787-135">Remotefx-Medien Umleitungs-API</span><span class="sxs-lookup"><span data-stu-id="94787-135">RemoteFX Media Redirection API</span></span>](remotefx-api.md)
</dt> <dd>

<span data-ttu-id="94787-136">Die remotefx-Medien Umleitungs-API wird in einer Remotedesktop Sitzung verwendet, um Bereiche des Servers zu identifizieren, die schnell veränderliche Inhalte, z. b. Video, anzeigen.</span><span class="sxs-lookup"><span data-stu-id="94787-136">The RemoteFX Media Redirection API is used in a Remote Desktop session to identify areas of the server that are displaying fast changing content, such as video.</span></span> <span data-ttu-id="94787-137">Dieser Inhalt kann dann Video codiert und im codierten Format an den Client gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="94787-137">This content can then be video encoded and sent to the client in encoded format.</span></span>

</dd> <dt>

[<span data-ttu-id="94787-138">Remotedesktopverbindung Broker-Client-API</span><span class="sxs-lookup"><span data-stu-id="94787-138">Remote Desktop Connection Broker client API</span></span>](connection-broker-client-api.md)
</dt> <dd>

<span data-ttu-id="94787-139">Beschreibt, wie die Remotedesktopverbindung Broker-Client-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="94787-139">Describes how to use the Remote Desktop Connection Broker client API.</span></span>

</dd> <dt>

[<span data-ttu-id="94787-140">API-Referenz für den persönlichen Desktop Task-Agent</span><span class="sxs-lookup"><span data-stu-id="94787-140">Personal desktop task agent API reference</span></span>](task-agent-api-reference.md)
</dt> <dd>

<span data-ttu-id="94787-141">Die API für den Personal Desktop Task-Agent wird verwendet, um geplante Updates für einen persönlichen virtuellen Desktop zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="94787-141">The personal desktop task agent API is used to handle scheduled updates to a personal virtual desktop.</span></span>

</dd> <dt>

[<span data-ttu-id="94787-142">Informationen zu Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="94787-142">About Remote Desktop Services</span></span>](about-terminal-services.md)
</dt> <dd>

<span data-ttu-id="94787-143">Remotedesktopdienste (früher als "Terminal Services" bezeichnet) bietet ähnliche Funktionen wie eine Terminal basierte, zentralisierte Host-oder Mainframe-Umgebung, in der mehrere Terminals eine Verbindung mit einem Host Computer herstellen.</span><span class="sxs-lookup"><span data-stu-id="94787-143">Remote Desktop Services (formerly known as Terminal Services) provides functionality similar to a terminal-based, centralized host, or mainframe, environment in which multiple terminals connect to a host computer.</span></span>

</dd> <dt>

[<span data-ttu-id="94787-144">Remotedesktop Management Services-Anbieter</span><span class="sxs-lookup"><span data-stu-id="94787-144">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> <dd>

<span data-ttu-id="94787-145">Der RDMs-Anbieter (Remotedesktop Management Services) verwaltet virtuelle Desktop Infrastruktur (VDI)-Umgebungen.</span><span class="sxs-lookup"><span data-stu-id="94787-145">The Remote Desktop Management Services (RDMS) Provider manages virtual desktop infrastructure (VDI) environments.</span></span>

</dd> <dt>

[<span data-ttu-id="94787-146">Remotedesktopdienste Referenz</span><span class="sxs-lookup"><span data-stu-id="94787-146">Remote Desktop Services reference</span></span>](terminal-services-reference.md)
</dt> <dd>

<span data-ttu-id="94787-147">Dokumentation zu Eigenschaften Methoden, die Sie verwenden können, um Remotedesktopdienste Benutzereigenschaften zu überprüfen und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="94787-147">Documentation of property methods that you can use to examine and configure Remote Desktop Services user properties.</span></span> <span data-ttu-id="94787-148">Remotedesktopdienste Funktionen, Strukturen und Remotedesktop-Webverbindung Skript fähige-Schnittstellen werden ebenfalls dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="94787-148">Remote Desktop Services functions, structures, and Remote Desktop Web Connection scriptable interfaces are also documented.</span></span>

</dd> <dt>

[<span data-ttu-id="94787-149">Remotedesktopdienste Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="94787-149">Remote Desktop Services Shortcut Keys</span></span>](terminal-services-shortcut-keys.md)
</dt> <dd>

<span data-ttu-id="94787-150">Eine Liste der Remotedesktopdienste Tastenkombinationen.</span><span class="sxs-lookup"><span data-stu-id="94787-150">A list of the Remote Desktop Services shortcut keys.</span></span>

</dd> <dt>

[<span data-ttu-id="94787-151">WMI-Anbieter Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="94787-151">Remote Desktop Services WMI provider</span></span>](terminal-services-wmi-provider.md)
</dt> <dd>

<span data-ttu-id="94787-152">Der Remotedesktopdienste WMI-Anbieter ermöglicht programmgesteuerten Zugriff auf die Informationen und Einstellungen, die vom Microsoft Management Console (MMC)-Snap-in "Remotedesktopdienste Configuration/Connections" verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="94787-152">The Remote Desktop Services WMI provider provides programmatic access to the information and settings that are exposed by the Remote Desktop Services Configuration/Connections Microsoft Management Console (MMC) snap-in.</span></span>

</dd> <dt>

[<span data-ttu-id="94787-153">Verwenden von Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="94787-153">Using Remote Desktop Services</span></span>](using-terminal-services.md)
</dt> <dd>

<span data-ttu-id="94787-154">Erfahren Sie, wie Sie in der Remotedesktopdienste Umgebung programmieren und Remotedesktopdienste (ehemals Terminaldienstetechnologie) mithilfe Remotedesktop-Webverbindung auf das Web erweitern.</span><span class="sxs-lookup"><span data-stu-id="94787-154">How to program in the Remote Desktop Services environment and how to extend Remote Desktop Services (formerly known as Terminal Services) technology to the web by using Remote Desktop Web Connection.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="94787-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="94787-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94787-156">Terminal Dienste sind jetzt Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="94787-156">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> </dl>

 

 




