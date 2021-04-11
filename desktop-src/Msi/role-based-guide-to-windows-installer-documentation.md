---
description: Windows Installer ist die empfohlene Lösung für die Installation und Einrichtung von Anwendungen unter Windows.
ms.assetid: 13f41020-5275-44cd-b26b-f45483700d8a
title: Rollenbasiertes Handbuch für Windows Installer-Dokumentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8a2138e963b6d29bd161df5e09144cf0cfd36b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041944"
---
# <a name="role-based-guide-to-windows-installer-documentation"></a><span data-ttu-id="d10fc-103">Rollenbasiertes Handbuch für Windows Installer-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="d10fc-103">Role-based Guide to Windows Installer Documentation</span></span>

<span data-ttu-id="d10fc-104">Windows Installer ist die empfohlene Lösung für die Installation und Einrichtung von Anwendungen unter Windows.</span><span class="sxs-lookup"><span data-stu-id="d10fc-104">Windows Installer is the recommended solution for the installation and setup of applications on Windows.</span></span> <span data-ttu-id="d10fc-105">Daher sind einige der in diesem SDK enthaltenen Informationen für eine Vielzahl von Software Entwicklungs-und IT-Experten von Interesse.</span><span class="sxs-lookup"><span data-stu-id="d10fc-105">Therefore, some of the information contained in this SDK will be of interest to a wide range of software development and IT professionals.</span></span> <span data-ttu-id="d10fc-106">Dieser Abschnitt dient als Leitfaden für Leser, die lieber Links zu Themen finden, die nach professionellen Rollen und allgemeinen Aufgaben Szenarios organisiert sind.</span><span class="sxs-lookup"><span data-stu-id="d10fc-106">This section is provided as a guide to readers who prefer to see links to topics organized by professional role and common task scenarios.</span></span> <span data-ttu-id="d10fc-107">Da sich die Rollen zwischen Organisationen stark voneinander unterscheiden können, sollte die folgende Gruppierung nur als Leitfaden für einen Standort betrachtet werden, um mit der Suche nach den benötigten Informationen zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="d10fc-107">Because roles can differ greatly between organizations, the following grouping should only be considered as a guide to a location to start searching for the information you need.</span></span>

-   [<span data-ttu-id="d10fc-108">Anwendungsentwickler</span><span class="sxs-lookup"><span data-stu-id="d10fc-108">Application Developers</span></span>](#application-developers)
-   [<span data-ttu-id="d10fc-109">Setup Autoren</span><span class="sxs-lookup"><span data-stu-id="d10fc-109">Setup Authors</span></span>](#setup-authors)
-   [<span data-ttu-id="d10fc-110">IT-Fachleute</span><span class="sxs-lookup"><span data-stu-id="d10fc-110">IT Professionals</span></span>](#it-professionals)
-   [<span data-ttu-id="d10fc-111">Infrastruktur Entwickler</span><span class="sxs-lookup"><span data-stu-id="d10fc-111">Infrastructure Developers</span></span>](#infrastructure-developers)

<span data-ttu-id="d10fc-112">Diese Dokumentation ist für Softwareentwickler gedacht, die Anwendungen erstellen möchten, die Windows Installer verwenden.</span><span class="sxs-lookup"><span data-stu-id="d10fc-112">This documentation is intended for software developers who want to make applications that use Windows Installer.</span></span> <span data-ttu-id="d10fc-113">Als Hauptquelle für das Referenzmaterial für das Installationsprogramm bietet das SDK Informationen zu Installationspaketen und zum Installerdienst.</span><span class="sxs-lookup"><span data-stu-id="d10fc-113">As the primary source of reference material for the installer, the SDK provides information about installation packages and the installer service.</span></span> <span data-ttu-id="d10fc-114">Es enthält umfassende Beschreibungen der Anwendungsprogrammierschnittstelle (Application Programming Interface, API) und der-Elemente der Installer-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d10fc-114">It contains complete descriptions of the application programming interface (API) and the elements of the installer database.</span></span>

<span data-ttu-id="d10fc-115">Weitere Informationen finden Sie unter [andere Quellen mit Windows Installer-Informationen](other-sources-of-windows-installer-information.md).</span><span class="sxs-lookup"><span data-stu-id="d10fc-115">For more information, see [Other Sources of Windows Installer Information](other-sources-of-windows-installer-information.md).</span></span>

## <a name="application-developers"></a><span data-ttu-id="d10fc-116">Anwendungsentwickler</span><span class="sxs-lookup"><span data-stu-id="d10fc-116">Application Developers</span></span>

<span data-ttu-id="d10fc-117">Anwendungsentwickler erstellen Anwendungen, die die Windows Installer-Anwendungsprogrammierschnittstelle aufzurufen und Windows Installer-Pakete zur Laufzeit installieren.</span><span class="sxs-lookup"><span data-stu-id="d10fc-117">Application developers create applications that call the Windows Installer application programming interface and install Windows installer packages at run time.</span></span> <span data-ttu-id="d10fc-118">Der Windows Installer kann in einer Anwendung funktionieren, z. b. bei der Selbstreparatur und bei der Installation bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="d10fc-118">The Windows Installer can do work in an application such as self-repair and installation-on-demand.</span></span> <span data-ttu-id="d10fc-119">Anwendungsentwickler führen in der Regel folgende Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="d10fc-119">Typically, application Developers do the following:</span></span>

-   <span data-ttu-id="d10fc-120">Aktivieren Sie die Installation bei Bedarf von Anwendungen zur Laufzeit in einer anderen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d10fc-120">Enable installation-on-demand of applications at run time from within another application.</span></span>

    <span data-ttu-id="d10fc-121">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-121">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-122">Verwenden von Installer-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-122">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="d10fc-123">Installationsfunktionsverweis</span><span class="sxs-lookup"><span data-stu-id="d10fc-123">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="d10fc-124">Installation bei Bedarf</span><span class="sxs-lookup"><span data-stu-id="d10fc-124">Installation-On-Demand</span></span>](installation-on-demand.md)
    -   [<span data-ttu-id="d10fc-125">Verwaltung von Komponenten</span><span class="sxs-lookup"><span data-stu-id="d10fc-125">Component Management</span></span>](component-management.md)
    -   [<span data-ttu-id="d10fc-126">Bearbeiten von Installationsprogramm Kombinationen</span><span class="sxs-lookup"><span data-stu-id="d10fc-126">Editing Installer Shortcuts</span></span>](editing-installer-shortcuts.md)
    -   [<span data-ttu-id="d10fc-127">**Oleadvtsupport (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="d10fc-127">**OLEAdvtSupport Property**</span></span>](oleadvtsupport.md)
    -   [<span data-ttu-id="d10fc-128">Platt Form Unterstützung für Ankündigungen</span><span class="sxs-lookup"><span data-stu-id="d10fc-128">Platform Support of Advertisement</span></span>](platform-support-of-advertisement.md)

-   <span data-ttu-id="d10fc-129">Aktivieren Sie die Selbstreparatur von Anwendungen, indem Sie die Komponenten bei Bedarf zur Laufzeit neu installieren.</span><span class="sxs-lookup"><span data-stu-id="d10fc-129">Enable self-repair of applications by reinstalling components as needed at run time.</span></span>

    <span data-ttu-id="d10fc-130">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-130">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-131">Verwenden von Installer-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-131">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="d10fc-132">Installationsfunktionsverweis</span><span class="sxs-lookup"><span data-stu-id="d10fc-132">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="d10fc-133">Resilienz</span><span class="sxs-lookup"><span data-stu-id="d10fc-133">Resiliency</span></span>](resiliency.md)
    -   [<span data-ttu-id="d10fc-134">Quellen Resilienz</span><span class="sxs-lookup"><span data-stu-id="d10fc-134">Source Resiliency</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="d10fc-135">Suchen nach einer unterbrochenen Funktion oder Komponente</span><span class="sxs-lookup"><span data-stu-id="d10fc-135">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="d10fc-136">Ersetzen vorhandener Dateien</span><span class="sxs-lookup"><span data-stu-id="d10fc-136">Replacing Existing Files</span></span>](replacing-existing-files.md)

-   <span data-ttu-id="d10fc-137">Anzeigen einer Benutzeroberfläche, um Benutzerinformationen und Konfigurationseinstellungen zu erfassen, wenn eine Anwendung zum ersten Mal installiert oder ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d10fc-137">Display a user interface to collect user information and configuration preferences the first time an application is installed or run.</span></span> <span data-ttu-id="d10fc-138">Die Benutzeroberfläche muss vom Setup-Autor des Windows Installer Pakets hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d10fc-138">The user interface must be added by the Setup Author of the Windows Installer package.</span></span>

    <span data-ttu-id="d10fc-139">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-139">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-140">Verwenden von Installer-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-140">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="d10fc-141">Initialisieren einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="d10fc-141">Initializing an Application</span></span>](initializing-an-application.md)
    -   [<span data-ttu-id="d10fc-142">Dialog Feld "FIRSTRUN"</span><span class="sxs-lookup"><span data-stu-id="d10fc-142">FirstRun Dialog</span></span>](firstrun-dialog.md)
    -   [<span data-ttu-id="d10fc-143">Informationen zur Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d10fc-143">About the User Interface</span></span>](about-the-user-interface.md)

-   <span data-ttu-id="d10fc-144">Erstellen Sie Anwendungen, die ein dereferenzierungsmodell verwenden, um auf Komponenten mit paralleler Funktionalität zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="d10fc-144">Create applications that use an indirection model to refer to components with parallel functionality.</span></span> <span data-ttu-id="d10fc-145">Die qualifizierten Komponenten Kategorien müssen vom Setup Autor des Windows Installer Pakets hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d10fc-145">The qualified component categories must be added by the Setup Author of the Windows Installer package.</span></span>

    <span data-ttu-id="d10fc-146">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-146">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-147">Qualifizierte Komponenten</span><span class="sxs-lookup"><span data-stu-id="d10fc-147">Qualified Components</span></span>](qualified-components.md)
    -   [<span data-ttu-id="d10fc-148">Verwenden qualifizierter Komponenten</span><span class="sxs-lookup"><span data-stu-id="d10fc-148">Using Qualified Components</span></span>](using-qualified-components.md)

-   <span data-ttu-id="d10fc-149">Verwenden Sie private und parallele Assemblys, um Anwendungen zu isolieren und DLL-Konflikte zu verringern.</span><span class="sxs-lookup"><span data-stu-id="d10fc-149">Use private and side-by-side assemblies to isolate applications and reduce DLL conflicts.</span></span>

    <span data-ttu-id="d10fc-150">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-150">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-151">Assemblys</span><span class="sxs-lookup"><span data-stu-id="d10fc-151">Assemblies</span></span>](assemblies.md)
    -   [<span data-ttu-id="d10fc-152">Von Windows Installer geschriebene assemblyregistrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="d10fc-152">Assembly Registry Keys Written by Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="d10fc-153">Installieren von Win32-Assemblys für die parallele Freigabe unter Windows XP</span><span class="sxs-lookup"><span data-stu-id="d10fc-153">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
    -   [<span data-ttu-id="d10fc-154">Installieren von Win32-Assemblys für die private Verwendung einer Anwendung unter Windows XP</span><span class="sxs-lookup"><span data-stu-id="d10fc-154">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)
    -   [<span data-ttu-id="d10fc-155">MsiAssembly-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-155">MsiAssembly Table</span></span>](msiassembly-table.md)
    -   [<span data-ttu-id="d10fc-156">MsiAssemblyName-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-156">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)
    -   [<span data-ttu-id="d10fc-157">**Msiproviabassembly**</span><span class="sxs-lookup"><span data-stu-id="d10fc-157">**MsiProvideAssembly**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)
    -   [<span data-ttu-id="d10fc-158">**MsiWin32AssemblySupport-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="d10fc-158">**MsiWin32AssemblySupport Property**</span></span>](msiwin32assemblysupport.md)
    -   [<span data-ttu-id="d10fc-159">**MsiNetAssemblySupport (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="d10fc-159">**MsiNetAssemblySupport Property**</span></span>](msinetassemblysupport.md)
    -   [<span data-ttu-id="d10fc-160">**Isolierte Komponenten**</span><span class="sxs-lookup"><span data-stu-id="d10fc-160">**Isolated Components**</span></span>](isolated-components.md)

-   <span data-ttu-id="d10fc-161">Bereiten Sie die Anwendung vor, um Ihre eigenen umfassenden Upgrades zu installieren.</span><span class="sxs-lookup"><span data-stu-id="d10fc-161">Prepare the application to install its own comprehensive major upgrades.</span></span>

    <span data-ttu-id="d10fc-162">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-162">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-163">Patchen und Upgrades</span><span class="sxs-lookup"><span data-stu-id="d10fc-163">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="d10fc-164">Wichtige Upgrades</span><span class="sxs-lookup"><span data-stu-id="d10fc-164">Major Upgrades</span></span>](major-upgrades.md)
    -   [<span data-ttu-id="d10fc-165">**UpgradeCode-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="d10fc-165">**UpgradeCode Property**</span></span>](upgradecode.md)
    -   [<span data-ttu-id="d10fc-166">**Verwenden von UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="d10fc-166">**Using an UpgradeCode**</span></span>](using-an-upgradecode.md)
    -   [<span data-ttu-id="d10fc-167">Verhindern, dass ein altes Paket über eine neuere Version installiert wird</span><span class="sxs-lookup"><span data-stu-id="d10fc-167">Preventing an Old Package from Installing Over a Newer Version</span></span>](preventing-an-old-package-from-installing-over-a-newer-version.md)

-   <span data-ttu-id="d10fc-168">Bereiten Sie die Anwendung vor, um Ihre eigenen kleinen Upgrades, kleine Updates oder Korrekturen zu installieren.</span><span class="sxs-lookup"><span data-stu-id="d10fc-168">Prepare the application to install its own minor upgrades, small updates, or fixes.</span></span>

    <span data-ttu-id="d10fc-169">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-169">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-170">Patchen und Upgrades</span><span class="sxs-lookup"><span data-stu-id="d10fc-170">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="d10fc-171">Kleine Updates</span><span class="sxs-lookup"><span data-stu-id="d10fc-171">Small Updates</span></span>](small-updates.md)
    -   [<span data-ttu-id="d10fc-172">Kleinere Upgrades</span><span class="sxs-lookup"><span data-stu-id="d10fc-172">Minor Upgrades</span></span>](minor-upgrades.md)

-   <span data-ttu-id="d10fc-173">Organisieren Sie Anwendungs Ressourcen in Komponenten, die mit dem Windows Installer arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="d10fc-173">Organize application resources into components that can work with the Windows Installer.</span></span>

    <span data-ttu-id="d10fc-174">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-174">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-175">Windows Installer Komponenten</span><span class="sxs-lookup"><span data-stu-id="d10fc-175">Windows Installer Components</span></span>](windows-installer-components.md)
    -   [<span data-ttu-id="d10fc-176">Arbeiten mit Features und Komponenten</span><span class="sxs-lookup"><span data-stu-id="d10fc-176">Working with Features and Components</span></span>](working-with-features-and-components.md)
    -   [<span data-ttu-id="d10fc-177">Verwenden transitiv Komponenten</span><span class="sxs-lookup"><span data-stu-id="d10fc-177">Using Transitive Components</span></span>](using-transitive-components.md)
    -   [<span data-ttu-id="d10fc-178">Was geschieht, wenn die Komponenten Regeln beschädigt sind?</span><span class="sxs-lookup"><span data-stu-id="d10fc-178">What happens if the component rules are broken?</span></span>](what-happens-if-the-component-rules-are-broken.md)
    -   [<span data-ttu-id="d10fc-179">Organisieren von Anwendungen in Komponenten</span><span class="sxs-lookup"><span data-stu-id="d10fc-179">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)
    -   [<span data-ttu-id="d10fc-180">Isolierte Komponenten</span><span class="sxs-lookup"><span data-stu-id="d10fc-180">Isolated Components</span></span>](isolated-components.md)
    -   [<span data-ttu-id="d10fc-181">Qualifizierte Komponenten</span><span class="sxs-lookup"><span data-stu-id="d10fc-181">Qualified Components</span></span>](qualified-components.md)

## <a name="setup-authors"></a><span data-ttu-id="d10fc-182">Setup Autoren</span><span class="sxs-lookup"><span data-stu-id="d10fc-182">Setup Authors</span></span>

<span data-ttu-id="d10fc-183">Setup Autoren erstellen Windows Installer Pakete (MSI-Dateien), die die Setup Logik und die erforderlichen Informationen zum Installieren einer Anwendung enthalten.</span><span class="sxs-lookup"><span data-stu-id="d10fc-183">Setup Authors create Windows Installer packages (.msi files) that contain the setup logic and information needed to install an application.</span></span> <span data-ttu-id="d10fc-184">In der Regel verwenden Sie Erstellungs Tools wie [Orca.exe](orca-exe.md) , um die Windows Installer Datenbank mit der Setup Logik und den Informationen aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="d10fc-184">They typically use authoring tools such as [Orca.exe](orca-exe.md) to populate the Windows Installer database with the setup logic and information.</span></span> <span data-ttu-id="d10fc-185">In der Regel führen Setup Autoren folgende Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="d10fc-185">Typically, Setup Authors do the following:</span></span>

-   <span data-ttu-id="d10fc-186">Bestimmen Sie die Funktionalität, die mit verschiedenen Windows Installer Versionen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d10fc-186">Determine the functionality available with different Windows Installer versions.</span></span>

    <span data-ttu-id="d10fc-187">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-187">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-188">Bestimmen der Windows Installer Version</span><span class="sxs-lookup"><span data-stu-id="d10fc-188">Determining the Windows Installer Version</span></span>](determining-the-windows-installer-version.md)
    -   [<span data-ttu-id="d10fc-189">Veröffentlichte Versionen von Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d10fc-189">Released Versions of Windows Installer</span></span>](released-versions-of-windows-installer.md)
    -   [<span data-ttu-id="d10fc-190">Neues in Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d10fc-190">What's New in Windows Installer</span></span>](what-s-new-in-windows-installer.md)

-   <span data-ttu-id="d10fc-191">Organisieren von Anwendungs Ressourcen in Windows Installer-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="d10fc-191">Organize application resources into Windows Installer components.</span></span>

    <span data-ttu-id="d10fc-192">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-192">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-193">Windows Installer Komponenten</span><span class="sxs-lookup"><span data-stu-id="d10fc-193">Windows Installer Components</span></span>](windows-installer-components.md)
    -   [<span data-ttu-id="d10fc-194">Organisieren von Anwendungen in Komponenten</span><span class="sxs-lookup"><span data-stu-id="d10fc-194">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)
    -   [<span data-ttu-id="d10fc-195">Ändern des Komponenten Codes</span><span class="sxs-lookup"><span data-stu-id="d10fc-195">Changing the Component Code</span></span>](changing-the-component-code.md)
    -   [<span data-ttu-id="d10fc-196">Was geschieht, wenn die Komponenten Regeln beschädigt sind?</span><span class="sxs-lookup"><span data-stu-id="d10fc-196">What happens if the component rules are broken?</span></span>](what-happens-if-the-component-rules-are-broken.md)
    -   [<span data-ttu-id="d10fc-197">Windows Installer Beispiele</span><span class="sxs-lookup"><span data-stu-id="d10fc-197">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="d10fc-198">Verwenden Sie Windows Installer Paket Erstellungs Tools von Drittanbietern oder SDK-Tools wie [Orca.exe](orca-exe.md) , um eine Installations Datenbank aufzufüllen und ein Windows Installer Paket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d10fc-198">Use third-party Windows Installer package authoring tools or SDK tools such as [Orca.exe](orca-exe.md) to populate an installation database and create a Windows Installer package.</span></span>

    <span data-ttu-id="d10fc-199">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-199">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-200">Entwicklungs Tools für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d10fc-200">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
    -   [<span data-ttu-id="d10fc-201">Installationspaket, Informationen zur Installer-Datenbank</span><span class="sxs-lookup"><span data-stu-id="d10fc-201">Installation Package, About the Installer Database</span></span>](installation-package.md)
    -   [<span data-ttu-id="d10fc-202">Dateierweiterungen Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d10fc-202">Windows Installer File Extensions</span></span>](windows-installer-file-extensions.md)
    -   [<span data-ttu-id="d10fc-203">Datenbanktabellen</span><span class="sxs-lookup"><span data-stu-id="d10fc-203">Database Tables</span></span>](database-tables.md)
    -   [<span data-ttu-id="d10fc-204">Paket Codes</span><span class="sxs-lookup"><span data-stu-id="d10fc-204">Package Codes</span></span>](package-codes.md)
    -   [<span data-ttu-id="d10fc-205">Erstellen eines großen Pakets</span><span class="sxs-lookup"><span data-stu-id="d10fc-205">Authoring a Large Package</span></span>](authoring-a-large-package.md)
    -   [<span data-ttu-id="d10fc-206">Windows Installer auf 64-Bit-Betriebssystemen</span><span class="sxs-lookup"><span data-stu-id="d10fc-206">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)
    -   [<span data-ttu-id="d10fc-207">Benennen von benutzerdefinierten Tabellen, Eigenschaften und Aktionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-207">Naming Custom Tables, Properties, and Actions</span></span>](naming-custom-tables-properties-and-actions.md)
    -   [<span data-ttu-id="d10fc-208">OLE-Einschränkungen für Streams</span><span class="sxs-lookup"><span data-stu-id="d10fc-208">OLE Limitations on Streams</span></span>](ole-limitations-on-streams.md)
    -   [<span data-ttu-id="d10fc-209">Spalten Definitions Format</span><span class="sxs-lookup"><span data-stu-id="d10fc-209">Column Definition Format</span></span>](column-definition-format.md)
    -   [<span data-ttu-id="d10fc-210">Reduzieren der Größe einer MSI-Datei</span><span class="sxs-lookup"><span data-stu-id="d10fc-210">Reducing the Size of an .msi File</span></span>](reducing-the-size-of-an--msi-file.md)

-   <span data-ttu-id="d10fc-211">Erstellen Sie die Windows Installer Datenbank, um Dateien zu installieren.</span><span class="sxs-lookup"><span data-stu-id="d10fc-211">Author the Windows Installer database to install files.</span></span>

    <span data-ttu-id="d10fc-212">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-212">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-213">Kern Tabellen Gruppe</span><span class="sxs-lookup"><span data-stu-id="d10fc-213">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="d10fc-214">Datei Tabellen Gruppe</span><span class="sxs-lookup"><span data-stu-id="d10fc-214">File Tables Group</span></span>](file-tables-group.md)
    -   [<span data-ttu-id="d10fc-215">Dateitabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-215">File Table</span></span>](file-table.md)
    -   [<span data-ttu-id="d10fc-216">Dateisuche</span><span class="sxs-lookup"><span data-stu-id="d10fc-216">File Searching</span></span>](file-searching.md)
    -   [<span data-ttu-id="d10fc-217">Datei Kosten</span><span class="sxs-lookup"><span data-stu-id="d10fc-217">File Costing</span></span>](file-costing.md)
    -   [<span data-ttu-id="d10fc-218">Datei Installation</span><span class="sxs-lookup"><span data-stu-id="d10fc-218">File Installation</span></span>](file-installation.md)
    -   [<span data-ttu-id="d10fc-219">Begleit Dateien</span><span class="sxs-lookup"><span data-stu-id="d10fc-219">Companion Files</span></span>](companion-files.md)
    -   [<span data-ttu-id="d10fc-220">Regeln für die Datei Versionsverwaltung</span><span class="sxs-lookup"><span data-stu-id="d10fc-220">File Versioning Rules</span></span>](file-versioning-rules.md)
    -   [<span data-ttu-id="d10fc-221">Standardmäßige Datei Versionsverwaltung</span><span class="sxs-lookup"><span data-stu-id="d10fc-221">Default File Versioning</span></span>](default-file-versioning.md)
    -   [<span data-ttu-id="d10fc-222">Ersetzen vorhandener Dateien</span><span class="sxs-lookup"><span data-stu-id="d10fc-222">Replacing Existing Files</span></span>](replacing-existing-files.md)
    -   [<span data-ttu-id="d10fc-223">Verwenden von Schränken und komprimierten Quellen</span><span class="sxs-lookup"><span data-stu-id="d10fc-223">Using Cabinets and Compressed Sources</span></span>](using-cabinets-and-compressed-sources.md)
    -   [<span data-ttu-id="d10fc-224">Entfernen von gestrandeten Dateien</span><span class="sxs-lookup"><span data-stu-id="d10fc-224">Removing Stranded Files</span></span>](removing-stranded-files.md)
    -   [<span data-ttu-id="d10fc-225">Installieren von permanenten Komponenten, Dateien, Schriftarten, Registrierungs Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="d10fc-225">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
    -   [<span data-ttu-id="d10fc-226">Filesfpcatalog-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-226">FileSFPCatalog Table</span></span>](filesfpcatalog-table.md)
    -   [<span data-ttu-id="d10fc-227">Suchen nach einer Datei und Erstellen einer Eigenschaft mit dem Pfad der Datei</span><span class="sxs-lookup"><span data-stu-id="d10fc-227">Searching for a File and Creating a Property Holding the File's Path</span></span>](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
    -   [<span data-ttu-id="d10fc-228">Suchen nach einem Verzeichnis und einer Datei im Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="d10fc-228">Searching for a Directory and a File in the Directory</span></span>](searching-for-a-directory-and-a-file-in-the-directory.md)
    -   [<span data-ttu-id="d10fc-229">Windows Installer Beispiele</span><span class="sxs-lookup"><span data-stu-id="d10fc-229">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="d10fc-230">Erstellen Sie eine Windows Installer Datenbank, die eine Verzeichnisstruktur und Ordner installiert.</span><span class="sxs-lookup"><span data-stu-id="d10fc-230">Author a Windows Installer database that installs a directory structure and folders.</span></span>

    <span data-ttu-id="d10fc-231">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-231">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-232">Kern Tabellen Gruppe</span><span class="sxs-lookup"><span data-stu-id="d10fc-232">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="d10fc-233">Datei Tabellen Gruppe</span><span class="sxs-lookup"><span data-stu-id="d10fc-233">File Tables Group</span></span>](file-tables-group.md)
    -   [<span data-ttu-id="d10fc-234">Komponenten Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-234">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="d10fc-235">Verzeichnis Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-235">Directory Table</span></span>](directory-table.md)
    -   [<span data-ttu-id="d10fc-236">Verwenden der Verzeichnis Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-236">Using the Directory Table</span></span>](using-the-directory-table.md)
    -   [<span data-ttu-id="d10fc-237">Verwenden einer Verzeichnis Eigenschaft in einem Pfad</span><span class="sxs-lookup"><span data-stu-id="d10fc-237">Using a Directory Property in a Path</span></span>](using-a-directory-property-in-a-path.md)
    -   [<span data-ttu-id="d10fc-238">Eigenschaften von System Ordnern</span><span class="sxs-lookup"><span data-stu-id="d10fc-238">System Folder Properties</span></span>](property-reference.md)
    -   [<span data-ttu-id="d10fc-239">Tabelle "Buildordner"</span><span class="sxs-lookup"><span data-stu-id="d10fc-239">CreateFolder Table</span></span>](createfolder-table.md)
    -   [<span data-ttu-id="d10fc-240">Lockberechtigungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-240">LockPermissions Table</span></span>](lockpermissions-table.md)
    -   [<span data-ttu-id="d10fc-241">Msilockpermissionsex-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-241">MsiLockPermissionsEx Table</span></span>](msilockpermissionsex-table.md)
    -   [<span data-ttu-id="d10fc-242">Ändern des Zielspeicher Orts für ein Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="d10fc-242">Changing the Target Location for a Directory</span></span>](changing-the-target-location-for-a-directory.md)
    -   [<span data-ttu-id="d10fc-243">Windows Installer Beispiele</span><span class="sxs-lookup"><span data-stu-id="d10fc-243">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="d10fc-244">Erstellen Sie eine Windows Installer Datenbank, die Registrierungsschlüssel installiert.</span><span class="sxs-lookup"><span data-stu-id="d10fc-244">Author a Windows Installer database that installs registry keys.</span></span>

    <span data-ttu-id="d10fc-245">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-245">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-246">Kern Tabellen Gruppe</span><span class="sxs-lookup"><span data-stu-id="d10fc-246">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="d10fc-247">Registrierungs Tabellen Gruppe</span><span class="sxs-lookup"><span data-stu-id="d10fc-247">Registry Tables Group</span></span>](registry-tables-group.md)
    -   [<span data-ttu-id="d10fc-248">Registrierungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-248">Registry Table</span></span>](registry-table.md)
    -   [<span data-ttu-id="d10fc-249">Ändern der Registrierung</span><span class="sxs-lookup"><span data-stu-id="d10fc-249">Modifying the Registry</span></span>](modifying-the-registry.md)
    -   [<span data-ttu-id="d10fc-250">Hinzufügen oder Entfernen von Registrierungs Schlüsseln zum Installieren oder Entfernen von Komponenten</span><span class="sxs-lookup"><span data-stu-id="d10fc-250">Adding or Removing Registry Keys on the Installation or Removal of Components</span></span>](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)
    -   [<span data-ttu-id="d10fc-251">Hinzufügen und Entfernen einer Anwendung ohne Ablauf Verfolgung in der Registrierung</span><span class="sxs-lookup"><span data-stu-id="d10fc-251">Adding and Removing an Application and Leaving No Trace in the Registry</span></span>](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [<span data-ttu-id="d10fc-252">Installieren von permanenten Komponenten, Dateien, Schriftarten, Registrierungs Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="d10fc-252">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
    -   [<span data-ttu-id="d10fc-253">Suchen nach vorhandenen Anwendungen, Dateien, Registrierungs Einträgen oder INI-Datei Einträgen</span><span class="sxs-lookup"><span data-stu-id="d10fc-253">Searching for Existing Applications, Files, Registry Entries or .ini File Entries</span></span>](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
    -   [<span data-ttu-id="d10fc-254">Suchen nach einem Registrierungs Eintrag und Erstellen einer Eigenschaft mit dem Wert der Registrierung</span><span class="sxs-lookup"><span data-stu-id="d10fc-254">Searching for a Registry Entry and Creating a Property Holding the Value of the Registry</span></span>](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)
    -   [<span data-ttu-id="d10fc-255">Vom Windows Installer geschriebene assemblyregistrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="d10fc-255">Assembly Registry Keys Written by the Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="d10fc-256">Registrierungsschlüssel deinstallieren</span><span class="sxs-lookup"><span data-stu-id="d10fc-256">Uninstall Registry Key</span></span>](uninstall-registry-key.md)
    -   [<span data-ttu-id="d10fc-257">Selfreg-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-257">SelfReg Table</span></span>](selfreg-table.md)
    -   [<span data-ttu-id="d10fc-258">Angeben der Reihenfolge der Selbstregistrierung</span><span class="sxs-lookup"><span data-stu-id="d10fc-258">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
    -   [<span data-ttu-id="d10fc-259">Windows Installer Beispiele</span><span class="sxs-lookup"><span data-stu-id="d10fc-259">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="d10fc-260">Erstellen Sie eine Windows Installer Datenbank, mit der Dienste installiert werden.</span><span class="sxs-lookup"><span data-stu-id="d10fc-260">Author a Windows Installer database that installs services.</span></span>

    <span data-ttu-id="d10fc-261">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-261">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-262">Servicabstall-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-262">ServiceInstall Table</span></span>](serviceinstall-table.md)
    -   [<span data-ttu-id="d10fc-263">ServiceControl-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-263">ServiceControl Table</span></span>](servicecontrol-table.md)
    -   [<span data-ttu-id="d10fc-264">Komponenten Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-264">Component Table</span></span>](component-table.md)

-   <span data-ttu-id="d10fc-265">Erstellen Sie eine Windows Installer Datenbank, mit der isolierte Komponenten oder COM-Komponenten installiert werden.</span><span class="sxs-lookup"><span data-stu-id="d10fc-265">Author a Windows Installer database that installs isolated components or COM components.</span></span>

    <span data-ttu-id="d10fc-266">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-266">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-267">Registrierungs Tabellen Gruppe</span><span class="sxs-lookup"><span data-stu-id="d10fc-267">Registry Tables Group</span></span>](registry-tables-group.md)
    -   [<span data-ttu-id="d10fc-268">Klassen Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-268">Class Table</span></span>](class-table.md)
    -   [<span data-ttu-id="d10fc-269">ComPlus-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-269">Complus Table</span></span>](complus-table.md)
    -   [<span data-ttu-id="d10fc-270">Isolierte Komponenten</span><span class="sxs-lookup"><span data-stu-id="d10fc-270">Isolated Components</span></span>](isolated-components.md)
    -   [<span data-ttu-id="d10fc-271">Verwenden isolierter Komponenten</span><span class="sxs-lookup"><span data-stu-id="d10fc-271">Using Isolated Components</span></span>](using-isolated-components.md)
    -   [<span data-ttu-id="d10fc-272">Installation isolierter Komponenten</span><span class="sxs-lookup"><span data-stu-id="d10fc-272">Installation of Isolated Components</span></span>](installation-of-isolated-components.md)
    -   [<span data-ttu-id="d10fc-273">Neuinstallation isolierter Komponenten</span><span class="sxs-lookup"><span data-stu-id="d10fc-273">Reinstallation of Isolated Components</span></span>](reinstallation-of-isolated-components.md)
    -   [<span data-ttu-id="d10fc-274">Entfernen isolierter Komponenten</span><span class="sxs-lookup"><span data-stu-id="d10fc-274">Removal of Isolated Components</span></span>](removal-of-isolated-components.md)
    -   [<span data-ttu-id="d10fc-275">Installieren einer COM-Komponente an einem privaten Speicherort</span><span class="sxs-lookup"><span data-stu-id="d10fc-275">Installing a COM Component to a Private Location</span></span>](installing-a-com-component-to-a-private-location.md)
    -   [<span data-ttu-id="d10fc-276">Erstellen einer COM-Komponente in einem vorhandenen Paket</span><span class="sxs-lookup"><span data-stu-id="d10fc-276">Make a COM Component in an Existing Package Private</span></span>](make-a-com-component-in-an-existing-package-private.md)
    -   [<span data-ttu-id="d10fc-277">Installieren einer COM+-Anwendung mit der Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d10fc-277">Installing a COM+ Application with the Windows Installer</span></span>](installing-a-com--application-with-the-windows-installer.md)
    -   [<span data-ttu-id="d10fc-278">Installieren einer nicht-COM-Komponente an einem privaten Speicherort</span><span class="sxs-lookup"><span data-stu-id="d10fc-278">Installing a non-COM Component to a Private Location</span></span>](installing-a-non-com-component-to-a-private-location.md)
    -   [<span data-ttu-id="d10fc-279">Erstellen einer nicht-COM-Komponente in einem vorhandenen Paket</span><span class="sxs-lookup"><span data-stu-id="d10fc-279">Make a non-COM Component in an Existing Package Private</span></span>](make-a-non-com-component-in-an-existing-package-private.md)

-   <span data-ttu-id="d10fc-280">Erstellen Sie eine Windows Installer Datenbank, die Assemblys installiert.</span><span class="sxs-lookup"><span data-stu-id="d10fc-280">Author a Windows Installer database that installs assemblies.</span></span>

    <span data-ttu-id="d10fc-281">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-281">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-282">MsiAssembly-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-282">MsiAssembly Table</span></span>](msiassembly-table.md)
    -   [<span data-ttu-id="d10fc-283">MsiAssemblyName-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-283">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)
    -   [<span data-ttu-id="d10fc-284">Assemblys</span><span class="sxs-lookup"><span data-stu-id="d10fc-284">Assemblies</span></span>](assemblies.md)
    -   [<span data-ttu-id="d10fc-285">Vom Windows Installer geschriebene assemblyregistrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="d10fc-285">Assembly Registry Keys Written by the Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="d10fc-286">Installation von Win32-Assemblys</span><span class="sxs-lookup"><span data-stu-id="d10fc-286">Installation of Win32 Assemblies</span></span>](installation-of-win32-assemblies.md)

-   <span data-ttu-id="d10fc-287">Erstellen Sie eine Windows Installer Datenbank, die ODBC-Treiber und-Konvertierer installiert.</span><span class="sxs-lookup"><span data-stu-id="d10fc-287">Author a Windows Installer database that installs ODBC drivers and translators.</span></span>

    <span data-ttu-id="d10fc-288">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-288">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-289">Odbingtribute-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-289">ODBCAttribute Table</span></span>](odbcattribute-table.md)
    -   [<span data-ttu-id="d10fc-290">Odbcdriver-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-290">ODBCDriver Table</span></span>](odbcdriver-table.md)
    -   [<span data-ttu-id="d10fc-291">Odbctranslator-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-291">ODBCTranslator Table</span></span>](odbctranslator-table.md)
    -   [<span data-ttu-id="d10fc-292">ODBCDatasource-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-292">ODBCDataSource Table</span></span>](odbcdatasource-table.md)
    -   [<span data-ttu-id="d10fc-293">Odbcsourceattribute-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-293">ODBCSourceAttribute Table</span></span>](odbcsourceattribute-table.md)

-   <span data-ttu-id="d10fc-294">Erstellen Sie eine Windows Installer Datenbank, die MIME installiert.</span><span class="sxs-lookup"><span data-stu-id="d10fc-294">Author a Windows Installer database that installs MIME.</span></span>

    <span data-ttu-id="d10fc-295">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-295">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-296">MIME-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-296">MIME Table</span></span>](mime-table.md)
    -   [<span data-ttu-id="d10fc-297">Erweiterungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-297">Extension Table</span></span>](extension-table.md)
    -   [<span data-ttu-id="d10fc-298">Ändern der Registrierung</span><span class="sxs-lookup"><span data-stu-id="d10fc-298">Modifying the Registry</span></span>](modifying-the-registry.md)

-   <span data-ttu-id="d10fc-299">Erstellen Sie eine Windows Installer Datenbank, die Umgebungsvariablen installiert.</span><span class="sxs-lookup"><span data-stu-id="d10fc-299">Author a Windows Installer database that installs environment variables.</span></span>

    <span data-ttu-id="d10fc-300">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-300">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-301">Umgebungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-301">Environment Table</span></span>](environment-table.md)

-   <span data-ttu-id="d10fc-302">Erstellen Sie eine Windows Installer Datenbank, die Verknüpfungen installiert.</span><span class="sxs-lookup"><span data-stu-id="d10fc-302">Author a Windows Installer database that installs shortcuts.</span></span>

    <span data-ttu-id="d10fc-303">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-303">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-304">Verknüpfungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-304">Shortcut Table</span></span>](shortcut-table.md)
    -   [<span data-ttu-id="d10fc-305">Msishortcutproperty-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-305">MsiShortcutProperty Table</span></span>](msishortcutproperty-table.md)
    -   [<span data-ttu-id="d10fc-306">Bearbeiten von Installationsprogramm Kombinationen</span><span class="sxs-lookup"><span data-stu-id="d10fc-306">Editing Installer Shortcuts</span></span>](editing-installer-shortcuts.md)
    -   [<span data-ttu-id="d10fc-307">Windows Installer Beispiele</span><span class="sxs-lookup"><span data-stu-id="d10fc-307">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="d10fc-308">Erstellen Sie eine Windows Installer Datenbank, die mehrere Anwendungs Instanzen installiert.</span><span class="sxs-lookup"><span data-stu-id="d10fc-308">Author a Windows Installer database that installs multiple instances of applications.</span></span>

    <span data-ttu-id="d10fc-309">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-309">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-310">Installieren mehrerer Instanzen von Produkten und Patches</span><span class="sxs-lookup"><span data-stu-id="d10fc-310">Installing Multiple Instances of Products and Patches</span></span>](installing-multiple-instances-of-products-and-patches.md)
    -   [<span data-ttu-id="d10fc-311">Erstellen mehrerer Instanzen mit instanztransformationen</span><span class="sxs-lookup"><span data-stu-id="d10fc-311">Authoring Multiple Instances with Instance Transforms</span></span>](authoring-multiple-instances-with-instance-transforms.md)
    -   [<span data-ttu-id="d10fc-312">Installieren mehrerer Instanzen mit instanztransformationen</span><span class="sxs-lookup"><span data-stu-id="d10fc-312">Installing Multiple Instances with Instance Transforms</span></span>](installing-multiple-instances-with-instance-transforms.md)

-   <span data-ttu-id="d10fc-313">Geben Sie die Standardoptionen für die Funktionsauswahl an.</span><span class="sxs-lookup"><span data-stu-id="d10fc-313">Specify default feature selection states and options.</span></span>

    <span data-ttu-id="d10fc-314">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-314">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-315">Kern Tabellen Gruppe</span><span class="sxs-lookup"><span data-stu-id="d10fc-315">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="d10fc-316">Komponenten Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-316">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="d10fc-317">Funktions Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-317">Feature Table</span></span>](feature-table.md)
    -   [<span data-ttu-id="d10fc-318">FeatureComponents-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-318">FeatureComponents Table</span></span>](featurecomponents-table.md)
    -   [<span data-ttu-id="d10fc-319">Steuern von Funktionsauswahl Zuständen</span><span class="sxs-lookup"><span data-stu-id="d10fc-319">Controlling Feature Selection States</span></span>](controlling-feature-selection-states.md)
    -   [<span data-ttu-id="d10fc-320">Eigenschaften von featureinstallationsoptionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-320">Feature Installation Options Properties</span></span>](property-reference.md)

-   <span data-ttu-id="d10fc-321">Geben Sie Bedingungen an, die erfüllt sein müssen, um eine Anwendung oder ausgewählte Komponenten zu installieren.</span><span class="sxs-lookup"><span data-stu-id="d10fc-321">Specify conditions that must be met to install an application or selected components.</span></span>

    <span data-ttu-id="d10fc-322">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-322">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-323">Bedingungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-323">Condition Table</span></span>](condition-table.md)
    -   [<span data-ttu-id="d10fc-324">LaunchCondition-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-324">LaunchCondition Table</span></span>](launchcondition-table.md)
    -   [<span data-ttu-id="d10fc-325">Komponenten Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-325">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="d10fc-326">Verwenden von Eigenschaften in Bedingungs Anweisungen</span><span class="sxs-lookup"><span data-stu-id="d10fc-326">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
    -   [<span data-ttu-id="d10fc-327">Syntax der bedingten Anweisung</span><span class="sxs-lookup"><span data-stu-id="d10fc-327">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
    -   [<span data-ttu-id="d10fc-328">Während des Entfernens auszuführende Aufbereitungs Aktionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-328">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
    -   [<span data-ttu-id="d10fc-329">Beispiele für bedingte Anweisungs Syntax</span><span class="sxs-lookup"><span data-stu-id="d10fc-329">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)

-   <span data-ttu-id="d10fc-330">Erstellen Sie die Abfolge der Aktionen, die zum Installieren der Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d10fc-330">Author the sequence of actions used to install the application.</span></span>

    <span data-ttu-id="d10fc-331">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-331">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-332">Verwenden einer Sequenz Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-332">Using a Sequence Table</span></span>](using-a-sequence-table.md)
    -   [<span data-ttu-id="d10fc-333">Gruppe "Installationsprozedur Tabellen"</span><span class="sxs-lookup"><span data-stu-id="d10fc-333">Installation Procedure Tables Group</span></span>](installation-procedure-tables-group.md)
    -   [<span data-ttu-id="d10fc-334">Beispiel für eine detaillierte Sequenz Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-334">Sequence Table Detailed Example</span></span>](sequence-table-detailed-example.md)
    -   [<span data-ttu-id="d10fc-335">Aktionen mit Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="d10fc-335">Actions with Sequencing Restrictions</span></span>](actions-with-sequencing-restrictions.md)
    -   [<span data-ttu-id="d10fc-336">Aktionen ohne Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="d10fc-336">Actions without Sequencing Restrictions</span></span>](actions-without-sequencing-restrictions.md)
    -   [<span data-ttu-id="d10fc-337">Verwenden von Eigenschaften in Bedingungs Anweisungen</span><span class="sxs-lookup"><span data-stu-id="d10fc-337">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
    -   [<span data-ttu-id="d10fc-338">Syntax der bedingten Anweisung</span><span class="sxs-lookup"><span data-stu-id="d10fc-338">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
    -   [<span data-ttu-id="d10fc-339">Beispiele für bedingte Anweisungs Syntax</span><span class="sxs-lookup"><span data-stu-id="d10fc-339">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)
    -   [<span data-ttu-id="d10fc-340">Während des Entfernens auszuführende Aufbereitungs Aktionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-340">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
    -   [<span data-ttu-id="d10fc-341">Standard Aktionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-341">Standard Actions</span></span>](standard-actions.md)
    -   [<span data-ttu-id="d10fc-342">Windows Installer Beispiele</span><span class="sxs-lookup"><span data-stu-id="d10fc-342">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="d10fc-343">Bereiten Sie das Installationspaket der Anwendung für zukünftige Upgrades der Anwendung durch den Windows Installer-Dienst vor.</span><span class="sxs-lookup"><span data-stu-id="d10fc-343">Prepare the installation package of the application for future upgrades of the application by the Windows Installer service.</span></span>

    <span data-ttu-id="d10fc-344">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-344">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-345">Patchen und Upgrades</span><span class="sxs-lookup"><span data-stu-id="d10fc-345">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="d10fc-346">Vorbereiten einer Anwendung für zukünftige größere Upgrades</span><span class="sxs-lookup"><span data-stu-id="d10fc-346">Preparing an Application for Future Major Upgrades</span></span>](preparing-an-application-for-future-major-upgrades.md)
    -   [<span data-ttu-id="d10fc-347">Verwenden von UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="d10fc-347">Using an UpgradeCode</span></span>](using-an-upgradecode.md)
    -   [<span data-ttu-id="d10fc-348">Upgradetabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-348">Upgrade Table</span></span>](upgrade-table.md)
    -   [<span data-ttu-id="d10fc-349">**UpgradeCode-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="d10fc-349">**UpgradeCode Property**</span></span>](upgradecode.md)
    -   [<span data-ttu-id="d10fc-350">Verhindern, dass ein altes Paket über eine neuere Version installiert wird</span><span class="sxs-lookup"><span data-stu-id="d10fc-350">Preventing an Old Package from Installing Over a Newer Version</span></span>](preventing-an-old-package-from-installing-over-a-newer-version.md)
    -   [<span data-ttu-id="d10fc-351">Ändern des Produktcodes</span><span class="sxs-lookup"><span data-stu-id="d10fc-351">Changing the Product Code</span></span>](changing-the-product-code.md)
    -   [<span data-ttu-id="d10fc-352">Aktualisieren von Assemblys</span><span class="sxs-lookup"><span data-stu-id="d10fc-352">Updating Assemblies</span></span>](updating-assemblies.md)
    -   [<span data-ttu-id="d10fc-353">Windows Installer Beispiele</span><span class="sxs-lookup"><span data-stu-id="d10fc-353">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="d10fc-354">Problembehandlung bei Windows Installer Paketen in der Entwicklung.</span><span class="sxs-lookup"><span data-stu-id="d10fc-354">Troubleshoot Windows Installer packages under development.</span></span>

    <span data-ttu-id="d10fc-355">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-355">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-356">Paketvalidierung</span><span class="sxs-lookup"><span data-stu-id="d10fc-356">Package Validation</span></span>](package-validation.md)
    -   [<span data-ttu-id="d10fc-357">Interne Konsistenz Auswertung-ICES</span><span class="sxs-lookup"><span data-stu-id="d10fc-357">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)
    -   [<span data-ttu-id="d10fc-358">Windows Installer Protokollierung</span><span class="sxs-lookup"><span data-stu-id="d10fc-358">Windows Installer Logging</span></span>](windows-installer-logging.md)
    -   [<span data-ttu-id="d10fc-359">Überprüfen der Installation von Features, Komponenten, Dateien</span><span class="sxs-lookup"><span data-stu-id="d10fc-359">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
    -   [<span data-ttu-id="d10fc-360">Erstellen eines großen Pakets</span><span class="sxs-lookup"><span data-stu-id="d10fc-360">Authoring a Large Package</span></span>](authoring-a-large-package.md)
    -   [<span data-ttu-id="d10fc-361">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="d10fc-361">Wilogutl.exe</span></span>](wilogutl-exe.md)
    -   [<span data-ttu-id="d10fc-362">Entwicklungs Tools für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d10fc-362">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
    -   [<span data-ttu-id="d10fc-363">Validieren von Mergemodulen</span><span class="sxs-lookup"><span data-stu-id="d10fc-363">Validating Merge Modules</span></span>](validating-merge-modules.md)
    -   [<span data-ttu-id="d10fc-364">Überprüfen einer Installations Datenbank</span><span class="sxs-lookup"><span data-stu-id="d10fc-364">Validating an Installation Database</span></span>](validating-an-installation-database.md)
    -   [<span data-ttu-id="d10fc-365">Überprüfen eines Installations Upgrades</span><span class="sxs-lookup"><span data-stu-id="d10fc-365">Validating an Installation Upgrade</span></span>](validating-an-installation-upgrade.md)
    -   [<span data-ttu-id="d10fc-366">Suchen nach einer unterbrochenen Funktion oder Komponente</span><span class="sxs-lookup"><span data-stu-id="d10fc-366">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="d10fc-367">Windows Installer von Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="d10fc-367">Windows Installer Error Messages</span></span>](windows-installer-error-messages.md)
    -   [<span data-ttu-id="d10fc-368">Protokollierung von Neustart Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d10fc-368">Logging of Reboot Requests</span></span>](logging-of-reboot-requests.md)

-   <span data-ttu-id="d10fc-369">Stellen Sie eine sichere Einrichtung und Installation der Anwendung sicher.</span><span class="sxs-lookup"><span data-stu-id="d10fc-369">Ensure a secure setup and installation of the application.</span></span>

    <span data-ttu-id="d10fc-370">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-370">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-371">Richtlinien für das Erstellen von sicheren Installationen</span><span class="sxs-lookup"><span data-stu-id="d10fc-371">Guidelines for Authoring Secure Installations</span></span>](guidelines-for-authoring-secure-installations.md)
    -   [<span data-ttu-id="d10fc-372">Richtlinien zum Sichern von benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-372">Guidelines for Securing Custom Actions</span></span>](guidelines-for-securing-custom-actions.md)
    -   [<span data-ttu-id="d10fc-373">Sicherheit für benutzerdefinierte Aktionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-373">Custom Action Security</span></span>](custom-action-security.md)
    -   [<span data-ttu-id="d10fc-374">Richtlinien zum Sichern von Paketen auf gesperrten Computern</span><span class="sxs-lookup"><span data-stu-id="d10fc-374">Guidelines for Securing Packages on Locked-Down Computers</span></span>](guidelines-for-securing-packages-on-locked-down-computers.md)
    -   [<span data-ttu-id="d10fc-375">Erstellen einer vollständig überprüften signierten Installation mithilfe von Automation</span><span class="sxs-lookup"><span data-stu-id="d10fc-375">Authoring a Fully Verified Signed Installation Using Automation</span></span>](authoring-a-fully-verified-signed-installation-using-automation.md)
    -   [<span data-ttu-id="d10fc-376">URL-basiertes Windows Installer-Installationsbeispiel</span><span class="sxs-lookup"><span data-stu-id="d10fc-376">A URL-Based Windows Installer Installation Example</span></span>](a-url-based-windows-installer-installation-example.md)
    -   [<span data-ttu-id="d10fc-377">Erstellen der Benutzeroberfläche für die Kenn Wort Eingabe</span><span class="sxs-lookup"><span data-stu-id="d10fc-377">Authoring the User Interface for Password Input</span></span>](authoring-the-user-interface-for-password-input.md)
    -   [<span data-ttu-id="d10fc-378">Digitale Signaturen und Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d10fc-378">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
    -   [<span data-ttu-id="d10fc-379">Verwenden von Windows Installer mit UAC</span><span class="sxs-lookup"><span data-stu-id="d10fc-379">Using Windows Installer with UAC</span></span>](using-windows-installer-with-uac.md)
    -   [<span data-ttu-id="d10fc-380">Patching der Benutzerkontensteuerung (User Account Control, UAC)</span><span class="sxs-lookup"><span data-stu-id="d10fc-380">User Account Control (UAC) Patching</span></span>](user-account-control--uac--patching.md)
    -   [<span data-ttu-id="d10fc-381">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="d10fc-381">Msicert.exe</span></span>](msicert-exe.md)
    -   [<span data-ttu-id="d10fc-382">**AdminUser (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="d10fc-382">**AdminUser property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="d10fc-383">**Privilegierte Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="d10fc-383">**Privileged property**</span></span>](privileged.md)
    -   [<span data-ttu-id="d10fc-384">**Securecustomproperties (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="d10fc-384">**SecureCustomProperties property**</span></span>](securecustomproperties.md)

-   <span data-ttu-id="d10fc-385">Erstellen Sie eine Benutzeroberfläche, um Optionen zum Konfigurieren der Installation und zum Abrufen von Informationen vom Benutzer zum ausstehenden Installationsvorgang zu präsentieren.</span><span class="sxs-lookup"><span data-stu-id="d10fc-385">Create a user interface to present options to configure the installation and obtain information from the user about the pending installation process.</span></span>

    <span data-ttu-id="d10fc-386">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-386">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-387">Informationen zur Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d10fc-387">About the User Interface</span></span>](about-the-user-interface.md)
    -   [<span data-ttu-id="d10fc-388">Hinzufügen von Steuerelementen und Text</span><span class="sxs-lookup"><span data-stu-id="d10fc-388">Adding Controls and Text</span></span>](adding-controls-and-text.md)
    -   [<span data-ttu-id="d10fc-389">Erstellen eines ProgressBar-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="d10fc-389">Authoring a ProgressBar Control</span></span>](authoring-a-progressbar-control.md)
    -   [<span data-ttu-id="d10fc-390">Erstellen von Datenträger Aufforderungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="d10fc-390">Authoring Disk Prompt Messages</span></span>](authoring-disk-prompt-messages.md)
    -   [<span data-ttu-id="d10fc-391">Erstellen einer bedingten "Bitte warten..." Meldungs Feld</span><span class="sxs-lookup"><span data-stu-id="d10fc-391">Authoring a Conditional "Please Wait . . ." Message Box</span></span>](authoring-a-conditional-please-wait-------message-box.md)
    -   [<span data-ttu-id="d10fc-392">Anzeigen der Vorschau der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d10fc-392">Previewing the User Interface</span></span>](previewing-the-user-interface.md)
    -   [<span data-ttu-id="d10fc-393">Hinzufügen von in einer Eigenschaft gespeicherten Text</span><span class="sxs-lookup"><span data-stu-id="d10fc-393">Adding Text Stored in a Property</span></span>](adding-text-stored-in-a-property.md)
    -   [<span data-ttu-id="d10fc-394">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="d10fc-394">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

-   <span data-ttu-id="d10fc-395">Erstellen Sie eine externe Benutzeroberfläche, um eine benutzerdefinierte Benutzeroberfläche zum Konfigurieren der Installation und zum Abrufen von Informationen vom Benutzer zum ausstehenden Installationsvorgang zu präsentieren.</span><span class="sxs-lookup"><span data-stu-id="d10fc-395">Create an external user interface to present a custom user interface to configure the installation and obtain information from the user about the pending installation process.</span></span>

    <span data-ttu-id="d10fc-396">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-396">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-397">**Msiseeltexternalui**</span><span class="sxs-lookup"><span data-stu-id="d10fc-397">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
    -   [<span data-ttu-id="d10fc-398">Überwachen einer Installation mithilfe von "msiabtexternaluirecord"</span><span class="sxs-lookup"><span data-stu-id="d10fc-398">Monitoring an Installation Using MsiSetExternalUIRecord</span></span>](monitoring-an-installation-using-msisetexternaluirecord.md)
    -   [<span data-ttu-id="d10fc-399">Windows Installer Meldungen werden verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d10fc-399">Parsing Windows Installer Messages</span></span>](parsing-windows-installer-messages.md)
    -   [<span data-ttu-id="d10fc-400">Zurückgeben von Werten von einem externen Benutzeroberflächen Handler</span><span class="sxs-lookup"><span data-stu-id="d10fc-400">Returning Values from an External User Interface Handler</span></span>](returning-values-from-an-external-user-interface-handler.md)
    -   [<span data-ttu-id="d10fc-401">installui- \_ Handler</span><span class="sxs-lookup"><span data-stu-id="d10fc-401">INSTALLUI\_HANDLER</span></span>](/windows/desktop/api/Msi/nc-msi-installui_handlera)
    -   [<span data-ttu-id="d10fc-402">Verarbeiten von Statusmeldungen mithilfe von "msieintexternalui"</span><span class="sxs-lookup"><span data-stu-id="d10fc-402">Handling Progress Messages Using MsiSetExternalUI</span></span>](handling-progress-messages-using-msisetexternalui.md)
    -   [<span data-ttu-id="d10fc-403">Überwachen einer Installation mithilfe von "msieintexternalui"</span><span class="sxs-lookup"><span data-stu-id="d10fc-403">Monitoring an Installation Using MsiSetExternalUI</span></span>](monitoring-an-installation-using-msisetexternalui.md)

-   <span data-ttu-id="d10fc-404">Festlegen von Informationen für die Anwendung **in "** Software" (ARP)</span><span class="sxs-lookup"><span data-stu-id="d10fc-404">Set information for the application in **Add/Remove Programs** (ARP.)</span></span>

    <span data-ttu-id="d10fc-405">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-405">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-406">Konfigurieren von "Programme hinzufügen/entfernen" mit Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d10fc-406">Configuring Add/Remove Programs with Windows Installer</span></span>](configuring-add-remove-programs-with-windows-installer.md)
    -   [<span data-ttu-id="d10fc-407">Hinzufügen und Entfernen einer Anwendung ohne Ablauf Verfolgung in der Registrierung</span><span class="sxs-lookup"><span data-stu-id="d10fc-407">Adding and Removing an Application and Leaving No Trace in the Registry</span></span>](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [<span data-ttu-id="d10fc-408">Registrierungsschlüssel deinstallieren</span><span class="sxs-lookup"><span data-stu-id="d10fc-408">Uninstall Registry Key</span></span>](uninstall-registry-key.md)

-   <span data-ttu-id="d10fc-409">Schreiben Sie benutzerdefinierte Aktionen, um die Setup Logik zu behandeln, die von Windows Installer nicht System intern unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d10fc-409">Write custom actions to handle setup logic that is not natively supported by Windows Installer.</span></span>

    <span data-ttu-id="d10fc-410">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-410">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-411">Benutzerdefinierte Aktionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-411">Custom Actions</span></span>](custom-actions.md)
    -   [<span data-ttu-id="d10fc-412">Zusammenfassungs Liste aller benutzerdefinierten Aktions Typen</span><span class="sxs-lookup"><span data-stu-id="d10fc-412">Summary List of All Custom Action Types</span></span>](summary-list-of-all-custom-action-types.md)
    -   [<span data-ttu-id="d10fc-413">Richtlinien zum Sichern von benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-413">Guidelines for Securing Custom Actions</span></span>](guidelines-for-securing-custom-actions.md)
    -   [<span data-ttu-id="d10fc-414">Referenz zu benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-414">Custom Action Reference</span></span>](custom-action-reference.md)
    -   [<span data-ttu-id="d10fc-415">Verwenden einer benutzerdefinierten Aktion zum Erstellen von Benutzerkonten auf einem lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="d10fc-415">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="d10fc-416">Verwenden einer benutzerdefinierten Aktion zum Starten einer installierten Datei am Ende der Installation</span><span class="sxs-lookup"><span data-stu-id="d10fc-416">Using a Custom Action to Launch an Installed File at the End of the Installation</span></span>](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
    -   [<span data-ttu-id="d10fc-417">Zugreifen auf eine Datenbank oder eine Sitzung innerhalb einer benutzerdefinierten Aktion</span><span class="sxs-lookup"><span data-stu-id="d10fc-417">Accessing a Database or Session from Inside a Custom Action</span></span>](accessing-a-database-or-session-from-inside-a-custom-action.md)
    -   [<span data-ttu-id="d10fc-418">Zugreifen auf die aktuelle Installer-Sitzung innerhalb einer benutzerdefinierten Aktion</span><span class="sxs-lookup"><span data-stu-id="d10fc-418">Accessing the Current Installer Session from Inside a Custom Action</span></span>](accessing-the-current-installer-session-from-inside-a-custom-action.md)
    -   [<span data-ttu-id="d10fc-419">Ändern des System Status mithilfe einer benutzerdefinierten Aktion</span><span class="sxs-lookup"><span data-stu-id="d10fc-419">Changing the System State Using a Custom Action</span></span>](changing-the-system-state-using-a-custom-action.md)

-   <span data-ttu-id="d10fc-420">Bootstrap der Windows Installer auf den Computer eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="d10fc-420">Bootstrap the Windows Installer onto a user's computer.</span></span>

    <span data-ttu-id="d10fc-421">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-421">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-422">Bootstrapping</span><span class="sxs-lookup"><span data-stu-id="d10fc-422">Bootstrapping</span></span>](bootstrapping.md)
    -   [<span data-ttu-id="d10fc-423">Instmsi.exe</span><span class="sxs-lookup"><span data-stu-id="d10fc-423">Instmsi.exe</span></span>](instmsi-exe.md)
    -   [<span data-ttu-id="d10fc-424">Internetdownload-Bootstrapping</span><span class="sxs-lookup"><span data-stu-id="d10fc-424">Internet Download Bootstrapping</span></span>](internet-download-bootstrapping.md)
    -   [<span data-ttu-id="d10fc-425">Msistuff.exe</span><span class="sxs-lookup"><span data-stu-id="d10fc-425">Msistuff.exe</span></span>](msistuff-exe.md)
    -   [<span data-ttu-id="d10fc-426">URL-basiertes Windows Installer-Installationsbeispiel</span><span class="sxs-lookup"><span data-stu-id="d10fc-426">A URL-Based Windows Installer Installation Example</span></span>](a-url-based-windows-installer-installation-example.md)
    -   [<span data-ttu-id="d10fc-427">Konfigurieren der Setup.exe Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d10fc-427">Configuring the Setup.exe Resources</span></span>](configuring-the-setup-exe-resources.md)
    -   [<span data-ttu-id="d10fc-428">Herunterladen einer Installation aus dem Internet</span><span class="sxs-lookup"><span data-stu-id="d10fc-428">Downloading an Installation from the Internet</span></span>](downloading-an-installation-from-the-internet.md)

-   <span data-ttu-id="d10fc-429">Beachten Sie Active Accessibility Richtlinien beim Schreiben von Windows Installer Paketen.</span><span class="sxs-lookup"><span data-stu-id="d10fc-429">Adhere to Active Accessibility guidelines when writing Windows Installer packages.</span></span>

    <span data-ttu-id="d10fc-430">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-430">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-431">Bedienungshilfen</span><span class="sxs-lookup"><span data-stu-id="d10fc-431">Accessibility</span></span>](accessibility.md)

-   <span data-ttu-id="d10fc-432">Bereiten Sie die Internationalisierung eines Anwendungs Setups vor.</span><span class="sxs-lookup"><span data-stu-id="d10fc-432">Prepare for the internationalization of an application setup.</span></span>

    <span data-ttu-id="d10fc-433">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-433">For more information, see the following:</span></span>

    -   <span data-ttu-id="d10fc-434">[Vorbereiten eines Windows Installer Pakets für die Lokalisierung](preparing-a-windows-installer-package-for-localization.md)</span><span class="sxs-lookup"><span data-stu-id="d10fc-434">[Preparing a Windows Installer Package for Localization](preparing-a-windows-installer-package-for-localization.md),</span></span>
    -   [<span data-ttu-id="d10fc-435">Lokalisieren eines Windows Installer Pakets</span><span class="sxs-lookup"><span data-stu-id="d10fc-435">Localizing a Windows Installer Package</span></span>](localizing-a-windows-installer-package.md)
    -   [<span data-ttu-id="d10fc-436">Code Page Behandlung (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="d10fc-436">Code Page Handling (Windows Installer)</span></span>](code-page-handling-windows-installer-.md)
    -   [<span data-ttu-id="d10fc-437">Hinzufügen lokalisierter Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d10fc-437">Adding Localized Resources</span></span>](adding-localized-resources.md)
    -   [<span data-ttu-id="d10fc-438">Beispiel für eine Lokalisierung</span><span class="sxs-lookup"><span data-stu-id="d10fc-438">A Localization Example</span></span>](a-localization-example.md)
    -   [<span data-ttu-id="d10fc-439">Lokalisieren von Fehler-und Aktions Text Tabellen</span><span class="sxs-lookup"><span data-stu-id="d10fc-439">Localizing the Error and ActionText Tables</span></span>](localizing-the-error-and-actiontext-tables.md)
    -   [<span data-ttu-id="d10fc-440">Lokalisieren von Daten Bank Spalten</span><span class="sxs-lookup"><span data-stu-id="d10fc-440">Localizing Database Columns</span></span>](localizing-database-columns.md)
    -   [<span data-ttu-id="d10fc-441">Erstellen einer Datenbank mit einer neutralen Codepage</span><span class="sxs-lookup"><span data-stu-id="d10fc-441">Creating a Database with a Neutral Code Page</span></span>](creating-a-database-with-a-neutral-code-page.md)
    -   [<span data-ttu-id="d10fc-442">Code Page Behandlung importierter und exportierter Tabellen</span><span class="sxs-lookup"><span data-stu-id="d10fc-442">Code Page Handling of Imported and Exported Tables</span></span>](code-page-handling-of-imported-and-exported-tables.md)
    -   [<span data-ttu-id="d10fc-443">Lokalisieren der von Dialogfeldern angezeigten Sprache</span><span class="sxs-lookup"><span data-stu-id="d10fc-443">Localizing the Language Displayed by Dialogs</span></span>](localizing-the-language-displayed-by-dialogs.md)
    -   [<span data-ttu-id="d10fc-444">Importieren lokalisierter Fehler-und Aktions Text Tabellen</span><span class="sxs-lookup"><span data-stu-id="d10fc-444">Importing Localized Error and ActionText Tables</span></span>](importing-localized-error-and-actiontext-tables.md)
    -   [<span data-ttu-id="d10fc-445">Aktualisieren von productlanguage-und ProductCode-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d10fc-445">Updating ProductLanguage and ProductCode Properties</span></span>](updating-productlanguage-and-productcode-properties.md)
    -   [<span data-ttu-id="d10fc-446">Aktualisieren eines Zusammenfassungs Informationsdaten Stroms</span><span class="sxs-lookup"><span data-stu-id="d10fc-446">Updating a Summary Information Stream</span></span>](updating-a-summary-information-stream.md)
    -   [<span data-ttu-id="d10fc-447">Qualifizierte Komponenten</span><span class="sxs-lookup"><span data-stu-id="d10fc-447">Qualified Components</span></span>](qualified-components.md)
    -   [<span data-ttu-id="d10fc-448">UIText-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-448">UIText Table</span></span>](uitext-table.md)
    -   [<span data-ttu-id="d10fc-449">Verwalten von Sprache und Codepage</span><span class="sxs-lookup"><span data-stu-id="d10fc-449">Manage Language and Codepage</span></span>](manage-language-and-codepage.md)
    -   [<span data-ttu-id="d10fc-450">Die Codepage der Installations Datenbank wird überprüft.</span><span class="sxs-lookup"><span data-stu-id="d10fc-450">Checking the Installation Database Code Page</span></span>](checking-the-installation-database-code-page.md)

-   <span data-ttu-id="d10fc-451">Erstellen Sie Windows Installer Pakete für 32-Bit-und 64-Bit-Plattformen.</span><span class="sxs-lookup"><span data-stu-id="d10fc-451">Create Windows Installer packages for 32-bit and 64-bit platforms.</span></span>

    <span data-ttu-id="d10fc-452">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-452">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-453">Windows Installer auf 64-Bit-Betriebssystemen</span><span class="sxs-lookup"><span data-stu-id="d10fc-453">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)
    -   [<span data-ttu-id="d10fc-454">benutzerdefinierte 64-Bit-Aktionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-454">64-Bit Custom Actions</span></span>](64-bit-custom-actions.md)
    -   [<span data-ttu-id="d10fc-455">Verwenden von benutzerdefinierten 64-Bit-Aktionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-455">Using 64-bit Custom Actions</span></span>](using-64-bit-custom-actions.md)
    -   [<span data-ttu-id="d10fc-456">Verwenden von 64-Bit-Mergemodulen</span><span class="sxs-lookup"><span data-stu-id="d10fc-456">Using 64-bit Merge Modules</span></span>](using-64-bit-merge-modules.md)

-   <span data-ttu-id="d10fc-457">Verteilen Sie freigegebene Windows Installer Komponenten und Setup Logik als Mergemodule neu.</span><span class="sxs-lookup"><span data-stu-id="d10fc-457">Redistribute shared Windows Installer components and setup logic as merge modules.</span></span>

    <span data-ttu-id="d10fc-458">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-458">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-459">Mergemodule</span><span class="sxs-lookup"><span data-stu-id="d10fc-459">Merge Modules</span></span>](merge-modules.md)
    -   [<span data-ttu-id="d10fc-460">Erstellen einer sprach Transformation für ein Mergemodul mit mehreren Sprachen</span><span class="sxs-lookup"><span data-stu-id="d10fc-460">Authoring a Language Transform for a Multiple Language Merge Module</span></span>](authoring-a-language-transform-for-a-multiple-language-merge-module.md)
    -   [<span data-ttu-id="d10fc-461">Anwenden eines konfigurierbaren Mergemoduls mit Anpassungen</span><span class="sxs-lookup"><span data-stu-id="d10fc-461">Applying a Configurable Merge Module with Customizations</span></span>](applying-a-configurable-merge-module-with-customizations.md)

-   <span data-ttu-id="d10fc-462">Planen oder Unterdrücken von Neustarts während einer Windows Installer Installation.</span><span class="sxs-lookup"><span data-stu-id="d10fc-462">Schedule or suppress reboots during a Windows Installer installation.</span></span>

    <span data-ttu-id="d10fc-463">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-463">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-464">System Neustarts</span><span class="sxs-lookup"><span data-stu-id="d10fc-464">System Reboots</span></span>](system-reboots.md)
    -   [<span data-ttu-id="d10fc-465">Protokollierung von Neustart Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d10fc-465">Logging of Reboot Requests</span></span>](logging-of-reboot-requests.md)

-   <span data-ttu-id="d10fc-466">Erstellen Sie Updates oder Korrekturen für eine vorhandene Anwendung, indem Sie einen Patch erstellen.</span><span class="sxs-lookup"><span data-stu-id="d10fc-466">Create updates or fixes for an existing application by creating a patch.</span></span>

    <span data-ttu-id="d10fc-467">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-467">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-468">Erstellen eines kleinen Update-Patches</span><span class="sxs-lookup"><span data-stu-id="d10fc-468">Creating a Small Update Patch</span></span>](creating-a-small-update-patch.md)
    -   [<span data-ttu-id="d10fc-469">Beispiel für ein kleines Update-Patching</span><span class="sxs-lookup"><span data-stu-id="d10fc-469">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)

-   <span data-ttu-id="d10fc-470">Erstellen Sie ein Paket mit zwei Zweck, mit dem eine Anwendung entweder nur für den aktuellen Benutzer oder für alle Benutzer des Computers installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="d10fc-470">Author a dual-purpose package capable of installing an application either for only the current user or for all users of the computer.</span></span>

    <span data-ttu-id="d10fc-471">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-471">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-472">Installations Kontext</span><span class="sxs-lookup"><span data-stu-id="d10fc-472">Installation Context</span></span>](installation-context.md)
    -   [<span data-ttu-id="d10fc-473">Erstellung eines einzelnen Pakets</span><span class="sxs-lookup"><span data-stu-id="d10fc-473">Single Package Authoring</span></span>](single-package-authoring.md)
    -   [<span data-ttu-id="d10fc-474">Beispiel für eine einmalige Paket Erstellung</span><span class="sxs-lookup"><span data-stu-id="d10fc-474">Single Package Authoring Example</span></span>](single-package-authoring-example.md)

-   <span data-ttu-id="d10fc-475">Passen Sie die Dienste auf dem Computer mithilfe der Windows Installer an.</span><span class="sxs-lookup"><span data-stu-id="d10fc-475">Customize services on the computer using the Windows Installer.</span></span>

    <span data-ttu-id="d10fc-476">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-476">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-477">Verwenden der Dienst Konfiguration</span><span class="sxs-lookup"><span data-stu-id="d10fc-477">Using Services Configuration</span></span>](using-services-configuration.md)

-   <span data-ttu-id="d10fc-478">Sichern Sie die Ressourcen auf dem Computer mithilfe der Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d10fc-478">Secure resources on the computer using the Windows Installer.</span></span>

    <span data-ttu-id="d10fc-479">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-479">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-480">Richtlinien für das Erstellen von sicheren Installationen</span><span class="sxs-lookup"><span data-stu-id="d10fc-480">Guidelines for Authoring Secure Installations</span></span>](guidelines-for-authoring-secure-installations.md)
    -   [<span data-ttu-id="d10fc-481">Sichern von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d10fc-481">Securing Resources</span></span>](securing-resources-.md)

-   <span data-ttu-id="d10fc-482">Listet alle auf dem Computer installierten Komponenten auf und ruft den Schlüssel Pfad für die Komponente ab.</span><span class="sxs-lookup"><span data-stu-id="d10fc-482">Enumerate all components installed on the computer and obtain the key path for the component.</span></span>

    <span data-ttu-id="d10fc-483">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-483">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-484">Auflisten von Komponenten</span><span class="sxs-lookup"><span data-stu-id="d10fc-484">Enumerating Components</span></span>](enumerating-components-.md)

-   <span data-ttu-id="d10fc-485">Installieren Sie mehrere Pakete mithilfe der [*Transaktionsverarbeitung*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d10fc-485">Install multiple packages using [*transaction processing*](t-gly.md).</span></span>

    <span data-ttu-id="d10fc-486">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-486">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-487">Installationen mit mehreren Paketen</span><span class="sxs-lookup"><span data-stu-id="d10fc-487">Multiple-Package Installations</span></span>](multiple-package-installations.md)

-   <span data-ttu-id="d10fc-488">Betten Sie eine benutzerdefinierte Benutzeroberfläche in das Windows Installer-Paket ein.</span><span class="sxs-lookup"><span data-stu-id="d10fc-488">Embed a custom user interface in the Windows Installer package.</span></span>

    <span data-ttu-id="d10fc-489">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-489">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-490">Verwenden der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d10fc-490">Using the User Interface</span></span>](using-the-user-interface.md)
    -   [<span data-ttu-id="d10fc-491">Verwenden einer eingebetteten Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d10fc-491">Using an Embedded UI</span></span>](using-an-embedded-ui.md)

## <a name="it-professionals"></a><span data-ttu-id="d10fc-492">IT-Fachleute</span><span class="sxs-lookup"><span data-stu-id="d10fc-492">IT Professionals</span></span>

<span data-ttu-id="d10fc-493">IT-Fachleute und Administratoren passen vorhandene Windows Installer Pakete an und stellen Sie bereit.</span><span class="sxs-lookup"><span data-stu-id="d10fc-493">IT Professionals and Administrators customize and deploy existing Windows Installer packages.</span></span> <span data-ttu-id="d10fc-494">Diese Benutzer Verpacken Setups für vorhandene Anwendungen in Windows Installer Installationspaketen und installieren und warten administrative Images von Windows Installer Installationen in Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="d10fc-494">These users repackage setups for existing applications into Windows Installer installation packages, and install and maintain administrative images of Windows Installer installations on networks.</span></span>

-   <span data-ttu-id="d10fc-495">Anpassen von Anwendungen und Setup durch das erzeugen und Anwenden von Windows Installer Transformationen</span><span class="sxs-lookup"><span data-stu-id="d10fc-495">Customize applications and setup by generating and applying Windows Installer transforms</span></span>

    <span data-ttu-id="d10fc-496">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-496">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-497">Anpassung</span><span class="sxs-lookup"><span data-stu-id="d10fc-497">Customization</span></span>](customization.md)
    -   [<span data-ttu-id="d10fc-498">Daten Bank Transformationen</span><span class="sxs-lookup"><span data-stu-id="d10fc-498">Database Transforms</span></span>](database-transforms.md)
    -   [<span data-ttu-id="d10fc-499">Beispiel für eine Anpassungs Transformation</span><span class="sxs-lookup"><span data-stu-id="d10fc-499">A Customization Transform Example</span></span>](a-customization-transform-example.md)
    -   [<span data-ttu-id="d10fc-500">Zusammenführungen und Transformationen</span><span class="sxs-lookup"><span data-stu-id="d10fc-500">Merges and Transforms</span></span>](merges-and-transforms.md)
    -   [<span data-ttu-id="d10fc-501">Verwenden von Transformationen zum Hinzufügen von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d10fc-501">Using Transforms to Add Resources</span></span>](using-transforms-to-add-resources.md)
    -   [<span data-ttu-id="d10fc-502">Generieren einer Transformation</span><span class="sxs-lookup"><span data-stu-id="d10fc-502">Generate a Transform</span></span>](generate-a-transform.md)
    -   [<span data-ttu-id="d10fc-503">Befehlszeilenoptionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-503">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="d10fc-504">Msitran.exe</span><span class="sxs-lookup"><span data-stu-id="d10fc-504">Msitran.exe</span></span>](msitran-exe.md)
    -   [<span data-ttu-id="d10fc-505">Anwenden einer Transformation</span><span class="sxs-lookup"><span data-stu-id="d10fc-505">Apply a Transform</span></span>](apply-a-transform.md)
    -   [<span data-ttu-id="d10fc-506">Anzeigen einer Transformation</span><span class="sxs-lookup"><span data-stu-id="d10fc-506">View a Transform</span></span>](view-a-transform.md)
    -   [<span data-ttu-id="d10fc-507">Anzeigen von Unterschieden zwischen zwei Datenbanken</span><span class="sxs-lookup"><span data-stu-id="d10fc-507">View Differences Between Two Databases</span></span>](view-differences-between-two-databases.md)
    -   [<span data-ttu-id="d10fc-508">Patchen von angepassten Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d10fc-508">Patching Customized Applications</span></span>](patching-customized-applications.md)

-   <span data-ttu-id="d10fc-509">Stellen Sie ein Windows Installer Installationspaket, ein Update oder einen Patch bereit.</span><span class="sxs-lookup"><span data-stu-id="d10fc-509">Deploy a Windows Installer installation package, update, or patch.</span></span>

    <span data-ttu-id="d10fc-510">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-510">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-511">Installieren einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="d10fc-511">Installing an Application</span></span>](installing-an-application.md)
    -   [<span data-ttu-id="d10fc-512">Patchen und Upgrades</span><span class="sxs-lookup"><span data-stu-id="d10fc-512">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="d10fc-513">Transformationen</span><span class="sxs-lookup"><span data-stu-id="d10fc-513">Transforms</span></span>](transforms.md)
    -   [<span data-ttu-id="d10fc-514">Installieren eines Pakets mit erhöhten Rechten für einen nicht Administrator</span><span class="sxs-lookup"><span data-stu-id="d10fc-514">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="d10fc-515">Anwenden von größeren Upgrades durch Patchen der lokalen Installation des Produkts</span><span class="sxs-lookup"><span data-stu-id="d10fc-515">Applying Major Upgrades by Patching the Local Installation of the Product</span></span>](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="d10fc-516">Anwenden von größeren Upgrades durch Installieren des Produkts</span><span class="sxs-lookup"><span data-stu-id="d10fc-516">Applying Major Upgrades by Installing the Product</span></span>](applying-major-upgrades-by-installing-the-product.md)
    -   [<span data-ttu-id="d10fc-517">Anwenden von kleinen Updates durch Patchen der lokalen Installation des Produkts</span><span class="sxs-lookup"><span data-stu-id="d10fc-517">Applying Small Updates by Patching the Local Installation of the Product</span></span>](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="d10fc-518">Anwenden von kleinen Updates durch Neuinstallation des Produkts</span><span class="sxs-lookup"><span data-stu-id="d10fc-518">Applying Small Updates by Reinstalling the Product</span></span>](applying-small-updates-by-reinstalling-the-product.md)
    -   [<span data-ttu-id="d10fc-519">Anwenden von kleinen Updates durch Patchen eines administrativen Abbilds</span><span class="sxs-lookup"><span data-stu-id="d10fc-519">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="d10fc-520">Patchen von erst Installationen</span><span class="sxs-lookup"><span data-stu-id="d10fc-520">Patching Initial Installations</span></span>](patching-initial-installations.md)
    -   [<span data-ttu-id="d10fc-521">Befehlszeilenoptionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-521">Command Line Options</span></span>](command-line-options.md)

-   <span data-ttu-id="d10fc-522">Behandeln von Problemen mit Windows Installer Paketen</span><span class="sxs-lookup"><span data-stu-id="d10fc-522">Troubleshoot Windows Installer packages.</span></span>

    <span data-ttu-id="d10fc-523">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-523">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-524">Windows Installer Protokollierung</span><span class="sxs-lookup"><span data-stu-id="d10fc-524">Windows Installer Logging</span></span>](windows-installer-logging.md)
    -   [<span data-ttu-id="d10fc-525">Überprüfen der Installation von Features, Komponenten, Dateien</span><span class="sxs-lookup"><span data-stu-id="d10fc-525">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
    -   [<span data-ttu-id="d10fc-526">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="d10fc-526">Wilogutl.exe</span></span>](wilogutl-exe.md)
    -   [<span data-ttu-id="d10fc-527">Suchen nach einer unterbrochenen Funktion oder Komponente</span><span class="sxs-lookup"><span data-stu-id="d10fc-527">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="d10fc-528">Windows Installer von Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="d10fc-528">Windows Installer Error Messages</span></span>](windows-installer-error-messages.md)
    -   [<span data-ttu-id="d10fc-529">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="d10fc-529">Msicert.exe</span></span>](msicert-exe.md)

-   <span data-ttu-id="d10fc-530">Verwenden Sie Skripts zum Abfragen von Windows Installer Paketen, um Informationen zu einem Produkt zu finden und die Installation zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d10fc-530">Use scripting to query Windows Installer packages for information about a product and modify the installation.</span></span>

    <span data-ttu-id="d10fc-531">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-531">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-532">Automatisierungsschnittstelle</span><span class="sxs-lookup"><span data-stu-id="d10fc-532">Automation Interface</span></span>](automation-interface.md)
    -   [<span data-ttu-id="d10fc-533">Skript Beispiele für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d10fc-533">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
    -   [<span data-ttu-id="d10fc-534">Verwenden von Windows Installer mit WMI</span><span class="sxs-lookup"><span data-stu-id="d10fc-534">Using Windows Installer with WMI</span></span>](using-windows-installer-with-wmi.md)

-   <span data-ttu-id="d10fc-535">Erstellen und warten Sie administrative Installationen.</span><span class="sxs-lookup"><span data-stu-id="d10fc-535">Create and maintain administrative installations.</span></span>

    <span data-ttu-id="d10fc-536">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-536">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-537">Administrative Installation</span><span class="sxs-lookup"><span data-stu-id="d10fc-537">Administrative Installation</span></span>](administrative-installation.md)
    -   [<span data-ttu-id="d10fc-538">Befehlszeilenoptionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-538">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="d10fc-539">**Adminproperties (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="d10fc-539">**AdminProperties Property**</span></span>](adminproperties.md)
    -   [<span data-ttu-id="d10fc-540">Anwenden von kleinen Updates durch Patchen eines administrativen Abbilds</span><span class="sxs-lookup"><span data-stu-id="d10fc-540">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="d10fc-541">Anwenden eines Patchpakets auf eine administrative Installation</span><span class="sxs-lookup"><span data-stu-id="d10fc-541">Applying a Patch Package to an Administrative Installation</span></span>](applying-a-patch-package-to-an-administrative-installation.md)
    -   [<span data-ttu-id="d10fc-542">Aktions Ausführungsreihenfolge</span><span class="sxs-lookup"><span data-stu-id="d10fc-542">Action Execution Order</span></span>](action-execution-order.md)
    -   [<span data-ttu-id="d10fc-543">**Isadminpackage (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="d10fc-543">**IsAdminPackage Property**</span></span>](isadminpackage.md)
    -   [<span data-ttu-id="d10fc-544">Reihenfolge der Eigenschafts Rangfolge</span><span class="sxs-lookup"><span data-stu-id="d10fc-544">Order of Property Precedence</span></span>](order-of-property-precedence.md)
    -   [<span data-ttu-id="d10fc-545">**Adminproperties (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="d10fc-545">**AdminProperties Property**</span></span>](adminproperties.md)

-   <span data-ttu-id="d10fc-546">Stellen Sie eine Anwendung für alle Benutzer eines Computers oder nur für einen bestimmten Benutzer zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d10fc-546">Make an application available to all users of a computer or to a specified user only.</span></span>

    <span data-ttu-id="d10fc-547">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-547">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-548">Installations Kontext</span><span class="sxs-lookup"><span data-stu-id="d10fc-548">Installation Context</span></span>](installation-context.md)
    -   [<span data-ttu-id="d10fc-549">**ALLUSERS (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="d10fc-549">**ALLUSERS Property**</span></span>](allusers.md)

-   <span data-ttu-id="d10fc-550">Verwenden Sie die Befehlszeile, um Pakete zu interpretieren, Produkte zu installieren und Funktions Optionen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d10fc-550">Interpret packages, install products, and configure feature options using a command line.</span></span>

    <span data-ttu-id="d10fc-551">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-551">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-552">Befehlszeilenoptionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-552">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="d10fc-553">Festlegen von Werten für öffentliche Eigenschaften in der Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="d10fc-553">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
    -   [<span data-ttu-id="d10fc-554">Eigenschaften werden erhalten und festgelegt</span><span class="sxs-lookup"><span data-stu-id="d10fc-554">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
    -   [<span data-ttu-id="d10fc-555">Neuinstallieren eines Features oder einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="d10fc-555">Reinstalling a Feature or Application</span></span>](reinstalling-a-feature-or-application.md)
    -   [<span data-ttu-id="d10fc-556">Anwenden von kleinen Updates durch Patchen der lokalen Installation des Produkts</span><span class="sxs-lookup"><span data-stu-id="d10fc-556">Applying Small Updates by Patching the Local Installation of the Product</span></span>](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="d10fc-557">Anwenden von kleinen Updates durch Neuinstallation des Produkts</span><span class="sxs-lookup"><span data-stu-id="d10fc-557">Applying Small Updates by Reinstalling the Product</span></span>](applying-small-updates-by-reinstalling-the-product.md)
    -   [<span data-ttu-id="d10fc-558">Ändern des Zielspeicher Orts für ein Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="d10fc-558">Changing the Target Location for a Directory</span></span>](changing-the-target-location-for-a-directory.md)
    -   [<span data-ttu-id="d10fc-559">Anwenden von kleinen Updates durch Patchen eines administrativen Abbilds</span><span class="sxs-lookup"><span data-stu-id="d10fc-559">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="d10fc-560">Anwenden von größeren Upgrades durch Installieren des Produkts</span><span class="sxs-lookup"><span data-stu-id="d10fc-560">Applying Major Upgrades by Installing the Product</span></span>](applying-major-upgrades-by-installing-the-product.md)
    -   [<span data-ttu-id="d10fc-561">Konfigurations Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d10fc-561">Configuration Properties</span></span>](property-reference.md)
    -   [<span data-ttu-id="d10fc-562">Eigenschaften von featureinstallationsoptionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-562">Feature Installation Options Properties</span></span>](property-reference.md)

-   <span data-ttu-id="d10fc-563">Arbeiten Sie mit der Richtlinie, um Zugriffsrechte und Berechtigungen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="d10fc-563">Work with policy to manage access rights and permissions.</span></span>

    <span data-ttu-id="d10fc-564">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-564">For more information, see the following:</span></span>

    -   <span data-ttu-id="d10fc-565">[Computer Richtlinien](machine-policies.md),</span><span class="sxs-lookup"><span data-stu-id="d10fc-565">[Machine Policies](machine-policies.md),</span></span>
    -   <span data-ttu-id="d10fc-566">[Benutzerrichtlinien](user-policies.md)</span><span class="sxs-lookup"><span data-stu-id="d10fc-566">[User Policies](user-policies.md),</span></span>
    -   [<span data-ttu-id="d10fc-567">Installieren eines Pakets mit erhöhten Rechten für einen nicht Administrator</span><span class="sxs-lookup"><span data-stu-id="d10fc-567">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="d10fc-568">Ankündigen einer Per-User Anwendung, die mit erhöhten Rechten installiert werden soll</span><span class="sxs-lookup"><span data-stu-id="d10fc-568">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [<span data-ttu-id="d10fc-569">Verwenden einer benutzerdefinierten Aktion zum Erstellen von Benutzerkonten auf einem lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="d10fc-569">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="d10fc-570">**AdminUser (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="d10fc-570">**AdminUser Property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="d10fc-571">**Privilegierte Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="d10fc-571">**Privileged Property**</span></span>](privileged.md)
    -   [<span data-ttu-id="d10fc-572">**Enableusercontrol (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="d10fc-572">**EnableUserControl Property**</span></span>](enableusercontrol.md)
    -   [<span data-ttu-id="d10fc-573">**UserSID-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="d10fc-573">**UserSID Property**</span></span>](usersid.md)
    -   [<span data-ttu-id="d10fc-574">**Securecustomproperties (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="d10fc-574">**SecureCustomProperties Property**</span></span>](securecustomproperties.md)

-   <span data-ttu-id="d10fc-575">Installieren Sie mehrere Pakete mithilfe der [*Transaktionsverarbeitung*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d10fc-575">Install multiple packages using [*transaction processing*](t-gly.md).</span></span>

    <span data-ttu-id="d10fc-576">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-576">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-577">Installationen mit mehreren Paketen</span><span class="sxs-lookup"><span data-stu-id="d10fc-577">Multiple-Package Installations</span></span>](multiple-package-installations.md)

-   <span data-ttu-id="d10fc-578">Betten Sie eine benutzerdefinierte Benutzeroberfläche in ein Windows Installer Paket ein.</span><span class="sxs-lookup"><span data-stu-id="d10fc-578">Embed a custom user interface within a Windows Installer package..</span></span>

    <span data-ttu-id="d10fc-579">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-579">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-580">Verwenden der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d10fc-580">Using the User Interface</span></span>](using-the-user-interface.md)
    -   [<span data-ttu-id="d10fc-581">Verwenden einer eingebetteten Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d10fc-581">Using an Embedded UI</span></span>](using-an-embedded-ui.md)

## <a name="infrastructure-developers"></a><span data-ttu-id="d10fc-582">Infrastruktur Entwickler</span><span class="sxs-lookup"><span data-stu-id="d10fc-582">Infrastructure Developers</span></span>

<span data-ttu-id="d10fc-583">Infrastruktur Entwickler können einheitliche Plattformen für die Bereitstellung und Verwaltung von Software erstellen, die den Windows Installer-Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="d10fc-583">Infrastructure Developers can create unified platforms for the deployment and management of software that uses the Windows Installer service.</span></span> <span data-ttu-id="d10fc-584">Sie können die Windows Installer Programmierschnittstelle verwenden, um Anwendungen, Patches und Quellen auf einem System abzufragen, zu verwalten und zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="d10fc-584">They can use the Windows Installer programming interface to query, manage, and distribute applications, patches, and sources on a system.</span></span>

-   <span data-ttu-id="d10fc-585">Suchen, inventarisieren und Abfragen des Zustands, der Informationen und der Clients von Komponenten.</span><span class="sxs-lookup"><span data-stu-id="d10fc-585">Locate, inventory and query for the state, information, and clients of components.</span></span>

    <span data-ttu-id="d10fc-586">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-586">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-587">Komponenten spezifische Funktionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-587">Component-Specific Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="d10fc-588">System Status Funktionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-588">System Status Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="d10fc-589">Installer-Objekt</span><span class="sxs-lookup"><span data-stu-id="d10fc-589">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="d10fc-590">Product-Objekt</span><span class="sxs-lookup"><span data-stu-id="d10fc-590">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="d10fc-591">Patch-Objekt</span><span class="sxs-lookup"><span data-stu-id="d10fc-591">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="d10fc-592">Inventarisieren Sie Informationen und den Status von Produkten und Features, und Fragen Sie Sie ab.</span><span class="sxs-lookup"><span data-stu-id="d10fc-592">Inventory and query for information and the state of products and features.</span></span>

    <span data-ttu-id="d10fc-593">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-593">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-594">Inventur Produkte und Patches</span><span class="sxs-lookup"><span data-stu-id="d10fc-594">Inventory products and patches</span></span>](inventory-products-and-patches-.md)
    -   [<span data-ttu-id="d10fc-595">System Status Funktionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-595">System Status Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="d10fc-596">Product Query-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-596">Product Query Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="d10fc-597">Installer-Objekt</span><span class="sxs-lookup"><span data-stu-id="d10fc-597">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="d10fc-598">Product-Objekt</span><span class="sxs-lookup"><span data-stu-id="d10fc-598">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="d10fc-599">Patch-Objekt</span><span class="sxs-lookup"><span data-stu-id="d10fc-599">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="d10fc-600">Verbessern Sie die Resilienz der Quelle, indem Sie die Windows Installer zum Inventarisieren, Abfragen und Ändern der Quell Liste von Anwendungen, Upgrades und Patches verwenden.</span><span class="sxs-lookup"><span data-stu-id="d10fc-600">Improve source resiliency by using the Windows Installer to inventory, query, and modify the source list of applications, upgrades, and patches.</span></span>

    <span data-ttu-id="d10fc-601">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-601">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-602">**SourceList-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="d10fc-602">**SOURCELIST Property**</span></span>](sourcelist.md)
    -   [<span data-ttu-id="d10fc-603">**Quellen Resilienz**</span><span class="sxs-lookup"><span data-stu-id="d10fc-603">**Source Resiliency**</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="d10fc-604">Installations-und Konfigurationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-604">Installation and Configuration Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="d10fc-605">Installer-Objekt</span><span class="sxs-lookup"><span data-stu-id="d10fc-605">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="d10fc-606">Product-Objekt</span><span class="sxs-lookup"><span data-stu-id="d10fc-606">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="d10fc-607">Patch-Objekt</span><span class="sxs-lookup"><span data-stu-id="d10fc-607">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="d10fc-608">Verbessern Sie die Resilienz der Quelle, indem Sie mithilfe der Windows Installer Medienquellen inventarisieren, Abfragen und ändern.</span><span class="sxs-lookup"><span data-stu-id="d10fc-608">Improve source resiliency by using the Windows Installer to inventory, query, and modify media sources.</span></span>

    <span data-ttu-id="d10fc-609">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-609">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-610">**SourceList-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="d10fc-610">**SOURCELIST Property**</span></span>](sourcelist.md)
    -   [<span data-ttu-id="d10fc-611">Quellen Resilienz</span><span class="sxs-lookup"><span data-stu-id="d10fc-611">Source Resiliency</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="d10fc-612">Installations-und Konfigurationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="d10fc-612">Installation and Configuration Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="d10fc-613">Product-Objekt</span><span class="sxs-lookup"><span data-stu-id="d10fc-613">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="d10fc-614">Patch-Objekt</span><span class="sxs-lookup"><span data-stu-id="d10fc-614">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="d10fc-615">Inventarisieren Sie Informationen und den Status von Patches, um diese abzufragen.</span><span class="sxs-lookup"><span data-stu-id="d10fc-615">Inventory and query for information and the state of patches.</span></span>

    <span data-ttu-id="d10fc-616">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-616">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-617">Inventur Produkte und Patches</span><span class="sxs-lookup"><span data-stu-id="d10fc-617">Inventory products and patches</span></span>](inventory-products-and-patches-.md)
    -   [<span data-ttu-id="d10fc-618">Installationsfunktionsverweis</span><span class="sxs-lookup"><span data-stu-id="d10fc-618">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="d10fc-619">Patch-Objekt</span><span class="sxs-lookup"><span data-stu-id="d10fc-619">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="d10fc-620">Arbeiten Sie mit der Richtlinie, um Zugriffsrechte und Berechtigungen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="d10fc-620">Work with policy to manage access rights and permissions.</span></span>

    <span data-ttu-id="d10fc-621">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="d10fc-621">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d10fc-622">Computer Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d10fc-622">Machine Policies</span></span>](machine-policies.md)
    -   [<span data-ttu-id="d10fc-623">Benutzerrichtlinien</span><span class="sxs-lookup"><span data-stu-id="d10fc-623">User Policies</span></span>](user-policies.md)
    -   [<span data-ttu-id="d10fc-624">Installieren eines Pakets mit erhöhten Rechten für einen nicht Administrator</span><span class="sxs-lookup"><span data-stu-id="d10fc-624">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="d10fc-625">Ankündigen einer Per-User Anwendung, die mit erhöhten Rechten installiert werden soll</span><span class="sxs-lookup"><span data-stu-id="d10fc-625">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [<span data-ttu-id="d10fc-626">Verwenden einer benutzerdefinierten Aktion zum Erstellen von Benutzerkonten auf einem lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="d10fc-626">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="d10fc-627">**AdminUser (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="d10fc-627">**AdminUser Property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="d10fc-628">**Privilegierte Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="d10fc-628">**Privileged Property**</span></span>](privileged.md)
    -   [<span data-ttu-id="d10fc-629">**Enableusercontrol (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="d10fc-629">**EnableUserControl Property**</span></span>](enableusercontrol.md)
    -   [<span data-ttu-id="d10fc-630">**UserSID-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="d10fc-630">**UserSID Property**</span></span>](usersid.md)
    -   [<span data-ttu-id="d10fc-631">**Securecustomproperties (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="d10fc-631">**SecureCustomProperties Property**</span></span>](securecustomproperties.md)

 

 



