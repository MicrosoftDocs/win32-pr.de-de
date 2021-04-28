---
description: Remotedesktopdienste (Cookbook zur Anwendungsqualität unter Windows 7 und Windows Server 2008 R2)
ms.assetid: 94ac6a91-1e00-45f3-9374-3ac48ac63765
title: Remotedesktopdienste (Cookbook zur Anwendungsqualität unter Windows 7 und Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725844d49f465c3c79dbc19fd01ec0f18b09759e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116118"
---
# <a name="remote-desktop-services-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="2f820-103">Remotedesktopdienste (Cookbook zur Anwendungsqualität unter Windows 7 und Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="2f820-103">Remote Desktop Services (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="2f820-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="2f820-104">Affected Platforms</span></span>

<span data-ttu-id="2f820-105">**Server** – Windows Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2f820-105">**Servers** – Windows Server 2008 \| Windows Server 2008 R2</span></span>  

## <a name="description"></a><span data-ttu-id="2f820-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f820-106">Description</span></span>

<span data-ttu-id="2f820-107">Remotedesktopdienste (früher als Terminaldienste bezeichnet) ermöglicht mehreren gleichzeitigen Benutzern den Zugriff auf Windows Server, um Anwendungs- und Datenhostingdienste mithilfe der Microsoft Presentation Virtualization-Technologie zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="2f820-107">Remote Desktop Services (formerly known as Terminal Services) allows multiple concurrent users to access Windows Server in order to provide application and data hosting services using Microsoft "Presentation Virtualization" technology.</span></span>

<span data-ttu-id="2f820-108">Während die meisten 32-Bit- und 64-Bit-Anwendungen wie unter Windows Remotedesktopdienste ausgeführt werden, werden einige andere aufgrund des Unterschieds in der Plattform (Umgebung mit mehreren Benutzern, gleichzeitiger Zugriff durch mehrere Benutzer und so weiter) nicht wie erwartet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f820-108">While most 32-bit and 64-bit applications run as is on Windows Remote Desktop Services, several others do not perform as expected due to the difference in the platform (multi-user environment, concurrent access by multiple users, and so on).</span></span>

<span data-ttu-id="2f820-109">Weitere Informationen zur Anwendungsqualität finden Sie im Whitepaper *Anwendungsbereitschaft für Terminaldienste.*</span><span class="sxs-lookup"><span data-stu-id="2f820-109">For further information regarding application quality, please read the *Application Readiness for Terminal Services* white paper.</span></span> <span data-ttu-id="2f820-110">Besuchen Sie die Remotedesktopdienste-Produktseite, und auf den TS TechNet-Websites erfahren Sie mehr über Remotedesktopdienste.</span><span class="sxs-lookup"><span data-stu-id="2f820-110">Visit the Remote Desktop Services product page and the TS TechNet websites learn more about Remote Desktop Services.</span></span> <span data-ttu-id="2f820-111">Weitere Informationen zum Entwickeln von Anwendungen für Remotedesktopdienste finden Sie in den Terminal Services Programming Guidelines (Richtlinien für die *Terminaldiensteprogrammierung).*</span><span class="sxs-lookup"><span data-stu-id="2f820-111">To learn more about developing applications for Remote Desktop Services, review the *Terminal Services Programming Guidelines*.</span></span> <span data-ttu-id="2f820-112">(Diese Ressourcen sind in einigen Sprachen und Ländern/Regionen möglicherweise nicht verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="2f820-112">(These resources may not be available in some languages and countries/regions.)</span></span>

## <a name="manifestation-of-impacts-and-their-mitigations"></a><span data-ttu-id="2f820-113">Abwehr von Auswirkungen und deren Entschärfungen</span><span class="sxs-lookup"><span data-stu-id="2f820-113">Manifestation of Impacts and Their Mitigations</span></span>

<span data-ttu-id="2f820-114">Drei Änderungen in Windows 7 wirken sich auf Anwendungen auf Remotedesktopdienste:</span><span class="sxs-lookup"><span data-stu-id="2f820-114">Three changes in Windows 7 affect applications on Remote Desktop Services:</span></span>

-   <span data-ttu-id="2f820-115">Windows Server 2008 R2 ist nur 64-Bit</span><span class="sxs-lookup"><span data-stu-id="2f820-115">Windows Server 2008 R2 is 64-bit only</span></span>
-   <span data-ttu-id="2f820-116">IP-Virtualisierung pro Sitzung</span><span class="sxs-lookup"><span data-stu-id="2f820-116">Per-session IP Virtualization</span></span>
-   <span data-ttu-id="2f820-117">MSI-basierte Bereitstellungen – benutzerspezifische Schlüssel</span><span class="sxs-lookup"><span data-stu-id="2f820-117">MSI-based deployments – User-specific keys</span></span>

<span data-ttu-id="2f820-118">**Nur 64-Bit-Version von Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2f820-118">**64-bit Only Windows Server 2008 R2**</span></span>

<span data-ttu-id="2f820-119">Anwendungen, die für 32-Bit-Server geschrieben wurden, werden im WoW-Modus und nicht nativ unter Windows Server 2008 R2 oder daher auf Remotedesktopdienste.</span><span class="sxs-lookup"><span data-stu-id="2f820-119">Applications written for 32-bit server will run in WoW mode and not natively on the Windows Server 2008 R2 or, hence, on Remote Desktop Services.</span></span> <span data-ttu-id="2f820-120">Weitere Informationen finden Sie im Thema Nur 64-Bit-Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2f820-120">See the Windows 7 64-Bit Only topic for details.</span></span>

<span data-ttu-id="2f820-121">*Risikominderungen nur für 64-Bit-Versionen von Windows Server 2008 R2*</span><span class="sxs-lookup"><span data-stu-id="2f820-121">*Mitigations for 64-bit only Windows Server 2008 R2*</span></span>

<span data-ttu-id="2f820-122">Die meisten Anwendungen, die für 32-Bit geschrieben wurden, funktionieren im WoW-Modus weiterhin wie gewohnt.</span><span class="sxs-lookup"><span data-stu-id="2f820-122">Most applications written for 32-bit will continue to work as normal in WoW mode.</span></span> <span data-ttu-id="2f820-123">Alle neuen Anwendungen, die für Windows 7 Remotedesktopdienste geschrieben wurden, sollten für die Bereitstellung auf 64-Bit-Plattformen entwickelt und getestet werden.</span><span class="sxs-lookup"><span data-stu-id="2f820-123">Any new applications written for Windows 7 Remote Desktop Services should be developed and tested for deployment on 64-bit platforms.</span></span>

<span data-ttu-id="2f820-124">**IP-Virtualisierung**</span><span class="sxs-lookup"><span data-stu-id="2f820-124">**IP Virtualization**</span></span>

<span data-ttu-id="2f820-125">Remotedesktop-IP-Virtualisierung ermöglicht es dem Benutzer, Remotedesktopverbindungen pro Sitzung oder pro Programm IP-Adressen zuzuweisen:</span><span class="sxs-lookup"><span data-stu-id="2f820-125">Remote Desktop IP Virtualization allows the user to assign IP addresses to remote desktop connections on a per-session or per-program basis:</span></span>

-   <span data-ttu-id="2f820-126">Wenn Sie IP-Adressen pro Sitzung zuweisen, verwenden alle Anwendungen die Sitzungs-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="2f820-126">If you assign IP addresses on a per-session basis, all of the applications will use the session IP address.</span></span>
-   <span data-ttu-id="2f820-127">Wenn Sie pro Programm IP-Adressen zuweisen, verwenden nur die angegebenen Anwendungen die Sitzungs-IP-Adresse, und die verbleibenden Anwendungen in der Sitzung sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="2f820-127">If you assign IP addresses on a per-program basis, only the specified applications will use the session IP address and the remaining applications in the session will not be affected.</span></span>
-   <span data-ttu-id="2f820-128">Wenn Sie IP-Adressen für mehrere Programme zuweisen, wird eine Sitzungs-IP-Adresse gemeinsam verwendet.</span><span class="sxs-lookup"><span data-stu-id="2f820-128">If you assign IP addresses for multiple programs, they will share a session IP address.</span></span>
-   <span data-ttu-id="2f820-129">Wenn auf dem Computer mehrere Netzwerkadapter installiert sind, müssen Sie auch einen netzwerkadapter für Remotedesktop-IP-Virtualisierung auswählen.</span><span class="sxs-lookup"><span data-stu-id="2f820-129">If you have more than one network adapter on the computer, you must also choose one of them for Remote Desktop IP Virtualization.</span></span>

<span data-ttu-id="2f820-130">*Entschärfungen für DIE IP-Virtualisierung*</span><span class="sxs-lookup"><span data-stu-id="2f820-130">*Mitigations for IP Virtualization*</span></span>

<span data-ttu-id="2f820-131">Einige Programme erfordern eine eindeutige IP-Adresse für jede Instanz der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2f820-131">Some programs require a unique IP address for each instance of the application.</span></span> <span data-ttu-id="2f820-132">Vor Windows Server 2008 R2 hat jede Sitzung auf einem Remotedesktopserver dieselbe IP-Adresse gemeinsam genutzt, was zu Kompatibilitätsproblemen für diese Anwendungen führt.</span><span class="sxs-lookup"><span data-stu-id="2f820-132">Prior to Windows Server 2008 R2, every session on a remote desktop server shared the same IP address, resulting in compatibility issues for these applications.</span></span> <span data-ttu-id="2f820-133">Remotedesktop-IP-Virtualisierung ermöglicht die Ausführung dieser Anwendungen auf einem Remotedesktop Server.</span><span class="sxs-lookup"><span data-stu-id="2f820-133">Remote Desktop IP Virtualization allows these applications to run on a Remote Desktop Server.</span></span>

<span data-ttu-id="2f820-134">**MSI-basierte Bereitstellungen**</span><span class="sxs-lookup"><span data-stu-id="2f820-134">**MSI-based Deployments**</span></span>

<span data-ttu-id="2f820-135">Die RDS-Kompatibilität von Microsoft Installer ist ein neues Feature, das in Remotedesktopdienste in Windows Server 2008 R2 enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="2f820-135">Microsoft Installer RDS Compatibility is a new feature included with Remote Desktop Services in Windows Server 2008 R2.</span></span> <span data-ttu-id="2f820-136">Mit Remotedesktopdienste in Windows Server 2008 R2 werden Anwendungsinstallationen pro Benutzer vom Remotedesktop Server in die Warteschlange eingereiht und dann vom Microsoft Installer verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="2f820-136">With Remote Desktop Services in Windows Server 2008 R2, per-user application installations are queued by the Remote Desktop Server and then handled by the Microsoft Installer.</span></span>

<span data-ttu-id="2f820-137">In Windows Server 2008 R2 können Sie ein Programm auf dem Remotedesktop Server genauso installieren wie auf einem lokalen Desktop.</span><span class="sxs-lookup"><span data-stu-id="2f820-137">In Windows Server 2008 R2, you can install a program on the Remote Desktop Server just as you would install the program on a local desktop.</span></span> <span data-ttu-id="2f820-138">Stellen Sie jedoch sicher, dass Sie das Programm für alle Benutzer installieren und alle Komponenten des Programms lokal auf dem Remotedesktop Server installieren.</span><span class="sxs-lookup"><span data-stu-id="2f820-138">Ensure, however, that you install the program for all users and install all components of the program locally on the Remote Desktop Server.</span></span>

<span data-ttu-id="2f820-139">*Entschärfungen für MSI-basierte Bereitstellungen*</span><span class="sxs-lookup"><span data-stu-id="2f820-139">*Mitigations for MSI based Deployments*</span></span>

<span data-ttu-id="2f820-140">Vor der Windows Server 2008 R2-Version von Remotedesktopdienste unterstützte Windows nur eine installation Windows Installer gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="2f820-140">Prior to the Windows Server 2008 R2 version of Remote Desktop Services, Windows supported only one Windows Installer installation at a time.</span></span> <span data-ttu-id="2f820-141">Für Anwendungen, die benutzerspezifische Konfigurationen erforderten, z. B. Microsoft Office Word, musste ein Administrator die Anwendung vorab installieren, und Anwendungsentwickler mussten diese Anwendungen sowohl auf dem Remotedesktopclient als auch auf dem Remotedesktop-Sitzungshost.</span><span class="sxs-lookup"><span data-stu-id="2f820-141">For applications that required per-user configurations, such as Microsoft Office Word, an administrator needed to pre-install the application, and application developers needed to test these applications on both the remote desktop client and the Remote Desktop Session Host.</span></span> <span data-ttu-id="2f820-142">Windows Installer RDS-Kompatibilitätsfeature ermöglicht es, fehlende Konfigurationen pro Benutzer für mehrere Benutzer gleichzeitig zu identifizieren und zu installieren, und die Anwendungsinstallation auf Remotedesktop Server ähnelt der auf einem lokalen Desktop.</span><span class="sxs-lookup"><span data-stu-id="2f820-142">Windows Installer RDS Compatibility feature allows identifying and installing missing per-user configurations for multiple users simultaneously and makes the application installation experience on Remote Desktop Server similar to that on a local desktop.</span></span>

<span data-ttu-id="2f820-143">**Windows Server 2008 R2 mit [aktivierter Remotedesktopdienste](../termserv/terminal-services-portal.md) Rolle:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2f820-143">**Windows Server 2008 R2 with the [Remote Desktop Services](../termserv/terminal-services-portal.md) role enabled:** Not supported.</span></span> <span data-ttu-id="2f820-144">Eine Installation mehrerer Pakete mithilfe der [MsiEmbeddedChainer-Tabelle](../msi/msiembeddedchainer-table.md) schlägt fehl, wenn [die](../termserv/terminal-services-portal.md) Remotedesktopdienste aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2f820-144">A multiple package installation using the [MsiEmbeddedChainer table](../msi/msiembeddedchainer-table.md) fails if the [Remote Desktop Services](../termserv/terminal-services-portal.md) role is enabled.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="2f820-145">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2f820-145">Links to Other Resources</span></span>

-   [<span data-ttu-id="2f820-146">Programmierrichtlinien für Terminaldienste</span><span class="sxs-lookup"><span data-stu-id="2f820-146">Terminal Services Programming Guidelines</span></span>](../termserv/terminal-services-programming-guidelines.md)
-   [<span data-ttu-id="2f820-147">Terminal services product home page (Produkt-Homepage der Terminaldienste)</span><span class="sxs-lookup"><span data-stu-id="2f820-147">Terminal Services product home page</span></span>](https://www.microsoft.com/windowsserver2008/en/us/rds-product-home.aspx)
-   [<span data-ttu-id="2f820-148">Whitepaper "Anwendungsbereitschaft für Terminaldienste"</span><span class="sxs-lookup"><span data-stu-id="2f820-148">Application Readiness for Terminal Services white paper</span></span>](/collaborate/connect-redirect)

> [!Note]  
> <span data-ttu-id="2f820-149">Diese Ressourcen sind in einigen Sprachen und Ländern/Regionen möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2f820-149">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
