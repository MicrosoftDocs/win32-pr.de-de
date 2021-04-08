---
title: Neues in Windows Server 2008 R2
description: Windows Server 2008 R2 führt die folgenden neuen Programmier Elemente für Remotedesktopdienste ein.
ms.assetid: 605a9a34-11fa-433a-9ccd-8368c75b10f0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fec9c29a142d8c97a17d4a73ee1015f84702851
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "103948388"
---
# <a name="whats-new-in-windows-server-2008-r2"></a><span data-ttu-id="9b435-103">Neues in Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9b435-103">What's New in Windows Server 2008 R2</span></span>

<span data-ttu-id="9b435-104">Windows Server 2008 R2 führt die folgenden neuen Programmier Elemente für Remotedesktopdienste ein.</span><span class="sxs-lookup"><span data-stu-id="9b435-104">Windows Server 2008 R2 introduces the following new programming elements for Remote Desktop Services.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b435-105">Terminal Dienste sind jetzt Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="9b435-105">Terminal Services Is Now Remote Desktop Services</span></span><br/></td>
<td><span data-ttu-id="9b435-106">Terminal Dienste wurde Remotedesktopdienste umbenannt.</span><span class="sxs-lookup"><span data-stu-id="9b435-106">Terminal Services has been renamed Remote Desktop Services.</span></span> <span data-ttu-id="9b435-107">Ein Server, auf dem der Rollen Dienst Remotedesktop-Sitzungshost (RD-Sitzungshost) installiert ist, wird jetzt als RD-Sitzungshost Server anstelle eines Terminal Servers bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9b435-107">A server that has the Remote Desktop Session Host (RD Session Host) role service installed is now called an RD Session Host server, instead of a terminal server.</span></span><br/>
<ul>
<li><span data-ttu-id="9b435-108"><a href="terminal-services-is-now-remote-desktop-services.md">Terminal Dienste sind jetzt Remotedesktopdienste</a></span><span class="sxs-lookup"><span data-stu-id="9b435-108"><a href="terminal-services-is-now-remote-desktop-services.md">Terminal Services Is Now Remote Desktop Services</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b435-109">Remotedesktop virtualisierungsapi</span><span class="sxs-lookup"><span data-stu-id="9b435-109">Remote Desktop Virtualization API</span></span><br/></td>
<td><span data-ttu-id="9b435-110">Die Remotedesktop virtualisierungsapi bietet Enumerationen, Schnittstellen und Strukturen, die Sie verwenden können, um benutzerdefinierte Plug-ins zu erstellen, die die Standard Umleitungs Logik von Remotedesktopverbindung Broker (RD-Verbindungsbroker) überschreiben.</span><span class="sxs-lookup"><span data-stu-id="9b435-110">The Remote Desktop Virtualization API provides enumerations, interfaces, and structures that you can use to create custom plug-ins that override the standard redirection logic of Remote Desktop Connection Broker (RD Connection Broker).</span></span> <span data-ttu-id="9b435-111">RD-Verbindungsbroker (ehemals TS-Sitzungs Broker) wurde erweitert, um Verbindungen mit virtuellen Maschinen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9b435-111">RD Connection Broker (formerly known as TS Session Broker) was expanded to support connections to virtual machines.</span></span><br/>
<ul>
<li><span data-ttu-id="9b435-112"><a href="using-the-remote-desktop-virtualization-api.md">Verwenden der Remotedesktop Virtualization-API</a></span><span class="sxs-lookup"><span data-stu-id="9b435-112"><a href="using-the-remote-desktop-virtualization-api.md">Using the Remote Desktop Virtualization API</a></span></span></li>
<li><span data-ttu-id="9b435-113"><a href="terminal-services-virtualization-api-reference.md">Referenz zur Remotedesktop virtualisierungsapi</a></span><span class="sxs-lookup"><span data-stu-id="9b435-113"><a href="terminal-services-virtualization-api-reference.md">Remote Desktop Virtualization API Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b435-114">Remotedesktopprotokoll Anbieter</span><span class="sxs-lookup"><span data-stu-id="9b435-114">Remote Desktop Protocol Provider</span></span><br/></td>
<td><span data-ttu-id="9b435-115">Die Remotedesktopprotokoll Anbieter-API kann verwendet werden, um ein Protokoll zu erstellen, mit dem die Interaktion zwischen dem Remotedesktopdienste-Dienst und den Desktop Clients angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="9b435-115">The Remote Desktop Protocol Provider API can be used to create a protocol that customizes the interaction between the Remote Desktop Services service and desktop clients.</span></span><br/>
<ul>
<li><span data-ttu-id="9b435-116"><a href="creating-a-custom-remote-protocol.md">Erstellen eines Remotedesktopprotokoll Anbieters</a></span><span class="sxs-lookup"><span data-stu-id="9b435-116"><a href="creating-a-custom-remote-protocol.md">Creating a Remote Desktop Protocol Provider</a></span></span></li>
<li><span data-ttu-id="9b435-117"><a href="custom-remote-protocol-reference.md">Remotedesktopprotokoll Anbieter Referenz</a></span><span class="sxs-lookup"><span data-stu-id="9b435-117"><a href="custom-remote-protocol-reference.md">Remote Desktop Protocol Provider Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b435-118">Remotedesktopdienste audioendpoint-API</span><span class="sxs-lookup"><span data-stu-id="9b435-118">Remote Desktop Services AudioEndpoint API</span></span><br/></td>
<td><span data-ttu-id="9b435-119">Die Remotedesktopdienste audioendpoint-API unterstützt Enumeration, Schnittstellen und Strukturen für die audioendpunkt-Registrierung und den Datentransport.</span><span class="sxs-lookup"><span data-stu-id="9b435-119">The Remote Desktop Services AudioEndpoint API supports enumeration, interfaces, and structures for audio endpoint registration and data transport.</span></span><br/>
<ul>
<li><span data-ttu-id="9b435-120"><a href="terminal-services-audioendpoint-api-reference.md">Remotedesktopdienste audioendpoint-API-Referenz</a></span><span class="sxs-lookup"><span data-stu-id="9b435-120"><a href="terminal-services-audioendpoint-api-reference.md">Remote Desktop Services AudioEndpoint API Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b435-121">RemoteApp-und Desktopverbindungsverwaltung Dienst-API</span><span class="sxs-lookup"><span data-stu-id="9b435-121">RemoteApp and Desktop Connection Management Service API</span></span><br/></td>
<td><span data-ttu-id="9b435-122">Die RemoteApp-und Desktopverbindungsverwaltung Service-API unterstützt Schnittstellen und Strukturen, die Sie verwenden können, um eine benutzerdefinierte Filterung von Ressourcen durchzuführen und Unterstützung für Dateitypen bereitzustellen, die in Windows Server 2008 R2 nicht nativ unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="9b435-122">The RemoteApp and Desktop Connection Management Service API supports interfaces and structures that you can use to perform custom filtering of resources and provide support for file types that are not natively supported in Windows Server 2008 R2.</span></span><br/>
<ul>
<li><span data-ttu-id="9b435-123"><a href="centralized-publishing-api-reference.md">RemoteApp-und Desktopverbindungsverwaltung Dienst-API-Referenz</a></span><span class="sxs-lookup"><span data-stu-id="9b435-123"><a href="centralized-publishing-api-reference.md">RemoteApp and Desktop Connection Management Service API Reference</a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 





