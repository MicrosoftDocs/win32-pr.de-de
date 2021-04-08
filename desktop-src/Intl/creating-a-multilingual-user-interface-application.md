---
description: In diesem Tutorial wird veranschaulicht, wie Sie eine monolingual-Anwendung erstellen und Sie als weltweit bereitstellen. Diese Anwendung ist in Form einer umfassenden Lösung, die in Microsoft Visual Studio erstellt wird.
ms.assetid: 6d71aa90-8444-4f30-a2f8-f1a2aab015b0
title: Hinzufügen von Unterstützung für mehrsprachige Benutzeroberflächen zu Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192d9053513a7fe915990c80deb32ffdb9114910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867944"
---
# <a name="adding-multilingual-user-interface-support-to-an-application"></a><span data-ttu-id="11792-104">Hinzufügen von Unterstützung für mehrsprachige Benutzeroberflächen zu Anwendungen</span><span class="sxs-lookup"><span data-stu-id="11792-104">Adding Multilingual User Interface Support to an Application</span></span>

<span data-ttu-id="11792-105">In diesem Tutorial wird veranschaulicht, wie Sie eine monolingual-Anwendung erstellen und Sie als weltweit bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="11792-105">This tutorial demonstrates how to take a monolingual application and make it world-ready.</span></span> <span data-ttu-id="11792-106">Diese Anwendung ist in Form einer umfassenden Lösung, die in Microsoft Visual Studio erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="11792-106">This application is in the form of a complete solution that is built within Microsoft Visual Studio.</span></span>

-   [<span data-ttu-id="11792-107">Übersicht</span><span class="sxs-lookup"><span data-stu-id="11792-107">Overview</span></span>](#splitting-the-various-language-resource-modules-an-overview)
    -   [<span data-ttu-id="11792-108">Die Idee hinter Hello MUI</span><span class="sxs-lookup"><span data-stu-id="11792-108">The Idea Behind Hello MUI</span></span>](#the-idea-behind-hello-mui)
-   [<span data-ttu-id="11792-109">Einrichten der Hello MUI-Lösung</span><span class="sxs-lookup"><span data-stu-id="11792-109">Setting up the Hello MUI Solution</span></span>](#setting-up-the-hello-mui-solution)
    -   [<span data-ttu-id="11792-110">Platt Form Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11792-110">Platform Requirements</span></span>](#platform-requirements)
    -   [<span data-ttu-id="11792-111">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="11792-111">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="11792-112">Schritt 0: Erstellen der hart codierten Hello MUI</span><span class="sxs-lookup"><span data-stu-id="11792-112">Step 0: Creating the Hard-coded Hello MUI</span></span>](#step-0-creating-the-hard-coded-hello-mui)
-   [<span data-ttu-id="11792-113">Schritt 1: Implementieren des grundlegenden Ressourcen Moduls</span><span class="sxs-lookup"><span data-stu-id="11792-113">Step 1: Implementing the Basic Resource Module</span></span>](#step-1-implementing-the-basic-resource-module)
-   [<span data-ttu-id="11792-114">Schritt 2: aufbauen des grundlegenden Ressourcen Moduls</span><span class="sxs-lookup"><span data-stu-id="11792-114">Step 2: Building the Basic Resource Module</span></span>](#step-2-building-the-basic-resource-module)
    -   [<span data-ttu-id="11792-115">Aufteilen der verschiedenen Sprachressourcen Module: eine Übersicht</span><span class="sxs-lookup"><span data-stu-id="11792-115">Splitting the Various Language Resource Modules: An Overview</span></span>](#splitting-the-various-language-resource-modules-an-overview)
    -   [<span data-ttu-id="11792-116">Aufteilen der verschiedenen Sprachressourcen Module: Erstellen der Dateien</span><span class="sxs-lookup"><span data-stu-id="11792-116">Splitting the Various Language Resource Modules: Creating the Files</span></span>](#splitting-the-various-language-resource-modules-creating-the-files)
-   [<span data-ttu-id="11792-117">Schritt 3: Erstellen eines Resource-Savvy "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="11792-117">Step 3: Creating a Resource-Savvy "Hello MUI"</span></span>](#step-3-creating-a-resource-savvy-hello-mui)
-   [<span data-ttu-id="11792-118">Schritt 4: Globalisieren von "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="11792-118">Step 4: Globalizing "Hello MUI"</span></span>](#step-4-globalizing-hello-mui)
-   [<span data-ttu-id="11792-119">Schritt 5: Anpassen von "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="11792-119">Step 5: Customizing "Hello MUI"</span></span>](#step-5-customizing-hello-mui)
-   [<span data-ttu-id="11792-120">Weitere Überlegungen zu MUI</span><span class="sxs-lookup"><span data-stu-id="11792-120">Additional Considerations for MUI</span></span>](#additional-considerations-for-mui)
    -   [<span data-ttu-id="11792-121">Unterstützung für Konsolen Anwendungen</span><span class="sxs-lookup"><span data-stu-id="11792-121">Support for Console Applications</span></span>](#support-for-console-applications)
    -   [<span data-ttu-id="11792-122">Bestimmung der zur Laufzeit zu unterstützten Sprachen</span><span class="sxs-lookup"><span data-stu-id="11792-122">Determination of Languages to Support at Run-Time</span></span>](#determination-of-languages-to-support-at-run-time)
    -   [<span data-ttu-id="11792-123">Unterstützung komplexer Skripts in Versionen vor Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11792-123">Complex Script Support in Versions Prior to Windows Vista</span></span>](#complex-script-support-in-versions-prior-to-windows-vista)
-   [<span data-ttu-id="11792-124">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="11792-124">Summary</span></span>](#summary)

## <a name="overview"></a><span data-ttu-id="11792-125">Übersicht</span><span class="sxs-lookup"><span data-stu-id="11792-125">Overview</span></span>

<span data-ttu-id="11792-126">Ab Windows Vista wurde das Windows-Betriebssystem von Grund auf als mehrsprachige Plattform entwickelt, mit zusätzlicher Unterstützung, die es Ihnen ermöglicht, mehrsprachige Anwendungen zu erstellen, die das Windows MUI-Ressourcenmodell verwenden.</span><span class="sxs-lookup"><span data-stu-id="11792-126">Beginning with Windows Vista, the Windows operating system itself was built from the ground up to be a multilingual platform, with additional support that enables you to create multilingual applications that use the Windows MUI resource model.</span></span>

<span data-ttu-id="11792-127">Dieses Tutorial veranschaulicht diese neue Unterstützung für mehrsprachige Anwendungen, indem die folgenden Aspekte abgedeckt werden:</span><span class="sxs-lookup"><span data-stu-id="11792-127">This tutorial illustrates this new support for multilingual applications by covering the following aspects:</span></span>

-   <span data-ttu-id="11792-128">Verwendet die verbesserte MUI-Platt Form Unterstützung, um mehrsprachige Anwendungen problemlos zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="11792-128">Uses the improved MUI platform support to easily enable multilingual applications.</span></span>
-   <span data-ttu-id="11792-129">Erweitert mehrsprachige Anwendungen für die Ausführung unter Windows-Versionen vor Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="11792-129">Extends multilingual applications to run on versions of Windows prior to Windows Vista.</span></span>
-   <span data-ttu-id="11792-130">Berührt die zusätzlichen Überlegungen bei der Entwicklung von spezialisierten mehrsprachigen Anwendungen, wie z. b. Konsolen Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="11792-130">Touches on the additional considerations involved in developing specialized multilingual applications such as console applications.</span></span>

<span data-ttu-id="11792-131">Diese Links helfen Ihnen, eine schnelle Auffrischung der Konzepte bei Internationalisierung und MUI zu ermöglichen:</span><span class="sxs-lookup"><span data-stu-id="11792-131">These links help provide a quick refresher on the concepts on internationalization and MUI:</span></span>

-   <span data-ttu-id="11792-132">[Kurze Übersicht](understanding-internationalization.md)über die Internationalisierung.</span><span class="sxs-lookup"><span data-stu-id="11792-132">[Quick overview of internationalization](understanding-internationalization.md).</span></span>
-   <span data-ttu-id="11792-133">[MUI-Konzepte](understanding-mui.md).</span><span class="sxs-lookup"><span data-stu-id="11792-133">[MUI Concepts](understanding-mui.md).</span></span>
-   <span data-ttu-id="11792-134">[Verwenden von MUI zum Entwickeln von Win32-Anwendungen](using-multilingual-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="11792-134">[Using MUI to develop Win32 applications](using-multilingual-user-interface.md).</span></span>

### <a name="the-idea-behind-hello-mui"></a><span data-ttu-id="11792-135">Die Idee hinter Hello MUI</span><span class="sxs-lookup"><span data-stu-id="11792-135">The Idea Behind Hello MUI</span></span>

<span data-ttu-id="11792-136">Sie sind wahrscheinlich mit der klassischen Hallo Welt Anwendung vertraut, die grundlegende Programmier Konzepte veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="11792-136">You are probably familiar with the classic Hello World application, which illustrates basic programming concepts.</span></span> <span data-ttu-id="11792-137">Dieses Tutorial veranschaulicht, wie Sie mit dem MUI-Ressourcenmodell eine monolingual-Anwendung aktualisieren, um eine mehrsprachige Version mit dem Namen "Hello MUI" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="11792-137">This tutorial takes a similar approach to illustrate how to use the MUI resource model to update a monolingual application to create a multilingual version called Hello MUI.</span></span>

> [!Note]  
> <span data-ttu-id="11792-138">Die Aufgaben in diesem Tutorial werden anhand der Genauigkeit, mit der diese Aktivitäten ausgeführt werden müssen, in ausführlichen Schritten beschrieben. Außerdem müssen Sie die Details für Entwickler, die nur wenig mit diesen Aufgaben vertraut sind, erläutern.</span><span class="sxs-lookup"><span data-stu-id="11792-138">The tasks in this tutorial are described in detailed steps because of the precision with which these activities must be performed, and the need to explain the details to developers who have little experience with these tasks.</span></span>

 

## <a name="setting-up-the-hello-mui-solution"></a><span data-ttu-id="11792-139">Einrichten der Hello MUI-Lösung</span><span class="sxs-lookup"><span data-stu-id="11792-139">Setting up the Hello MUI Solution</span></span>

<span data-ttu-id="11792-140">Diese Schritte beschreiben, wie Sie die Erstellung der Hello MUI-Lösung vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="11792-140">These steps outline how to prepare to create the Hello MUI solution.</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="11792-141">Plattformanforderungen</span><span class="sxs-lookup"><span data-stu-id="11792-141">Platform Requirements</span></span>

<span data-ttu-id="11792-142">Die Codebeispiele in diesem Tutorial müssen mithilfe des Windows Software Development Kit (SDK) für Windows 7 und Visual Studio 2008 kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="11792-142">You must compile the code samples in this tutorial using the Windows Software Development Kit (SDK) for Windows 7 and Visual Studio 2008.</span></span> <span data-ttu-id="11792-143">Das Windows 7 SDK wird unter Windows XP, Windows Vista und Windows 7 installiert, und die Beispiellösung kann auf jeder dieser Betriebssystemversionen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="11792-143">The Windows 7 SDK will install on Windows XP, Windows Vista and Windows 7, and the sample solution can be built on any of these operating system versions.</span></span>

<span data-ttu-id="11792-144">Alle Codebeispiele in diesem Tutorial sind für die Ausführung auf x86-und x64-Versionen von Windows XP, Windows Vista und Windows 7 konzipiert.</span><span class="sxs-lookup"><span data-stu-id="11792-144">All code samples in this tutorial are designed to be executed on x86 and x64 versions of Windows XP, Windows Vista and Windows 7.</span></span> <span data-ttu-id="11792-145">Bestimmte Teile, die unter Windows XP nicht funktionieren, werden bei Bedarf genannt.</span><span class="sxs-lookup"><span data-stu-id="11792-145">Specific parts that will not work on Windows XP are called out where appropriate.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="11792-146">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="11792-146">Prerequisites</span></span>

1.  <span data-ttu-id="11792-147">Installieren Sie Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="11792-147">Install Visual Studio 2008.</span></span>

    <span data-ttu-id="11792-148">Weitere Informationen finden Sie im [Visual Studio Developer Center](https://msdn.microsoft.com/vstudio/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="11792-148">For more information, see the [Visual Studio Developer Center](https://msdn.microsoft.com/vstudio/default.aspx).</span></span>

2.  <span data-ttu-id="11792-149">Installieren Sie die Windows SDK für Windows 7.</span><span class="sxs-lookup"><span data-stu-id="11792-149">Install the Windows SDK for Windows 7.</span></span>

    <span data-ttu-id="11792-150">Sie können Sie über die Seite Windows SDK des [Windows Developer Centers](https://msdn.microsoft.com/windowsserver/bb980924.aspx)installieren.</span><span class="sxs-lookup"><span data-stu-id="11792-150">You can install it from the Windows SDK page of the [Windows Developer Center](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span></span> <span data-ttu-id="11792-151">Das SDK umfasst Hilfsprogramme zum Entwickeln von Anwendungen für Betriebssystemversionen ab Windows XP bis zu den neuesten Versionen.</span><span class="sxs-lookup"><span data-stu-id="11792-151">The SDK includes utilities to develop applications for OS versions starting from Windows XP through the most recent.</span></span>

    > [!Note]  
    > <span data-ttu-id="11792-152">Wenn Sie das Paket nicht am Standard Speicherort installieren, oder wenn Sie nicht auf dem Systemlaufwerk installieren, bei dem es sich normalerweise um das Laufwerk C handelt, notieren Sie sich den Installationspfad.</span><span class="sxs-lookup"><span data-stu-id="11792-152">If you are not installing the package to the default location, or if you are not installing on the system drive, which is usually the C drive, make note of the install path.</span></span>

     

3.  <span data-ttu-id="11792-153">Konfigurieren Sie die Visual Studio-Befehlszeilenparameter.</span><span class="sxs-lookup"><span data-stu-id="11792-153">Configure the Visual Studio command line parameters.</span></span>

    1.  <span data-ttu-id="11792-154">Öffnen Sie ein Visual Studio-Befehlsfenster.</span><span class="sxs-lookup"><span data-stu-id="11792-154">Open a Visual Studio command window.</span></span>
    2.  <span data-ttu-id="11792-155">Der **Pfad für die Typmenge**.</span><span class="sxs-lookup"><span data-stu-id="11792-155">Type **set path**.</span></span>
    3.  <span data-ttu-id="11792-156">Vergewissern Sie sich, dass die PATH-Variable den Pfad des Ordners bin des Windows 7 SDK enthält:... Microsoft sdert \\ Windows \\ v 7.0 \\ bin</span><span class="sxs-lookup"><span data-stu-id="11792-156">Confirm that the path variable includes the path of the bin folder of the Windows 7 SDK: ...Microsoft SDKs\\Windows\\v7.0\\bin</span></span>

4.  <span data-ttu-id="11792-157">Installieren Sie das Add-on-Paket Microsoft nls-kompatible-APIs.</span><span class="sxs-lookup"><span data-stu-id="11792-157">Install the Microsoft NLS downlevel APIs add-on package.</span></span>
    > [!Note]  
    > <span data-ttu-id="11792-158">Im Rahmen dieses Tutorials ist dieses Paket nur erforderlich, wenn Sie die Anwendung so anpassen, dass Sie unter Windows-Versionen vor Windows Vista ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="11792-158">In the context of this tutorial, this package is necessary only if you will be customizing the application to run on Windows versions prior to Windows Vista.</span></span> <span data-ttu-id="11792-159">Weitere Informationen finden Sie unter [Schritt 5: Anpassen von Hello MUI](#step-5-customizing-hello-mui).</span><span class="sxs-lookup"><span data-stu-id="11792-159">See [Step 5: Customizing Hello MUI](#step-5-customizing-hello-mui).</span></span>

     

    1.  <span data-ttu-id="11792-160">Laden Sie das Paket von seiner [Download Website](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en)herunter, und installieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="11792-160">Download and install the package from its [download site](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en).</span></span>
    2.  <span data-ttu-id="11792-161">Wenn Sie das Paket nicht am Standard Speicherort installieren, oder wenn Sie nicht auf dem Systemlaufwerk installieren (normalerweise Laufwerk C), notieren Sie sich den Installationspfad, wenn Sie das Paket nicht am Standard Speicherort installieren. Windows SDK</span><span class="sxs-lookup"><span data-stu-id="11792-161">As with the Windows SDK, if you are not installing the package to the default location, or if you are not installing on the system drive, which is usually the C drive, make note of the install path.</span></span>
    3.  <span data-ttu-id="11792-162">Wenn Ihre Entwicklungsplattform Windows XP oder Windows Server 2003 ist, vergewissern Sie sich, dass Nlsdl.dll ordnungsgemäß installiert und registriert ist.</span><span class="sxs-lookup"><span data-stu-id="11792-162">If your development platform is Windows XP or Windows Server 2003, confirm that Nlsdl.dll is installed and registered correctly.</span></span>

        1.  <span data-ttu-id="11792-163">Navigieren Sie zum Ordner "Redist" unter dem Speicherort des Installations Pfads.</span><span class="sxs-lookup"><span data-stu-id="11792-163">Browse to the "redist" folder under the install path location.</span></span>
        2.  <span data-ttu-id="11792-164">Führen Sie die entsprechende verteilbare nlsdl aus \* . exe, z. b. nlsdl.x86.exe.</span><span class="sxs-lookup"><span data-stu-id="11792-164">Run the appropriate redistributable Nlsdl.\*.exe, such as nlsdl.x86.exe.</span></span> <span data-ttu-id="11792-165">In diesem Schritt werden Nlsdl.dll installiert und registriert.</span><span class="sxs-lookup"><span data-stu-id="11792-165">This step installs and registers Nlsdl.dll.</span></span>

    > [!Note]  
    > <span data-ttu-id="11792-166">Wenn Sie eine Anwendung entwickeln, die MUI verwendet und unter Windows-Versionen vor Windows Vista ausgeführt werden muss, müssen Nlsdl.dll auf der Windows-Zielplattform vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="11792-166">If you develop an application that uses MUI and that must run on Windows versions prior to Windows Vista, Nlsdl.dll must be present on the destination Windows platform.</span></span> <span data-ttu-id="11792-167">In den meisten Fällen bedeutet dies, dass die Anwendung das verteilbare nlsdl-Installationsprogramm ausführen und installieren muss (und nicht nur Nlsdl.dll selbst kopieren).</span><span class="sxs-lookup"><span data-stu-id="11792-167">In most cases, this means that the application needs to carry and install the redistributable Nlsdl installer (and not merely copy Nlsdl.dll itself).</span></span>

     

## <a name="step-0-creating-the-hard-coded-hello-mui"></a><span data-ttu-id="11792-168">Schritt 0: Erstellen der hart codierten Hello MUI</span><span class="sxs-lookup"><span data-stu-id="11792-168">Step 0: Creating the Hard-coded Hello MUI</span></span>

<span data-ttu-id="11792-169">Dieses Tutorial beginnt mit der Version der Version "Hello MUI" in der Version.</span><span class="sxs-lookup"><span data-stu-id="11792-169">This tutorial begins with the monolingual version of the Hello MUI application.</span></span> <span data-ttu-id="11792-170">Die Anwendung geht von der Verwendung der C++-Programmiersprache, breit Zeichenfolgen und der [**MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) -Funktion für die Ausgabe aus.</span><span class="sxs-lookup"><span data-stu-id="11792-170">The application assumes the use of the C++ programming language, wide character strings, and the [**MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) function for output.</span></span>

<span data-ttu-id="11792-171">Erstellen Sie zunächst die anfängliche Anwendung "guistep \_ 0" und die Lösung "hellomui", die alle Anwendungen in diesem Tutorial enthält.</span><span class="sxs-lookup"><span data-stu-id="11792-171">Begin by creating the initial GuiStep\_0 application, as well as the HelloMUI solution, which contain all of the applications in this tutorial.</span></span>

1.  <span data-ttu-id="11792-172">Erstellen Sie in Visual Studio 2008 ein neues Projekt.</span><span class="sxs-lookup"><span data-stu-id="11792-172">In Visual Studio 2008, create a new project.</span></span> <span data-ttu-id="11792-173">Verwenden Sie die folgenden Einstellungen und Werte:</span><span class="sxs-lookup"><span data-stu-id="11792-173">Use the following settings and values:</span></span>

    1.  <span data-ttu-id="11792-174">Projekttyp: Wählen Sie unter Visual C++ Win32 aus, und wählen Sie dann unter von Visual Studio installierte Vorlagen Win32-Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="11792-174">Project type: Under Visual C++ select Win32, and then under Visual Studio installed templates select Win32 Project.</span></span>
    2.  <span data-ttu-id="11792-175">Name: guistep \_ 0.</span><span class="sxs-lookup"><span data-stu-id="11792-175">Name: GuiStep\_0.</span></span>
    3.  <span data-ttu-id="11792-176">Speicherort: *projectrootdirectory* (spätere Schritte verweisen auf dieses Verzeichnis).</span><span class="sxs-lookup"><span data-stu-id="11792-176">Location: *ProjectRootDirectory* (Later steps reference this directory).</span></span>
    4.  <span data-ttu-id="11792-177">Projektmappenname: hellomui.</span><span class="sxs-lookup"><span data-stu-id="11792-177">Solution Name: HelloMUI.</span></span>
    5.  <span data-ttu-id="11792-178">Aktivieren Sie Projektmappenverzeichnis erstellen.</span><span class="sxs-lookup"><span data-stu-id="11792-178">Select Create directory for solution.</span></span>
    6.  <span data-ttu-id="11792-179">Wählen Sie im Win32-Anwendungs-Assistenten den Standard Anwendungstyp: Windows-Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="11792-179">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="11792-180">Konfigurieren Sie das Projekt Threading Modell:</span><span class="sxs-lookup"><span data-stu-id="11792-180">Configure the project threading model:</span></span>

    1.  <span data-ttu-id="11792-181">Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf das Projekt guistep \_ 0, und wählen Sie dann Eigenschaften aus.</span><span class="sxs-lookup"><span data-stu-id="11792-181">In the Solution Explorer, right-click the project GuiStep\_0, and then select Properties.</span></span>
    2.  <span data-ttu-id="11792-182">Im Dialogfeld Eigenschaften Seiten für Projekt:</span><span class="sxs-lookup"><span data-stu-id="11792-182">In the project Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="11792-183">Legen Sie in der Dropdown-Dropdown-Dropdown-Datei die Konfiguration auf alle Konfigurationen fest</span><span class="sxs-lookup"><span data-stu-id="11792-183">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="11792-184">Erweitern Sie unter Konfigurations Eigenschaften die Option C/C++, wählen Sie Code Generierung aus, und legen Sie Lauf Zeit Bibliothek: Multithread Debuggen (/MTD) fest.</span><span class="sxs-lookup"><span data-stu-id="11792-184">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="11792-185">Ersetzen Sie den Inhalt von "guistep \_ 0. cpp" durch den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="11792-185">Replace the contents of GuiStep\_0.cpp with the following code:</span></span>
    ```C++
    // GuiStep_0.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_0.h"

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        MessageBoxW(NULL,L"Hello MUI",L"HelloMUI!",MB_OK | MB_ICONINFORMATION);
        return 0;
    }
    ```

    

4.  <span data-ttu-id="11792-186">Erstellen Sie die Anwendung, und führen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="11792-186">Build and run the application.</span></span>

<span data-ttu-id="11792-187">Der unkomplizierte Quellcode ist die vereinfachte Entwurfs Auswahl von Hard-Coding oder Einbettungen, die gesamte Ausgabe, die dem Benutzer angezeigt wird – in diesem Fall der Text "Hello MUI".</span><span class="sxs-lookup"><span data-stu-id="11792-187">The straightforward source code above makes the simplistic design choice of hard-coding, or embedding, all the output the user will see—in this case the text "Hello MUI".</span></span> <span data-ttu-id="11792-188">Diese Auswahl schränkt das Hilfsprogramm der Anwendung für Benutzer ein, die das englische Wort "Hello" nicht kennen.</span><span class="sxs-lookup"><span data-stu-id="11792-188">This choice limits the utility of the application for users who don't recognize the English word "Hello."</span></span> <span data-ttu-id="11792-189">Da MUI ein Technologie basiertes englisches Akronym ist, wird für dieses Tutorial angenommen, dass die Zeichenfolge für alle Sprachen "MUI" bleibt.</span><span class="sxs-lookup"><span data-stu-id="11792-189">Because MUI is a technology-based English acronym, it is assumed for this tutorial that the string remains "MUI" for all languages.</span></span>

## <a name="step-1-implementing-the-basic-resource-module"></a><span data-ttu-id="11792-190">Schritt 1: Implementieren des grundlegenden Ressourcen Moduls</span><span class="sxs-lookup"><span data-stu-id="11792-190">Step 1: Implementing the Basic Resource Module</span></span>

<span data-ttu-id="11792-191">Microsoft Win32 bietet den Anwendungsentwicklern seit langem die Möglichkeit, ihre UI-Ressourcen Daten aus dem Quellcode der Anwendung zu trennen.</span><span class="sxs-lookup"><span data-stu-id="11792-191">Microsoft Win32 has long exposed the capability for application developers to separate their UI resource data from application source code.</span></span> <span data-ttu-id="11792-192">Diese Trennung erfolgt in Form des Win32-Ressourcen Modells, in dem Zeichen folgen, Bitmaps, Symbole, Meldungen und andere Elemente, die normalerweise für einen Benutzer angezeigt werden, in einen unterschiedlichen Abschnitt der ausführbaren Datei gepackt werden, der vom ausführbaren Code getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="11792-192">This separation comes in the form of the Win32 resource model, in which strings, bitmaps, icons, messages and other items normally displayed to a user are packaged into a distinct section of the executable, separated from executable code.</span></span>

<span data-ttu-id="11792-193">Um diese Trennung zwischen ausführbarem Code und Ressourcen Daten Verpackung zu veranschaulichen, wird in diesem Schritt die zuvor hart codierte "Hello"-Zeichenfolge (die "en-US"-Ressource) in diesem Schritt in den Ressourcenabschnitt eines dll-Moduls im Projekt "hellomodule \_ en US" eingefügt \_ .</span><span class="sxs-lookup"><span data-stu-id="11792-193">To illustrate this separation between executable code and resource data packaging, in this step the tutorial places the previously hard-coded "Hello" string (the "en-US" resource) into the resource section of a DLL module in the HelloModule\_en\_us project.</span></span>

<span data-ttu-id="11792-194">Diese Win32-DLL kann auch eine ausführbare Bibliothekstypen Funktion enthalten (wie jede andere dll möglicherweise).</span><span class="sxs-lookup"><span data-stu-id="11792-194">This Win32 DLL could also contain library type executable functionality (as any other DLL might).</span></span> <span data-ttu-id="11792-195">Um sich auf die im Zusammenhang mit Win32-ressourcenbezogenen Aspekte zu konzentrieren, lassen wir den Code der Lauf Zeit-dll in "DllMain. cpp" aus.</span><span class="sxs-lookup"><span data-stu-id="11792-195">But to help focus on the Win32 resource-related aspects, we leave the run-time DLL code stubbed out in dllmain.cpp.</span></span> <span data-ttu-id="11792-196">In den nachfolgenden Abschnitten dieses Tutorials werden die hier erstellten Ressourcen Daten von hellomodule verwendet, und es werden auch der entsprechende Lauf Zeit Code dargestellt.</span><span class="sxs-lookup"><span data-stu-id="11792-196">Subsequent sections of this tutorial make use of the HelloModule resource data being built here and also present appropriate runtime code.</span></span>

<span data-ttu-id="11792-197">Um ein Win32-Ressourcen Modul zu erstellen, erstellen Sie zunächst eine DLL mit einem stubout-DllMain:</span><span class="sxs-lookup"><span data-stu-id="11792-197">To construct a Win32 resource module, start by creating a DLL with a stubbed out dllmain:</span></span>

1.  <span data-ttu-id="11792-198">Fügen Sie der Projekt Mappe "hellomui" ein neues Projekt hinzu:</span><span class="sxs-lookup"><span data-stu-id="11792-198">Add a new project to the HelloMUI solution:</span></span>

    1.  <span data-ttu-id="11792-199">Wählen Sie im Menü Datei die Option hinzufügen und dann neues Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="11792-199">From the File menu, select Add, and then New Project.</span></span>
    2.  <span data-ttu-id="11792-200">Projekttyp: Win32-Projekt.</span><span class="sxs-lookup"><span data-stu-id="11792-200">Project type: Win32 Project.</span></span>
    3.  <span data-ttu-id="11792-201">Name: hellomodule \_ en \_ US.</span><span class="sxs-lookup"><span data-stu-id="11792-201">Name: HelloModule\_en\_us.</span></span>
    4.  <span data-ttu-id="11792-202">Speicherort: *projectrootdirectory* \\ hellomui.</span><span class="sxs-lookup"><span data-stu-id="11792-202">Location: *ProjectRootDirectory*\\HelloMUI.</span></span>
    5.  <span data-ttu-id="11792-203">Wählen Sie im Win32-Anwendungs-Assistenten Anwendungstyp: dll aus.</span><span class="sxs-lookup"><span data-stu-id="11792-203">In the Win32 Application Wizard, select Application type: DLL.</span></span>

2.  <span data-ttu-id="11792-204">Das Threading Modell dieses Projekts konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="11792-204">Configure this project's threading model:</span></span>

    1.  <span data-ttu-id="11792-205">Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf das Projekt hellomodule \_ en \_ US, und wählen Sie Eigenschaften aus.</span><span class="sxs-lookup"><span data-stu-id="11792-205">In the Solution Explorer, right-click the project HelloModule\_en\_us and select Properties.</span></span>
    2.  <span data-ttu-id="11792-206">Im Dialogfeld Eigenschaften Seiten des Projekts:</span><span class="sxs-lookup"><span data-stu-id="11792-206">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="11792-207">Legen Sie in der Dropdown-Dropdown-Dropdown-Datei die Konfiguration auf alle Konfigurationen fest</span><span class="sxs-lookup"><span data-stu-id="11792-207">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="11792-208">Erweitern Sie unter Konfigurations Eigenschaften die Option C/C++, wählen Sie Code Generierung aus, und legen Sie Lauf Zeit Bibliothek: Multithread Debuggen (/MTD) fest.</span><span class="sxs-lookup"><span data-stu-id="11792-208">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="11792-209">Untersuchen Sie DllMain. cpp.</span><span class="sxs-lookup"><span data-stu-id="11792-209">Examine dllmain.cpp.</span></span> <span data-ttu-id="11792-210">(Es kann sein, dass Sie den Verweis \_ hinzufügen möchten. Parameter Makros für den generierten Code, wie hier beschrieben, damit es auf Warnstufe 4 kompiliert werden kann.)</span><span class="sxs-lookup"><span data-stu-id="11792-210">(You may want to add the UNREFERENCED\_PARAMETER macros to the generated code, as we have here, to enable it to compile at warning level 4.)</span></span>
    ```C++
    // dllmain.cpp : Defines the entry point for the DLL application.
    #include "stdafx.h"

    BOOL APIENTRY DllMain( HMODULE hModule,
                           DWORD  ul_reason_for_call,
                           LPVOID lpReserved
                         )
    {
        UNREFERENCED_PARAMETER(hModule);
        UNREFERENCED_PARAMETER(lpReserved);

        switch (ul_reason_for_call)
        {
        case DLL_PROCESS_ATTACH:
        case DLL_THREAD_ATTACH:
        case DLL_THREAD_DETACH:
        case DLL_PROCESS_DETACH:
            break;
        }
        return TRUE;
    }
    ```

    

4.  <span data-ttu-id="11792-211">Fügen Sie dem Projekt eine Ressourcen Definitionsdatei "hellomodule. RC" hinzu:</span><span class="sxs-lookup"><span data-stu-id="11792-211">Add a resource-definition file HelloModule.rc to the project:</span></span>

    1.  <span data-ttu-id="11792-212">Klicken Sie im Projekt hellomodule en mit der \_ \_ rechten Maustaste auf den Ordner Ressourcen Dateien, und wählen Sie hinzufügen und dann neues Element aus.</span><span class="sxs-lookup"><span data-stu-id="11792-212">Under the project HelloModule\_en\_us, right-click the Resource Files folder, and select Add, and then select New Item.</span></span>
    2.  <span data-ttu-id="11792-213">Wählen Sie im Dialogfeld Neues Element hinzufügen Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="11792-213">In the Add New Item dialog box, choose the following:</span></span>

        1.  <span data-ttu-id="11792-214">Kategorien: Wählen Sie unter Visual C++ Ressource auswählen aus, und wählen Sie dann unter "installierte Vorlagen von Visual Studio" die Ressourcen Datei (. RC) aus.</span><span class="sxs-lookup"><span data-stu-id="11792-214">Categories: Under Visual C++ select Resource, and then under "Visual Studio installed templates" select Resource File (.rc).</span></span>
        2.  <span data-ttu-id="11792-215">Name: hellomodule.</span><span class="sxs-lookup"><span data-stu-id="11792-215">Name: HelloModule.</span></span>
        3.  <span data-ttu-id="11792-216">Speicherort: übernehmen Sie die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="11792-216">Location: accept the default.</span></span>
        4.  <span data-ttu-id="11792-217">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="11792-217">Click Add.</span></span>

    3.  <span data-ttu-id="11792-218">Geben Sie an, dass die neue Datei "hellomodule. RC" als Unicode gespeichert werden soll:</span><span class="sxs-lookup"><span data-stu-id="11792-218">Specify that the new HelloModule.rc file is to be saved as Unicode:</span></span>

        1.  <span data-ttu-id="11792-219">Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf hellomodule. RC, und wählen Sie Code anzeigen aus.</span><span class="sxs-lookup"><span data-stu-id="11792-219">In the Solution Explorer, right-click HelloModule.rc, and select View Code.</span></span>
        2.  <span data-ttu-id="11792-220">Wenn eine Meldung angezeigt wird, in der Sie darüber informiert werden, dass die Datei bereits geöffnet ist, und Sie gefragt werden, ob Sie Sie schließen möchten, klicken Sie auf Ja.</span><span class="sxs-lookup"><span data-stu-id="11792-220">If you see a message that tells you that the file is already open, and asks whether you want to close it, click Yes.</span></span>
        3.  <span data-ttu-id="11792-221">Wenn die Datei als Text angezeigt wird, erstellen Sie die Menü Auswahl Datei und dann erweiterte Speicheroptionen.</span><span class="sxs-lookup"><span data-stu-id="11792-221">With the file displayed as text, make the menu selection File and then Advanced Save Options.</span></span>
        4.  <span data-ttu-id="11792-222">Geben Sie unter Codierung die Angabe Unicode-Codepage 1200 an.</span><span class="sxs-lookup"><span data-stu-id="11792-222">Under Encoding, specify Unicode - Codepage 1200.</span></span>
        5.  <span data-ttu-id="11792-223">Klicken Sie auf OK.</span><span class="sxs-lookup"><span data-stu-id="11792-223">Click OK.</span></span>
        6.  <span data-ttu-id="11792-224">Speichern und schließen Sie hellomodule. rc.</span><span class="sxs-lookup"><span data-stu-id="11792-224">Save and close HelloModule.rc.</span></span>

    4.  <span data-ttu-id="11792-225">Fügen Sie eine Zeichen folgen Tabelle mit der Zeichenfolge "Hello" hinzu:</span><span class="sxs-lookup"><span data-stu-id="11792-225">Add a string table containing the "Hello" string:</span></span>

        1.  <span data-ttu-id="11792-226">Klicken Sie im Ressourcenansicht mit der rechten Maustaste auf hellomodule. RC, und wählen Sie Ressource hinzufügen aus.</span><span class="sxs-lookup"><span data-stu-id="11792-226">In the Resource View, right-click HelloModule.rc and select Add Resource.</span></span>
        2.  <span data-ttu-id="11792-227">Wählen Sie Zeichen folgen Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="11792-227">Select String Table.</span></span>
        3.  <span data-ttu-id="11792-228">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="11792-228">Click New.</span></span>
        4.  <span data-ttu-id="11792-229">Fügen Sie der Zeichen folgen Tabelle eine Zeichenfolge hinzu:</span><span class="sxs-lookup"><span data-stu-id="11792-229">Add a string to the String Table:</span></span>

            1.  <span data-ttu-id="11792-230">ID: Hello \_ MUI \_ Str \_ 0.</span><span class="sxs-lookup"><span data-stu-id="11792-230">ID: HELLO\_MUI\_STR\_0.</span></span>
            2.  <span data-ttu-id="11792-231">Wert: 0.</span><span class="sxs-lookup"><span data-stu-id="11792-231">Value: 0.</span></span>
            3.  <span data-ttu-id="11792-232">Beschriftung: Hello.</span><span class="sxs-lookup"><span data-stu-id="11792-232">Caption: Hello.</span></span>

        <span data-ttu-id="11792-233">Wenn Sie "hellomodule. RC" jetzt als Text anzeigen, werden verschiedene Teile des Ressourcen spezifischen Quellcodes angezeigt.</span><span class="sxs-lookup"><span data-stu-id="11792-233">If you view HelloModule.rc as text now, you will see various pieces of resource-specific source code.</span></span> <span data-ttu-id="11792-234">Das größte Interesse ist der Abschnitt, der die Zeichenfolge "Hello" beschreibt:</span><span class="sxs-lookup"><span data-stu-id="11792-234">The one of greatest interest is the section that describes the "Hello" string:</span></span>

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "Hello"
        END
        ```

        

        <span data-ttu-id="11792-235">Diese "Hello"-Zeichenfolge ist die Ressource, die lokalisiert (übersetzt, übersetzt) werden muss, in jede Sprache, die von der Anwendung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="11792-235">This "Hello" string is the resource that needs to be localized (that is, translated) into every language that the application hopes to support.</span></span> <span data-ttu-id="11792-236">Beispielsweise enthält die hellomodule- \_ TA \_ in Project (die im nächsten Schritt erstellt wird) eine eigene lokalisierte Version von hellomodule. RC für "TA-in":</span><span class="sxs-lookup"><span data-stu-id="11792-236">For example, the HelloModule\_ta\_in project (which you will create in the next step) will contain its own localized version of HelloModule.rc for "ta-IN":</span></span>

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "வணக்கம்"
        END
        ```

        

    5.  <span data-ttu-id="11792-237">Erstellen Sie das Projekt "hellomodule \_ en \_ US", um sicherzustellen, dass keine Fehler vorliegen.</span><span class="sxs-lookup"><span data-stu-id="11792-237">Build the HelloModule\_en\_us project to be sure there are no errors.</span></span>

5.  <span data-ttu-id="11792-238">Erstellen Sie sechs weitere Projekte in der hellomui-Lösung (oder beliebig viele), um sechs weitere Ressourcen-DLLs für zusätzliche Sprachen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="11792-238">Create six more projects in the HelloMUI solution (or as many of them as you wish) to create six more resource DLLs for additional languages.</span></span> <span data-ttu-id="11792-239">Verwenden Sie die Werte in dieser Tabelle:</span><span class="sxs-lookup"><span data-stu-id="11792-239">Use the values in this table:</span></span>

    | <span data-ttu-id="11792-240">Projektname</span><span class="sxs-lookup"><span data-stu-id="11792-240">Project name</span></span>        | <span data-ttu-id="11792-241">Name der RC-Datei</span><span class="sxs-lookup"><span data-stu-id="11792-241">Name of .rc file</span></span> | <span data-ttu-id="11792-242">Zeichenfolgen-ID</span><span class="sxs-lookup"><span data-stu-id="11792-242">String ID</span></span>          | <span data-ttu-id="11792-243">Zeichenfolgenwert</span><span class="sxs-lookup"><span data-stu-id="11792-243">String value</span></span> | <span data-ttu-id="11792-244">Zeichen folgen Beschriftung</span><span class="sxs-lookup"><span data-stu-id="11792-244">String caption</span></span> |
    |---------------------|------------------|--------------------|--------------|----------------|
    | <span data-ttu-id="11792-245">Hellomodule \_ de \_ de</span><span class="sxs-lookup"><span data-stu-id="11792-245">HelloModule\_de\_de</span></span> | <span data-ttu-id="11792-246">Hellomodule</span><span class="sxs-lookup"><span data-stu-id="11792-246">HelloModule</span></span>      | <span data-ttu-id="11792-247">Hello \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="11792-247">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="11792-248">0</span><span class="sxs-lookup"><span data-stu-id="11792-248">0</span></span>            | <span data-ttu-id="11792-249">Hallo</span><span class="sxs-lookup"><span data-stu-id="11792-249">Hallo</span></span>          |
    | <span data-ttu-id="11792-250">Hellomodule \_ es \_ es</span><span class="sxs-lookup"><span data-stu-id="11792-250">HelloModule\_es\_es</span></span> | <span data-ttu-id="11792-251">Hellomodule</span><span class="sxs-lookup"><span data-stu-id="11792-251">HelloModule</span></span>      | <span data-ttu-id="11792-252">Hello \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="11792-252">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="11792-253">0</span><span class="sxs-lookup"><span data-stu-id="11792-253">0</span></span>            | <span data-ttu-id="11792-254">Nachdrücklich</span><span class="sxs-lookup"><span data-stu-id="11792-254">Hola</span></span>           |
    | <span data-ttu-id="11792-255">Hellomodule \_ fr \_ fr</span><span class="sxs-lookup"><span data-stu-id="11792-255">HelloModule\_fr\_fr</span></span> | <span data-ttu-id="11792-256">Hellomodule</span><span class="sxs-lookup"><span data-stu-id="11792-256">HelloModule</span></span>      | <span data-ttu-id="11792-257">Hello \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="11792-257">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="11792-258">0</span><span class="sxs-lookup"><span data-stu-id="11792-258">0</span></span>            | <span data-ttu-id="11792-259">Bonjour</span><span class="sxs-lookup"><span data-stu-id="11792-259">Bonjour</span></span>        |
    | <span data-ttu-id="11792-260">Hellomodule \_ Hi \_ in</span><span class="sxs-lookup"><span data-stu-id="11792-260">HelloModule\_hi\_in</span></span> | <span data-ttu-id="11792-261">Hellomodule</span><span class="sxs-lookup"><span data-stu-id="11792-261">HelloModule</span></span>      | <span data-ttu-id="11792-262">Hello \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="11792-262">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="11792-263">0</span><span class="sxs-lookup"><span data-stu-id="11792-263">0</span></span>            | <span data-ttu-id="11792-264">नमस्</span><span class="sxs-lookup"><span data-stu-id="11792-264">नमस्</span></span>           |
    | <span data-ttu-id="11792-265">Hellomodule \_ ru \_ ru</span><span class="sxs-lookup"><span data-stu-id="11792-265">HelloModule\_ru\_ru</span></span> | <span data-ttu-id="11792-266">Hellomodule</span><span class="sxs-lookup"><span data-stu-id="11792-266">HelloModule</span></span>      | <span data-ttu-id="11792-267">Hello \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="11792-267">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="11792-268">0</span><span class="sxs-lookup"><span data-stu-id="11792-268">0</span></span>            | <span data-ttu-id="11792-269">"", "".</span><span class="sxs-lookup"><span data-stu-id="11792-269">Здравствуйте</span></span>   |
    | <span data-ttu-id="11792-270">Hellomodule- \_ TA \_ in</span><span class="sxs-lookup"><span data-stu-id="11792-270">HelloModule\_ta\_in</span></span> | <span data-ttu-id="11792-271">Hellomodule</span><span class="sxs-lookup"><span data-stu-id="11792-271">HelloModule</span></span>      | <span data-ttu-id="11792-272">Hello \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="11792-272">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="11792-273">0</span><span class="sxs-lookup"><span data-stu-id="11792-273">0</span></span>            | <span data-ttu-id="11792-274">வணக்கம்</span><span class="sxs-lookup"><span data-stu-id="11792-274">வணக்கம்</span></span>        |

    

     

<span data-ttu-id="11792-275">Weitere Informationen zur. rc-Dateistruktur und-Syntax finden Sie unter [Informationen zu Ressourcen Dateien](../menurc/about-resource-files.md).</span><span class="sxs-lookup"><span data-stu-id="11792-275">For more about .rc file structure and syntax, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

## <a name="step-2-building-the-basic-resource-module"></a><span data-ttu-id="11792-276">Schritt 2: aufbauen des grundlegenden Ressourcen Moduls</span><span class="sxs-lookup"><span data-stu-id="11792-276">Step 2: Building the Basic Resource Module</span></span>

<span data-ttu-id="11792-277">Die Verwendung früherer Ressourcen Modelle führt zum Aufbau eines der sieben hellomodule-Projekte zu sieben separaten DLLs.</span><span class="sxs-lookup"><span data-stu-id="11792-277">Using previous resource models, building any one of the seven HelloModule projects would result in seven separate DLLs.</span></span> <span data-ttu-id="11792-278">Jede DLL enthält einen Ressourcenabschnitt mit einer einzelnen Zeichenfolge, die in der entsprechenden Sprache lokalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="11792-278">Each DLL would contain a resource section with a single string localized into the appropriate language.</span></span> <span data-ttu-id="11792-279">Obwohl es für das historische Win32-Ressourcenmodell geeignet ist, nutzt dieser Entwurf nicht MUI.</span><span class="sxs-lookup"><span data-stu-id="11792-279">Although appropriate for the historic Win32 resource model, this design does not take advantage of MUI.</span></span>

<span data-ttu-id="11792-280">Im Windows Vista SDK und höher bietet MUI die Möglichkeit, ausführbare Dateien in Quellcode und lokalisierbare Inhalts Module aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="11792-280">In the Windows Vista SDK and later, MUI provides the ability to split executables into source code and localizable content modules.</span></span> <span data-ttu-id="11792-281">Mit der zusätzlichen Anpassung, die später in Schritt 5 behandelt wird, können Anwendungen für die mehrsprachige Unterstützung für Versionen vor Windows Vista aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="11792-281">With the additional customization that is covered later in Step 5, applications can be enabled for multi-lingual support to run on versions prior to Windows Vista.</span></span>

<span data-ttu-id="11792-282">Die primären Mechanismen zum Aufteilen von Ressourcen aus ausführbarem Code, beginnend mit Windows Vista, sind folgende:</span><span class="sxs-lookup"><span data-stu-id="11792-282">The primary mechanisms available to split resources from executable code, starting with Windows Vista, are:</span></span>

-   <span data-ttu-id="11792-283">Verwenden von rc.exe (dem RC-Compiler) mit bestimmten Switches oder</span><span class="sxs-lookup"><span data-stu-id="11792-283">Using rc.exe (the RC Compiler) with specific switches, or</span></span>
-   <span data-ttu-id="11792-284">Verwenden eines Tools zum Aufteilen von postbuilds namens muirct.exe.</span><span class="sxs-lookup"><span data-stu-id="11792-284">Using a post-build style splitting tool named muirct.exe.</span></span>

<span data-ttu-id="11792-285">Weitere Informationen finden Sie unter [Ressourcen Hilfsprogramme](resource-utilities.md) .</span><span class="sxs-lookup"><span data-stu-id="11792-285">See [Resource Utilities](resource-utilities.md) for more information.</span></span>

<span data-ttu-id="11792-286">Der Einfachheit halber wird in diesem Tutorial muirct.exe verwendet, um die ausführbare Datei "Hello MUI" aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="11792-286">For the sake of simplicity, this tutorial uses muirct.exe to split the "Hello MUI" executable.</span></span>

### <a name="splitting-the-various-language-resource-modules-an-overview"></a><span data-ttu-id="11792-287">Aufteilen der verschiedenen Sprachressourcen Module: eine Übersicht</span><span class="sxs-lookup"><span data-stu-id="11792-287">Splitting the Various Language Resource Modules: An Overview</span></span>

<span data-ttu-id="11792-288">Ein mehrstufiges Verfahren ist daran beteiligt, die DLLs in eine ausführbare HelloModule.dll und eine HelloModule.dll. MUI für jede der sieben unterstützten Sprachen in diesem Tutorial aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="11792-288">A multi-part process is involved in splitting the DLLs into one executable HelloModule.dll, plus a HelloModule.dll.mui for each of the seven supported languages within this tutorial.</span></span> <span data-ttu-id="11792-289">In dieser Übersicht werden die erforderlichen Schritte beschrieben. der nächste Abschnitt enthält eine Befehlsdatei, die diese Schritte ausführt.</span><span class="sxs-lookup"><span data-stu-id="11792-289">This overview describes the required steps; the next section presents a command file that performs those steps.</span></span>

<span data-ttu-id="11792-290">Teilen Sie zunächst das englische HelloModule.dll Modul mit dem folgenden Befehl:</span><span class="sxs-lookup"><span data-stu-id="11792-290">First, split the English-only HelloModule.dll module by using the command:</span></span>


```C++
mkdir .\en-US
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
```



<span data-ttu-id="11792-291">In der obigen Befehlszeile wird die Konfigurationsdatei "dorevercmuiloc. rcconfig" verwendet.</span><span class="sxs-lookup"><span data-stu-id="11792-291">The command line above uses the configuration file DoReverseMuiLoc.rcconfig.</span></span> <span data-ttu-id="11792-292">Diese Art von Konfigurationsdatei wird in der Regel von muirct.exe verwendet, um Ressourcen zwischen der sprach neutralen dll (LN) und den sprach abhängigen MUI-Dateien aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="11792-292">This type of configuration file is typically used by muirct.exe to split resources between the language-neutral (LN) DLL and the language-dependent .mui files.</span></span> <span data-ttu-id="11792-293">In diesem Fall gibt die XML-Datei "dorevertarmuiloc. rcconfig" (aufgelistet im nächsten Abschnitt) viele Ressourcentypen an, Sie sind jedoch in der Kategorie "localizedresources" oder der MUI-Datei enthalten, und es sind keine Ressourcen in der sprach neutralen Kategorie vorhanden.</span><span class="sxs-lookup"><span data-stu-id="11792-293">In this case, the DoReverseMuiLoc.rcconfig xml file (listed in the next section) indicates many resource types, but they all fall into the "localizedResources" or .mui file category, and there are no resources in the language-neutral category.</span></span> <span data-ttu-id="11792-294">Weitere Informationen zum Vorbereiten einer Ressourcen Konfigurationsdatei finden Sie unter [Vorbereiten einer Ressourcen Konfigurationsdatei](preparing-a-resource-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="11792-294">For more information about how to prepare a resource configuration file, see [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>

<span data-ttu-id="11792-295">Zusätzlich zum Erstellen einer HelloModule.dll. MUI-Datei, die die englische Zeichenfolge "Hello" enthält, bettet muirct.exe auch während der Aufteilung eine MUI-Ressource in das HelloModule.dll-Modul ein.</span><span class="sxs-lookup"><span data-stu-id="11792-295">In addition to creating a HelloModule.dll.mui file which contains the English string "Hello", muirct.exe also embeds a MUI resource into the HelloModule.dll module during the splitting.</span></span> <span data-ttu-id="11792-296">Um zur Laufzeit die entsprechenden Ressourcen aus den sprachspezifischen HelloModule.dll. MUI-Modulen ordnungsgemäß zu laden, muss für jede MUI-Datei die Prüfsummen korrigiert werden, damit Sie mit den Prüfsummen im sprach neutralen LN-Modul der Baseline identisch sind.</span><span class="sxs-lookup"><span data-stu-id="11792-296">In order to properly load at run-time the appropriate resources from the language-specific HelloModule.dll.mui modules, each .mui file must have its checksums fixed-up to match the checksums in the baseline language-neutral LN module.</span></span> <span data-ttu-id="11792-297">Dies wird durch einen Befehl wie z. b.:</span><span class="sxs-lookup"><span data-stu-id="11792-297">This is done by a command such as:</span></span>


```C++
muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui
```



<span data-ttu-id="11792-298">Auf ähnliche Weise wird muirct.exe aufgerufen, um eine HelloModule.dll MUI-Datei für jede andere Sprache zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="11792-298">Similarly, muirct.exe is invoked to create a HelloModule.dll.mui file for each of the other languages.</span></span> <span data-ttu-id="11792-299">In diesen Fällen wird die sprachneutrale dll jedoch verworfen, da nur der erste erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="11792-299">However, in those cases the language-neutral DLL is discarded, as only the first one created will be needed.</span></span> <span data-ttu-id="11792-300">Die Befehle, die die Spanisch-und Französisch-Ressourcen verarbeiten, sehen wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="11792-300">The commands that process the Spanish and French resources look like this:</span></span>


```C++
mkdir .\es-ES
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

mkdir .\fr-FR
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui
```



<span data-ttu-id="11792-301">Eine der wichtigsten Punkte, die in den obigen muirct.exe Befehlszeilen zu beachten ist, besteht darin, dass das-x-Flag verwendet wird, um eine Zielsprachen-ID anzugeben.</span><span class="sxs-lookup"><span data-stu-id="11792-301">One of the most important things to notice in the muirct.exe command lines above is that the -x flag is used to specify a target language ID.</span></span> <span data-ttu-id="11792-302">Der für muirct.exe angegebene Wert ist für jedes sprachspezifische HelloModule.dll Modul anders.</span><span class="sxs-lookup"><span data-stu-id="11792-302">The value provided to muirct.exe is different for each language-specific HelloModule.dll module.</span></span> <span data-ttu-id="11792-303">Dieser sprach Wert ist zentral und wird von muirct.exe verwendet, um die MUI-Datei beim Aufteilen entsprechend zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="11792-303">This language value is central and is used by muirct.exe to appropriately mark the .mui file during splitting.</span></span> <span data-ttu-id="11792-304">Ein falscher Wert erzeugt Fehler beim Laden von Ressourcen für diese bestimmte MUI-Datei zur Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="11792-304">An incorrect value produces resource loading failures for that particular .mui file at run-time.</span></span> <span data-ttu-id="11792-305">Weitere Informationen zum Zuordnen von Sprachen Namen zu LCID finden Sie unter [sprach Bezeichner-Konstanten und-](language-identifier-constants-and-strings.md) Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="11792-305">See [Language Identifier Constants and Strings](language-identifier-constants-and-strings.md) for more details on mapping language name to LCID.</span></span>

<span data-ttu-id="11792-306">Jede "Split. MUI"-Datei wird am Ende in ein Verzeichnis eingefügt, das dem Sprachnamen entspricht, und zwar direkt unterhalb des Verzeichnisses, in dem sich die sprachneutrale HelloModule.dll befinden wird.</span><span class="sxs-lookup"><span data-stu-id="11792-306">Each split .mui file ends up being placed into a directory corresponding to its language name, immediately underneath the directory in which the language-neutral HelloModule.dll will reside.</span></span> <span data-ttu-id="11792-307">Weitere Informationen zum Platzieren von MUI-Dateien finden Sie unter [Anwendungs Bereitstellung](application-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="11792-307">For more about .mui file placement, see [Application Deployment](application-deployment.md).</span></span>

### <a name="splitting-the-various-language-resource-modules-creating-the-files"></a><span data-ttu-id="11792-308">Aufteilen der verschiedenen Sprachressourcen Module: Erstellen der Dateien</span><span class="sxs-lookup"><span data-stu-id="11792-308">Splitting the Various Language Resource Modules: Creating the Files</span></span>

<span data-ttu-id="11792-309">In diesem Tutorial erstellen Sie eine Befehlsdatei, die die Befehle zum Aufteilen der verschiedenen DLLs enthält, und Sie rufen Sie manuell auf.</span><span class="sxs-lookup"><span data-stu-id="11792-309">For this tutorial you create a command file containing the commands to split the various DLLs, and you invoke it manually.</span></span> <span data-ttu-id="11792-310">Beachten Sie, dass Sie bei der eigentlichen Entwicklung das Potenzial von Buildfehlern reduzieren können, indem Sie diese Befehle als Präbuildereignisse oder Postbuildereignisse in der hellomui-Lösung einschließen, aber dies würde den Rahmen dieses Tutorials sprengen.</span><span class="sxs-lookup"><span data-stu-id="11792-310">Note that in actual development work, you could reduce the potential for build errors by including these commands as pre-build or post-build events in the HelloMUI solution, but that is beyond the scope of this tutorial.</span></span>

<span data-ttu-id="11792-311">Erstellen Sie die Dateien für den Debugbuild:</span><span class="sxs-lookup"><span data-stu-id="11792-311">Create the files for the debug build:</span></span>

1.  <span data-ttu-id="11792-312">Erstellen Sie die Befehlsdatei "dorevercmuiloc. cmd", die die folgenden Befehle enthält:</span><span class="sxs-lookup"><span data-stu-id="11792-312">Create a command file DoReverseMuiLoc.cmd containing the following commands:</span></span>
    ```C++
    mkdir .\en-US
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui

    mkdir .\de-DE
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0407 -g 0x0407 .\HelloModule_de_de.dll .\HelloModule_discard.dll .\de-DE\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e de-DE\HelloModule.dll.mui

    mkdir .\es-ES
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

    mkdir .\fr-FR
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui

    mkdir .\hi-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0439 -g 0x0407 .\HelloModule_hi_in.dll .\HelloModule_discard.dll .\hi-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e hi-IN\HelloModule.dll.mui

    mkdir .\ru-RU
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0419 -g 0x0407 .\HelloModule_ru_ru.dll .\HelloModule_discard.dll .\ru-RU\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ru-RU\HelloModule.dll.mui

    mkdir .\ta-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0449 -g 0x0407 .\HelloModule_ta_in.dll .\HelloModule_discard.dll .\ta-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ta-IN\HelloModule.dll.mui
    pause
    ```

    

2.  <span data-ttu-id="11792-313">Erstellen Sie die XML-Datei "dorevercmuiloc. rcconfig", die die folgenden Zeilen enthält:</span><span class="sxs-lookup"><span data-stu-id="11792-313">Create an xml file DoReverseMuiLoc.rcconfig containing the following lines:</span></span>
    ```C++
    <?xml version="1.0" encoding="utf-8"?>
        <localization>
            <resources>
                <win32Resources fileType="Application">
                    <neutralResources>
                    </neutralResources>
                    <localizedResources>
                        <resourceType typeNameId="#1"/>
                        <resourceType typeNameId="#10"/>
                        <resourceType typeNameId="#1024"/>
                        <resourceType typeNameId="#11"/>
                        <resourceType typeNameId="#12"/>
                        <resourceType typeNameId="#13"/>
                        <resourceType typeNameId="#14"/>
                        <resourceType typeNameId="#15"/>
                        <resourceType typeNameId="#16"/>
                        <resourceType typeNameId="#17"/>
                        <resourceType typeNameId="#18"/>
                        <resourceType typeNameId="#19"/>
                        <resourceType typeNameId="#2"/>
                        <resourceType typeNameId="#20"/>
                        <resourceType typeNameId="#2110"/>
                        <resourceType typeNameId="#23"/>
                        <resourceType typeNameId="#240"/>
                        <resourceType typeNameId="#3"/>
                        <resourceType typeNameId="#4"/>
                        <resourceType typeNameId="#5"/>
                        <resourceType typeNameId="#6"/>
                        <resourceType typeNameId="#7"/>
                        <resourceType typeNameId="#8"/>
                        <resourceType typeNameId="#9"/>
                        <resourceType typeNameId="HTML"/>
                        <resourceType typeNameId="MOFDATA"/>
                    </localizedResources>
                </win32Resources>
            </resources>
        </localization>
    ```

    

3.  <span data-ttu-id="11792-314">Kopieren Sie doreversemuiloc. cmd und doreversemuiloc. rcconfig in *projectrootdirectory* \\ hellomui \\ Debug.</span><span class="sxs-lookup"><span data-stu-id="11792-314">Copy DoReverseMuiLoc.cmd and DoReverseMuiLoc.rcconfig to *ProjectRootDirectory*\\HelloMUI\\Debug.</span></span>
4.  <span data-ttu-id="11792-315">Öffnen Sie die Visual Studio 2008-Eingabeaufforderung, und navigieren Sie zum Debugverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="11792-315">Open the Visual Studio 2008 command prompt and navigate to the Debug directory.</span></span>
5.  <span data-ttu-id="11792-316">Führen Sie doreverdormuiloc. cmd aus.</span><span class="sxs-lookup"><span data-stu-id="11792-316">Run DoReverseMuiLoc.cmd.</span></span>

<span data-ttu-id="11792-317">Wenn Sie einen Releasebuild erstellen, kopieren Sie die gleichen Dateien "doreversemuiloc. cmd" und "doreversemuiloc. rcconfig" in das releaseverzeichnis, und führen Sie dort die Befehlsdatei aus.</span><span class="sxs-lookup"><span data-stu-id="11792-317">When you create a release build, you copy the same DoReverseMuiLoc.cmd and DoReverseMuiLoc.rcconfig files to the Release directory and run the command file there.</span></span>

## <a name="step-3-creating-a-resource-savvy-hello-mui"></a><span data-ttu-id="11792-318">Schritt 3: Erstellen eines Resource-Savvy "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="11792-318">Step 3: Creating a Resource-Savvy "Hello MUI"</span></span>

<span data-ttu-id="11792-319">Aufbauend auf dem ersten hart codierten guistep \_0.exe Beispiel oben können Sie die Reichweite der Anwendung auf mehrere sprach Benutzer ausweiten, indem Sie das Win32-Ressourcenmodell integrieren.</span><span class="sxs-lookup"><span data-stu-id="11792-319">Building on the initial hard-coded GuiStep\_0.exe example from above, you could extend the reach of the application to multiple language users by choosing to incorporate the Win32 resource model.</span></span> <span data-ttu-id="11792-320">Der in diesem Schritt vorgestellte neue Lauf Zeit Code umfasst das Laden von Modulen ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) und das Abrufen von Zeichen folgen ([**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)).</span><span class="sxs-lookup"><span data-stu-id="11792-320">The new run-time code presented in this step includes the module loading ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) and string retrieval ([**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)) logic.</span></span>

1.  <span data-ttu-id="11792-321">Fügen Sie der Projekt Mappe hellomui (mithilfe der Menü Auswahl Datei, hinzufügen und neues Projekt) ein neues Projekt mit den folgenden Einstellungen und Werten hinzu:</span><span class="sxs-lookup"><span data-stu-id="11792-321">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="11792-322">Projekttyp: Win32-Projekt.</span><span class="sxs-lookup"><span data-stu-id="11792-322">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="11792-323">Name: guistep \_ 1.</span><span class="sxs-lookup"><span data-stu-id="11792-323">Name: GuiStep\_1.</span></span>
    3.  <span data-ttu-id="11792-324">Speicherort: übernehmen Sie die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="11792-324">Location: accept the default.</span></span>
    4.  <span data-ttu-id="11792-325">Wählen Sie im Win32-Anwendungs-Assistenten den Standard Anwendungstyp: Windows-Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="11792-325">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="11792-326">Legen Sie fest, dass dieses Projekt in Visual Studio ausgeführt wird, und konfigurieren Sie das Thread Modell:</span><span class="sxs-lookup"><span data-stu-id="11792-326">Set this project to run from within Visual Studio, and configure its threading model:</span></span>

    1.  <span data-ttu-id="11792-327">Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf das Projekt guistep \_ 1, und wählen Sie als Startprojekt festlegen aus.</span><span class="sxs-lookup"><span data-stu-id="11792-327">In the Solution Explorer, right-click the project GuiStep\_1 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="11792-328">Klicken Sie erneut mit der rechten Maustaste, und wählen Sie Eigenschaften aus.</span><span class="sxs-lookup"><span data-stu-id="11792-328">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="11792-329">Im Dialogfeld Eigenschaften Seiten des Projekts:</span><span class="sxs-lookup"><span data-stu-id="11792-329">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="11792-330">Legen Sie in der Dropdown-Dropdown-Dropdown-Datei die Konfiguration auf alle Konfigurationen fest</span><span class="sxs-lookup"><span data-stu-id="11792-330">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="11792-331">Erweitern Sie unter Konfigurations Eigenschaften die Option C/C++, wählen Sie Code Generierung aus, und legen Sie Lauf Zeit Bibliothek: Multithread Debuggen (/MTD) fest.</span><span class="sxs-lookup"><span data-stu-id="11792-331">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="11792-332">Ersetzen Sie den Inhalt von guistep \_ 1. cpp durch den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="11792-332">Replace the contents of GuiStep\_1.cpp with the following code:</span></span>
    ```C++
    // GuiStep_1.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_1.h"
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Basic application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 2. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 3. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 4. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }
    ```

    

4.  <span data-ttu-id="11792-333">Erstellen Sie die Anwendung, und führen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="11792-333">Build and run the application.</span></span> <span data-ttu-id="11792-334">Die Ausgabe wird in der Sprache angezeigt, die zurzeit als Anzeige Sprache des Computers festgelegt ist (vorausgesetzt, es handelt sich dabei um eine der sieben Sprachen, die wir erstellt haben).</span><span class="sxs-lookup"><span data-stu-id="11792-334">The output will be displayed in the language currently set as the display language of the computer (provided it is one of the seven languages we have built).</span></span>

## <a name="step-4-globalizing-hello-mui"></a><span data-ttu-id="11792-335">Schritt 4: Globalisieren von "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="11792-335">Step 4: Globalizing "Hello MUI"</span></span>

<span data-ttu-id="11792-336">Obwohl im vorherigen Beispiel die Ausgabe in verschiedenen Sprachen angezeigt werden kann, ist Sie in einigen Bereichen kurz.</span><span class="sxs-lookup"><span data-stu-id="11792-336">Although the previous example is able to display its output in different languages, it falls short in a number of areas.</span></span> <span data-ttu-id="11792-337">Vielleicht das auffälligste ist, dass die Anwendung nur in einer kleinen Teilmenge von Sprachen verfügbar ist, im Vergleich zum Windows-Betriebssystem selbst.</span><span class="sxs-lookup"><span data-stu-id="11792-337">Perhaps the most noticeable is that the application is only available in a small subset of languages when compared to the Windows operating system itself.</span></span> <span data-ttu-id="11792-338">Wenn z. b. die Anwendung "guistep \_ 1" aus dem vorherigen Schritt auf einem japanischen Build von Windows installiert wurde, wäre es wahrscheinlich, dass Ressourcen Speicherort Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="11792-338">If, for example, the GuiStep\_1 application from the previous step were installed on a Japanese build of Windows, resource location failures would be likely.</span></span>

<span data-ttu-id="11792-339">Um diese Situation zu beheben, haben Sie zwei primäre Optionen:</span><span class="sxs-lookup"><span data-stu-id="11792-339">To address this situation, you have two primary options:</span></span>

-   <span data-ttu-id="11792-340">Stellen Sie sicher, dass Ressourcen in einer vordefinierten, ultimativen Fall Back Sprache eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="11792-340">Ensure that resources in a predetermined ultimate fallback language are included.</span></span>
-   <span data-ttu-id="11792-341">Bieten Sie dem Endbenutzer die Möglichkeit, Ihre Spracheinstellungen aus der Teilmenge von Sprachen zu konfigurieren, die speziell von der Anwendung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="11792-341">Provide a way for the end user to configure their language preferences from among the subset of languages specifically supported by the application.</span></span>

<span data-ttu-id="11792-342">Diese Optionen sind dringend empfehlenswert und werden in diesem Tutorial implementiert, indem das Flag "-g" an muirct.exe übergeben wird, wie oben gezeigt.</span><span class="sxs-lookup"><span data-stu-id="11792-342">Of these options, the one providing an ultimate fallback language is highly advisable and is implemented in this tutorial by passing the -g flag to muirct.exe, as seen above.</span></span> <span data-ttu-id="11792-343">Dieses Flag weist muirct.exe an, eine bestimmte Sprache (de-de/0x0407) zu der Ultimate-Fall Back Sprache zu machen, die dem sprach neutralen dll-Modul (HelloModule.dll) zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="11792-343">This flag tells muirct.exe to make a specific language (de-DE / 0x0407) the ultimate fallback language associated with the language-neutral dll module (HelloModule.dll).</span></span> <span data-ttu-id="11792-344">Zur Laufzeit wird dieser Parameter als letztes Mittel zum Generieren von Text verwendet, der dem Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="11792-344">At run-time this parameter is used as a last resort to generate text to display to the user.</span></span> <span data-ttu-id="11792-345">Wenn eine ultimative Fall Back Sprache nicht gefunden wird und in der sprach neutralen Binärdatei keine geeignete Ressource verfügbar ist, tritt beim Laden der Ressource ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="11792-345">In the event that an ultimate fallback language is not found and no appropriate resource is available in the language-neutral binary, loading of the resource fails.</span></span> <span data-ttu-id="11792-346">Daher sollten Sie sorgfältig die Szenarien ermitteln, die Ihre Anwendung möglicherweise trifft, und die endgültige Fall Back Sprache entsprechend planen.</span><span class="sxs-lookup"><span data-stu-id="11792-346">Therefore you should carefully determine the scenarios that your application might encounter and plan the ultimate fallback language accordingly.</span></span>

<span data-ttu-id="11792-347">Die andere Möglichkeit, konfigurierbare Spracheinstellungen zuzulassen und Ressourcen basierend auf dieser benutzerdefinierten Hierarchie zu laden, kann die Kundenzufriedenheit erheblich steigern.</span><span class="sxs-lookup"><span data-stu-id="11792-347">The other option of allowing for configurable language preferences and loading resources based on this user-defined hierarchy can greatly increase customer satisfaction.</span></span> <span data-ttu-id="11792-348">Leider ist es auch komplizierter, wenn die Funktionalität innerhalb der Anwendung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="11792-348">Unfortunately, it also complicates the functionality needed within the application.</span></span>

<span data-ttu-id="11792-349">In diesem Schritt des Tutorials wird ein vereinfachter Textdatei-Mechanismus verwendet, um die benutzerdefinierte Benutzer Sprachkonfiguration zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="11792-349">This step of the tutorial uses a simplified text file mechanism to enable custom user language configuration.</span></span> <span data-ttu-id="11792-350">Die Textdatei wird zur Laufzeit von der Anwendung analysiert, und die analysierte und validierte Sprachliste wird beim Einrichten einer benutzerdefinierten Fall Back Liste verwendet.</span><span class="sxs-lookup"><span data-stu-id="11792-350">The text file is parsed at run-time by the application, and the parsed and validated language list is used in establishing a custom fallback list.</span></span> <span data-ttu-id="11792-351">Nachdem die benutzerdefinierte Fall Back Liste festgelegt wurde, werden die Ressourcen von den Windows-APIs entsprechend der in dieser Liste aufgeführten sprach Rangfolge geladen.</span><span class="sxs-lookup"><span data-stu-id="11792-351">After the custom fallback list is established, the Windows APIs will load resources according to the language precedence set forth in this list.</span></span> <span data-ttu-id="11792-352">Der Rest des Codes ähnelt dem, der im vorherigen Schritt gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="11792-352">The remainder of the code is similar to that found in the preceding step.</span></span>

1.  <span data-ttu-id="11792-353">Fügen Sie der Projekt Mappe hellomui (mithilfe der Menü Auswahl Datei, hinzufügen und neues Projekt) ein neues Projekt mit den folgenden Einstellungen und Werten hinzu:</span><span class="sxs-lookup"><span data-stu-id="11792-353">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="11792-354">Projekttyp: Win32-Projekt.</span><span class="sxs-lookup"><span data-stu-id="11792-354">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="11792-355">Name: guistep \_ 2.</span><span class="sxs-lookup"><span data-stu-id="11792-355">Name: GuiStep\_2.</span></span>
    3.  <span data-ttu-id="11792-356">Speicherort: übernehmen Sie die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="11792-356">Location: accept the default.</span></span>
    4.  <span data-ttu-id="11792-357">Wählen Sie im Win32-Anwendungs-Assistenten den Standard Anwendungstyp: Windows-Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="11792-357">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="11792-358">Legen Sie fest, dass dieses Projekt in Visual Studio ausgeführt wird, und konfigurieren Sie das Thread Modell:</span><span class="sxs-lookup"><span data-stu-id="11792-358">Set this project to run from within Visual Studio, and configure its threading model:</span></span>

    1.  <span data-ttu-id="11792-359">Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf das Projekt guistep \_ 2, und wählen Sie als Startprojekt festlegen aus.</span><span class="sxs-lookup"><span data-stu-id="11792-359">In the Solution Explorer, right-click the project GuiStep\_2 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="11792-360">Klicken Sie erneut mit der rechten Maustaste, und wählen Sie Eigenschaften aus.</span><span class="sxs-lookup"><span data-stu-id="11792-360">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="11792-361">Im Dialogfeld Eigenschaften Seiten des Projekts:</span><span class="sxs-lookup"><span data-stu-id="11792-361">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="11792-362">Legen Sie in der Dropdown-Dropdown-Dropdown-Datei die Konfiguration auf alle Konfigurationen fest</span><span class="sxs-lookup"><span data-stu-id="11792-362">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="11792-363">Erweitern Sie unter Konfigurations Eigenschaften die Option C/C++, wählen Sie Code Generierung aus, und legen Sie Lauf Zeit Bibliothek: Multithread Debuggen (/MTD) fest.</span><span class="sxs-lookup"><span data-stu-id="11792-363">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="11792-364">Ersetzen Sie den Inhalt von guistep \_ 2. cpp durch den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="11792-364">Replace the contents of GuiStep\_2.cpp with the following code:</span></span>
    ```C++
    // GuiStep_2.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_2.h"
    #include <strsafe.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now sets the appropriate fallback list
        DWORD langCount = 0;
        // next commented out line of code could be used on Windows 7 and later
        // using SetProcessPreferredUILanguages is recomended for new applications (esp. multi-threaded applications)
    //    if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        // the following line of code is supported on Windows Vista and later
        if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to set the user defined languages, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // NOTES on step #1:
        // an application developer that makes the assumption the fallback list provided by the
        // system / OS is entirely sufficient may or may not be making a good assumption based 
        // mostly on:
        // A. your choice of languages installed with your application
        // B. the languages on the OS at application install time
        // C. the OS users propensity to install/uninstall language packs
        // D. the OS users propensity to change laguage settings

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) && 
                    IsValidLocaleName(next))
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  <span data-ttu-id="11792-365">Erstellen Sie eine Unicode-Textdatei langs.txt mit der folgenden Zeile:</span><span class="sxs-lookup"><span data-stu-id="11792-365">Create a Unicode text file langs.txt containing the following line:</span></span>

    ``` syntax
    hi-IN ta-IN ru-RU fr-FR es-ES en-US
    ```

    > [!Note]  
    > <span data-ttu-id="11792-366">Stellen Sie sicher, dass Sie die Datei als Unicode speichern.</span><span class="sxs-lookup"><span data-stu-id="11792-366">Be sure to save the file as Unicode.</span></span>

     

    <span data-ttu-id="11792-367">Kopieren Sie langs.txt in das Verzeichnis, in dem das Programm ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="11792-367">Copy langs.txt to the directory from which the program will run:</span></span>

    -   <span data-ttu-id="11792-368">Wenn Sie in Visual Studio ausführen, kopieren Sie Sie in *projectrootdirectory* \\ hellomui \\ guistep \_ 2.</span><span class="sxs-lookup"><span data-stu-id="11792-368">If running from within Visual Studio, copy it to *ProjectRootDirectory*\\HelloMUI\\GuiStep\_2.</span></span>
    -   <span data-ttu-id="11792-369">Wenn Sie den Windows-Explorer ausführen, kopieren Sie ihn in dasselbe Verzeichnis wie die guistep- \_2.exe.</span><span class="sxs-lookup"><span data-stu-id="11792-369">If running from Windows Explorer, copy it to the same directory as GuiStep\_2.exe.</span></span>

5.  <span data-ttu-id="11792-370">Erstellen Sie das Projekt, und führen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="11792-370">Build and run the project.</span></span> <span data-ttu-id="11792-371">Bearbeiten Sie langs.txt, damit unterschiedliche Sprachen am Anfang der Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="11792-371">Try editing langs.txt so that different languages appear at the front of the list.</span></span>

## <a name="step-5-customizing-hello-mui"></a><span data-ttu-id="11792-372">Schritt 5: Anpassen von "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="11792-372">Step 5: Customizing "Hello MUI"</span></span>

<span data-ttu-id="11792-373">Eine Reihe von Lauf Zeit Features, die bisher in diesem Tutorial erwähnt wurden, sind nur unter Windows Vista und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="11792-373">A number of the run-time features mentioned so far within this tutorial are available only on Windows Vista and later.</span></span> <span data-ttu-id="11792-374">Möglicherweise möchten Sie den Aufwand für die Lokalisierung und Aufteilung von Ressourcen wieder verwenden, indem Sie die Anwendung auf Windows-Betriebssystemversionen unter Windows XP (Windows XP) anwenden.</span><span class="sxs-lookup"><span data-stu-id="11792-374">You may wish to re-use the effort invested in localizing and splitting resources by making the application work on downlevel Windows operating system versions, such as Windows XP.</span></span> <span data-ttu-id="11792-375">Dieser Prozess beinhaltet das Anpassen des vorherigen Beispiels in zwei wichtigen Bereichen:</span><span class="sxs-lookup"><span data-stu-id="11792-375">This process involves adjusting the previous example in two key areas:</span></span>

-   <span data-ttu-id="11792-376">Die Funktionen zum Laden von Ressourcen vor Windows Vista (z. b. [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona), [**LoadBitmap**](/windows/win32/api/winuser/nf-winuser-loadbitmapa), [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)usw.) sind nicht MUI-fähig.</span><span class="sxs-lookup"><span data-stu-id="11792-376">The pre-Windows Vista resource loading functions (such as [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona), [**LoadBitmap**](/windows/win32/api/winuser/nf-winuser-loadbitmapa), [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), and others) are non-MUI aware.</span></span> <span data-ttu-id="11792-377">Anwendungen, die mit Split-Ressourcen ausgeliefert werden (LN-und MUI-Dateien), müssen Ressourcen Module mithilfe einer dieser beiden Funktionen laden:</span><span class="sxs-lookup"><span data-stu-id="11792-377">Applications that ship with split resources (LN and .mui files) must load resource modules using one of these two functions:</span></span>

    -   <span data-ttu-id="11792-378">Wenn die Anwendung nur unter Windows Vista und höher ausgeführt werden soll, sollte Sie Ressourcen Module mit [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)laden.</span><span class="sxs-lookup"><span data-stu-id="11792-378">If the application is to be run only on Windows Vista and later, it should load resource modules with [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span></span>
    -   <span data-ttu-id="11792-379">Wenn die Anwendung auf Versionen vor Windows Vista und Windows Vista oder höher ausgeführt werden soll, muss Sie [**loadmuilibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)verwenden. dabei handelt es sich um eine bestimmte kompatible-Funktion, die im Windows 7 SDK bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="11792-379">If the application is to be run on versions prior to Windows Vista, as well as Windows Vista or later, it must use [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya), which is a specific downlevel function provided in the Windows 7 SDK.</span></span>

-   <span data-ttu-id="11792-380">Die Unterstützung der sprach Verwaltung und der sprach Fall Back Reihenfolge, die in Versionen vor Windows Vista des Windows-Betriebssystems angeboten wird, unterscheidet sich deutlich von der in Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="11792-380">The language management and language fallback order support offered in pre-Windows Vista versions of the Windows operating system differs significantly from that in Windows Vista and later.</span></span> <span data-ttu-id="11792-381">Aus diesem Grund müssen Anwendungen, die den Benutzer konfigurierten sprach Fall Back zulassen, die sprach Verwaltungsverfahren anpassen:</span><span class="sxs-lookup"><span data-stu-id="11792-381">For this reason, applications that allow user-configured language fallback must adjust their language management practices:</span></span>

    -   <span data-ttu-id="11792-382">Wenn die Anwendung nur unter Windows Vista und höher ausgeführt werden soll, ist das Festlegen der Sprachliste mithilfe von [**setthreadpreferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) ausreichend.</span><span class="sxs-lookup"><span data-stu-id="11792-382">If the application is to be run only on Windows Vista and later, setting the language list using [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) is sufficient.</span></span>
    -   <span data-ttu-id="11792-383">Wenn die Anwendung unter allen Windows-Versionen ausgeführt werden soll, muss Code erstellt werden, der auf downlevelplattformen ausgeführt wird, um die Liste der Benutzer konfigurierten Sprachen zu durchlaufen und nach dem gewünschten Ressourcen Modul zu suchen.</span><span class="sxs-lookup"><span data-stu-id="11792-383">If the application is to be run on all Windows versions, code must be constructed that will run on downlevel platforms to iterate through the user configured language list and probe for the desired resource module.</span></span> <span data-ttu-id="11792-384">Dies ist in den Abschnitten 1C und 2 des Codes zu sehen, der später in diesem Schritt bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="11792-384">This can be seen in sections 1c and 2 of the code provided later in this step.</span></span>

<span data-ttu-id="11792-385">Erstellen Sie ein Projekt, das die lokalisierten Ressourcen Module für jede Windows-Version verwenden kann:</span><span class="sxs-lookup"><span data-stu-id="11792-385">Create a project that can use the localized resource modules on any version of Windows:</span></span>

1.  <span data-ttu-id="11792-386">Fügen Sie der Projekt Mappe hellomui (mithilfe der Menü Auswahl Datei, hinzufügen und neues Projekt) ein neues Projekt mit den folgenden Einstellungen und Werten hinzu:</span><span class="sxs-lookup"><span data-stu-id="11792-386">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="11792-387">Projekttyp: Win32-Projekt.</span><span class="sxs-lookup"><span data-stu-id="11792-387">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="11792-388">Name: guistep \_ 3.</span><span class="sxs-lookup"><span data-stu-id="11792-388">Name: GuiStep\_3.</span></span>
    3.  <span data-ttu-id="11792-389">Speicherort: übernehmen Sie die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="11792-389">Location: accept the default.</span></span>
    4.  <span data-ttu-id="11792-390">Wählen Sie im Win32-Anwendungs-Assistenten den Standard Anwendungstyp: Windows-Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="11792-390">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="11792-391">Legen Sie fest, dass dieses Projekt in Visual Studio ausgeführt wird, und konfigurieren Sie das Threading Modell.</span><span class="sxs-lookup"><span data-stu-id="11792-391">Set this project to run from within Visual Studio, and configure its threading model.</span></span> <span data-ttu-id="11792-392">Konfigurieren Sie Sie außerdem so, dass die erforderlichen Header und Bibliotheken hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="11792-392">Also, configure it to add the necessary headers and libraries.</span></span>

    > [!Note]  
    > <span data-ttu-id="11792-393">Bei den in diesem Tutorial verwendeten Pfaden wird davon ausgegangen, dass das Windows 7 SDK und das Microsoft nls-kompatible-APIs-Paket in ihren Standardverzeichnissen installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="11792-393">The paths used in this tutorial assume that the Windows 7 SDK and the Microsoft NLS downlevel APIs package were installed to their default directories.</span></span> <span data-ttu-id="11792-394">Wenn dies nicht der Fall ist, ändern Sie die Pfade entsprechend.</span><span class="sxs-lookup"><span data-stu-id="11792-394">If that is not the case, modify the paths appropriately.</span></span>

     

    1.  <span data-ttu-id="11792-395">Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf das Projekt, \_ und wählen Sie als Startprojekt festlegen aus.</span><span class="sxs-lookup"><span data-stu-id="11792-395">In the Solution Explorer, right-click the project GuiStep\_3 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="11792-396">Klicken Sie erneut mit der rechten Maustaste, und wählen Sie Eigenschaften aus.</span><span class="sxs-lookup"><span data-stu-id="11792-396">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="11792-397">Im Dialogfeld Eigenschaften Seiten des Projekts:</span><span class="sxs-lookup"><span data-stu-id="11792-397">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="11792-398">Legen Sie in der Dropdown-Dropdown-Dropdown-Datei die Konfiguration auf alle Konfigurationen fest</span><span class="sxs-lookup"><span data-stu-id="11792-398">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="11792-399">Erweitern Sie unter Konfigurations Eigenschaften die Option C/C++, wählen Sie Code Generierung aus, und legen Sie Lauf Zeit Bibliothek: Multithread Debuggen (/MTD) fest.</span><span class="sxs-lookup"><span data-stu-id="11792-399">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>
        3.  <span data-ttu-id="11792-400">Wählen Sie Allgemein aus, und fügen Sie weitere Includeverzeichnisse hinzu:</span><span class="sxs-lookup"><span data-stu-id="11792-400">Select General and add to Additional Include Directories:</span></span>

            -   <span data-ttu-id="11792-401">"C: \\ Microsoft nls-Downlevel-APIs \\ enthalten".</span><span class="sxs-lookup"><span data-stu-id="11792-401">"C:\\Microsoft NLS Downlevel APIs\\Include".</span></span>

        4.  <span data-ttu-id="11792-402">Wählen Sie Sprache aus, und legen Sie WCHAR \_ t als integrierten Typ: Nein (/Zc: WCHAR \_ t-) fest.</span><span class="sxs-lookup"><span data-stu-id="11792-402">Select Language and set Treat wchar\_t as Built-in Type: No (/Zc:wchar\_t-).</span></span>
        5.  <span data-ttu-id="11792-403">Wählen Sie erweitert aus, und legen Sie die Aufruf Konvention fest: \_ StdCall (/gz).</span><span class="sxs-lookup"><span data-stu-id="11792-403">Select Advanced and set Calling Convention: \_stdcall (/Gz).</span></span>
        6.  <span data-ttu-id="11792-404">Erweitern Sie unter Konfigurations Eigenschaften die Option Linker, wählen Sie Eingabe aus, und fügen Sie zusätzliche Abhängigkeiten hinzu:</span><span class="sxs-lookup"><span data-stu-id="11792-404">Under Configuration Properties expand Linker, select Input, and add to Additional Dependencies:</span></span>

            -   <span data-ttu-id="11792-405">"C: \\ Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ lib \\ muiload. lib".</span><span class="sxs-lookup"><span data-stu-id="11792-405">"C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Lib\\MUILoad.lib".</span></span>
            -   <span data-ttu-id="11792-406">"C: \\ Microsoft nls-Downlevel-APIs \\ lib \\ x86 \\ nlsdl. lib".</span><span class="sxs-lookup"><span data-stu-id="11792-406">"C:\\Microsoft NLS Downlevel APIs\\Lib\\x86\\Nlsdl.lib".</span></span>

3.  <span data-ttu-id="11792-407">Ersetzen Sie den Inhalt von guistep \_ 3. cpp durch den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="11792-407">Replace the contents of GuiStep\_3.cpp with the following code:</span></span>
    ```C++
    // GuiStep_3.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_3.h"
    #include <strsafe.h>
    #include <Nlsdl.h>
    #include <MUILoad.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now attempts to set the fallback list - this is much different for a down-level 
        // shipping application when compared to a Windows Vista or Windows 7 only shipping application    
        BOOL setSuccess = FALSE;
        DWORD setLangCount = 0;
        HMODULE hDLL = GetModuleHandleW(L"kernel32.dll");
        if( hDLL )
        {
            typedef BOOL (* SET_PREFERRED_UI_LANGUAGES_PROTOTYPE ) ( DWORD, PCWSTR, PULONG );
            SET_PREFERRED_UI_LANGUAGES_PROTOTYPE fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE)NULL;
            fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetProcessPreferredUILanguages");
            if( fp_SetPreferredUILanguages )
            {
                // call SetProcessPreferredUILanguages if it is available in Kernel32.dll's export table - Windows 7 and later
                setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
            else
            {
                fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetThreadPreferredUILanguages");
                // call SetThreadPreferredUILanguages if it is available in Kernel32.dll's export table - Windows Vista and later
                if(fp_SetPreferredUILanguages)
                    setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
        }

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module
        // LoadMUILibrary is the preferred alternative for loading of resource modules
        // when the application is potentially run on OS versions prior to Windows Vista
        // LoadMUILibrary is available via Windows SDK releases in Windows Vista and later
        // When available, it is advised to get the most up-to-date Windows SDK (e.g., Windows 7)
        HMODULE resContainer = NULL;
        if(setSuccess) // Windows Vista and later OS scenario
        {
            resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        else // this block should only be hit on Windows XP and earlier OS platforms as setSuccess will be TRUE on Windows Vista and later
        {
            // need to provide your own fallback mechanism such as the implementation below
            // in essence the application will iterate through the user configured language list
            WCHAR * next = userLanguagesMultiString;
            while(!resContainer && *next != L'\0')
            {
                // convert the language name to an appropriate LCID
                // DownlevelLocaleNameToLCID is available via standalone download package 
                // and is contained in Nlsdl.h / Nlsdl.lib
                LCID nextLcid = DownlevelLocaleNameToLCID(next,DOWNLEVEL_LOCALE_NAME);
                // then have LoadMUILibrary attempt to probe for the right .mui module
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,(LANGID)nextLcid);
                // increment to the next language name in our list
                size_t nextStrLen = 0;
                if(SUCCEEDED(StringCchLengthW(next,LOCALE_NAME_MAX_LENGTH,&nextStrLen)))
                    next += (nextStrLen + 1);
                else
                    break; // string is invalid - need to exit
            }
            // if the user configured list did not locate a module then try the languages associated with the system
            if(!resContainer)
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeMUILibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) 
                    && DownlevelLocaleNameToLCID(next,0) != 0)
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string 
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  <span data-ttu-id="11792-408">Erstellen oder kopieren Sie langs.txt in das entsprechende Verzeichnis, wie zuvor in [Schritt 4: Globalisieren von "Hello MUI"](#step-4-globalizing-hello-mui)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="11792-408">Create or copy langs.txt to the appropriate directory, as previously described in [Step 4: Globalizing "Hello MUI"](#step-4-globalizing-hello-mui).</span></span>
5.  <span data-ttu-id="11792-409">Erstellen Sie das Projekt, und führen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="11792-409">Build and run the project.</span></span>

> [!Note]  
> <span data-ttu-id="11792-410">Wenn die Anwendung unter Windows-Versionen vor Windows Vista ausgeführt werden soll, lesen Sie unbedingt die Dokumente, die im Paket mit den [Microsoft nls-kompatible-APIs](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) für die Neuverteilung Nlsdl.dll.</span><span class="sxs-lookup"><span data-stu-id="11792-410">If the application should run on Windows versions prior to Windows Vista, be sure to read the documents that came with the [Microsoft NLS downlevel APIs](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) package on how to redistribute Nlsdl.dll.</span></span>

 

## <a name="additional-considerations-for-mui"></a><span data-ttu-id="11792-411">Weitere Überlegungen zu MUI</span><span class="sxs-lookup"><span data-stu-id="11792-411">Additional Considerations for MUI</span></span>

### <a name="support-for-console-applications"></a><span data-ttu-id="11792-412">Unterstützung für Konsolen Anwendungen</span><span class="sxs-lookup"><span data-stu-id="11792-412">Support for Console Applications</span></span>

<span data-ttu-id="11792-413">Die in diesem Tutorial behandelten Verfahren können auch in Konsolen Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="11792-413">The techniques covered in this tutorial can also be used in console applications.</span></span> <span data-ttu-id="11792-414">Im Gegensatz zu den meisten standardmäßigen GUI-Steuerelementen können im Windows-Befehlsfenster jedoch keine Zeichen für alle Sprachen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="11792-414">However, unlike most standard GUI controls, the Windows command window cannot display characters for all languages.</span></span> <span data-ttu-id="11792-415">Aus diesem Grund erfordern mehrsprachige Konsolen Anwendungen besondere Aufmerksamkeit.</span><span class="sxs-lookup"><span data-stu-id="11792-415">For this reason, multilingual console applications require special attention.</span></span>

<span data-ttu-id="11792-416">Das Aufrufen der APIs [**setthreaduilanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) oder [**setthreadpreferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) mit bestimmten Filterflags bewirkt, dass die Funktionen zum Laden von Ressourcen Sprachressourcen Tests für bestimmte Sprachen entfernen, die normalerweise nicht innerhalb eines Befehls Fensters angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="11792-416">Calling the APIs [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) or [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) with specific filtering flags causes the resource loading functions to remove language resource probes for specific languages that are not normally displayed within a command window.</span></span> <span data-ttu-id="11792-417">Wenn diese Flags festgelegt sind, gestatten die sprach Einstellungs Algorithmen, dass nur die Sprachen, die im Befehlsfenster ordnungsgemäß angezeigt werden, in der Fall Back Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="11792-417">When these flags are set, the language-setting algorithms allow only those languages that will display properly in the command window to be on the fallback list.</span></span>

<span data-ttu-id="11792-418">Weitere Informationen zum Erstellen einer mehrsprachigen Konsolenanwendung mithilfe dieser APIs finden Sie in den Hinweisen zu den Abschnitten [**setthreaduilanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) und [**setthreadpreferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span><span class="sxs-lookup"><span data-stu-id="11792-418">For more information on using these APIs to build a multilingual console application, see the remarks sections of [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) and [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span></span>

### <a name="determination-of-languages-to-support-at-run-time"></a><span data-ttu-id="11792-419">Bestimmung der zu unterstützten Sprachen in Run-Time</span><span class="sxs-lookup"><span data-stu-id="11792-419">Determination of Languages to Support at Run-Time</span></span>

<span data-ttu-id="11792-420">Sie können einen der folgenden Entwurfsvorschläge anwenden, um zu bestimmen, welche Sprachen von Ihrer Anwendung zur Laufzeit unterstützt werden sollen:</span><span class="sxs-lookup"><span data-stu-id="11792-420">You can adopt one of the following design suggestions to determine which languages your application should support at run-time:</span></span>

-   <span data-ttu-id="11792-421">**Aktivieren Sie den Endbenutzer während der Installation, um die bevorzugte Sprache aus einer Liste unterstützter Sprachen auszuwählen.**</span><span class="sxs-lookup"><span data-stu-id="11792-421">**During installation, enable the end user to select the preferred language from a list of supported languages**</span></span>

-   <span data-ttu-id="11792-422">**Lesen einer Sprachliste aus einer Konfigurationsdatei**</span><span class="sxs-lookup"><span data-stu-id="11792-422">**Read a language list from a configuration file**</span></span>

    <span data-ttu-id="11792-423">Einige der Projekte in diesem Tutorial enthalten eine Funktion, die zum Analysieren einer langs.txt Konfigurationsdatei verwendet wird, die eine Sprachliste enthält.</span><span class="sxs-lookup"><span data-stu-id="11792-423">Some of the projects in this tutorial contain a function used to parse a langs.txt configuration file, which contains a language list.</span></span>

    <span data-ttu-id="11792-424">Da diese Funktion externe Eingaben annimmt, überprüfen Sie die Sprachen, die als Eingabe bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="11792-424">Because this function takes external input, validate the languages that are provided as input.</span></span> <span data-ttu-id="11792-425">Weitere Informationen zum Durchführen dieser Überprüfung finden Sie in den Funktionen [**isvalidlocalename**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) oder [**downlevellocalenametolcid**](downlevellocalenametolcid.md) .</span><span class="sxs-lookup"><span data-stu-id="11792-425">See the [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) or [**DownLevelLocaleNameToLCID**](downlevellocalenametolcid.md) functions for more details on performing that validation.</span></span>

-   <span data-ttu-id="11792-426">**Abfragen des Betriebssystems, um zu bestimmen, welche Sprachen installiert sind**</span><span class="sxs-lookup"><span data-stu-id="11792-426">**Query the operating system to determine which languages are installed**</span></span>

    <span data-ttu-id="11792-427">Dieser Ansatz hilft der Anwendung, die gleiche Sprache wie das Betriebssystem zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="11792-427">This approach helps the application use the same language as the operating system.</span></span> <span data-ttu-id="11792-428">Obwohl dies keine Benutzer Aufforderung erfordert, müssen Sie, wenn Sie diese Option auswählen, beachten, dass Betriebssystemsprachen jederzeit hinzugefügt oder entfernt werden können und sich ändern können, nachdem der Benutzer die Anwendung installiert hat.</span><span class="sxs-lookup"><span data-stu-id="11792-428">Although this does not require user prompting, if you choose this option, be aware that operating system languages can be added or removed at any time and can change after the user installs the application.</span></span> <span data-ttu-id="11792-429">Beachten Sie auch, dass in einigen Fällen das Betriebssystem mit eingeschränkter Sprachunterstützung installiert wird und die Anwendung mehr nutzen kann, wenn Sie Sprachen unterstützt, die vom Betriebssystem nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="11792-429">Also, be aware that in some cases, the operating system is installed with limited language support, and the application offers more value if it supports languages that the operating system does not support.</span></span>

    <span data-ttu-id="11792-430">Weitere Informationen zum Bestimmen der derzeit installierten Sprachen im Betriebssystem finden Sie unter der Funktion " [**enumuilanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) ".</span><span class="sxs-lookup"><span data-stu-id="11792-430">For more information on how to determine the currently installed languages in the operating system, see the [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) function.</span></span>

### <a name="complex-script-support-in-versions-prior-to-windows-vista"></a><span data-ttu-id="11792-431">Unterstützung komplexer Skripts in Versionen vor Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11792-431">Complex Script Support in Versions Prior to Windows Vista</span></span>

<span data-ttu-id="11792-432">Wenn eine Anwendung, die bestimmte komplexe Skripts unterstützt, auf einer Windows-Version vor Windows Vista ausgeführt wird, wird der Text in diesem Skript in GUI-Komponenten möglicherweise nicht ordnungsgemäß angezeigt.</span><span class="sxs-lookup"><span data-stu-id="11792-432">When an application that supports certain complex scripts runs on a version of Windows prior to Windows Vista, text in that script may not display properly in GUI components.</span></span> <span data-ttu-id="11792-433">Beispielsweise werden in diesem Lernprogramm im kompatible-Projekt möglicherweise in der MessageBox-und Ta-Skripts aufgrund von Problemen mit der Verarbeitung komplexer Skripts und dem Fehlen verwandter Schriftarten nicht in der MessageBox angezeigt.</span><span class="sxs-lookup"><span data-stu-id="11792-433">For example, in the downlevel project within this tutorial, hi-IN and ta-IN scripts may not display in the message box due to issues with processing complex scripts and the lack of related fonts.</span></span> <span data-ttu-id="11792-434">Normalerweise stellen Probleme dieser Art als quadratische Felder in der GUI-Komponente dar.</span><span class="sxs-lookup"><span data-stu-id="11792-434">Normally, problems of this nature present themselves as square boxes in the GUI component.</span></span>

<span data-ttu-id="11792-435">Weitere Informationen zum Aktivieren der komplexen Skript Verarbeitung finden Sie unter [Skript-und Schriftart Unterstützung in Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).</span><span class="sxs-lookup"><span data-stu-id="11792-435">More information about how to enable complex script processing can be found at [Script and Font Support in Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).</span></span>

## <a name="summary"></a><span data-ttu-id="11792-436">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="11792-436">Summary</span></span>

<span data-ttu-id="11792-437">In diesem Tutorial wurde eine monolingual-Anwendung globalisiert, und es wurden die folgenden bewährten Methoden demonstriert.</span><span class="sxs-lookup"><span data-stu-id="11792-437">This tutorial globalized a monolingual application and demonstrated the following best practices.</span></span>

-   <span data-ttu-id="11792-438">Entwerfen Sie die Anwendung, um das Win32-Ressourcenmodell zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="11792-438">Design the application to take advantage of the Win32 resource model.</span></span>
-   <span data-ttu-id="11792-439">Verwenden Sie die MUI-Aufteilung von Ressourcen in Satelliten Binärdateien (MUI-Dateien).</span><span class="sxs-lookup"><span data-stu-id="11792-439">Utilize MUI splitting of resources into satellite binaries (.mui files).</span></span>
-   <span data-ttu-id="11792-440">Stellen Sie sicher, dass der Lokalisierungsprozess die Ressourcen in den MUI-Dateien so aktualisiert, dass Sie für die Zielsprache geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="11792-440">Ensure that the localization process updates the resources in the .mui files to be appropriate for the target language.</span></span>
-   <span data-ttu-id="11792-441">Stellen Sie sicher, dass die Paket Erstellung und die Bereitstellung der Anwendung, zugeordneten MUI-Dateien und Konfigurations Inhalte ordnungsgemäß durchgeführt werden, damit die Ressourcen, die APIs laden, den lokalisierten Inhalt finden.</span><span class="sxs-lookup"><span data-stu-id="11792-441">Ensure that packaging and deployment of the application, associated .mui files, and configuration content is done correctly to allow the resource loading APIs to find the localized content.</span></span>
-   <span data-ttu-id="11792-442">Stellen Sie dem Endbenutzer einen Mechanismus bereit, um die Sprachkonfiguration der Anwendung anzupassen.</span><span class="sxs-lookup"><span data-stu-id="11792-442">Provide the end user a mechanism to adjust the language configuration of the application.</span></span>
-   <span data-ttu-id="11792-443">Passen Sie den Lauf Zeit Code so an, dass die Sprachkonfiguration genutzt wird, damit die Anwendung schneller auf die Anforderungen der Endbenutzer reagiert.</span><span class="sxs-lookup"><span data-stu-id="11792-443">Adjust the run-time code to take advantage of language configuration, to make the application more responsive to end user needs.</span></span>

 

 
