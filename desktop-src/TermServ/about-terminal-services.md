---
title: Informationen zu Remotedesktopdienste
description: Remotedesktopdienste (früher als "Terminal Services" bezeichnet) bietet ähnliche Funktionen wie eine Terminal basierte, zentralisierte Host-oder Mainframe-Umgebung, in der mehrere Terminals eine Verbindung mit einem Host Computer herstellen.
ms.assetid: 5b5b0f97-f973-4f52-a965-c9c2390e6c8d
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4644170cfca3b4bacdd6db647e35549d56844e9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340651"
---
# <a name="about-remote-desktop-services"></a><span data-ttu-id="6b16f-104">Informationen zu Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="6b16f-104">About Remote Desktop Services</span></span>

<span data-ttu-id="6b16f-105">Remotedesktopdienste (früher als "Terminal Services" bezeichnet) bietet ähnliche Funktionen wie eine Terminal basierte, zentralisierte Host-oder Mainframe-Umgebung, in der mehrere Terminals eine Verbindung mit einem Host Computer herstellen.</span><span class="sxs-lookup"><span data-stu-id="6b16f-105">Remote Desktop Services (formerly known as Terminal Services) provides functionality similar to a terminal-based, centralized host, or mainframe, environment in which multiple terminals connect to a host computer.</span></span> <span data-ttu-id="6b16f-106">Jedes Terminal stellt einen Kanal für die Eingabe und die Ausgabe zwischen einem Benutzer und dem Host Computer bereit.</span><span class="sxs-lookup"><span data-stu-id="6b16f-106">Each terminal provides a conduit for input and output between a user and the host computer.</span></span> <span data-ttu-id="6b16f-107">Ein Benutzer kann sich an einem Terminal anmelden und dann Anwendungen auf dem Host Computer ausführen, auf Dateien, Datenbanken, Netzwerkressourcen usw. zugreifen.</span><span class="sxs-lookup"><span data-stu-id="6b16f-107">A user can log on at a terminal, and then run applications on the host computer, accessing files, databases, network resources, and so on.</span></span> <span data-ttu-id="6b16f-108">Jede Terminalsitzung ist unabhängig, und das Host Betriebssystem verwaltet Konflikte zwischen mehreren Benutzern für gemeinsame Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="6b16f-108">Each terminal session is independent, with the host operating system managing conflicts between multiple users contending for shared resources.</span></span>

<span data-ttu-id="6b16f-109">Der Hauptunterschied zwischen Remotedesktopdienste und der herkömmlichen Main Frame-Umgebung besteht darin, dass die dummyterminals in einer Main Frame-Umgebung nur zeichenbasierte Eingaben und Ausgaben bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6b16f-109">The primary difference between Remote Desktop Services and the traditional mainframe environment is that the dumb terminals in a mainframe environment only provide character-based input and output.</span></span> <span data-ttu-id="6b16f-110">Ein-Remotedesktopverbindung (RDC)-Client oder-Emulator stellt eine komplette grafische Benutzeroberfläche bereit, einschließlich eines Windows-Betriebssystem Desktops und Unterstützung für eine Vielzahl von Eingabegeräten, z. b. Tastatur und Maus.</span><span class="sxs-lookup"><span data-stu-id="6b16f-110">A Remote Desktop Connection (RDC) client or emulator provides a complete graphical user interface including a Windows operating system desktop and support for a variety of input devices, such as a keyboard and mouse.</span></span>

<span data-ttu-id="6b16f-111">In der Remotedesktopdienste-Umgebung wird eine Anwendung vollständig auf dem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server (ehemals Terminal Server) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b16f-111">In the Remote Desktop Services environment, an application runs entirely on the Remote Desktop Session Host (RD Session Host) server (formerly known as a terminal server).</span></span> <span data-ttu-id="6b16f-112">Der RDC-Client führt keine lokale Verarbeitung der Anwendungssoftware aus.</span><span class="sxs-lookup"><span data-stu-id="6b16f-112">The RDC client performs no local processing of application software.</span></span> <span data-ttu-id="6b16f-113">Der Server überträgt die grafische Benutzeroberfläche an den Client.</span><span class="sxs-lookup"><span data-stu-id="6b16f-113">The server transmits the graphical user interface to the client.</span></span> <span data-ttu-id="6b16f-114">Der Client überträgt die Eingabe des Benutzers an den Server zurück.</span><span class="sxs-lookup"><span data-stu-id="6b16f-114">The client transmits the user's input back to the server.</span></span>

<span data-ttu-id="6b16f-115">Weitere Informationen finden Sie in den nachfolgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="6b16f-115">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6b16f-116">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="6b16f-116">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="6b16f-117">Ändern der Standardeinstellung für Geräte Umleitung</span><span class="sxs-lookup"><span data-stu-id="6b16f-117">Modify Device Redirection Default</span></span>](modify-device-redirection-default-.md)
</dt> <dd>

<span data-ttu-id="6b16f-118">Da Remotedesktop Gatewayserver versuchen, sichere Geräte Umleitungs Richtlinien zu erzwingen, bevor Sie die Client Verbindung an einen Remotedesktop-Sitzungshost Server weiterleiten, müssen Sie diese Standardeinstellung möglicherweise in einigen Fällen deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="6b16f-118">Because Remote Desktop Gateway servers attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server, you may need to disable this default in some cases.</span></span>

</dd> <dt>

[<span data-ttu-id="6b16f-119">Remotedesktopprotokoll</span><span class="sxs-lookup"><span data-stu-id="6b16f-119">Remote Desktop Protocol</span></span>](remote-desktop-protocol.md)
</dt> <dd>

<span data-ttu-id="6b16f-120">Das Microsoft-Remotedesktop Protokoll (RDP) bietet Remote Anzeige-und Eingabefunktionen über Netzwerkverbindungen für Windows-basierte Anwendungen, die auf einem Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6b16f-120">The Microsoft Remote Desktop Protocol (RDP) provides remote display and input capabilities over network connections for Windows-based applications running on a server.</span></span>

</dd> <dt>

[<span data-ttu-id="6b16f-121">Remotedesktopdienste-API</span><span class="sxs-lookup"><span data-stu-id="6b16f-121">Remote Desktop Services API</span></span>](terminal-services-api.md)
</dt> <dd>

<span data-ttu-id="6b16f-122">Die Remotedesktopdienste-API ist in erster Linie für Client/Server-Anwendungen und-Anwendungen zur Remotedesktopdienste Verwaltung nützlich.</span><span class="sxs-lookup"><span data-stu-id="6b16f-122">The Remote Desktop Services API is primarily useful to client/server applications and applications for Remote Desktop Services administration.</span></span>

</dd> <dt>

[<span data-ttu-id="6b16f-123">Remotedesktopdienste Verwaltungs Anwendungen</span><span class="sxs-lookup"><span data-stu-id="6b16f-123">Remote Desktop Services management applications</span></span>](terminal-services-management-applications.md)
</dt> <dd>

<span data-ttu-id="6b16f-124">Beschreibt die Verwaltungs Anwendungen, die von Remotedesktopdienste unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6b16f-124">Describes the management applications that Remote Desktop Services supports.</span></span>

</dd> <dt>

[<span data-ttu-id="6b16f-125">Programmier Richtlinien für Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="6b16f-125">Remote Desktop Services programming guidelines</span></span>](terminal-services-programming-guidelines.md)
</dt> <dd>

<span data-ttu-id="6b16f-126">Themen, in denen Richtlinien zum Entwickeln von Anwendungen in einer Remotedesktopdienste Umgebung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6b16f-126">Topics that provide guidelines for developing applications in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="6b16f-127">Remotedesktop Sitzungen</span><span class="sxs-lookup"><span data-stu-id="6b16f-127">Remote Desktop Sessions</span></span>](terminal-services-sessions.md)
</dt> <dd>

<span data-ttu-id="6b16f-128">Da jede Anmeldung bei einem Remotedesktopverbindung-Client (RDC) eine separate Sitzungs-ID erhält, ist die Benutzer Darstellung ähnlich wie bei mehreren Computern gleichzeitig. beispielsweise ein Office-Computer und ein Heimcomputer.</span><span class="sxs-lookup"><span data-stu-id="6b16f-128">Because each logon to a Remote Desktop Connection (RDC) client receives a separate session ID, the user-experience is similar to being logged on to multiple computers at the same time; for example, an office computer and a home computer.</span></span>

</dd> <dt>

[<span data-ttu-id="6b16f-129">Remotedesktop-Webverbindung</span><span class="sxs-lookup"><span data-stu-id="6b16f-129">Remote Desktop Web Connection</span></span>](remote-desktop-web-connection.md)
</dt> <dd>

<span data-ttu-id="6b16f-130">Hier wird beschrieben, wie ein Remotedesktop-Webverbindung installiert wird.</span><span class="sxs-lookup"><span data-stu-id="6b16f-130">Describes how to install a Remote Desktop Web Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="6b16f-131">Ressourcen auf einem Remotedesktop-Sitzungshost Server</span><span class="sxs-lookup"><span data-stu-id="6b16f-131">Resources on a Remote Desktop Session Host Server</span></span>](resources-on-a-terminal-server.md)
</dt> <dd>

<span data-ttu-id="6b16f-132">Mehrere Benutzer können sich gleichzeitig bei einem einzelnen RD-Sitzungshost Server anmelden und die Hardware-und Software Ressourcen des Servers freigeben.</span><span class="sxs-lookup"><span data-stu-id="6b16f-132">Multiple users can log on simultaneously to a single RD Session Host server, sharing the hardware and software resources of the server.</span></span>

</dd> <dt>

[<span data-ttu-id="6b16f-133">Neues in Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="6b16f-133">What's New in Remote Desktop Services</span></span>](what-s-new-in-terminal-services.md)
</dt> <dd>

<span data-ttu-id="6b16f-134">Themen, in denen die Änderungen in den einzelnen Releases der Remotedesktopdienste-API beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6b16f-134">Topics that describe the changes in each release of the Remote Desktop Services API.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="6b16f-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6b16f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b16f-136">Herstellen einer Verbindung mit einem anderen Computer mithilfe von Remotedesktopverbindung</span><span class="sxs-lookup"><span data-stu-id="6b16f-136">Connect to another computer using Remote Desktop Connection</span></span>](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7)
</dt> </dl>

 

 




