---
title: Virtuelle Kanäle Remotedesktopdienste
description: Virtuelle Kanäle sind Software Erweiterungen, die verwendet werden können, um einer Remotedesktopdienste Anwendung funktionale Verbesserungen hinzuzufügen.
ms.assetid: f7bdebec-ecc3-4f28-9327-f0d2f169c142
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce78331841a41502aa337de19e9879d42d85fe1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309891"
---
# <a name="remote-desktop-services-virtual-channels"></a><span data-ttu-id="a3283-103">Virtuelle Kanäle Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="a3283-103">Remote Desktop Services virtual channels</span></span>

<span data-ttu-id="a3283-104">*Virtuelle Kanäle* sind Software Erweiterungen, die verwendet werden können, um einer Remotedesktopdienste Anwendung funktionale Verbesserungen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a3283-104">*Virtual channels* are software extensions that can be used to add functional enhancements to a Remote Desktop Services application.</span></span> <span data-ttu-id="a3283-105">Beispiele für funktionale Verbesserungen: Unterstützung für spezielle Typen von Hardware, Audiodaten oder andere Ergänzungen der Kernfunktionen, die von der Remotedesktopdienste [Remotedesktopprotokoll](remote-desktop-protocol.md) (RDP) bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a3283-105">Examples of functional enhancements might include: support for special types of hardware, audio, or other additions to the core functionality provided by the Remote Desktop Services [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP).</span></span> <span data-ttu-id="a3283-106">Das RDP-Protokoll ermöglicht die Multiplex Verwaltung mehrerer virtueller Kanäle.</span><span class="sxs-lookup"><span data-stu-id="a3283-106">The RDP protocol provides multiplexed management of multiple virtual channels.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a3283-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a3283-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="a3283-108">Verwenden von Remotedesktopdienste virtuellen Kanälen</span><span class="sxs-lookup"><span data-stu-id="a3283-108">Using Remote Desktop Services virtual channels</span></span>](using-terminal-services-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="a3283-109">Zum Implementieren eines virtuellen Kanals stellen Sie die Server-und Client Module der Anwendung eines virtuellen Kanals bereit.</span><span class="sxs-lookup"><span data-stu-id="a3283-109">To implement a virtual channel, you provide the server and client modules of a virtual channel's application.</span></span>

</dd> <dt>

[<span data-ttu-id="a3283-110">Referenz zu dynamischen virtuellen Kanälen</span><span class="sxs-lookup"><span data-stu-id="a3283-110">Dynamic virtual channels reference</span></span>](dynamic-virtual-channels-reference.md)
</dt> <dd>

<span data-ttu-id="a3283-111">DVC-Client Schnittstellen (Dynamic Virtual Channel) werden von Remotedesktopdienste unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a3283-111">Dynamic virtual channel (DVC) client interfaces are supported by Remote Desktop Services.</span></span>

</dd> <dt>

[<span data-ttu-id="a3283-112">Referenz für virtuelle Grafik Kanäle</span><span class="sxs-lookup"><span data-stu-id="a3283-112">Graphics virtual channels reference</span></span>](graphics-virtual-channels-reference.md)
</dt> <dd>

<span data-ttu-id="a3283-113">Die Referenz für virtuelle Grafik Kanäle enthält Programmier Elemente, mit denen Sie einen virtuellen Grafik Kanal erstellen können.</span><span class="sxs-lookup"><span data-stu-id="a3283-113">The graphics virtual channels reference contains programming elements that enable you to create a virtual graphics channel.</span></span>

</dd> </dl>

<span data-ttu-id="a3283-114">Eine virtuelle Kanal Anwendung besteht aus zwei Teilen: einem Client Modul und einem Servermodul.</span><span class="sxs-lookup"><span data-stu-id="a3283-114">A virtual channel application has two parts, a client module and a server module.</span></span> <span data-ttu-id="a3283-115">Das Servermodul ist ein ausführbares Programm, das auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3283-115">The server module is an executable program running on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="a3283-116">Das Client Modul ist eine DLL, die beim Ausführen des RDC-Client Programms (Remotedesktopverbindung) in den Arbeitsspeicher auf dem Client Computer geladen werden muss.</span><span class="sxs-lookup"><span data-stu-id="a3283-116">The client module is a DLL that must be loaded into memory on the client computer when the Remote Desktop Connection (RDC) client program runs.</span></span>

<span data-ttu-id="a3283-117">Virtuelle Kanäle können einem Remotedesktopverbindung-Client (RDC) unabhängig vom RDP-Protokoll funktionale Verbesserungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a3283-117">Virtual channels can add functional enhancements to a Remote Desktop Connection (RDC) client, independent of the RDP protocol.</span></span> <span data-ttu-id="a3283-118">Durch die Unterstützung virtueller Kanäle können neue Funktionen hinzugefügt werden, ohne dass die Client-oder Server Software oder das RDP-Protokoll aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="a3283-118">With virtual channel support, new features can be added without having to update the client or server software, or the RDP protocol.</span></span>

<span data-ttu-id="a3283-119">Es wurden vier Hauptklassen von Benutzern von virtuellen Kanälen identifiziert:</span><span class="sxs-lookup"><span data-stu-id="a3283-119">Four major classes of users of virtual channels have been identified:</span></span>

-   <span data-ttu-id="a3283-120">Allgemeine Kernelmodustreiber, z. b. serielle oder Druckertreiber.</span><span class="sxs-lookup"><span data-stu-id="a3283-120">General kernel-mode drivers, such as serial or printer drivers.</span></span>
-   <span data-ttu-id="a3283-121">Dateisystem Umleitung (Hierbei handelt es sich nur um einen Sonderfall eines allgemeinen Kernelmodustreibers).</span><span class="sxs-lookup"><span data-stu-id="a3283-121">File system redirection (this is just a special case of a general kernel-mode driver).</span></span>
-   <span data-ttu-id="a3283-122">Benutzermodusanwendungen, z. b. Remote Ausschneiden und einfügen.</span><span class="sxs-lookup"><span data-stu-id="a3283-122">User mode applications, for example remote cut-and-paste.</span></span>
-   <span data-ttu-id="a3283-123">Audiogeräte.</span><span class="sxs-lookup"><span data-stu-id="a3283-123">Audio devices.</span></span>

<span data-ttu-id="a3283-124">Weitere Informationen finden Sie unter [Verwenden von Remotedesktopdienste virtuellen Kanälen](using-terminal-services-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="a3283-124">For more information, see [Using Remote Desktop Services Virtual Channels](using-terminal-services-virtual-channels.md).</span></span>

<span data-ttu-id="a3283-125">Wenn Sie in der Remotedesktopdienste-Bereitstellung eine virtuelle Channels-Anwendung aktiviert haben, können Sie die Anwendung auf Client Computern verfügbar machen, die über das Remotedesktop Microsoft ActiveX-Steuerelement auf den RD-Sitzungshost Server zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a3283-125">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make the application available to client computers that access the RD Session Host server by means of the Remote Desktop Microsoft ActiveX control.</span></span> <span data-ttu-id="a3283-126">Weitere Informationen finden Sie unter [Skript fähige virtuelle Kanäle](scriptable-virtual-channels.md) und [Verwenden des Remotedesktop ActiveX-Steuer Elements mit virtuellen Kanälen](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="a3283-126">For more information, see [Scriptable Virtual Channels](scriptable-virtual-channels.md) and [Using the Remote Desktop ActiveX Control with Virtual Channels](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span></span>

 

 




