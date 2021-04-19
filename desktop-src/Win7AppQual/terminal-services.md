---
description: .
ms.assetid: 94ac6a91-1e00-45f3-9374-3ac48ac63765
title: Remotedesktopdienste (Windows 7 und Windows Server 2008 R2 Anwendungsqualität Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46bd39785526b11ac2e4c0ede26bbb9971aadc9a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106357178"
---
# <a name="remote-desktop-services-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="72eb1-103">Remotedesktopdienste (Windows 7 und Windows Server 2008 R2 Anwendungsqualität Cookbook)</span><span class="sxs-lookup"><span data-stu-id="72eb1-103">Remote Desktop Services (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="72eb1-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="72eb1-104">Affected Platforms</span></span>

<span data-ttu-id="72eb1-105">**Server** – Windows Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="72eb1-105">**Servers** – Windows Server 2008 \| Windows Server 2008 R2</span></span>  

## <a name="description"></a><span data-ttu-id="72eb1-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72eb1-106">Description</span></span>

<span data-ttu-id="72eb1-107">Remotedesktopdienste (früher als "Terminal Services" bezeichnet) ermöglicht mehreren gleichzeitigen Benutzern den Zugriff auf Windows Server, um Anwendungs-und datenhostingdienste mithilfe von Microsoft "Presentation Virtualization"-Technologie bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="72eb1-107">Remote Desktop Services (formerly known as Terminal Services) allows multiple concurrent users to access Windows Server in order to provide application and data hosting services using Microsoft "Presentation Virtualization" technology.</span></span>

<span data-ttu-id="72eb1-108">Während die meisten 32-Bit-und 64-Bit-Anwendungen unter Windows Remotedesktopdienste ausgeführt werden, unterscheiden sich einige andere nicht erwartungsgemäß durch den Unterschied in der Plattform (mehr Benutzerumgebung, gleichzeitiger Zugriff durch mehrere Benutzer usw.).</span><span class="sxs-lookup"><span data-stu-id="72eb1-108">While most 32-bit and 64-bit applications run as is on Windows Remote Desktop Services, several others do not perform as expected due to the difference in the platform (multi-user environment, concurrent access by multiple users, and so on).</span></span>

<span data-ttu-id="72eb1-109">Weitere Informationen zur Anwendungsqualität finden Sie im Whitepaper " *Anwendungs Bereitschaft für Terminal Dienste* ".</span><span class="sxs-lookup"><span data-stu-id="72eb1-109">For further information regarding application quality, please read the *Application Readiness for Terminal Services* white paper.</span></span> <span data-ttu-id="72eb1-110">Besuchen Sie die Produktseite Remotedesktopdienste und die TS TechNet-Websites Weitere Informationen zu Remotedesktopdienste.</span><span class="sxs-lookup"><span data-stu-id="72eb1-110">Visit the Remote Desktop Services product page and the TS TechNet websites learn more about Remote Desktop Services.</span></span> <span data-ttu-id="72eb1-111">Weitere Informationen zum Entwickeln von Anwendungen für Remotedesktopdienste finden Sie in den *Programmier Richtlinien für Terminal Dienste*.</span><span class="sxs-lookup"><span data-stu-id="72eb1-111">To learn more about developing applications for Remote Desktop Services, review the *Terminal Services Programming Guidelines*.</span></span> <span data-ttu-id="72eb1-112">(Diese Ressourcen sind in einigen Sprachen und Ländern bzw. Regionen möglicherweise nicht verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="72eb1-112">(These resources may not be available in some languages and countries/regions.)</span></span>

## <a name="manifestation-of-impacts-and-their-mitigations"></a><span data-ttu-id="72eb1-113">Demonstration von Auswirkungen und deren entschärfungen</span><span class="sxs-lookup"><span data-stu-id="72eb1-113">Manifestation of Impacts and Their Mitigations</span></span>

<span data-ttu-id="72eb1-114">Drei Änderungen in Windows 7 wirken sich auf Anwendungen auf Remotedesktopdienste aus:</span><span class="sxs-lookup"><span data-stu-id="72eb1-114">Three changes in Windows 7 affect applications on Remote Desktop Services:</span></span>

-   <span data-ttu-id="72eb1-115">Windows Server 2008 R2 ist nur 64 Bit</span><span class="sxs-lookup"><span data-stu-id="72eb1-115">Windows Server 2008 R2 is 64-bit only</span></span>
-   <span data-ttu-id="72eb1-116">Pro Sitzung-IP-Virtualisierung</span><span class="sxs-lookup"><span data-stu-id="72eb1-116">Per-session IP Virtualization</span></span>
-   <span data-ttu-id="72eb1-117">MSI-basierte bereit Stellungen – benutzerspezifische Schlüssel</span><span class="sxs-lookup"><span data-stu-id="72eb1-117">MSI-based deployments – User-specific keys</span></span>

<span data-ttu-id="72eb1-118">**64-Bit nur Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="72eb1-118">**64-bit Only Windows Server 2008 R2**</span></span>

<span data-ttu-id="72eb1-119">Anwendungen, die für den 32-Bit-Server geschrieben wurden, werden im WOW-Modus ausgeführt, nicht nativ auf Windows Server 2008 R2 oder, daher auf Remotedesktopdienste.</span><span class="sxs-lookup"><span data-stu-id="72eb1-119">Applications written for 32-bit server will run in WoW mode and not natively on the Windows Server 2008 R2 or, hence, on Remote Desktop Services.</span></span> <span data-ttu-id="72eb1-120">Ausführliche Informationen finden Sie im Thema nur Windows 7 64-Bit.</span><span class="sxs-lookup"><span data-stu-id="72eb1-120">See the Windows 7 64-Bit Only topic for details.</span></span>

<span data-ttu-id="72eb1-121">*Entschärfungen für nur 64-Bit-Windows Server 2008 R2*</span><span class="sxs-lookup"><span data-stu-id="72eb1-121">*Mitigations for 64-bit only Windows Server 2008 R2*</span></span>

<span data-ttu-id="72eb1-122">Die meisten Anwendungen, die für 32-Bit geschrieben wurden, funktionieren im WOW-Modus weiterhin wie gewohnt.</span><span class="sxs-lookup"><span data-stu-id="72eb1-122">Most applications written for 32-bit will continue to work as normal in WoW mode.</span></span> <span data-ttu-id="72eb1-123">Alle neuen Anwendungen für Windows 7-Remotedesktopdienste sollten für die Bereitstellung auf 64-Bit-Plattformen entwickelt und getestet werden.</span><span class="sxs-lookup"><span data-stu-id="72eb1-123">Any new applications written for Windows 7 Remote Desktop Services should be developed and tested for deployment on 64-bit platforms.</span></span>

<span data-ttu-id="72eb1-124">**IP-Virtualisierung**</span><span class="sxs-lookup"><span data-stu-id="72eb1-124">**IP Virtualization**</span></span>

<span data-ttu-id="72eb1-125">Remotedesktop-IP-Virtualisierung ermöglicht dem Benutzer das Zuweisen von IP-Adressen zu Remote Desktop Verbindungen pro Sitzung oder pro Programm:</span><span class="sxs-lookup"><span data-stu-id="72eb1-125">Remote Desktop IP Virtualization allows the user to assign IP addresses to remote desktop connections on a per-session or per-program basis:</span></span>

-   <span data-ttu-id="72eb1-126">Wenn Sie IP-Adressen pro Sitzung zuweisen, verwenden alle Anwendungen die Sitzungs-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="72eb1-126">If you assign IP addresses on a per-session basis, all of the applications will use the session IP address.</span></span>
-   <span data-ttu-id="72eb1-127">Wenn Sie IP-Adressen pro Programm zuweisen, werden nur die angegebenen Anwendungen die Sitzungs-IP-Adresse verwenden, und die übrigen Anwendungen in der Sitzung werden nicht beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="72eb1-127">If you assign IP addresses on a per-program basis, only the specified applications will use the session IP address and the remaining applications in the session will not be affected.</span></span>
-   <span data-ttu-id="72eb1-128">Wenn Sie IP-Adressen für mehrere Programme zuweisen, wird die IP-Adresse der Sitzung gemeinsam genutzt.</span><span class="sxs-lookup"><span data-stu-id="72eb1-128">If you assign IP addresses for multiple programs, they will share a session IP address.</span></span>
-   <span data-ttu-id="72eb1-129">Wenn Sie über mehr als einen Netzwerkadapter auf dem Computer verfügen, müssen Sie auch einen davon für Remotedesktop-IP-Virtualisierung auswählen.</span><span class="sxs-lookup"><span data-stu-id="72eb1-129">If you have more than one network adapter on the computer, you must also choose one of them for Remote Desktop IP Virtualization.</span></span>

<span data-ttu-id="72eb1-130">*Entschärfungen bei der IP-Virtualisierung*</span><span class="sxs-lookup"><span data-stu-id="72eb1-130">*Mitigations for IP Virtualization*</span></span>

<span data-ttu-id="72eb1-131">Einige Programme erfordern eine eindeutige IP-Adresse für jede Instanz der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="72eb1-131">Some programs require a unique IP address for each instance of the application.</span></span> <span data-ttu-id="72eb1-132">Vor Windows Server 2008 R2 teilte jede Sitzung auf einem Remote Desktop Server die gleiche IP-Adresse, was zu Kompatibilitätsproblemen für diese Anwendungen führte.</span><span class="sxs-lookup"><span data-stu-id="72eb1-132">Prior to Windows Server 2008 R2, every session on a remote desktop server shared the same IP address, resulting in compatibility issues for these applications.</span></span> <span data-ttu-id="72eb1-133">Remotedesktop-IP-Virtualisierung können diese Anwendungen auf einem Remotedesktop Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="72eb1-133">Remote Desktop IP Virtualization allows these applications to run on a Remote Desktop Server.</span></span>

<span data-ttu-id="72eb1-134">**MSI-basierte bereit Stellungen**</span><span class="sxs-lookup"><span data-stu-id="72eb1-134">**MSI-based Deployments**</span></span>

<span data-ttu-id="72eb1-135">Die Microsoft Installer RDS-Kompatibilität ist ein neues Feature, das in Remotedesktopdienste in Windows Server 2008 R2 enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="72eb1-135">Microsoft Installer RDS Compatibility is a new feature included with Remote Desktop Services in Windows Server 2008 R2.</span></span> <span data-ttu-id="72eb1-136">Mit Remotedesktopdienste in Windows Server 2008 R2 werden Anwendungen für anwendungsspezifische Anwendungen vom Remotedesktop Server in die Warteschlange eingereiht und dann vom Microsoft Installer verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="72eb1-136">With Remote Desktop Services in Windows Server 2008 R2, per-user application installations are queued by the Remote Desktop Server and then handled by the Microsoft Installer.</span></span>

<span data-ttu-id="72eb1-137">In Windows Server 2008 R2 können Sie ein Programm auf dem Remotedesktop Server genau so installieren, wie Sie es auf einem lokalen Desktop installieren.</span><span class="sxs-lookup"><span data-stu-id="72eb1-137">In Windows Server 2008 R2, you can install a program on the Remote Desktop Server just as you would install the program on a local desktop.</span></span> <span data-ttu-id="72eb1-138">Stellen Sie jedoch sicher, dass Sie das Programm für alle Benutzer installieren und alle Komponenten des Programms lokal auf dem Remotedesktop Server installieren.</span><span class="sxs-lookup"><span data-stu-id="72eb1-138">Ensure, however, that you install the program for all users and install all components of the program locally on the Remote Desktop Server.</span></span>

<span data-ttu-id="72eb1-139">*Entschärfungen für MSI-basierte bereit Stellungen*</span><span class="sxs-lookup"><span data-stu-id="72eb1-139">*Mitigations for MSI based Deployments*</span></span>

<span data-ttu-id="72eb1-140">Vor der Windows Server 2008 R2-Version von Remotedesktopdienste unterstützte Windows jeweils nur eine Windows Installer Installation.</span><span class="sxs-lookup"><span data-stu-id="72eb1-140">Prior to the Windows Server 2008 R2 version of Remote Desktop Services, Windows supported only one Windows Installer installation at a time.</span></span> <span data-ttu-id="72eb1-141">Für Anwendungen, die benutzerspezifische Konfigurationen erfordern (z. b. Microsoft Office Word), musste ein Administrator die Anwendung vorab installieren, und Anwendungsentwickler mussten diese Anwendungen sowohl auf dem Remote Desktop Client als auch auf dem Remotedesktop-Sitzungshost testen.</span><span class="sxs-lookup"><span data-stu-id="72eb1-141">For applications that required per-user configurations, such as Microsoft Office Word, an administrator needed to pre-install the application, and application developers needed to test these applications on both the remote desktop client and the Remote Desktop Session Host.</span></span> <span data-ttu-id="72eb1-142">Mit Windows Installer RDS-Kompatibilitäts Funktion können fehlende benutzerspezifische Konfigurationen für mehrere Benutzer gleichzeitig identifiziert und installiert werden. so wird die Anwendungs Installation auf Remotedesktop Server ähnlich wie auf einem lokalen Desktop ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="72eb1-142">Windows Installer RDS Compatibility feature allows identifying and installing missing per-user configurations for multiple users simultaneously and makes the application installation experience on Remote Desktop Server similar to that on a local desktop.</span></span>

<span data-ttu-id="72eb1-143">**Windows Server 2008 R2 mit aktivierter [Remotedesktopdienste](../termserv/terminal-services-portal.md) Rolle:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="72eb1-143">**Windows Server 2008 R2 with the [Remote Desktop Services](../termserv/terminal-services-portal.md) role enabled:** Not supported.</span></span> <span data-ttu-id="72eb1-144">Eine mehrfach Paketinstallation mithilfe der [msiembeddedchainer-Tabelle](../msi/msiembeddedchainer-table.md) schlägt fehl, wenn die [Remotedesktopdienste](../termserv/terminal-services-portal.md) Rolle aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="72eb1-144">A multiple package installation using the [MsiEmbeddedChainer table](../msi/msiembeddedchainer-table.md) fails if the [Remote Desktop Services](../termserv/terminal-services-portal.md) role is enabled.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="72eb1-145">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="72eb1-145">Links to Other Resources</span></span>

-   [<span data-ttu-id="72eb1-146">Programmier Richtlinien für Terminal Dienste</span><span class="sxs-lookup"><span data-stu-id="72eb1-146">Terminal Services Programming Guidelines</span></span>](../termserv/terminal-services-programming-guidelines.md)
-   [<span data-ttu-id="72eb1-147">Startseite für das Terminal Dienste-Produkt</span><span class="sxs-lookup"><span data-stu-id="72eb1-147">Terminal Services product home page</span></span>](https://www.microsoft.com/windowsserver2008/en/us/rds-product-home.aspx)
-   [<span data-ttu-id="72eb1-148">Whitepaper zur Anwendungs Bereitschaft für Terminal Dienste</span><span class="sxs-lookup"><span data-stu-id="72eb1-148">Application Readiness for Terminal Services white paper</span></span>](/collaborate/connect-redirect)

> [!Note]  
> <span data-ttu-id="72eb1-149">Diese Ressourcen sind in einigen Sprachen und Ländern bzw. Regionen möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="72eb1-149">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
