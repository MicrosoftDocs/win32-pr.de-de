---
title: Remotezugriff
description: Verwenden Sie RAS (Remote Access Service), um Client Anwendungen zu erstellen.
ms.assetid: 4e6c04d4-f989-4248-901f-ec15f61582da
keywords:
- RAS-Dienst RAS
- RAS-RAS
- RAS-Dienst-RAS, Startseite
- RAS-RAS, siehe Remote Zugriff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a4b1c06656b51395c8c4fc666e59d6115bd839
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101298"
---
# <a name="remote-access"></a><span data-ttu-id="c1b7b-107">Remotezugriff</span><span class="sxs-lookup"><span data-stu-id="c1b7b-107">Remote Access</span></span>

## <a name="purpose"></a><span data-ttu-id="c1b7b-108">Zweck</span><span class="sxs-lookup"><span data-stu-id="c1b7b-108">Purpose</span></span>

<span data-ttu-id="c1b7b-109">Verwenden Sie RAS (Remote Access Service), um Client Anwendungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-109">Use Remote Access Service (RAS) to create client applications.</span></span> <span data-ttu-id="c1b7b-110">Diese Anwendungen zeigen allgemeine RAS-Dialogfelder an, verwalten RAS-Verbindungen und-Geräte und bearbeiten Telefonbucheinträge.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-110">These applications display RAS common dialog boxes, manage remote access connections and devices, and manipulate phone-book entries.</span></span> <span data-ttu-id="c1b7b-111">RAS bietet auch die nächste Generation von Serverfunktionen für den RAS-Dienst (RAS) für Windows.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-111">RAS also provides the next generation of server functionality for the Remote Access Service (RAS) for Windows.</span></span> <span data-ttu-id="c1b7b-112">Die RRAS-Server Funktion folgt und baut auf dem RAS-Dienst (Remote Access Service) auf.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-112">The RRAS server functionality follows and builds upon the Remote Access Service (RAS).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="c1b7b-113">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="c1b7b-113">Where applicable</span></span>

<span data-ttu-id="c1b7b-114">Der RAS-Dienst ist in jeder Computerumgebung anwendbar, in der eine WAN-Verbindung (Wide Area Network) oder ein virtuelles privates Netzwerk (VPN) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-114">The Remote Access Service is applicable in any computing environment that uses a Wide Area Network (WAN) link or a Virtual Private Network (VPN).</span></span> <span data-ttu-id="c1b7b-115">RAS ermöglicht das Herstellen einer Verbindung zwischen einem Remote Client Computer und einem Netzwerkserver über eine WAN-Verbindung oder ein VPN.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-115">RAS makes it possible to connect a remote client computer to a network server over a WAN link or a VPN.</span></span> <span data-ttu-id="c1b7b-116">Der Remote Computer fungiert dann im LAN des Servers, als wäre der Remote Computer direkt mit dem LAN verbunden.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-116">The remote computer then functions on the server's LAN as though the remote computer was connected to the LAN directly.</span></span> <span data-ttu-id="c1b7b-117">Mithilfe der RAS-API können Programmierer Programm gesteuert auf die Features von RAS zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-117">The RAS API enables programmers to access the features of RAS programmatically.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="c1b7b-118">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="c1b7b-118">Developer audience</span></span>

<span data-ttu-id="c1b7b-119">Die RAS-API ist für die Verwendung durch C/C++-Programmierer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-119">The RAS API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="c1b7b-120">Microsoft Visual Basic Programmierer können die API auch nützlich finden.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-120">Microsoft Visual Basic programmers may also find the API useful.</span></span> <span data-ttu-id="c1b7b-121">Programmierer sollten mit den Netzwerk Konzepten vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-121">Programmers should be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c1b7b-122">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="c1b7b-122">Run-time requirements</span></span>

<span data-ttu-id="c1b7b-123">Einige der Funktionen in der RAS-API werden nur auf Netzwerkservern unterstützt, und andere Funktionen werden nur auf Netzwerk Clients unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-123">Some of the functions in the RAS API are supported only on network servers and other functions are supported only on network clients.</span></span> <span data-ttu-id="c1b7b-124">Spezifischere Informationen dazu, welche Betriebssysteme eine bestimmte Funktion unterstützen, finden Sie in den Abschnitten zu den Anforderungen in der-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-124">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

<span data-ttu-id="c1b7b-125">Die [erweiterte RAS-Funktionalität](function-comparison-windows-2000-versus-rras-redistributable.md) von RRAS ist für Windows NT Server 4,0 verfügbar, indem die [weitervertreibbare RRAS](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp)-Datei installiert wird.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-125">The [enhanced RAS functionality](function-comparison-windows-2000-versus-rras-redistributable.md) of RRAS is available for Windows NT Server 4.0 by installing the [RRAS redistributable](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp).</span></span> <span data-ttu-id="c1b7b-126">Die gesamte Funktionalität von RRAS ist in Windows 2000 Server, Windows Server 2003 und Windows Server 2008 integriert.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-126">All the functionality of RRAS is incorporated into Windows 2000 Server, Windows Server 2003, and Windows Server 2008.</span></span> <span data-ttu-id="c1b7b-127">RRAS-Anwendungen können nicht auf Windows NT-Arbeitsstationen 4,0 oder Client Betriebssystemen wie Windows 95 ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-127">RRAS applications cannot run on Windows NT Workstation 4.0 or on client operating systems, such as Windows 95.</span></span> <span data-ttu-id="c1b7b-128">Spezifischere Informationen dazu, welche Betriebssysteme eine bestimmte Funktion unterstützen, finden Sie in den Abschnitten zu den Anforderungen in der-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-128">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c1b7b-129">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c1b7b-129">In this section</span></span>



| <span data-ttu-id="c1b7b-130">Thema</span><span class="sxs-lookup"><span data-stu-id="c1b7b-130">Topic</span></span>                                                                                             | <span data-ttu-id="c1b7b-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1b7b-131">Description</span></span>                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1b7b-132">RAS-Dienst</span><span class="sxs-lookup"><span data-stu-id="c1b7b-132">Remote Access Service</span></span>](about-remote-access-service.md)<br/>                               | <span data-ttu-id="c1b7b-133">RAS-Dienst (RAS) bietet Remote Zugriffs Funktionen für Client Anwendungen auf Computern, auf denen Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-133">Remote Access Service (RAS) provides remote access capabilities to client applications on computers running Windows.</span></span><br/>                                                                                          |
| [<span data-ttu-id="c1b7b-134">Remote Zugriffs Dienst-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="c1b7b-134">Remote Access Service Administration</span></span>](about-remote-access-service-administration.md)<br/> | <span data-ttu-id="c1b7b-135">Die Remote Zugriffs-Dienst Verwaltung bietet eine Reihe von Funktionen zum Verwalten von Benutzerberechtigungen und Ports auf RAS-Servern.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-135">Remote Access Service Administration provides a set of functions for administering user permissions and ports on RAS servers.</span></span> <span data-ttu-id="c1b7b-136">Mithilfe dieser Funktionen können Sie eine RAS-Server-Verwaltungs Anwendung entwickeln.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-136">Using these functions, you can develop a RAS server administration application.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="c1b7b-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c1b7b-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1b7b-138">Routing</span><span class="sxs-lookup"><span data-stu-id="c1b7b-138">Routing</span></span>](routing-start-page.md)
</dt> <dt>

[<span data-ttu-id="c1b7b-139">Routing Protokolle</span><span class="sxs-lookup"><span data-stu-id="c1b7b-139">Routing Protocols</span></span>](routing-protocols-start-page.md)
</dt> </dl>

 

 





